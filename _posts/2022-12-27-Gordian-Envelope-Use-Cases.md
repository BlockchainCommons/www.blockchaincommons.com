---
title: "Gordian Envelope Use Cases Overview"
excerpt_separator: "<!--more-->"
categories:
  - Introduction
tags:
  - Gordian Architecture
  - Gordian Envelope
classes:
  - wide
image: https://raw.githubusercontent.com/BlockchainCommons/Gordian/master/Images/Envelope-Examples-DO.jpg
---

Gordian Envelopes can be used to store and transmit information in a structured, privacy preserving way. By what does that mean? Following are examples of four categories of usage that could benefit from the capabilities of Gordian Envelope. Specific use cases have been written for each. For a specific listing of those, see the [Use Cases README](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Use-Cases/README.md) in the Gordian repo.

## Educational & Credential Industry Use Cases

Gordian Envelopes can be used in the education sector to securely and privately transmit and store student records such as transcripts, test scores, and other sensitive information. The ability of a Gordian Envelope to elide specific information without invalidating the seal on the Envelope is particularly useful in the education industry (as well as other credential-issuing industries) because it allows different parties such as employers or regulators to access only the information they need for their specific purposes, while still preserving both the authenticity and the privacy of the rest of the data.

The following privacy-preserving features are demonstrated in educational use cases:

* Any holder can elide content within a credential, without changing any signatures.
* Any holder can repackage a credential by adding additional information or even new credentials.
* Credential issuing is not limited to centralized authorities: peer-to-peer issuing is also possible, with metadata providing context.
* Credentials can be bundled to create herd privacy.
* Bundled credentials can be carefully organized to reduce correlation.
* Entities can use selective correlation of bundled credential to verify known information without acquiring new, toxic data.

See the [Educational & Credential Industry Use Cases](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Use-Cases/Educational.md) for illustrated examples of these features as well as further discussions of their advantages.

## Wellness Use Cases

Wellness data, which can include everything from info collected by activity trackers to doctors' records, tends to be highly sensitive. However, it can also be highly helpful, able to not only detail an individual's health needs, but also to help society through clinical trials, contract tracing, and more. Gordian Envelopes can help wellness data to fulfill these two opposed needs: privacy and appropriate sharing.

The following privacy-presevering features are demonstrated in wellness use cases:

* Envelope data can be structured and encrypted to ensure its openness and privacy.
* Encryption can further protect intermediaries from toxic data.
* SSKR can be used to ensure that encrypted data is not lost.
* Envelope data can be elided to protect sensitive data while sharing.
* Multipermits can support data-streaming to multiple parties.
* Signatures can prove provenance of data.
* Data can be further anonymized while provenance is maintained with those signatures.
* Hashes can prove contribution of data without any other revelation.
* People and places alike can be protect through herd privacy of hashing.

See the [Wellness Use Cases](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Use-Cases/Wellness.md) for illustrated examples of these features and further discussion.

## Data Distribution Use Cases

Because of their focus on privacy, Gordian Envelopes can be used to store sensitive data that might be revealed to different people in different ways under different circumstances. The data distribution use cases focus on how a simple user-data program such as `webfinger` could benefit from this new paradigm.

The following data distribution features are demonstrated in use cases:

* Envelope data can be structured.
* Envelope data can be made verifiable through signatures.
* Envelope data can include additional metadata, such as timestamps, which itself can be verified.
* Elision can allow envelopes to be released in different ways to different viewers.
* Selective correlation can enable data lookup without widespread release.
* Selective correlation can automate progressive releases of data.

See the [Data Distribution Use Cases](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Use-Cases/Data.md) for illustrated examples of these features and further discussion.

## Software & AI Industry Use Cases

Gordian Envelopes can be used in the software and AI industry to provide authentication for software source code, AI training sets, and model data. This helps to ensure that the integrity of the code (or models) is maintained throughout the software development life-cycle. It can be particularly useful for the signing of software releases, with Gordian Envelopes supporting multiple signatures, dynamically changing signatures, and even anonymous signatures. Gordian Envelopes can also support the reliability and availability of software infrastructure by securely transmitting configuration data and cryptographic keys.

The following signing & release features are demonstrated in software use cases:

* Envelope data can be precisely structured.
* Envelopes can be signed by multiple parties, and each signature can be individually verified.
* Envelopes can be further signed by third parties, allowing for a variety of validation.
* Envelopes can use metadata to chain back to previous envelopes, reducing validation costs.
* Envelopes can include attestations or other types of verifiable metadata.
* Envelopes can incorporate signer changes into their data chains, again reducing validation costs.
* Envelopes can be signed anonymously, depending on a Web of Trust for validation.
* Anonymous signers can later provably come forward, if thoughtful Envelope design was used from the start.

