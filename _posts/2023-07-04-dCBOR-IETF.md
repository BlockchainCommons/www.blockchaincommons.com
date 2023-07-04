---
title: "Deterministic CBOR Goes to IETF"
excerpt_separator: "<!--more-->"
categories:
  - Specifications
tags:
  - CBOR
  - Gordian Architecture
  - Gordian Envelope
  - Standards
  - IETF
classes:
  - wide
---

If you'll be at IETF 117, we hope you'll join us for dCBOR discussions there on Monday July 24th. The CBOR meeting will be 17:30-18:30 July 24th (Session IV) in the Continental 5 room. We have 15 minutes to discuss dCBOR. We'll also be holding a public side meeting on Gordian Envelope immediately before that, at 15:30-17:00 July 24th (Session III) in the Golden Gate 4 room, and we expect to have some discussions of dCBOR there too, since it's the foundation of Envelope. {: .notice--info}

<a href="https://www.youtube.com/watch?v=uoD5_Vr6qzw"><img src="https://img.youtube.com/vi/uoD5_Vr6qzw/mqdefault.jpg" style="float: right; border: 1px solid white"></a>

CBOR has been Blockchain Commons' data format of choice since we began work on [Uniform Resources](https://github.com/BlockchainCommons/crypto-commons/blob/master/Docs/ur-1-overview.md). The binary format is  concise, compact, and self-describing. It's also good in constrained environments and platform and language agnostic. But perhaps most importantly, it's standardized as an [IETF RFC](https://datatracker.ietf.org/doc/html/rfc8949). Altogether, that's made it a perfect data format for storing and transmitting the crucial data that protects cryptocurrency and other digital assets.

However, CBOR also includes a lightly described option that can make it even more useful: using the requirements of [§4.2 of the RFC](https://datatracker.ietf.org/doc/html/rfc8949#name-deterministically-encoded-c), CBOR can be deterministically encoded. This means that the same data will always produce the same output. This ability was crucial for our work on [Gordian Envelope](https://www.blockchaincommons.com/introduction/Envelope-Intro/), which builds out a Merkle Tree of hashes: for the Merkle Tree to be consistent, the hashes must be consistent, and so the underlying data must be consistent. Using the deterministic version of CBOR ensures that.

Unfortunately there was not strong support for deterministic CBOR. Though there are certainly a number of use cases that call for data consistency, the major libraries just adopted the main conventions of CBOR. If someone was using the deterministic features, they were doing so in a more _ad hoc_ way, in part because the RFC only partially defines the requirements: there's the opportunity for different applications to decide to encode elements such as `-0` or `NaN` or even numbers in different ways.

As a result, Blockchain Commons has been working with the IETF CBOR community this year to develop an official dCBOR specification.

Our Internet-Draft contains our current interpretation:

* [dCBOR I-D](https://datatracker.ietf.org/doc/draft-mcnally-deterministic-cbor/) — dCBOR: Deterministic CBOR Implementation Practices

We've supported that with Rust and Swift libraries plus a CLI program:

* [bc-dcbor-rust](https://github.com/BlockchainCommons/bc-dcbor-rust) — dCBOR for Rust
* [BCSwiftDCBOR](https://github.com/BlockchainCommons/BCSwiftDCBOR) — dCBOR for Swift
* [dcbor-cli](https://github.com/BlockchainCommons/dcbor-cli) — dCBOR command-line parser/validator

None of this is final! We've presented to IETF Dispatch and we've been engaging in discussions on the CBOR mailing list since February. 

* [Many Links](https://github.com/BlockchainCommons/crypto-commons/blob/master/dcbor.md) — Our dCBOR links page

At this point, we're expecting the CBOR community to produce the next iteration of the specification, which will split the work into one I-D that defines profiles for dCBOR and another that discusses dCBOR numeric reduction, which has been one of the biggest sticking points. We’re very enthusiastic to see this new iteration, as multiple perspectives and contributions from a number of collaborators is how internet standards come to be.

If you're interested in a deterministic version of CBOR and/or if you're using our own Gordian Envelope, which requires it, we invite you to join our discussions on the [CBOR mailing list](https://www.ietf.org/mailman/listinfo/cbor) and as a member of our [Gordian Developer community](https://www.blockchaincommons.com/subscribe.html#gordian-developers).
