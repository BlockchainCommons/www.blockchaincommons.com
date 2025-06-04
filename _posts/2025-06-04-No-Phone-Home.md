---
title: "Blockchain Commons Signs No Phone Home Initiative"
tagline: "(And Why It's Important)"
author: Christopher Allen
excerpt_separator: "<!--more-->"
categories:
  - News
tags:
  - Top Articles
  - Advocacy
  - Credentials
classes:
  - wide
---

<img src="/images/nph.png" width=300px style="float: right">

At Blockchain Commons, we design open infrastructure that prioritizes privacy, autonomy, and human dignity. That’s why I support and personally signed the **[No Phone Home Initiative](https://nophonehome.com)**. It is not just a position, it’s a call to preserve a foundational principle of decentralized identity: ***Credentials must be verifiable without enabling surveillance!***.

## Why “No Phone Home” Matters

The problem is simple: when verifying a digital credential such as a mobile driver’s license or a diploma, many systems require contacting the original issuer. This creates a digital trail of who is verifying what, when, and why. That trail can be used to profile and surveil, allowing issuers to track credential holders without their knowledge. 

Manu Sporny, in an email to the W3C Credentials Community Group ([June 3, 2025](https://lists.w3.org/Archives/Public/public-credentials/2025Jun/0008.html)), clarified the stakes:

> *"Retrieving a status list could be misinterpreted as 'phoning home' ... but it's not anywhere near the same level of "phoning home" that contacting the issuer and telling them 'I've got Steve here at
booze-hut.com, is he over 21?' achieves."*

But the threat of direct identity leak is just the tip of the iceberg. That's because credential presentation isn't a one-off event. It’s recurrent. Even when identifiers or interactions are pseudonymous, repeated verifications leak sensitive metadata, allowing issuers or third parties to correlate time, location, and use-pattern metadata into behavioral profiles. 

The Decentralized Identity Foundation talks about some of this in ["Nearly 100 Experts Are Saying 'No Phone Home'"](https://blog.identity.foundation/no-phone-home/):

> *"The risks multiply when applied across domains. Federated protocols developed for use within organizations become surveillance systems when used between different sectors or jurisdictions. Phone home capabilities that seem innocuous within a single domain can become tools for tracking and control when applied broadly without aggressive oversight and fine-tuning."*

Problematically, this is how these systems are designed to work! As Kim Hamilton Duffy says in the first of a series of articles [on mDL privacy](https://kimdhamilton.com/latent_surveillance/) that she's currently working on:

> *"This isn’t an unintended consequence—it’s an architectural feature that can trivially enable persistent record-keeping of when and where you use your credentials, creating patterns that can be analyzed long after the original transaction by unknown third parties."*

This also reveals yet another danger: how "normal" it feels to let credential issuers remain silently in the loop.

## Revocation Without Surveillance

Some argue that checking for the revocation of a credential requires phoning home. But that’s a false dilemma. In the [same W3C thread](https://lists.w3.org/Archives/Public/public-credentials/2025Jun/0009.html), Sporny noted:

> *"There are a few ways to retrieve a status list without directly contacting the issuer that use commonly deployed web technology.""*

Technical mitigations discussed and developed by the community include:

* **Large, pseudonymous status lists** (e.g., Bitstring Status List)
* **Use of CDNs or file mirrors** to avoid direct issuer contact
* **Oblivious HTTP (OHTTP)** for unlinkable status fetching

There are still issues with these potential mitigations. For example, Kyle Den Hartog (Pryvit NZ) raised [concerns](https://lists.w3.org/Archives/Public/public-credentials/2025Jun/0004.html) about status list misuse:

> *“An issuer creates a bitstring list of sufficiently large size, but only includes 1 active credential index per bitstring list. All other indexes are spoofed. The rest of the list would look active to the holder/verifiers but could still be a tracking mechanism by the issuer."*

But, these edge-case attacks reinforce why the core architecture must be surveillance-resistant by default.

Privacy isn't the only issue with revocation checking: it's also a structural risk. If we tie credential validity to live status checks, we quietly shift power from holders to issuers. It becomes a form of dependency injection, one that contradicts the goal of self-sovereign identity.

## Not Just Technical: It’s Ethical

This isn't just a technical issue. It goes to the ethical heart of self-sovereign identity design.

Daniel Hardman offered this framing in a [related thread](https://lists.w3.org/Archives/Public/public-credentials/2025May/0050.html) on edge cases:

> *"Verifiable credentials verify without issuer coordination; that is what the 'verifiable' in 'verifiable credential' means."*

Joe Andrieu argued in the same [May 2025 thread](https://lists.w3.org/Archives/Public/public-credentials/2025May/0009.html):

> *The identity system that wins is going to be the one we can use in any circumstance by anyone. ... It's my wallet. I expect it to serve me, as a user agent. I do not accept that it might also serve the state as a surveillance platform.
 
At Blockchain Commons, we agree. The ability to verify credentials offline, without depending on a central service, is essential for resilience and civil liberties.

A report prepared for the [American Civil Liberties Union](https://www.aclu.org/publications/aclu-digital-id-state-legislative-recommendations) (ACLU) put it clearly by requiring "No Issuer ability to track via phone home mechanism" and saying: 

> *"One way a digital ID can differ from physical ID is that it can enable the issuers of the digital ID to track where, when, and to whom one shows their ID. This tracking can reveal very private and sensitive information about the digital ID holder — namely, when and where, online or off, they present their ID. Standards and technologies should be designed so that the issuer (or any of its agents or contractors) cannot engage in any of these forms of tracking."*

## Emergencies Are Not an Excuse

Some use cases such as disaster response or first responder tracking have prompted discussions around consent-based “check-ins.” These are complex and worthy of consideration. But the [VC Data Model 2.0 spec](https://www.w3.org/TR/vc-data-model-2.0/#verification) is clear:

> *"Credential status specifications MUST NOT enable tracking of individuals, such as an issuer being notified (either directly or indirectly) when a verifier is interested in a specific holder or subject. Unacceptable approaches include "phoning home ..."*

But compliance doesn’t equal safety. Even digital credentials that conform to existing standards—such as ISO 18013-5—can still include implementation choices that enable surveillance. Privacy must be baked into system design, not retrofitted through policy disclaimers.

As Alexis Hancock of the [Electronic Frontier Foundation (EFF)](https:www.eff.org) warned _(via [State Scoop](https://statescoop.com/no-phone-home-mobile-drivers-license-privacy/))_:

> *“We have to act now because governments are enthusiastic about digital ID, but if we don’t pin down these basic principles now, it’s going to be a problem later.”*

We can build systems that are **opt-in**, **purpose-specific**, and **out-of-band**, without compromising the privacy baseline for everyone else.

## Our Commitment

At Blockchain Commons, we believe decentralized identity should empower the individual, not quietly report on them. We are actively designing open standards such as [Gordian Envelope](https://github.com/BlockchainCommons/BCSwiftSecureComponents/blob/master/Docs/GordianEnvelope.md) and [dCBOR](https://github.com/BlockchainCommons/Research/blob/master/papers/dCBOR-2023.md) to support truly private, verifiable, interoperable credentials.

We support “No Phone Home” because surveillance should never be the default. And we invite others to join us in making sure the future of identity remains decentralized, private, and just.