See the [Software Industry Use Cases](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Use-Cases/Software.md) for illustrated examples of these advantages.

## Financial Industry Use Cases

Gordian Envelopes can be used to securely and privately transmit and store financial records, such as bank statements and transaction records, as well as digital assets, such as seeds and private keys. Gordian Envelopes can also be used to securely transmit financial data between institutions, helping not only to prevent tampering, but also to minimize toxic data through proofs of inclusion. The ability to use permits to allow multiple useres to open Envelopes in multiple ways can also support dual-control access requirements.

The following privacy features are demonstrated in financial use cases, which are focused on the self-sovereign control of assets:

* Envelope data can be partially or fully encrypted for security.
* Unencrypted metadata can be used to improve resilience with "hints".
* Metadata can be elided when data needs to be partially revealed.
* Envelope data can be salted to reduce correlation when that data is elided.
* Encrypted data can be locked with sharded keys to further improve resilience.
* Encrypted data can be locked via multiple methods to even further improve resilience.

See the [Financial Industry Use Cases](https://github.com/BlockchainCommons/Gordian/blob/master/Envelope/Use-Cases/Financial.md) for illustrated examples of these features and additional discussion.

## Other Data Distribution Use Cases

A number of additional industries can benefit from the data-distribution possibilities of Gordian Envelopes.

**Agriculture Industry Use Cases.** Gordian Envelopes could be used to securely transmit data related to agriculture such as crop yields, soil quality data, and weather data, between different parties. This could help to prevent tampering or other security breaches, ensuring that only verified, trustworthy data is transmitted.

**Energy Industry Use Cases.** Gordian Envelopes could also be used to securely transmit data related to the energy industry such as electricity usage data and grid configuration data between different parties.

**Environmental Industry Use Cases.** Gordian Envelopes could also be used to securely transmit data related to the environment such as water quality data, air quality data, and weather data between different parties.

**Healthcare Industry Use Cases.** Gordian Envelopes can be used in the healthcare industry to securely and privately transmit and store patient health records, allowing authorized parties to access only the information they are authorized to view. This can help healthcare organizations comply with privacy regulations, such as HIPAA in the United States. Support of decentralized access to medical information can provide also additional benefit since most healthcare is distributed.

**Law, Government, and Public Sector Industry Use Cases.** In the legal, government, and public sector, Gordian Envelopes can be used to encode and transmit sensitive legal documents such as contracts and court orders, while preserving their complex data structures and ensuring personal privacy. The ability of Gordian Envelopes to offer selective disclosure of information is useful in this sector where only certain parties may be authorized to view certain information. This can help to protect the human rights of individuals by ensuring that personal data is not misused. Additionally, the use of Gordian Envelopes can support transparency and accountability in government by allowing for the selective disclosure of public data to authorized parties, helping to prevent the misuse of government power.

**Supply Chain Use Cases.** Gordian Envelopes can be used to encode and transmit sensitive information, such as production schedules, inventory levels, shipping records, and quality control data, while preserving their complex data structures and ensuring privacy. The ability of Gordian Envelopes to elide or externally reference certain parts of the envelope allows for cooperation among diverse supply chain parties and promotes fair trade by preventing unfair competition. 

**Telecommunications Use Cases.** Gordian Envelopes could also be used to securely transmit data related to telecommunications networks, such as network configuration data and customer data, between different parties in the telecommunications industry.

**Transportation Use Cases.** Gordian Envelopes could also be used to securely transmit data related to the movement of people and goods, such as flight plans and cargo manifests, between different parties in the transportation industry. 

## The Common Thread of Use Cases

Though Gordian Envelopes support a wide variety of usage, a few common threads reveal their particular strengths.

1. **Sensitivity.** Gordian Envelopes can protect sensitive data, both to prevent tampering and security breaches while simultaneously allowing the data to be verified by external parties. (Healthcare and finances demonstrate some of the prime use cases for this thread. Human right use cases can also be quite important.)
2. **Complexity.** Because of Gordian Envelope's ability to built iterative data structures, complex data is another strong use case, especially when its sensititivty is sufficient to require privacy protections.
3. **Diversity.** Gordian Envelopes can help a variety of parties with different business models, risk models, and trust boundaries to each protect data in ways that meet their own requirements, while still interacting with each other. (B2B use cases of various types tend to demonstrate this common thread.)

The core value proposition of the privacy features of Gordian Envelopes cannot be overstated: through its support for selective disclosure and [progressive trust](https://www.blockchaincommons.com/musings/musings-progressive-trust/), Gordian Envelopes can help a variety of parties to main privacy and security for their data.


