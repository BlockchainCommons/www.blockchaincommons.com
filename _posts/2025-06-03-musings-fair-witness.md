---
header:
  overlay_color: "#00f"
  overlay_filter: "0.5"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "From Heinlein to Gordian Envelope"
title: "Musings of a Trust Architect: Fair Witnessing in a Decentralized World"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
tags:
  - Zcash
  - Standards
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

> ABSTRACT: "Fair Witnessing" is a new approach for asserting and interpreting digital claims in a way that mirrors real-world human trust: through personal observation, contextual disclosure, and progressive validation. It can be implemented with the decentralized architecture of Gordian Envelopes to allow individuals to make verifiable statements while balancing privacy, accountability, and interpretability. At its core, fair witnessing is not about declaring truth, it's about showing your work.

In the early days of decentralized identity, we referred to what we were working on as "Verifiable Claims." The idea was simple: let people make cryptographically signed statements and allow others to verify them. But something unexpected happened. People assumed these claims would settle arguments or stop disinformation. They saw the term “verifiable” and equated it with “truth.”

The reality was more modest: we could verify the source of a claim but not its accuracy. We could assert that a claim came from a specific person or organization (or even camera or other object) but not whether that claim was unbiased, well-observed, or contextually complete.

This misunderstanding revealed a deeper problem: how do we represent what someone actually saw and how they saw it, in a way that honors the complexity of human trust?

### A Heinleinian Inspiration

<img src="https://www.blockchaincommons.com/images/posts/fw-stranger.jpg" style="float: right" width=250>

Iin _Stranger in a Strange Land_, Robert Heinlein described a special profession: the Fair Witness. A Fair Witness would be trained to observe carefully, report precisely, make no assumptions, and avoid bias. If asked what color a house was, a Fair Witness would respond, “It appears to be white on this side.”

It is this spirit we want to capture to fulfill the promise of the original verifiable claims.

A Fair Witness in our digital era is someone who not only asserts a claim but also shares the conditions under which it was made, including context, methodology, limitations, and bias:

- What were the physical conditions of the observation?
- Was the observer physically present?
- Did they act independently?
- What interests or leanings might have shaped their perception?
- How did they minimize those biases?

These are not just nice-to-haves. They are necessary components of evaluating a claim's credibility.

### Beyond Binary Trust

Fair witnessing challenges binary notions of trust. Traditional systems ask a "yes" or "no" question: do you trust this certificate? This issuer? 

But trust is rarely binary like this in the real world. It is layered, contextual, and progressive. The claim made by a pseudonymous environmental scientist might start out with low trust but could grow in credibility as:

- They reveal their professional history.
- Others endorse their work.
- They disclose how they mitigated their potential biases.

Trust builds over time, not in a single transaction. That's [progressive trust](https://www.blockchaincommons.com/musings/musings-progressive-trust-lifecycle/).

### Trust as a Nested Statement

To marry a fair witness claim to the notion of progressive trust requires the nesting of information. As shown in the example of the environmental scientist, the witnessing of an observation gains weight as the context is added: turning the scientist's claims into a fair-witness statement required collecting together information about who the scientist is, what their training is, and what their peers think of them. 

But as noted, progressive trust isn't something that occurs in a single transaction: it's revealed over time. We don't _want_ it to all be revealed at once, because that could result in information overload for someone consulting a claim and could have privacy implications for the witness.

A progressive trust model of fair witnessing requires that you show what you must and that you withhold what’s not needed&mdash;until it is. 

### Privacy and Accountability, Together

This model strikes a crucial balance. On one hand, it empowers individuals (fair witnesses) to speak from experience without needing permission from a centralized authority. On the other hand, it allows others to verify the integrity of the claim **without requiring total exposure**.

There are numerous use cases:

* You can prove you were trained without revealing your name.
* You can demonstrate personal observation without revealing your exact location.
* You can commit to a fact today and prove you knew it later.

### Fair Witnessing with Gordian Envelope

The demands of Fair Witnessing go beyond the capabilities of traditional verifiable credentials (VCs), primarily because VCs can't remove signed information but maintain its validation—and the ability to do so is critically important if you want to nest information for revelation over time.

Fortunately, a technology already exists that provides this precise capability: Blockchain Commons' [Gordian Envelope](https://developer.blockchaincommons.com/envelope/), which allows for: the organized storage of information; the validation of that information through signatures; the elision of that information; the continued validation of the information after elision; and the provable restoration of that information.

Any subject, predicate, or object in Gordian Envelope can itself be a claim, optionally encrypted or elided. This enables a deeply contextual, inspectable form of expression.

For example:
- Alice could make a fair-witness observation, which would be an envelope.
- Information on the context of Alice's assertion can be a sub-envelope.
- A credential for fair witness training can be a sub-envelope.
- Endorsements of Alice's work as a fair witness can be sub-envelopes.
- Endorsements, credentials, and even the entire envelope can be signed by the appropriate parties.
- Any envelope or sub-envelope can be elided, without affecting these signatures and without impacting the ability to provably restore the data later.

It's progressive trust appropriate for use with fair witnessing in an existing form!

### Toward a New Epistemology

Being a Fair Witness isn’t about declaring truth. It’s about saying what's known, with context, so others can assess what's truth. Truth, in this model, is _interpreted_, not imposed. A verifier—or a jury—decides if a claim is credible, not because a central authority says so, but because the Fair Witness has provided information with sufficient context and endorsements.

In other words, fair witnessing is not about **what is true**, but about **how we responsibly say what we believe to be true—and what others can do with that**.

This is epistemology (the theory of knowledge) that's structured as a graph. It's cryptographically sound, privacy-respecting, and human-auditable. It reflects real-world trust: messy, contextual, and layered. By modeling that complexity rather than flattening it, we gain both rigor and realism.

### Conclusion

In a world of machine-generated misinformation, ideological polarization, and institutional distrust, we must return to the foundations: observation, context, and human responsibility.

Fair witnessing offers a new path forward&mdash;one that is verifiable, privacy-respecting, and grounded in how humans actually trust.

Learn more: [ [Progressive Trust](https://developer.blockchaincommons.com/progressive-trust/) | [Gordian Envelope](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2024-006-envelope-graph.md) ]
