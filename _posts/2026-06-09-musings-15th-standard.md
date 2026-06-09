---
header:
  overlay_color: "#00f"
  overlay_filter: "0.5"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "Sometimes, It's About Design"
title: "Musings of a Trust Architect: On Being the Fifteenth Standard"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
tags:
  - Gordian Envelope
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

Often, the first thing that I hear when I describe [Gordian Envelope](https://developer.blockchaincommons.com/envelope/) is that we already have too many credential formats. They're right. We've got JWT, SD-JWT, JWE, COSE, mDoc, JSON-LD VCs, AnonCreds, BBS+ presentations, and at least five more depending on which working group is awake this quarter. [XKCD 927](https://xkcd.com/927/), "The 15th Standard", is the obligatory citation, and it lands. So I want to start with the question I also get asked: why build another one, and why now?

The short answer is that proliferation is not actually the deepest problem (and I say that having spent thirty years architecting trust systems and watching credentials standards evolve to the ones we have today, and having co-authored TLS 1.0). Instead, it's that most of the existing formats share a small number of design choices that I think are wrong.

As an example, I watched cryptographic agility get oversold in the '90s, retrofitted with ciphersuite negotiation, exploited through downgrade attacks, and finally walked back in TLS 1.3. That arc isn't unique to TLS. It shows up everywhere: optionality has long been treated as a design feature rather than a liability. JOSE is the most recent and visible example. The `alg` header put attackers in the verifier's seat, and the standard has spent a decade patching around it rather than admitting the choice was wrong. There are any number of situations like this where our design choices were wrong, including not just in-band algorithm negotiation, but also signature over literal bytes rather than over meaning, issuer-controlled disclosure, JSON's malleability, layer violations, and singular private keys. 

I say "wrong" with affection. The JOSE working group built something that shipped, got adopted, and pays a lot of mortgages. That matters. But we should be willing to look at what shipped and say: the optionality is the problem. The bag-of-attributes JSON is the problem. The signature over literal bytes rather than over meaning is the problem. The bolt-on for selective disclosure is the problem. Each of these is a place where the standards bodies did the best they could under the constraints of the moment but they produced something that comes up short when we measure it against the trust properties we actually want for the next decade.

No amount of additional formats sharing these incorrect choices will solve the underlying problems. But a new format with new design choices could.

## A New Solution

So that's "Why build another?" But what about "Why now?" I'll be transparent about the timing. When JWT and JSON-LD fought it out during the DID 1.0 process (and that fight slowed the standard down by years), I didn't feel that I could object. Both sides had real problems. I had opinions, but in the old IETF tradition, opinions without shipping code don't count for much. 

Though I didn't have shipping code, I do now.

Gordian Envelope is my attempt to make different choices at the substrate layer and see what falls out. Whether that justifies the fifteenth standard is a question I'll come back to at the end.

So: what does Gordian Envelope do differently?

Gordian Envelope is a substrate, not a credential format. It's dCBOR underneath, structured as semantic triples (subject, predicate, object), with every node carrying a digest and the whole thing forming a Merkle-like tree. A signature commits to the root. Any subtree can be elided (any subject, predicate, object, or assertion) and the signature still verifies. The holder (not the issuer) gets to decide what to reveal. This is the property I want as a human first and an architect second.

Envelope is also *radically recursive*. Any subject, object, or assertion can itself be an envelope. That recursion is what lets the same substrate carry property graphs, hypergraphs, labeled directed multigraphs, and several other shapes — not by adding modes or options, but because the structure is general enough that those graph models fall out of it. My Lead Researcher, Wolf McNally, and I wrote that up in [BCR-2024-006](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2024-006-envelope-graph.md). I want to be precise about what this is and isn't: it is not cryptographic agility in disguise. There is one encoding, one signature semantics, one elision mechanism. The expressivity lives in the data model, not in protocol switches.

### The Advantages of Envelope

I also want to be specific about what Gordian Envelope buys you, because vague privacy claims have done enough damage already.

It buys you **canonical encoding**. dCBOR has one representation per semantic content. Two parties assembling the same envelope from the same facts produce byte-identical outputs. JSON cannot do this without enormous effort and a lot of footguns. JSON Canonicalization Scheme exists, but ask the people who tried to deploy it how it went. JSON-LD's situation is worse, and worth naming specifically: to canonicalize the bytes you have to first understand the semantic layer above them. That's because the RDF Dataset Canonicalization algorithm (URDNA2015 and its successors) requires you to parse the JSON-LD into an RDF graph, resolve the `@context`, expand IRIs, and canonicalize *that*, before you can produce a stable byte sequence to sign. That's a layer violation, or even an inversion! The encoding layer has been made dependent on the meaning layer, and any disagreement at the meaning layer (such as a context that dereferences differently, a blank-node labeling difference, or an unresolvable IRI) breaks the signature. Envelope refuses that dependency. dCBOR canonicalizes at the encoding layer, full stop, and the semantic structure is built on top of bytes that are already stable.

It buys you **data minimization** that doesn't depend on the issuer's foresight. SD-JWT requires the issuer to commit, at issuance time, to a set of disclosable fields. The issuer is deciding, in advance, what you might want to share. With Envelope, the issuer signs everything and walks away. You — the holder — then decide what to reveal at presentation time. That's closer to what [RFC 6973 "Privacy Considerations for Internet Protocols"](https://datatracker.ietf.org/doc/html/rfc6973) actually calls for. It's also closer to how human trust works in the real world, which is the entire premise of [progressive trust](https://www.blockchaincommons.com/musings/musings-progressive-trust/).

It buys you **cryptography that doesn't negotiate with attackers**. The verifier knows what it accepts. The envelope doesn't tell it. We learned this from TLS. We learned it again from JOSE. I would like us not to have to learn it a third time.

It buys you **composable structure**. Signatures are assertions. Expiration is an assertion. Audience binding, witness attestation, revocation, and notarization are all assertions. The protocol layer and the application layer share a uniform shape, and you extend the format by adding assertions, not by petitioning a registry for another reserved claim name.

### The Challenges for Envelope

Now the honest part.

We made mistakes in the early design. The most public is BLAKE3, which we originally used to produce the hashes that are signed. We picked it because it's modern and fast. We then discovered that our actual use cases (air-gapped wallets, constrained devices, and hardware seed managers) don't need BLAKE3's streaming features and do need SHA-256's ubiquity. Backing out to use SHA-256 instead cost us code, drafts, docs, and credibility. I wrote about it in ["Problems of Cryptographic Agility"](https://www.blockchaincommons.com/musings/musings-agility/). If we'd shipped with cipher-suite agility, we could have just deprecated the algorithm and moved on. We chose not to, and we paid for that choice with a year of cleanup. I still think the choice was right. Optionality is a debt you eventually have to pay.

In addition, adoption is small. Reference implementations are in [Rust](https://github.com/BlockchainCommons/bc-envelope-rust) and [Swift](https://github.com/BlockchainCommons/BCSwiftEnvelope). We have a third-party [Typescript library](https://github.com/paritytech/bcts/tree/main/packages/envelope), but JavaScript support is overall thin, and the credential world runs on JavaScript whether we like it or not. Meanwhile, our [IETF draft for Envelope](https://datatracker.ietf.org/doc/draft-mcnally-envelope/) is still at the "individual-submission" stage. Finally, there's no IANA registry entry that makes a procurement officer's life easier. None of this is fixed yet, and I won't pretend otherwise.

Ultimately, I don't think Gordian Envelope will replace JWT. JWT will continue being the bearer-token shape for OAuth and OIDC for the foreseeable future, and that's mostly fine: OIDC is a short-lived-token use case where many of JWT's worst properties are tolerable. The places I want Envelope to win are the ones where the holder has to live with the document for years. Credentials. Key and seed storage. Capability tokens. Software-release attestations. Healthcare consent. Anything where data minimization and progressive trust matter more than fitting in an HTTP header.

## Final Notes

The XKCD punchline is "there are now 15 competing standards." It doesn't say one of the fifteen can't be better than the previous fourteen. It says that adding the fifteenth, *framed as unification*, is the joke. I don't frame Envelope as an unification. It's a substrate that respects principles I've spent three decades trying to articulate: human dignity, holder agency, progressive trust, minimum viable architecture. If a better substrate emerges that respects those principles, I'll migrate to it. The principles are what matter; the format is the carrier.

I'd rather we argue about whether the principles are right than whether we have too many standards. We have too many standards because we keep ducking the harder conversation. Let's have it.

— *with thanks to Wolf McNally, who actually writes the code; to Shannon Appelcline who writes the docs and tests our ideas; to the Decentralized Web community, who pushes back when I'm wrong; and to the dCBOR working group at IETF, who are doing the unglamorous foundational work.*

---

## Envelope Intro Videos

See our videos <a href="https://www.youtube.com/watch?v=-vcLCFKQvik">Understanding Envelope Part One</a> and <a href="https://www.youtube.com/watch?v=uFxStP3ATkw">Understanding Envelope Part Two</a> for more on Gordian Envelope

<table width="100%">
    <tr>
        <td>
            <b>Envelope Structure:</b>
            <a href="https://www.blockchaincommons.com/images/envelope-intro-0.jpg"><img src="https://www.blockchaincommons.com/images/envelope-intro-0.jpg"></a>
        </td>
        <td>
            <b>Envelope Hashes:</b>
            <a href="https://www.blockchaincommons.com/images/envelope-intro-1.jpg"><img src="https://www.blockchaincommons.com/images/envelope-intro-1.jpg"></a>
        </td>
        <td>
            <b>Redacted Hashes:</b>
            <a href="https://www.blockchaincommons.com/images/envelope-intro-2.jpg"><img src="https://www.blockchaincommons.com/images/envelope-intro-2.jpg"></a>
        </td>
    </tr>
</table>

## Related Reading

- BCR-2024-006, *Envelope as a Universal Graph Substrate* — https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2024-006-envelope-graph.md
- *Problems of Cryptographic Agility* — https://www.blockchaincommons.com/musings/musings-agility/
- *Data Minimization & Selective Disclosure* — https://www.blockchaincommons.com/musings/musings-data-minimization/
- *Progressive Trust* — https://www.blockchaincommons.com/musings/musings-progressive-trust/
- *Progress Trust Life Cycle* — https://www.blockchaincommons.com/musings/musings-progressive-trust-lifecycle/
- *Minimum Viable Architecture* — https://www.blockchaincommons.com/musings/musings-mva/
- *When Technical Standards Meet Geopolitical Reality* — https://www.blockchaincommons.com/musings/gdc25/
