---
header:
  overlay_color: "#00f"
  overlay_filter: "0.35"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "Limiting Shared Data & Minimizing Undesirable Correlation"
title: "Musings of a Trust Architect: Data Minimization & Selective Disclosure"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
tags:
  - Trust
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

_I have been struggling for a while to communicate my framing of definitions for Data Minimization and Selective Disclosure, which are privacy-focused data-protection techniques that Blockchain Commons is now incorporating into [Gordian Envelope](https://www.blockchaincommons.com/introduction/Envelope-Intro/)._

_A few years ago, I supported an RWOT paper on [the topic](https://nbviewer.org/github/WebOfTrustInfo/rebooting-the-web-of-trust-fall2017/blob/master/final-documents/data-minimization-sd.pdf), but it ultimately didn't match my vision, in part due to a traditional focus on government credentials that we're (unfortunately) unlikely to be able to influence._

_This year I gave it a new try by authoring [an advanced-reading paper for RWOT 11](https://github.com/WebOfTrustInfo/rwot11-the-hague/blob/master/advance-readings/elision-redaction-correlation-smart-documents.md) talking about our use of redaction and noncorrelation in Gordian Envelope. It's generated an interesting discussion (and upcoming collaborative RWOT white paper) on when correlation is purposeful and when it's accidental. It's also provided me with the opportunity to more explicitly write down my thoughts on data minimization and selective disclosure, which I've excerpted below to continue my series of [Musings of a Trust Architect](https://www.blockchaincommons.com/categories/#musings)._

<!--more-->

## Data Minimization

<a href="/musings.html"><img src="https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png" width=200 height=200 style="border: 1px solid black; float: right;"></a>

Data Minimization is the practice of limiting the amount of shared data to the minimum necessary: just enough for parties to successfully transact, accomplish a task, or otherwise meet a goal with each other, while minimizing risks to all parties by omitting unnecessary content. 

Though essential as part of security best practices (along with [Least privilege](https://en.wikipedia.org/wiki/Principle_of_least_privilege), a topic for a future musing), Minimimal Disclosure is, in particular, is mandated practice for maintaining the privacy of people using digital identities and thus requires special attention  when collecting and sharing, to curtail personal information to only that which is absolutely necessary.

The best practices of Data Minimization guide the design and implementation of personal data protection regulations, such as the General Data Protection Regulation (GDPR) in the European Union. They include:

* Service providers must only collect the minimum amount of personal information necessary to perform a specific task or service.
* Service providers must imit the length of time personal information is retained and must delete it when it is no longer needed.
* Individuals should only share personal information with third parties when it is necessary to perform a task or service.

The GDPR supports these best practices by requiring companies to have a legal basis for collecting and processing personal information and by giving individuals the right to access, correct, and delete their personal information. The GDPR also requires companies to implement appropriate security measures to protect personal information and to notify individuals and authorities in case of a data breach.

Other regulations that require some form of Data Minimization include:

* The California Consumer Privacy Act (CCPA) in the United States, which requires businesses to disclose the categories of personal information that they collect, use, disclose, and sell and also to obtain consumer consent for the sale of personal information.
* The Payment Card Industry Data Security Standard (PCI DSS), which is a set of security standards for organizations that handle credit card information and which requires merchants to limit the amount of cardholder data that is stored, processed, or transmitted.
* The Personal Information Protection and Electronic Documents Act (PIPEDA) in Canada, which requires organizations to collect only the personal information that is necessary for the identified purpose.
* The Health Insurance Portability and Accountability Act (HIPAA) in the United States, which requires healthcare organizations to protect the privacy of patient health information and to collect only the minimum necessary information to provide care.
* The Cybersecurity Information Sharing Act (CISA) in the United States, which encourages organizations to share information about cybersecurity threats, but also requires companies to protect personal information and to limit the collection of data to that which is necessary to address the threat.

In general, Data Minimization is enacted by policy decisions that limit the amount, duration, and scope of data collection and use.

* **Content minimization (amount)** involves collecting only the minimum amount of data necessary.
* **Temporal minimization (duration)** involves retaining data only for the minimum amount of time necessary to execute the task.
* **Scope minimization (scope)** involves using data only for the specific purpose of the active task.

In the digital credentials ecosystem, data minimization is primarily implemented through policy decisions made by stakeholders: credential issuers ensure that credentials can be presented in a way that enables data minimization, and credential inspectors establish policies in advance regarding the minimum data necessary to accomplish a task, the minimum time data can be stored, and the processes that ensure data is only applied to the task at hand.

Subjects may desire data minimization for various reasons, such as reducing the risk of undesired correlation or providing information gradually ([Progressive Trust](https://www.blockchaincommons.com/musings/musings-progressive-trust/)). Verifiers may also desire data minimization for other reasons, such as avoiding appearing threatening, protecting from "I told you so" situations, avoiding potential collection of "toxic" GDPR data, and reducing the cost of storing information.

ISO (International Organization for Standardization) has several standards related to data protection and privacy that include principles of data minimization. Some examples include:

* **ISO/IEC 27001:2013 - Information security management systems (ISMS)** provides a framework for managing sensitive information and includes a requirement for organizations to minimize the amount of sensitive information that is collected, used, and retained.
* **ISO/IEC 29100:2011 - Privacy framework** provides a framework for protecting personal information and includes a requirement for organizations to only collect personal information that is necessary for the specific purpose for which it is being collected.
* **ISO/IEC 27701:2019 - Extension to ISO/IEC 27001 and ISO/IEC 27002 for privacy information management** provides a framework for managing personal information and includes a requirement for organizations to minimize the amount of personal information that is collected, used, and retained.
* **ISO/IEC 29151:2012 - Information technology - Security techniques - Data-at-rest protection** provides guidance for protecting data when it is stored and includes a requirement for organizations to minimize the amount of sensitive information that is stored.
* **ISO/IEC 27040:2015 - Storage security** provides guidance for protecting data when it is stored and includes a requirement for organizations to minimize the amount of sensitive information that is stored.

Data minimization can be challenging to implement due to a number of factors, such as:

* **Difficulty in determining the minimum necessary data:** It can be difficult to determine exactly how much data is necessary to accomplish a specific task or goal, especially when dealing with complex systems and processes.
* **Balance of data minimization with other goals:** Organizations may be torn between the need to collect and retain data for legitimate business purposes and the need to minimize data to protect privacy and security.
* **Usage of data silos:** Data may be collected and stored across multiple systems and departments, making it difficult to identify and remove unnecessary data.
* **Lack of user consent:** Data minimization may not be possible if users are not willing to share their personal information, which can make it difficult to implement privacy-enhancing technologies such as selective disclosure.

## Selective Disclosure

"Selective Disclosure" is one of a number of privacy-enhancing techniques that go beyond Data Minimization to also protect against correlation. Selective Disclosure allows individuals or organizations to share only specific pieces of information, rather than sharing all of them, and prevents using correlation inappropriately to merge information from different contexts without consent. Selective Disclosure offers approaches that balance the need to share information for legitimate purposes against the need to protect the privacy and security of people and to minimize risks. 

GDPR does not mandate the use of Selective Disclosure, but the GDPR does gives individuals the right to control their personal information, the right to access, correct, and delete their personal information, and the right to object to certain processing activities. The California Consumer Privacy Act (CCPA) also allows individuals to know what personal information is being collected and shared and to opt out of the sale of their personal information.

In addition, some organizations have developed their own standards for Selective Disclosure, such as the Platform for Privacy Preferences (P3P) which provides a mechanism for websites to disclose their data collection and sharing practices and for individuals to set their privacy preferences.

Some requirements for Selective Disclosure include:

* **Granularity:** Allow individual or organizations to share only specific pieces of information, rather than sharing all of their personal information. This enables users to share only the information that is necessary to accomplish a specific task or goal.
* **Control:** Give users more control over their personal information by allowing them to decide what information they want to share, and with whom they want to share it.
* **Transparency:** Allow users to see what information is being shared and with whom, which enhances trust and transparency in the sharing process.
* **Security:** Use cryptographic techniques to secure the information shared, ensuring that only authorized individuals or organizations can access the information.
* **Privacy:** Minimize the amount of personal information that is shared, reducing the risk of data breaches or unauthorized access to personal information.
* **Compliance:** Help organizations to comply with data protection regulations, such as GDPR, by minimizing the amount of personal data collected, used and retained.
* **Auditability:** Allow organizations to track and audit information-sharing activities, providing transparency on how the data is being used.
* **Flexibility:** Allow organizations to adapt the sharing process to different scenarios and use cases, providing necessary flexibility.

More specifically, Selective Disclosure can help address some of the challenges of Data Minimization mentioned above:

*  **Difficulty in determining the minimum necessary data:** By allowing users to share only the specific information needed to accomplish a task or goal, Selective Disclosure can limit the data collection to only necessary information, avoiding additional information that is sensitive and potentially toxic.
* **Balance of data minimization with other goals:** By requiring granulatity in Selective Disclosure, the different goals of different groups can be evaluated and addressed.
* **Usage of data silos:** Selective Disclosure can help with data silos by allowing users to share information from different systems and departments while ensuring that only authorized individuals or organizations can access the information and that it is not shared or stored for longer than necessary. This can also help organizations to comply with data protection regulations such as GDPR.
* **Lack of user consent:** By giving users more control over their personal information, Selective Disclosure allows organizations to obtain user consent for information sharing in a more effective way. Users can choose what information they want to share and with whom, giving them control over what information an organization has access to. This can also increase trust and transparency between the organization and its users.

## Cryptographic Techniques for Selective Disclosure

Cryptographic Selective Disclosure leverages cryptography to allow individuals to selectively share specific pieces of their information while keeping the rest of their information private. It allows parties to prove certain attributes about themselves, without revealing their entire identity.

There are three important approaches to cryptographic Selective Disclosure: 

* **Hash-based Elision (or Redaction):** A hash is a cryptographic fingerprint for a set of data. It takes an input and creates a unique output. In Hash-based Elision, one party (the prover) presents to another party (the verifier) a hash of a piece of personal information without revealing the actual information (redacts it). One advantage of using cryptographic hashes for selective disclosure is that they are relatively simple and efficient method for hiding personal information, don't require complex mathematical calculations, and doesn't necessitate a trusted third party. A disadvantage of using cryptographic hashes is that without multiple round-trips they do not provide any cryptographic guarantees that the prover knows the original data (they may be just passing the hash forward). Another disadvantage is that there is a correlation risk if the same hash is given to multiple parties, which requires techiques like salting.
* **Zero-Knowledge proof (ZKP):** This cryptographic techique allows one party (the prover) to prove to another party (the verifier) that they possess certain information, without revealing the actual information. This is done by allowing the prover to demonstrate that they know the information. ZKP can be used to prove a wide range of attributes like knowledge of a password, possession of a private key, and membership in a group. As compared to a cryptographic hashes, ZKP is a method for proving knowledge of a piece of information without revealing the actual information, while cryptographic hashes are a way to hide the actual information, but not the knowledge of it. A disadvantage of ZKP is that it can be computationally expensive or require a large amount of communication between the prover and verifier; both can be a bottleneck in certain scenarios where low latency is a concern or where constrained hardware is being used.
* **Blind Signature:** As the name implies, this is a technique in which a signature is "blinded" before it is signed, hiding the identity of the signer. This allows the signer to prove that they possess a certain attribute, such as being over 18 years old, without revealing their name or other personal information. The signature can then be "unblinded" to reveal the identity of the signer. This makes it useful in scenarios where it is important to prove that a document has been signed by a specific individual without revealing their identity. One disadvantage of blind signatures is that they rely on a trusted third party, which can be a bottleneck and a centralization or security risk.

There are also adjacent technologies that may allow the leverage of cryptography for Selective Disclosure, but are not as broadly being investigated today.

* **Secret Sharing:** This technique allows a secret to be divided into specific number of shares, sent to parties from whom a specific number of shares are required (a quorum) to reconstruct the secret. This can be used as an escrow for a Selective Disclosure. A disadvantage is that restoring original secret requires one party to be entrusted to restore the quorum.
* **Secure Multi-Party Computation (MPC):** This technique allows multiple parties to jointly compute a function without revealing their inputs to each other. This is another method of escrow, one that solves the problems inherent to secret sharing, but at the cost of multiple rounds of interaction between the parties, and computational complexity.
* **Homomorphic Encryption:** This technique allows computations to be performed on ciphertext, resulting in the same plaintext output as if the computation was performed on the plaintext. As a result, computations can be performed on encrypted data without decrypting it first or revealing the actual data. However, these techniques are extremely computationally expensive (by multiple orders of magnitude).
