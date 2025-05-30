---
cover: false
header:
  overlay_color: "#000"
  overlay_filter: "0.25"
  overlay_image: /images/qr-background.jpg
  og_image: /images/bcc-card.jpg
title: Our Projects
toc: true
toc_label: Projects
hide_description: true
permalink: /projects/
redirect_from: /projects.html
sidebar:
  nav: subpages
---

_Blockchain Commons produces projects that fulfill its
[**Vision**](https://www.blockchaincommons.com/vision.html)._

Much of this centers on an
[**Architecture**](#the-gordian-architecture) that focuses on our
[Gordian Principles](https://developer.blockchaincommons.com/principles/) of independence, privacy, resilience, and openness
and that encourages responsible key management. This Architecture is
built upon [**Specifications**](#gordian-specifications) that have been
created in conjunction with the [**Wallet Community**](https://www.blockchaincommons.com/subscribe/#gordian-developers).
[**Developer Support**](#gordian-developer-support) enables the usage of these
specifications, while [**Reference Apps**](#gordian-reference-apps) further demonstrate that usage.

Beyond its architectural core, Blockchain Commons also supports
[**Events**](#events), [**Educational Projects**](#educational-projects), and [**Advocacy Projects**](#advocacy-projects).

## The Gordian Architecture

**Overview:** [Architecture](https://developer.blockchaincommons.com/architecture/), [Principles](https://developer.blockchaincommons.com/principles/), [Roles](https://developer.blockchaincommons.com/architecture/roles/)<br>
**Topics:** [Why CBOR?](https://www.blockchaincommons.com/introduction/Why-CBOR/), [Progressive Trust Life Cycle](https://developer.blockchaincommons.com/progressive-trust/)<br>
**Articles:** [Musings of a Trust Architect](https://www.blockchaincommons.com/musings.html)

_The Gordian Architecture is the heart of Blockchain Commons' work. It's a partitioned architecture and a set of backup, communication, and encoding specifications, built to support the [Gordian Principles](https://developer.blockchaincommons.com/principles/)._

<center>
<a href="https://www.youtube.com/watch?v=RYgOFSdUqWY"><img src="https://img.youtube.com/vi/RYgOFSdUqWY/hqdefault.jpg" style="border: 2px solid blue"></a>
</center>

<br>

The Gordian Architecture supports users through those four principles.

* **Independence.** The Gordian Architecture supports self-sovereign control of digital assets. Users are in control, not centralized organizations.
* **Privacy.** The Gordian Architecture is privacy-protecting, allowing selective protection and disclosure of data.
* **Resilience.** The Gordian Architecture focuses on [#SmartCustody](https://www.smartcustody.com/index.html) to eliminate Single Points of Failure and Compromise; controlling your own assets can be tricky, and the Gordian Architecture makes it as safe as possible while also maximizing security.
* **Openness.** The Gordian Architecture helps developers to come together using open specifications that allow interoperability.

The Gordian Architecture is a future-looking design that covers everything that from the high-level architecture of a Gordian ecosystem through the specifications and UX best practices that make it possible. It allows blockchain, wallet, and web developers to deploy fully featured applications that incorporate all the current best practices of the digital-asset community.

## Gordian Specifications

The Gordian architecture is built on specifications that empower our [Vision](https://www.blockchaincommons.com/vision.html). These specifications are what create the independence, privacy, resilience, and openness of our designs. They are broken into three main categories: [the core stack](https://developer.blockchaincommons.com/#the-core-stack), [the UX stack](https://developer.blockchaincommons.com/#the-ux-stack), and [the crypto stack](https://developer.blockchaincommons.com/#the-crypto-stack).

<center>
<a href="https://developer.blockchaincommons.com"><img src="https://developer.blockchaincommons.com/assets/images/bc-stack.png"></a>
</center>

### Core Stack Specifications

* **Identifiers:** [Cliques](https://developer.blockchaincommons.com/cliques/), [Self-Sovereign Identity (SSI)](https://www.lifewithalacrity.com/article/the-path-to-self-soverereign-identity/), [XIDs](https://developer.blockchaincommons.com/xid/)
* **Collaborative Seed Recovery:** [CSR](https://developer.blockchaincommons.com/csr/)
  * **Blockchain Commons Depo:** [bc-depo-rust](https://github.com/BlockchainCommons/bc-depo-rust)
  * **Depo API:** [bc-depo-api](https://github.com/BlockchainCommons/bc-depo-api-rust)
* **Envelope:** [Envelope](https://developer.blockchaincommons.com/envelope/), [Request/Response](https://developer.blockchaincommons.com/envelope/request/), [Gordian Sealed Transaction Protocol (GSTP)](https://developer.blockchaincommons.com/envelope/gstp/), [Encrypted State Continuations (ESC)](https://developer.blockchaincommons.com/envelope/esc/)
   * **Envelope IETF Draft:** [Envelope I-D](https://datatracker.ietf.org/doc/draft-mcnally-envelope/)
   * **Introduction to Envelope Videos:** [Teaser](https://www.youtube.com/watch?v=uDI5ihfTB2Y&list=PLCkrqxOY1FbooYwJ7ZhpJ_QQk8Az1aCnG), [Understanding Envelope](https://www.youtube.com/watch?v=-vcLCFKQvik&list=PLCkrqxOY1FbooYwJ7ZhpJ_QQk8Az1aCnG), [Understanding Extensions](https://www.youtube.com/watch?v=uFxStP3ATkw&list=PLCkrqxOY1FbooYwJ7ZhpJ_QQk8Az1aCnG)
* **CBOR:** [dCBOR](https://developer.blockchaincommons.com/dcbor/)
   * **dCBOR IETF Draft:** [dCBOR I-D](https://datatracker.ietf.org/doc/draft-mcnally-deterministic-cbor/)

Blockchain Commons’ Core Stack includes its major user-facing innovations, as well as the foundational encoding that allows them:

* **Identifiers** support SSI by allowing users to control their identity.
* [**Collaborative Seed Recovery (CSR)**](https://developer.blockchaincommons.com/envelope/) is a system intended to improve the resilience of seeds and other digital assets by allowing them to be split up and then stored on a variety of share servers. 
* [**Envelope**](https://developer.blockchaincommons.com/envelope/) allows for the compact storage and transmission of data, as well as hashed elision and encryption.
* [**dCBOR**](https://developer.blockchaincommons.com/dcbor/) defines a deterministic version of CBOR, crucial for a variety of tasks including the hashed storage of data.

### UX Stack Specifications

* **Object Identity Block:** [OIB](https://developer.blockchaincommons.com/oib/), [LifeHash](https://developer.blockchaincommons.com/lifehash/)
   * **Lifehash Explainer Video:** [Video](https://www.youtube.com/watch?v=cu0K__KLxKo)
   * **Lifehash Website Demo:** [Lifehash.info](https://lifehash.info/)
* **Uniform Resources:** [ByteWords](https://developer.blockchaincommons.com/bytewords/), [URs](https://developer.blockchaincommons.com/ur/). [Animated QRs](https://developer.blockchaincommons.com/animated-qrs/)
   * **Multipart URs:** [MUR Implementation Guide](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2024-001-multipart-ur.md)

Blockchain Commons' OIB helps users to identify digital assets:

* [OIB](https://developer.blockchaincommons.com/oib/) is a standardized block of info to identify a digital asset.
* [Lifehash](https://developer.blockchaincommons.com/oib/) LifeHash is a method of hash visualization that creates beautiful icons that are deterministic, yet distinct and unique given the input data.
Blockchain Commons UR stack allows for the encoding of CBOR binary strings as text strings or as QRs:

* [Bytewords](https://developer.blockchaincommons.com/bytewords/) is a method for encoding binary data as four-letter words, used by URs.
* [URs](https://developer.blockchaincommons.com/ur/) underlie Envelope and Animated QRs and ensure interoperability.
* [Animated QRs](https://developer.blockchaincommons.com/animated-qrs/) support the transmission of larger amounts of data across air gaps.

### Crypto Stack Specifications

* **CKM:** [CKM](https://developer.blockchaincommons.com/ckm/), [FROST](https://developer.blockchaincommons.com/frost/), [MuSig2](https://developer.blockchaincommons.com/musig/)
   * **FROST Implementer Meetings:** [November 2023](https://developer.blockchaincommons.com/frost/meeting1/), [September 2024](https://developer.blockchaincommons.com/frost/meeting2/)
   * **FROST Developer Meetings:** [April 2024](https://developer.blockchaincommons.com/frost/developers1/), [December 2024](https://developer.blockchaincommons.com/frost/developers2/)
* **Sharding:** [SSKR](https://developer.blockchaincommons.com/sskr/)
   * **SSKR Security Review:** [2021 Review](https://github.com/BlockchainCommons/bc-sskr/blob/master/SECURITY-REVIEW.md)<br>

The Crypto Layer supports the resilience and independence of digital assets through cryptographic protections that allow users to use and maintain those assets.

* [CKM](https://developer.blockchaincommons.com/clm/) is a next-generation system of collaborative key management.
* [FROST](https://developer.blockchaincommons.com/frost/) is one of the multi-sig methods that could be used for CKM.
* [MuSig](https://developer.blockchaincommons.com/frost/) is another multi-sig method that can be used for CKM.
* [SSKR](https://developer.blockchaincommons.com/sskr/) is Sharded Secret Key Reconstruction, which is our current methodology for sharding and reconstructing a key.

### Research Papers

**Repo:** [Research](https://github.com/BlockchainCommons/Research)<br>
**Video:** [Overview](https://www.youtube.com/watch?v=RYgOFSdUqWY)

Most of our specifications begin with "BCR" Research papers, which describe and detail the use of new, interoperable specifications for blockchain and Bitcoin. The ultimate goal is to upgrade BCRs to BCPs when they come into use by multiple parties, then to turn them into specifications. 
   
## Gordian Developer Support

_The Blockchain Commons repos include libraries and apps that help developers to develop and test the Gordian specifications._

### Open Integrity

<img src="https://www.blockchaincommons.com/images/openintegrity.png" style="float: right" width="150px">

**Repo:** [Open Integrity Project](https://github.com/openintegrityproject)<br>
**Documents:** [Architecture](https://www.blockchaincommons.com/musings/open-integrity/), [Problem Statement](https://github.com/OpenIntegrityProject/core/blob/main/docs/Open_Integrity_Problem_Statement.md), [Script Snippets](https://github.com/OpenIntegrityProject/core/blob/main/docs/Open_Integrity_Script_Snippets.md)

Open Integrity seeks to increase the trust of Git repos by creating a foundational root of trust with an inception commit and by creating a chain of trust from that point, allowing the rotation of keys and authorized users. It does so with scripts and aliases that don't replace Git, but instead supplement it. This is something that we recommend for all developers.

### Developer Libraries

**Developers:** [Library Listing](https://developer.blockchaincommons.com/libraries/)

Reference libraries demonstrate the use of our specifications. They were originally coded in C or C++, and some have been recoded by us in Rust and Swift. Other developers have also produced conversions for Java, Python, and other languages.

### CLI & Web Apps

**Developer Resources:** [Developer Website](https://developer.blockchaincommons.com/)<br>
**CLI Apps:** [Bytewords-CLI](https://github.com/BlockchainCommons/bc-bytewords-cli), [dCBOR-CLI](https://github.com/BlockchainCommons/bc-dcbor-cli), [Envelope-CLI-Rust](https://github.com/BlockchainCommons/bc-envelope-cli-rust), [LifeHash-CLI](https://github.com/BlockchainCommons/lifehash-cli), [Provenance-Mark-CLI-Rust](https://github.com/BlockchainCommons/provenance-mark-cli-rust), [Seedtool-CLI-Rust](https://github.com/BlockchainCommons/seedtool-cli-rust) <br>
**Older CLIs:** [Envelope-CLI-Swift](https://github.com/BlockchainCommons/envelope-cli-swift), [Keytool-CLI](https://github.com/BlockchainCommons/bc-keytool-cli), [Musign-CLI](https://github.com/BlockchainCommons/musign-cli), [Seedtool-CLI-Swift](https://github.com/BlockchainCommons/bc-seedtool-cli)
**iOS Apps:** [URDemo](https://github.com/BlockchainCommons/URDemo)<br>
**Web Apps:** [lifehash.info](https://lifehash.info/), [seedtool.info](https://seedtool.info/), [Spotbit](https://github.com/BlockchainCommons/spotbit)

Apps for the command-line and for iOS and the web can aid developers in testing out their work.

## Gordian Reference Apps

Whereas Developer Apps are meant for testing, the Gordian Reference Apps offer best practices and examples of how to incorporate Reference Libraries into applies that support the [Gordian Principles](https://github.com/BlockchainCommons/Gordian#gordian-principles).

### Gordian Depo (CSR)

**Repo:** [Depo](https://github.com/BlockchainCommons/bc-depo-rust)<br>
**API:** [Depo API](https://github.com/BlockchainCommons/bc-depo-api-rust)<br>
**Introduction:** [CSR Overview](https://developer.blockchaincommons.com/csr/)<br>
**CSR Architecture:** [Architectural Overview](https://developer.blockchaincommons.com/csr/architecture/)<br>
**Next Step:** [CKM Overview](https://github.com/BlockchainCommons/Gordian/blob/master/CKM/README.md)

Collaborative Seed Recovery, or CSR,  automates the recovery of seeds and other sensitive digital data in a way that is safe, secure, and simple to use. It manages this by sharding secrets and then storing shares on different servers. This is not a methodology to prevent compromise, but simply to add resilience to recovery in the case of failure or loss. It is an exemplar for how to introduce a key management role into a Gordian Architecture.

Blockchain Commons's reference app for CSR is built on the [SSKR](https://developer.blockchainscommons.com) library and the [Depo Server](https://github.com/BlockchainCommons/bc-depo-rust), which uses the [Depo API](https://github.com/BlockchainCommons/bc-depo-api-rust) for communication. We expect other partners will use different servers for their share storage.

<a href="/images/projects/SeedTool.png"><img src="/images/projects/SeedTool.png" style="border: 1px solid black; float: left; margin-right: 1em" width="110"></a>

### Gordian Seed Tool (iOS)

**Repo:** [Seed Tool](https://github.com/BlockchainCommons/GordianSeedTool-iOS)<br>
**Blog:** [Gordian Seed Tool Reveals the Foundations of Cryptography](https://www.blockchaincommons.com/apps/SeedTool-Release/) (7/15/21)

Gordian Seed Tool is Blockchain Commons' most fully featured reference app. It demonstrates independence and resilience by protecting your cryptographic seeds while also making them available for easy use. Using Seed Tool, you can generate seeds and store them securely on your device. You can then derive and share multi-signature signing and verification keys from those seeds or alternatively sign PSBTs directly from the app. Sophisticated backup procedures demonstrate the usage of Sharded Secret Key Reconstruction ([SSKR](https://github.com/BlockchainCommons/crypto-commons/blob/master/Docs/README.md#sharded-secret-key-reconstruction-sskr)) — which lets you split your seed into pieces and send them to trusted parties, who can send them back to you in an emergency for seed recovery. You can even use an entirely offline device (no internet access) to store your seeds and use QR codes to exchange necessary information with online devices running compatible wallet or signing software. A complete [manual](https://github.com/BlockchainCommons/GordianSeedTool-iOS/blob/master/Docs/MANUAL.md) details its functionality.

### Gordian Server (MacOS)

**Repo:** [Gordian Server](https://github.com/BlockchainCommons/GordianServer-macOS)<br>

Gordian Server installs a self-sovereign Bitcoin Core server, protected by Tor, on your Mac computer. This gives you complete control over your Bitcoin destiny, and supports easy connectivity with [Gordian Wallet](https://github.com/BlockchainCommons/GordianWallet-iOS), [Fully Noded](https://apps.apple.com/us/app/fully-noded/id1436425586), and other wallets that support the [QuickConnect API](https://github.com/BlockchainCommons/Gordian/blob/master/QuickConnect/README.md).


### Other Gordian Reference Apps

**Legacy Repos:** [Coordinator](https://github.com/BlockchainCommons/iOS-GordianCoordinator), [Cosigner iOS](https://github.com/BlockchainCommons/GordianCosigner-iOS), [Cosigner Android](https://github.com/BlockchainCommons/GordianSigner-Android), or [Cosigner macOS](https://github.com/BlockchainCommons/GordianSigner-macOS), [Wallet](https://github.com/BlockchainCommons/GordianWallet-iOS)<br>
**Hardware Repos:** [Lethekit](https://github.com/BlockchainCommons/lethekit)<br>
**Research Repos:** [Mori-CLI](https://github.com/BlockchainCommons/mori-cli), [Sweeptool](https://github.com/BlockchainCommons/sweeptool-cli)

Several other reference apps have been released to demonstrate specific Principles. Some of these apps have since become outdated or superceded by other applications. Several research reference apps have been written to test out new technologies and new ways to demonstrate our Vision, but haven't been upgraded to full reference status.


## Events

_One of the prime goals of Blockchain Commons is to bring together different parties to educate and to create consensus on the future development of our technologies and specifications. This happens through events._

### Gordian Meetings

**Meetings Website:** [Meetings List](https://developer.blockchaincommons.com/meetings/)
**Announcements List:** [Sign Up](https://www.blockchaincommons.com/subscribe/)

Blockchain Commons holds monthly meetings, usually on the first Wednesday of the month, that support wallet developers in advancing their work in an interoperable way. There are often discussions of updates to interoperable Blockchain Commons technologies, plus special presentations from other developers in the field highlighting their own work and advancements.

### FROST Round Table

**FROST Website:** [Developers FROST](https://developer.blockchaincommons.com/frost/)<br>
**Intro:** [A Layperson's Intro to Schnorr](https://www.blockchaincommons.com/musings/Schnorr-Intro/)<br>
**Implementer Round Tables:** [November 2023](https://developer.blockchaincommons.com/frost/meeting1/), [September 2024](https://developer.blockchaincommons.com/frost/meeting2/)<br>
**Developer Meetings:** [April 2024](https://developer.blockchaincommons.com/frost/developers1/), [December 2024](https://developer.blockchaincommons.com/frost/developers2/)

FROST is a threshold signature scheme for Schnorr signatures that provides a next-generation resilience methodology for the control of digital assets. Blockchain Commons has run a series of meetings to support its roll-out. Impementer Round Tables have brought together experts in the field and allowed them to discuss the challenges of implementation. Developer Meetings have supported wallet cerators in incorporating FROST into their own work.

### Silicon Salon

**Website:** [Siliconsalon.info](https://www.siliconsalon.info/)

The Silicon Salon seeks to create semiconductor solutions for cryptography by bringing together semiconductor manufacturers who are interested in creating silicon solutions specifically intended for cryptography with wallet creators and other cryptographic principals. Each event to date has included presentations from principles in the area and discussion among attendees. Our web site includes the presentations and summarizes the discussions.

### Rebooting the Web of Trust

**Website:** [weboftrust.info](https://www.weboftrust.info/)<br>
**GitHub Repos:** [WebofTrust Repos](https://github.com/WebofTrustInfo)

Rebooting the Web of Trust is a semiannual design workshop that was founded by Christopher Allen prior to the foundation of Blockchain Commons; many of its ideas in turn became the heart of our initial work. We continue to attend and support the workshops.

## Educational Projects

_Educational projects consist of books, tutorials, or courses, intended to teach the usage of blockchains to programmers and end users alike._

### Learning Bitcoin from the Command Line

**Repo:** [Learning-Bitcoin-from-the-Command-Line](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line)<br>
**Future:** [Topics for v3.0](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line/blob/master/TODO-30.md)<br>
**Blog:** [Learning Bitcoin Upgrades to v2](https://www.blockchaincommons.com/courses/Learning-Bitcoin-Upgrades-to-v2/) (10/30/20)

<center>
<a href="images/projects/lbtc.png"><img src="/images/projects/lbtc.png" border="1" width="500"></a>
</center>

This is a complete twenty-chapter course intended to teach system administrators, developers, and engineers who are already acquainted with the UNIX command line interface how to work with Bitcoin. It uses this methodology to teach the fundamentals of Bitcoin, from RPC communications to how transactions work and how scripts work. The majority of the course is focused on `bitcoin-cli`, but there's also information on scripting, on programming with the RPC interface, and on using other command-line programs, beginning with `lightning-cli`. Translations are now available for [Portuguese](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line/blob/master/pt/README.md), with the final iteration of [Spanish](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line/tree/spanish-translation/es) pending.

<a href="/images/projects/sc.png"><img src="/images/projects/sc.jpg" align="right" border="1" width="200"></a>  
### #SmartCustody

**PDF:** [#SC v1.01](https://bit.ly/SmartCustodyBookV101)<br>
**Book Site:** [WWW Site](https://www.smartcustody.com/)
**New Scenarios:** [Multisig Scenario](https://github.com/BlockchainCommons/SmartCustody/blob/master/Docs/Scenario-Multisig.md)
**New Technologies:** [Articles](https://github.com/BlockchainCommons/SmartCustody#smartcustody-tools)
**Case Studies:** [Overview](https://github.com/BlockchainCommons/SmartCustody/blob/master/Docs/Case-Studies-Overview.md)
**Repo:** [SmartCustody Repo](https://github.com/BlockchainCommons/SmartCustody), [SmartCustodyBook](https://github.com/BlockchainCommons/SmartCustodyBook)<br>
**Future:** [Outline for v2.0](https://github.com/BlockchainCommons/SmartCustodyBook/blob/master/TODO.md)<br>
**Blog:** [June TweetStorms on #SmartCustody Adversaries, 1-on-1 Advice, Supporting Smart Custody Book v2](https://www.smartcustody.com/2020-06-03-June-Tweetstorm/) (6/3/20)

_The Use of Advanced Cryptographic Tools to Improve the Care, Maintenance, Control, and Protection of Digital Assets._ This five-chapter (186-page) book is intended to make you rethink the security of your digital assets. It puts together a risk-modeling system with two additional building blocks: a cold-storage scenario for managing self-custody; and an extensively detailed list of potential adversaries. By working through the book, you can determine which adversaries are actually the most dangerous to your assets, and adjust your own self-custody scenario to accommodate them. Additional chapters talk about fiduciary duties with regard to digital assets. 

A v2.0 of this book is in the planning stage, to improve the accessibility of the course, to support additional hardware tools, and to introduce multi-signature scenarios. Our [multisig design article](https://github.com/BlockchainCommons/SmartCustody/blob/master/Docs/Multisig.md), our [sharding design article](https://github.com/BlockchainCommons/SmartCustody/blob/master/Docs/SSKR-Sharing.md), our [SSKR Dangers article](https://github.com/BlockchainCommons/SmartCustody/blob/master/Docs/SSKR-Dangers.md), [Timelock exploration article](https://github.com/BlockchainCommons/SmartCustody/blob/master/Docs/Timelocks.md), and our [multisig scenario](https://github.com/BlockchainCommons/SmartCustody/blob/master/Docs/Scenario-Multisig.md) will all be incorporated into #SC 2.0 in some form, per our [#SC 2.0 outline](https://github.com/BlockchainCommons/SmartCustodyBook/blob/master/TODO.md).


## Advocacy Projects

_Blockchain Commons isn't just about technological development. It also works to ensure that there's a solid legal foundation for our blockchain technologies. That's where Advocacy comes in_.

### Law & Advocacy

**Website:** [Law & Advocacy Website](https://advocacy.blockchaincommons.com)<Br>
**Repo:** [Law & Advocacy Website Repo](https://github.com/BlockchainCommons/law-and-advocacy)<br>
**Articles:** [Article Webpage](https://advocacy.blockchaincommons.com/articles/)
**Repo:** [Testimony Webpage](https://advocacy.blockchaincommons.com/testimony/)

Our Law & Advocacy repo includes both research that we've done on the current state of the law and advocacy that we've done to _change_ that status. 

## How to Get Involved

_Want to become involved in Blockchain Commons' projects? Here's how!_

* **Participate in the Gordian Developer Community.** Join our [meeting announcement lists and Signal groups](https://www.blockchaincommons.com/subscribe/).
* **Contribute to Projects.** Submit Issues to Projects or (even better) PRs, offering clear improvements. We welcome them on all our repos!
* **Become a Sponsor.** Support Blockchain Commons by becoming a [GitHub Sponsor](https://github.com/sponsors/BlockchainCommons). We welcome all donations, as they allow us to continue our industry-supporting work. If you're a company interested in becoming more involved, [talk with us](mailto:team@blockchaincommons.com) about becoming a Project Sponsor or a Sustaining Sponsor! We're happy to work with you on your specific interests!
