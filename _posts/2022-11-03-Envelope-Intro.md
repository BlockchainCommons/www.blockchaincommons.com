---
title: "An Introduction to Gordian Envelopes"
excerpt_separator: "<!--more-->"
categories:
  - Introduction
tags:
  - CSR
  - Gordian Architecture
  - Gordian Envelope
image: https://raw.githubusercontent.com/BlockchainCommons/Gordian/master/Images/Envelope-Examples-DO.jpg
---

<a href="https://www.youtube.com/watch?v=OcnpYqHn8NQ"><img src="https://img.youtube.com/vi/OcnpYqHn8NQ/mqdefault.jpg" style="float: right; border: 2px solid blue"></a>

Gordian Envelope is a specification for the achitecture of a “smart document". It supports the secure, reliable, and deterministic storage and transmission of data such as seeds, keys, decentralized identifiers, and verifiable credentials  in a way that enables privacy while preserving structure. Gordian Envelope's privacy features are built on a hashed Merkle Tree that provides implicit support for cryptography of your choice and explicit support for privacy-related methodologies such as [progressive trust](https://www.blockchaincommons.com/musings/musings-progressive-trust/) and Merkle-based selective disclosure.

Blockchain Commons is currently working with multiple companies on the development and deployment of Gordian Envelopes via regular biweekly meetings; [contact us](mailto:team@blockchaincommons.com) if you'd like to be involved. We are also presenting Envelopes as a prospective Informational Draft for the IETF and engaging in discussions with the W3C Credentials Community Group.

<div class="bold--excerpt--node">Read More</div>

<!--more-->

## The Envelope as Metaphor

The name "envelope" was chosen for this smart-document architecture because that provides an excellent metaphor for its capabilities.

