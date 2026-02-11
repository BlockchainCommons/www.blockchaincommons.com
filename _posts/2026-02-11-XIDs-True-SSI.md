---
header:
  overlay_color: "#00f"
  overlay_filter: "0.5"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "How XIDs can return SSI to its principles"
title: "Musings of a Trust Architect: How XIDs Demonstrate a True Self-Sovereign Identity"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
tags:
  - Self-Sovereign Identity
  - XID
  - Top Articles
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

It's been more than ten years since I founded the [Rebooting the Web of Trust workshop](https://www.weboftrust.info/) with the goal of reimagining the peer-to-peer web of trust first popularized by [Pretty Good Privacy (PGP)](https://en.wikipedia.org/wiki/Pretty_Good_Privacy). The idea of decentralized identity was at the heart of the workshop [from the start](https://github.com/WebOfTrustInfo/rwot1-sf/blob/master/final-documents/dpki.pdf), but work on it accelerated following the first workshop when I wrote ["The Path to Self-Sovereign Identity"](https://www.lifewithalacrity.com/article/the-path-to-self-soverereign-identity/) to provide a foundation for the continuing discussion of the topic. It was then at the second workshop that we really rolled up our sleeves and began developing what would eventually become [W3C's DID standard](https://www.w3.org/TR/did-1.0/).

So I've been there from the start. I have a solid basis in our original intent for self-sovereign identity (SSI), and I know where we went from there. I'm the co-editor of the W3C [Amira Engagement Model](https://w3c-ccg.github.io/amira/), which demonstrated many of our desires with decentralized identity, and also a co-author of the W3C DID standard and of [BTCR](https://w3c-ccg.github.io/didm-btcr/), the first DID method. 

Unfortunately, in the ten years since I wrote "The Path to Self-Sovereign Identity," I feel that SSI, as implemented, has become indistinguishable from the very systems we set out to disrupt. Worse, it has legitimized architectural choices that align more closely with centralized identity systems, such as the mDL/mDoc-style solutions now appearing in emerging EU digital wallet deployments.

I first wrote about these concerns in ["Has Our SSI Ecosystem Become Morally Bankrupt?"](https://www.blockchaincommons.com/musings/musings-ssi-bankruptcy/). In short, SSI was meant to be private, decentralized identity. You were meant to be able to decide what you revealed about your identity, and you were meant to not be beholden to any outside control or gatekeepers. 

But compromise after compromise ate away at those ideals. Early discussions of DID- and VC-based identity treated issuer, holder, and verifier as equal roles that any participant might play. When the W3C Verifiable Credentials standard was ratified, that symmetry was narrowed to a “three-party ecosystem,” and when the DID standard followed, even that framing disappeared. That's what made DID issuers rarefied powers within the DID ecosystem rather than your peers; it's why DID wallets are largely incapable of acting as issuers themselves.

To be honest, I saw the potential for these problems while the DID specification was under review for Recommendation, but as an Invited Expert at the W3C, I approved the draft without raising a formal objection. That's because I didn't have an alternative at the time. Since I didn't have that alternative, I didn't feel it was right to say that DIDs as proposed were wrong. There was certainly the hope that they would develop in the right way, that even with the compromises in the standard, the deployers of mass-market DIDs would stick with our goals of decentralization and privacy.

But, they didn't. 

As a result, we have self-sovereign identity in name only. Though a true decentralized identity could be built within the DID spec, that's not how the ecosystem has evolved. Instead, more often than not, a small, de-facto-centralized set of issuers structurally controls what you can do with your DID. They limit what you can redact and require phone-home behavior that not only keeps you tied to them, but also negates your privacy.

It's now been almost four years since the ratification of DID v1.0. While the working group has been drafting DID v1.1, I've been focused more on doing my own work to create a technology stack that better exemplifies what we first started back in May 2016, in the shadow of the United Nations and the inaugural [ID2020 summit](https://id2020.org/): a truly decentralized and self-sovereign identity.

I call it the [XID](https://developer.blockchaincommons.com/xid/) or eXtensible IDentifier. XIDs deliberately trade ecosystem convenience and institutional alignment for architectural clarity, holder control, and long-term privacy. They're not intended to replace every use of DIDs or VCs, but to demonstrate a holder-centric identifier model that can coexist with, wrap, or inform future decentralized identity systems. They're an exemplar of what is possible.

A lot of my work on XIDs goes back to the [Amira Engagement Model](https://w3c-ccg.github.io/amira/). At Rebooting the Web of Trust 5, in Boston, we imagined a programmer with a politically sensitive background who wanted to contribute her skills to social causes, but was afraid of repercussions for herself and her family. We then laid out a self-sovereign pseudonymous identity system that would allow her to do so by protecting her real identity while allowing her pseudonymous identity to gain reputation over time, all under her tight control. Amira was my North Star when I began work on XIDs: I wanted to create a new decentralized identifier that supported her use case in a way that the evolving DID ecosystem did not.

Here's the quick overview of the architecture:

XIDs can be created by anyone. They function as holder-controlled identifiers that can carry signed assertions and credentials without requiring issuer-controlled disclosure or online resolution. They are autonomous cryptographic objects that are self-contained and do not inherently phone home; network interaction occurs only if a viewer explicitly chooses to dereference a URL or other correlatable pointer, rather than using one of the more secure alternative resolution methods available. Most importantly, the holder of a XID can themselves choose to redact any of the information it contains, without invalidating any signatures that have been made to authenticate the XID or any credentials it might include. 

Blockchain Commons has developed a body of work around XIDs, including specifications, working code, and supporting materials. We've also used XIDs within Blockchain Commons for experimental identity workflows and as a testbed for privacy-preserving identity research.

If that all sounds intriguing, please jump to our [developer page](https://developer.blockchaincommons.com/xid/), which links all of our specfications, code, CLI apps, and other material. If you want to evaluate XIDs more  concretely, instead start with the [Quickstart](https://github.com/BlockchainCommons/XID-Quickstart) tutorial and concepts to see how these ideas work in practice. It's the fastest way to begin working with XIDs (though note that only the first two tutorials have been fully released at this point).

But if you want more details about why XIDs might be of interest to _you_, I've written a number of discussions that I think address why a variety of people might be interested in XIDs or why they might be reluctant to use them. See if one of them addresses your situation. (And if none of them do, let me know your concern or issue, and I'll be happy to add another discussion.)

**Concerns that DIDs address:**

* **["I have self-sovereignty concerns"](#I-have-self-sovereignty-concerns-or-I-already-use-DIDs)**
* **["I have privacy concerns"](#I-have-privacy-concerns)**

**issues you might want addressed before you adopt DIDs:**

* **["I already use DIDs"](#I-have-self-sovereignty-concerns-or-I-already-use-DIDs)**
* **["I need a new technology to be novel"](#I-need-a-new-technology-to-be-novel)**
* **["I don't need another standard"](#I-dont-need-another-standard)**

After you've read any sections that interest you, you should jump to the [**conclusion**](#Conclusion).

## "I have self-sovereignty concerns"; or <br>"I already use DIDs"

I've already written about the general issue with DIDs: that the standard allows developers to sidestep decentralization. Most specifically, the biggest problem I have with DIDs is that holder control never happened. That's the prime thing that XIDs are meant to rectify.

Now "holder control" is a pretty bloodless term. But, it's the heart of self-sovereignty, so when I say that DIDs don't have holder control, I mean that they don't have self-sovereignty either: you don't control your identity (which was the whole point of SSI!).

A lack of personal control pervades the SSI ecosystem, starting with the fact that you typically can't issue DIDs or VCs yourself. However, limitations on disclosure may be the most problematic. When an issuer produces a DID full of VC credentials and assertions, the issuers ultimately decide how disclosure of that information is managed. They might say that _their_ VCs are all-or-nothing: that you have to disclose them in its entirety. Or they might allow you to redact parts of the information, but only specific elements that they allow. So, if you have an identifier that contains your name, age, and address, they might allow you to redact your age or your address when you publish the identifier, but say that your name always has to be there! If the word "allow" in there pisses you off, it should. They decide, not you.

XIDs flip all of this. They allow a decentralized identifier to be created and filled with signed assertions and other credentials. The holder then decides what's shown and what's not, to the specific granularity they want. This allows one person to have multiple identity contexts and an infinity of faces. These facades show different parts of a XID to different people, but it's still all one XID: one identifier that the holder truly controls.

> _So why would you, as a DID adopter or someone concerned about self-sovereignty, choose XIDs? Because they hand control back to the holder of the identifier, as was always intended for self-sovereign identity._

## "I have privacy concerns"

Great! XIDs are definitely the thing for you then!

The problem with DIDs as they've evolved is that they don't prevent correlation. In fact, they often make it worse.

This is because your DID can be packed with correlatable information, possibly even including credentials and other assertions. It's a big honeypot of data that's been helpfully collected together, and that makes it easy to link it up to other things you've done online or even in the physical world, creating an even bigger honeypot of data to define you.

The solution to this problem is redaction: removing some of the information from the DID so that only the minimum necessary is shown (minimal disclosure). But DIDs usually limit the ability to determine what can be redacted to the issuer—and ultimately they're only going to allow redaction if it runs parallel to their business interests. So, batches of information that are too big are often sent out with DIDs, and that makes it easier to collect them all together, and that makes it easier to create even bigger honeypots by correlation with other information. That's the opposite of a privacy concern.

XIDs are designed under the fundamental assumption that issuers, verifiers, networks, and infrastructure providers may all act adversarially with respect to correlation and control. As a result, they support radical elision. The holder has the ability at any time to redact information down to the atomic level: any singular datum, or even any atomic part of that datum (e.g., a subject, a predicate or an object) can be redacted. Because privacy is a [central concern](https://developer.blockchaincommons.com/principles/) for me, I've also introduced additional technologies to make this radical elision more powerful: salted hashes can disguise redacted elements that might be easy to guess, while [Garner](https://developer.blockchaincommons.com/garner/) and [Hubert](https://developer.blockchaincommons.com/hubert/) are new transport technologies that make it even harder to correlate by providing support for hidden and offline use of XIDs. Though the current implementation doesn't support BBS and other anti-signature correlation zk-proofs, the architecture is designed with them in mind. We already support quantum-resistant signatures and encryption.

I should note that privacy is always a bit of hard sell. You're presumably reading this section because privacy is important to you, but if you're on the fence, I suggest a new lens for looking at privacy: *coercion-resistance*. One of the big problems with loss of privacy is that it can lead to you being coerced. You might be forced to withdraw your political opinion online due to death threats if your online identifier was correlated with your real-life identity; or you might be forced to hand over your Bitcoins if your Bitcoin addresses became correlated with your home address or the home addresses of your loved ones. Protecting privacy protects you against coercion, and that's a whole additional level of self-sovereignty: it's literally sovereigny over yourself.

_So why would you, as someone concerned about privacy, choose XIDs? Because they fight against the correlation that is the biggest threat to the privacy of not just your information but your actual self._

## "I need a new technology to be novel."

It is entirely fair to say that a new technology needs to bring something new to the table, especially if it runs straight against an existing technology (or in this case an existing standard!).

XIDs are.

Their novel elements include:

_XIDs support deterministic encoding._ Because XIDs build on my [dCBOR](https://developer.blockchaincommons.com/dcbor/) and [Envelope](https://developer.blockchaincommons.com/envelope/) technologies, the data in XIDs is encoded deterministically: given the same input, it will be serialized in the same way across platforms and implementations. This enables reliable comparison, hashing, and signing and ensures the stability and reproducibility of the encoded form of the data across various platform ecosystems and implementations of code. This approach was explicitly abandoned in the IETF’s JWT ecosystem and was only partially reintroduced in JSON-LD through complex, and often layer-violating, mechanisms.

_XIDs support radical elision._ This deterministic encoding enables any element of data in an XID to be redacted or encrypted (what we call _elided_), down to the atomic level of individual entities within its system of semantic triples. This makes minimal disclosure practical by allowing you to provide differently redacted or encrypted versions of the same XID to different parties, preserving privacy by design. By contrast, redaction support in other technologies has been limited or optional to date (the IETF, for example, treats it as optional in SD-JWT), and this level of fine-grained elision represents a substantial step beyond that.

_XIDs support progressive trust._ [Progressive trust](https://www.blockchaincommons.com/musings/musings-progressive-trust-lifecycle/)  is the ability to slowly expand what you reveal about yourself to other people over time. It's how identity works in real life, but it hasn't been the way digital identity systems work, because they're often built on all-or-nothing data disclosures: a binary "trust or not trust" model. Progressive trust was built into XIDs from the start: it's the only technology where gradients of trust are fundamental to the architecture.

_XIDs are supported by radically private communication methods._ Blockchain Commons has so far released two radically private communication methods that are closely linked to XIDs. [Hubert](https://developer.blockchaincommons.com/hubert/) supports communication through decentralized storage services such as BitTorrent and IPFS. [Garner](https://developer.blockchaincommons.com/garner/) links XIDs to Tor communication. These are both radical new ways to communicate privately, without the need for centralization. We've built proof-of-concepts for each to show how they can be easily applied.

> _So why would you, who wants to see innovation, adopt XIDs? Because they're indeed innovative. Deterministic encoding, radical elision, progressive trust, and the support of radically private communication are some of the most progressive ideas contained within._
  
## "I don't need another standard"

I hear you! You're already committed to a standard, or you say the standards process is too slow so you don't want to fight through the introduction of something new.

XIDs do not have to be a new standard because they're a functional proof of concept. Certainly, I invite you to adopt XIDs if they fit your needs. They're robust, they're well supported, and we'll continue to support them in the future. But that's not the only way to see the advancement of the technological goals such as minimal disclosure and coercion resistance that are exemplified in XIDs.

Even if XIDs themselves are never widely adopted, they would be a success if their holder-centric capabilities become unavoidable requirements in future identity standards. In other words, XIDs demonstrate what future iterations of DID or mDoc could evolve to become, but only if we are willing escape the shackles of legacy and older architectures. If we are willing to do something major, then standards bodies can look toward XIDs for what is possible.

Ultimately, if the only way to ensure self-sovereignty and to protect privacy is to push for wider adoption of XIDs, I'll do that, but I'd be even happier to see major standards pick up the core features of XIDs, which are also the ideals of our original self-sovereign identity movement that have been left by the wayside.

> _So why would you, who doesn't need another standard, adopt XIDs? Because they can be a stepping stone. They're a proof of concept meant to push their ideals into wider discussion and ultimately wider adoption. For now, adoption of XIDs as an alternative moves us along that path._

## Conclusion

I am pushing XIDs because there are historic stakes. Maintaining the self-sovereignty of identity is important because centralized identity repositories can be [horribly misused](https://www.blockchaincommons.com/articles/echoes-history/). DIDs were supposed to accomplish that, but they've [compromised](https://www.blockchaincommons.com/musings/musings-ssi-bankruptcy/) by failing to unequivocally hold the line on the core values of decentralization.

As a result, we need to point out their flaws, offer alternative technologies that can do what they fail to, and use that as the foundation of a new revolution in self-sovereign identity. XIDs (along with several related Blockchain Commons technologies) are my Declaration of Independence from the current DID standard. I invite you to join that declaration so that we can together argue for the true self-sovereignty and true privacy that are missing from today's DIDs.

Here's what you can do to support the revolution:

* [Join the Gordian Developer Community](https://www.blockchaincommons.com/subscribe/#gordian-developers) to talk about these technologies.
* [Join the SSI 10th Anniversary Community](https://www.blockchaincommons.com/subscribe/#ssi-tenth-anniversary) to talk about the future of self-sovereign identity.
* [Read more about XIDs](https://developer.blockchaincommons.com/xid/) on our developer pages.
* [Try out the XID Tutorial](https://github.com/BlockchainCommons/XID-Quickstart) on GitHub and submit issues for any questions you have.