![](https://raw.githubusercontent.com/BlockchainCommons/Gordian/master/Images/Envelope-Examples.jpg)

These capabilities include:

* **Envelopes can have things written on them.** Plaintext parts of a Gordian Envelope can be read by anyone.
* **Envelopes can have routing instructions.** That plaintext information can include data on how to use the Gordian Envelope, such as how to open or close it.
* **Envelopes can contain things.** Things can be placed within the structure of a Gordian Envelope.
* **Envelopes can contain envelopes.** The Gordian Envelope structure is fully recursive: any part of an envelope can actually be another envelope.
* **Envelopes can have a seal.** A signature can be made for the contents of a Gordian Envelope, verifying their authenticity and that they haven't been changed.
* **Envelopes can be certified.** Beyond just guarding against changes, a Gordian Envelope signature can also act as a certification of the envelope's contents by some authority.
* **Envelopes can be closed.** Encryption allows any part of a Gordian Envelope to be protected from prying eyes.
* **Envelopes can have windows.** Selective disclosure allows for some parts of a Gordian Envelope to be readable while others have been redacted. Merkle proofs can proof that those parts were present in the original envelope.
* **Different recipients can open envelopes in different ways.** Just as people might use letter openers, their fingers, or a machine to open a normal envelope, special permits can grant people different ways to open a Gordian Envelope.

## Why Envelopes Are Important

The Gordian Envelope is intended as a more privacy-focused encoding architecture than existing data formats such as JWT and JSON-LD. We believe it has a better security architecture than JWT and that it doesn't fall victim to the barriers of canonicalization complexity found in JSON-LD — which should together permit better security reviews of the Gordian Envelope design.

However, new features of Gordian Envelope not available in JWT or JSON-LD offer some of the best arguments for using the Smart Document structure.

![](https://raw.githubusercontent.com/BlockchainCommons/Gordian/master/Images/Envelope-Examples-DO.jpg)

### Fundamental Design

Gordian Envelope was designed with two key goals in mind: to be _Structure-Ready_, allowing for the reliable and interopable storage of information; and to be _Privacy-Ready_, ensuring that transmission of that data can occur in a privacy-protecting manner.

* **Structure-Ready.** Gordian Envelope is designed as a Smart Document, meant to store information about a subject. More than that, it's a meta-document that can contain or refer to other documents. It can support multiple data formats, from simple hierarchical structures to labeled property graphs, semantic triples, and other forms of structured graphs. Though its fundamental structure is a tree, it can even be used to create DAGs through references between Envelopes.
* **Privacy-Ready.** Gordian Envelope protects the privacy of its data through progressive trust, allowing for holders to minimally disclose information by using elision or encryption, and then to optionally increase that disclosure over time. The fact that a holder can control data revelation, not just an issuer, creates a new level of privacy for all stakeholders. The progressive trust in Gordian Envelopes is accomplished through hashing of all elements, which creates foundational support for cryptographic functions such as signing and encryption, without actually defining which cryptographic functions must be used. 

The following structural decisions support these goals:

* **Structured Merkle Tree.** A variant of the Merkle Tree structure is created by forming the hashing of  the elements in the Envelope into a tree of digests. (In this "structured Merkele Tree", all nodes contain both semantic content _and_ digests, rather than semantic content being limited to leaves.)
* **Deterministic Representation.** There is only one way to encode any semantic representation within a Gordian Envelope. This is accomplished through the use of [Deterministic CBOR](https://www.blockchaincommons.com/introduction/Why-CBOR/) and the sorting of the Envelope by hashes to create a lexicographic order. Any Envelope that doesn't follow these strict rules can be rejected; as a result, there's no need to worry about different people adding the assertions in a different order or at different times: if two Envelopes contain the same data, they will be encoded the same way.

### Elision Support

* **Elision of All Elements.** Gordian Envelopes innately support elision for any part of its data, including subjects, predicates, and objects.
* **Redaction, Compression, and Encryption.** Elision can be used for a variety of purposes including redaction (removing information), compression (removing duplicate information), and encryption (enciphering information).
* **Holder-initiated Redaction.** Elision can be performed by the Holder of a Gordian Envelope, not just the Issuer.
* **Granular Holder Control.** Elision can not only be performed by any Holder, but also for any data, allowing each entity to elide data as is appropriate for the management of their personal (or business) risk.
* **Progressive Trust.** The elision mechanics in Gordian Envelopes allow for [progressive trust](https://www.blockchaincommons.com/musings/musings-progressive-trust/), where increasing amounts of data are revealed over time. It can even be combined with encryption to escrow data to later be revealed.
* **Consistent Hashing.** Even when elided or encrypted, hashes for those parts of the Gordian Envelope remain the same.

### Privacy Support

* **Proof of Inclusion.** As an alternative to presenting redactive structures, proofs of inclusion can be included in top-level hashes.
* **Herd Privacy.** Proofs of inclusion allow for herd privacy where all members of a class can share data such as a VC or DID without revealing individual information.
* **Non-Correlation.** Encrypted Gordian Envelope data can optionally be made less correlatable with the addition of salt.

### Authentication Support

* **Symmetric Key Permits.** Gordian Envelopes can be locked ("closed") using a symmetric key.
* **SSKR Permits.** Gordian Envelopes can alternatively be locked ("closed") using a symmetric key sharded with Shamir's Secret Sharing, with the shares stored with copies of the Envelope, and the whole enveloped thus openable if  copies of the Envelope with a quorum of different shares are gathered.
* **Public Key Permits.** Gordian Envelopes can alternatively be locked ("closed") with a public key and then be opened with the associated private key, or vice versa.
* **Multiple Permits.** Gordian Envelopes can simultaneously be locked ("closed") via a variety of means and then openable by any appropriate individual method, with different methods likely held by different people.
 
### Future Looking

* **Data Storage.** The initial inspiration for Gordian Envelopes was for secure data storage.
* **Credentials & Presentations** The usage of Gordian Envelope signing techniques allows for the creation of credentials and the ability to present them to different verifiers in different ways.
* **Distributed or Decentralized Identifiers.** Self-Certifying Identifiers (SCIDs) can be created and shared with peers, certified with a trust authority, or registered on blockchain.
* **Future Techniques.** Beyonds its technical specifics, Gordian Envelopes still allows for cl-sigs, bbs+, and other privacy-preserving techniques such as zk-proofs, differential privacy, etc.
* **Cryptography Agnostic.** Generally, the Gordian Envelope architecture is cryptography agnostic, allowing it to work with everything from older algorithms with silicon support through more modern algorithms suited to blockchains and to future zk-proof or quantum-attack resistent cryptographic choices. These choices are made in sets via ciphersuites.

## Usage of Envelopes

Gordian Envelopes are a foundational architecture that we expect to support many advanced projects involving self-sovereign control of digital assets.

Currently, it's being used in two major Blockchain Commons projects.

* **Crypto-request/response.** Requests and responses are specified ways to ask for and send information needed for self-sovereign operations, including when transmitting across an Airgap. Our second generation of requests and responses encodes those communications in Gordian Envelopes.
* **Collaborative Seed Recovery.** The [CSR system](https://github.com/BlockchainCommons/Gordian/blob/master/CSR/README.md) requires the use of Smart Documents to store shares of seeds that have been sharded for backup and recovery. The Gordian Envelope is thus the heart of that system.

There are a broad swath of additional use cases, some of which can be found in our [Use Case Overview of Envelopes](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Use-Cases/README.md). These include:

* **User-centric Educational Certification**: All sorts of credentials can be created in Gordian Envelopes, but certifications and other educational credentials are likely to be some of the most popular. These can be credentials signed by accredited institutions or by Web of Trust peers. Elision and third-party manipulation can allow these credentials to be safely passed around for a variety of purposes. Herd privacy features can create even greater anonymity. 
   * _Example Transactions:_ institutions can issue centralized credentials; individuals can issue peer-to-peer credentials using metadata to assist validation; subjects can elide credentials to preserve privacy or prevent discrimination; third-party holders can further elide credentials based on their own risk models; all parties can repackage credentials with signatures or additional information; issuers can create large batches of credentials and issue individual proofs to credential holders, allowing them to either reveal their credentials or maintain herd privacy. _(See [Educational Use Case](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Use-Cases/Educational.md))_
* **Resilient Asset Control:** There are many different use cases for helping users to resiliently control their digital assets, going beyond the specific design of CSR. These include the inclusion of metadata for resilience, the usage of salts to block correlation, and the creation of variable-use permits to allow multiple ways to open an envelope. 
   * _Example Transactions:_ users can store private keys, seeds, or other vulnerable data using encryption; users can improve the resilience of data with unencrypted metadata; users can alternatively wrap envelopes to encrypt their data entirety; users can use Shamir's Secret Sharing or other sharding technologies to resiliently lock data so that it can be restored by bringing together multiple envelopes, each of which contains a share and the encrypted data; users can create multi-permits that further improve resilience by allowing their data to be recovered in multiple ways, such as either with sharded shares or a private key. _(See [Assets Use Case](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Use-Cases/Financial.md))_
* **Structured Software Release:** The standardization of Gordian Envelopes is another of their strengths. Case studies involving source-control signing demonstrate how a field that is currently managed in a variety of different ways could allow for real improvements in security.
   * _Example Transactions:_ structured data can standardize software releases and ensure that all validation data is in one place; multiple signatures can allow verification by multiple sources; releases can be chained, so that once a user trusts one software release, they know to trust all future software releases; changes in release signers can be introduced through chained releases in an automated way that maintains trust.  _(See [Software Industry Use Cases](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Use-Cases/Software.md).)_
* **Privacy-Focused Data Transfer:** The privacy-ready design of Gordian Envelopes allows for use cases where elision is used differently over time, including progressive trust and situations whree data is differently elided for different circumstances.
   * _Example Transactions:_ structured data can be publicly released; data can be authenticated through signatures and validation; data can be differently elided for different sorts of queries; data can be released through a model of progressive trust by slowly reducing elision; data can be entirely elided so that it's only visible to queries that know to ask for the data; data can be entirely elided so that it's only visible to queries if someone provides a hash and a proof that allows them to verify the data. _(See [Data Distribution Use Cases](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Use-Cases/Data.md).)_

## Envelope Links

### Introductions

* [Doc: A Technical Overview of Envelopes](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Intro-Tech.md)
* [Doc: Envelope Technical Documents](https://github.com/BlockchainCommons/Gordian/tree/master/Envelope#articles)
* [IETF Draft: The Envelope Structured Data Format](https://blockchaincommons.github.io/WIPs-IETF-draft-envelope/draft-mcnally-envelope.html)
* [CLI Usage Overview Transcript](https://github.com/BlockchainCommons/envelope-cli-swift/blob/master/Transcripts/1-OVERVIEW-TRANSCRIPT.md)

### Videos

* [Playlist: Full Gordian Envelope Playlist](https://www.youtube.com/playlist?list=PLCkrqxOY1FbooYwJ7ZhpJ_QQk8Az1aCnG)
  * [Video: Introduction to Envelopes](https://www.youtube.com/watch?v=OcnpYqHn8NQ)
  * [Video: Envelope MVA & Cipher Choices](https://www.youtube.com/watch?v=S0deyIHXukk)

### Use Cases

* [Doc: Overview of Envelope Use Cases](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Use-Cases/README.md)
  * [Article: Summary of Use Cases](https://www.blockchaincommons.com/introduction/Gordian-Envelope-Use-Cases/)
  * [Doc: Educational Use Case](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Use-Cases/Educational.md)
  * [Doc: Data Distribution Use Case](https://github.com/BlockchainCommons/Gordian/blob/masterEnvelope/Use-Cases/Data.md)
  * [Doc: Asset Control Use Case](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Use-Cases/Financial.md)
  * [Doc: Software Release Use Case](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Use-Cases/Software.md)

### Envelope CLI

* [Reference App: Envelope-CLI](https://github.com/BlockchainCommons/envelope-cli-swift)
* [Docs: Envelope-CLI Docs](https://github.com/BlockchainCommons/envelope-cli-swift/tree/master/Docs)
* [Videos: Envelope-CLI Complete Playlist](https://www.youtube.com/playlist?list=PLCkrqxOY1FbooYwJ7ZhpJ_QQk8Az1aCnG)
  * [Video: Envelope-CLI Commands Overview](https://www.youtube.com/watch?v=K2gFTyjbiYk)
  * [Transcripts: Transcripts of Videos](https://github.com/BlockchainCommons/envelope-cli-swift/tree/master/Transcripts)
