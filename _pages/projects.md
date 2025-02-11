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
Gordian Principles of independence, privacy, resilience, and openness
and that encourages responsible key management. This Architecture is
built upon [**Specifications**](#gordian-specifications) that have been
created in conjunction with the [**Wallet Community**](https://github.com/BlockchainCommons/Gordian-Developer-Community).
[**Developer Support**](#gordian-developer-support) enables the usage of these
specifications, while [**Reference Apps**](#gordian-reference-apps) further demonstrate that usage.

Beyond its architectural core, Blockchain Commons also supports
[**Events**](#events), [**Educational Projects**](#educational-projects), [**Advocacy Projects**](#advocacy-projects), and
[**Open Infrastructure Projects**](#open-infrastructure-projects).

## The Gordian Architecture

**Developers:** [Architecture](https://developer.blockchaincommons.com/architecture/)<br>
**Repo:** [Gordian](https://github.com/BlockchainCommons/Gordian)<br>
**Introduction:** [Gordian Architecture](https://github.com/BlockchainCommons/Gordian/blob/master/Architecture/README.md), [Roles](https://github.com/BlockchainCommons/Gordian/Architecture/Roles.md)<br>
**Q&A:** [Why CBOR?](https://www.blockchaincommons.com/introduction/Why-CBOR/)<br>
**Individual Topics:** [Animated QRs](https://www.blockchaincommons.com/devs/animated-qrs.html), [Musings of a Trust Architect](https://www.blockchaincommons.com/musings.html)

_The Gordian Architecture is the heart of Blockchain Commons' work. It's a partitioned architecture and a set of backup, communication, and encoding specifications, built to support the [Gordian Principles](https://github.com/BlockchainCommons/Gordian#gordian-principles)._

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

The Gordian architecture is built on specifications that empower our [Vision](https://www.blockchaincommons.com/vision.html). These specifications are what create the independence, privacy, resilience, and openness of our designs. They are broken into three main category: [Data Formats](https://developer.blockchaincommons.com/dataformat/), [Sovereign & Society Recovery](https://developer.blockchaincommons.com/seedrecovery/), and [UX Design](https://developer.blockchaincommons.com/ux/).

### Data Format Specifications

**Developers:** [Data Formats](https://developer.blockchaincommons.com/dataformat/), [Envelopes](https://developer.blockchaincommons.com/envelope/), [Animated QRs](https://developer.blockchaincommons.com/animated-qrs/), [URs](https://developer.blockchaincommons.com/ur/), [dCBOR](https://developer.blockchaincommons.com/dcbor/), [QuickConnect](https://developer.blockchaincommons.com/quickconnect/)<br>
**Envelope IETF Draft:** [Envelope I-D](https://datatracker.ietf.org/doc/draft-mcnally-envelope/)<br>
**Libraries:** [Library Listing](https://developer.blockchaincommons.com/libraries/)<br>

Blockchain Commons has produced a number of specifications that are intended to support interoperability among wallet developers and other digital-asset holders as well as resilience, privacy, and independence. 

* [Envelope](https://developer.blockchaincommons.com/envelope/) allows for the compact storage and transmission of data, as well as hashed elision and encryption.
* [Animated QRs](https://developer.blockchaincommons.com/animated-qrs/) support the transmission of larger amounts of data across air gaps.
* [URs](https://developer.blockchaincommons.com/ur/) underlie Envelope and Animated QRs and ensure interoperability.
* [dCBOR](https://developer.blockchaincommons.com/dcbor/) defines a deterministic version of CBOR, crucial for a variety of tasks including the hashed storage of data.
* [QuickConnect](https://developer.blockchaincommons.com/quickconnect/) defines a deep-link URI to provide further interoperability. 

### Lifehash & OIB Specifications

**Developers:** [UX Design](https://developer.blockchaincommons.com/ux/), [LifeHash](https://developer.blockchaincommons.com/lifehash/), [OIB](https://developer.blockchaincommons.com/oib/)<br>
**Online Demo:** [Lifehash.info](https://lifehash.info/)<br>
**Video:** [Explainer Video](https://www.youtube.com/watch?v=cu0K__KLxKo)

LifeHash is a method of hash visualization based on Conway's Game of Life that creates beautiful icons that are deterministic, yet distinct and unique given the input data. The basic concept is to take a SHA256 hash of the input data (which can be any data including another hash) and then use the 256-bit digest as a 16x16 pixel "seed" for running Conway’s Game of Life.

LifeHash is used by Blockchain Commons to create distinct and unique visual representations for your seeds and keys, so that you can recognize them at a glance. It appears as part of the Object Identity Block (OIB), which supplements that LifeHash with additional information on a digital object.

### CSR & SSKR Specification

**Developers:** [Sovereign & Social Recovery](https://developer.blockchaincommons.com/seedrecovery/), [Collaborative Seed Recovery](https://developer.blockchaincommons.com/csr/), [SSKR](https://developer.blockchaincommons.com/sskr/)<br>
**Blockchain Commons Depo:** [bc-depo-rust](https://github.com/BlockchainCommons/bc-depo-rust)<br>
**Depo API:** [bc-depo-api](https://github.com/BlockchainCommons/bc-depo-api-rust)<br>
**SSKR Security Review:** [2021 Review](https://github.com/BlockchainCommons/bc-sskr/blob/master/SECURITY-REVIEW.md)<br>

Collaborative Seed Recovery (CSR) is a system intended to improve the resilience of seeds and other digital assets by allowing them to be split up and those shares then stored on a variety of share servers. 

SSKR is Sharded Secret Key Reconstruction (SSKR). It's used by Blockchain Commons' implementation of CSR. It currently implements Shamir's Secret Sharing, allowing for sharding and reconstruction of a key.

The future of CSR involves the usage of [FROST](https://developer.blockchaincommons.com/frost/) to support Verifiable Secret Sharing (VSS) and [Collaborative Key Management (CKM)](https://developer.blockchaincommons.com/ckm/). Also see the [FROST Round Table](https://www.blockchaincommons.com/projects/#frost-round-table).

### Research Papers

**Repo:** [Research](https://github.com/BlockchainCommons/Research)<br>
**Video:** [Overview](https://www.youtube.com/watch?v=RYgOFSdUqWY)

Most of our specifications begin with "BCR" Research papers, which describe and detail the use of new, interoperable specifications for blockchain and Bitcoin. The ultimate goal is to upgrade BCRs to BCPs when they come into use by multiple parties, then to turn them into specifications. 
   
## Gordian Developer Support

_The Blockchain Commons repos include libraries and apps that help developers to develop and test the Gordian specifications._

### Developer Libraries

**Developers:** [Library Listing](https://developer.blockchaincommons.com/libraries/)

Reference libraries demonstrate the use of our specifications. They were originally coded in C or C++, and some have been recoded by us in Rust and Swift. Other developers have also produced conversions for Java, Python, and other languages.

### CLI & Web Apps

**Developer Resources:** [Developer Website](https://developer.blockchaincommons.com/)<br>
**CLI Apps:** [Bytewords-CLI](https://github.com/BlockchainCommons/bc-bytewords-cli), [dCBOR-CLI](https://github.com/BlockchainCommons/bc-dcbor-cli), [Envelope-CLI-Rust](https://github.com/BlockchainCommons/bc-envelope-cli-rust), [Envelope-CLI-Swift](https://github.com/BlockchainCommons/envelope-cli-swift), [Keytool-CLI](https://github.com/BlockchainCommons/bc-keytool-cli), [LifeHash-CLI](https://github.com/BlockchainCommons/lifehash-cli), [Musign-CLI](https://github.com/BlockchainCommons/musign-cli), [Seedtool-CLI](https://github.com/BlockchainCommons/bc-seedtool-cli) <br>
**iOS Apps:** [URDemo](https://github.com/BlockchainCommons/URDemo)<br>
**Web Apps:** [lifehash.info](https://lifehash.info/), [seedtool.info](https://seedtool.info/), [Spotbit]([spotbit](https://github.com/BlockchainCommons/spotbit)

Apps for the command-line and for iOS and the web can aid developers in testing out their work.

## Gordian Reference Apps

Whereas Developer Apps are meant for testing, the Gordian Reference Apps offer best practices and examples of how to incorporate Reference Libraries into applies that support the [Gordian Principles](https://github.com/BlockchainCommons/Gordian#gordian-principles).

### Gordian Coordinator (iOS)

**Repo:** [Coordinator](https://github.com/BlockchainCommons/iOS-GordianCoordinator)

Gordian Coordinator is a Multisig Bitcoin transaction coordinator for iOS. It demonstrates the use of request and response envelopes to communicate when creating multisig transactions in a way that is both resilient and easy to use.

### Gordian Depo (CSR)

**Repo:** [Depo](https://github.com/BlockchainCommons/bc-depo-rust)<br>
**API:** [Depo API](https://github.com/BlockchainCommons/bc-depo-api-rust)<br>
**Introduction:** [CSR Overview](https://developer.blockchaincommons.com/csr/)<br>
**CSR Architecture:** [Architectural Overview](https://developer.blockchaincommons.com/csr/architecture/)<br>
**Next Step:** [CKM Overview](https://github.com/BlockchainCommons/Gordian/blob/master/CKM/README.md)

Collaborative Seed Recovery, or CSR, is currently Blockchain Commons' major project, being developed in coordination with a number of partners. It's a system intended to automate the recovery of seeds and other sensitive digital data in a way that is safe, secure, and simple to use. It manages this by sharding secrets and then storing shares on different servers. This is not a methodology to prevent compromise, but simply to add resilience to recovery in the case of failure or loss. It is an exemplar for how to introduce a key management role into a Gordian Architecture.

Blockchain Commons's reference app for CSR is built on the [SSKR](https://developer.blockchainscommons.com) library and the [Depo Server](https://github.com/BlockchainCommons/bc-depo-rust), which uses the [Depo API](https://github.com/BlockchainCommons/bc-depo-api-rust) for communication. We expect other partners will use different servers for their share storage.

<a href="/images/projects/Cosigner.png"><img src="/images/projects/SeedTool.png" style="border: 1px solid black; float: left; margin-right: 1em" width="110"></a>

### Gordian Seed Tool (iOS)

**Repo:** [Seed Tool](https://github.com/BlockchainCommons/GordianSeedTool-iOS)<br>
**Blog:** [Gordian Seed Tool Reveals the Foundations of Cryptography](https://www.blockchaincommons.com/apps/SeedTool-Release/) (7/15/21)

Gordian Seed Tool is Blockchain Commons' most fully featured reference app. It demonstrates independence and resilience by protecting your cryptographic seeds while also making them available for easy use. Using Seed Tool, you can generate seeds and store them securely on your device. You can then derive and share multi-signature signing and verification keys from those seeds or alternatively sign PSBTs directly from the app. Sophisticated backup procedures demonstrate the usage of Sharded Secret Key Reconstruction ([SSKR](https://github.com/BlockchainCommons/crypto-commons/blob/master/Docs/README.md#sharded-secret-key-reconstruction-sskr)) — which lets you split your seed into pieces and send them to trusted parties, who can send them back to you in an emergency for seed recovery. You can even use an entirely offline device (no internet access) to store your seeds and use QR codes to exchange necessary information with online devices running compatible wallet or signing software. A complete [manual](https://github.com/BlockchainCommons/GordianSeedTool-iOS/blob/master/Docs/MANUAL.md) details its functionality.

### Gordian Server (MacOS)

**Repo:** [Gordian Server](https://github.com/BlockchainCommons/GordianServer-macOS)<br>

Gordian Server installs a self-sovereign Bitcoin Core server, protected by Tor, on your Mac computer. This gives you complete control over your Bitcoin destiny, and supports easy connectivity with [Gordian Wallet](https://github.com/BlockchainCommons/GordianWallet-iOS), [Fully Noded](https://apps.apple.com/us/app/fully-noded/id1436425586), and other wallets that support the [QuickConnect API](https://github.com/BlockchainCommons/Gordian/blob/master/QuickConnect/README.md).

<a href="/images/projects/lethekit.jpg"><img src="/images/projects/lethekit.jpg" align="right" border="1" width="200"></a>
### LetheKit (kit)

**Repo:** [lethekit](https://github.com/BlockchainCommons/lethekit)<br>
**Blog:** [Blockchain Commons Releases Feature-complete LetheKit](https://www.blockchaincommons.com/apps/Releasing-LetheKit/) (10/28/20)

LetheKit is a do-it-youself platform for performing various sensitive cryptographic operations on an offline airgapped device. It uses no WiFi or Bluetooth which could leak information and contains no local storage, and when the device is turned off it forgets any sensitive data stored in RAM. Thus the name Lethe (lee-thee), from the [mythological river](https://en.wikipedia.org/wiki/Lethe) of forgetfulness and oblivion.

### Other Gordian Reference Apps

**Legacy Repos:** [Cosigner iOS](https://github.com/BlockchainCommons/GordianCosigner-iOS), [Cosigner Android](https://github.com/BlockchainCommons/GordianSigner-Android), or [Cosigner macOS](https://github.com/BlockchainCommons/GordianSigner-macOS), [Wallet](https://github.com/BlockchainCommons/GordianWallet-iOS)<br>
**Research Repos:** [Mori-CLI](https://github.com/BlockchainCommons/mori-cli), [Sweeptool](https://github.com/BlockchainCommons/sweeptool-cli)

Several other reference apps have been released to demonstrate specific Principles. Some of these apps have since become outdated or superceded by other applications. Several research reference apps have been written to test out new technologies and new ways to demonstrate our Vision, but haven't been upgraded to full reference status.

## Events

_One of the prime goals of Blockchain Commons is to bring together different parties to educate and to create consensus on the future development of our technologies and specifications. This happens through events._

### FROST Round Table

**Website:** [Developers FROST](https://developer.blockchaincommons.com/frost/)
**Intro:** [A Layperson's Intro to Schnorr](https://www.blockchaincommons.com/musings/Schnorr-Intro/)
**Round Tables:** [Round Table I (November 2023)](https://developer.blockchaincommons.com/frost/meeting1/)

FROST is a threshold signature scheme for Schnorr signatures that provides a next-generation resilience methodology for the control of digital assets. Blockchain Commons is running a series of round tables intended to bring together experts in the field and allow them to discuss the challenges of its implementation. 

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

## Open Infrastructure Projects

_Open infrastructure projects create resources that can be used by the entire internet community._

### Esplora Server

**HTML Address:** http://esplora.blockchaincommons.com/<br>
**Onion Address (http):** http://pf4awrbzt3ohrtukpq6xx6y73gxqlnon4zh35ik7ald3kwfb5iedogad.onion<br>
**Onion Address (electrs):** pf4awrbzt3ohrtukpq6xx6y73gxqlnon4zh35ik7ald3kwfb5iedogad.onion:50001<br>

Blockchain Commons Esplora server.

### Spotbit Server

**Onion Address:** h6zwwkcivy2hjys6xpinlnz2f74dsmvltzsd4xb42vinhlcaoe7fdeqd.onion<br>
**Related Repo:** [spotbit](https://github.com/BlockchainCommons/spotbit)

An instance of Blockchain Commons' Spotbit Bitcoin price-aggregation server, available for public usage.

### Testnet Public Node

**Testnet Node IP Address:** 45.56.94.106:18333<br>
**Testnet Node Onion Address:** 71e355f8e097857c932cc315f321eb4a@ftemeyifladknw3cpdhilomt7fhb3cquebzczjb7hslia77khc7cnwid.onion:1309<br>
**Related Repo:** [GordianWallet-iOS](https://github.com/BlockchainCommons/GordianWallet-iOS)

Blockchain Commons maintains a public Bitcoin testnet node, primarily for use as an optional server for use with GordianWallet.

### Tor Exit Node

**Tor Node:**<br> [644074F47257F9A906F9AA5C6B8926C1540A1DA8](https://metrics.torproject.org/rs.html#details/644074F47257F9A906F9AA5C6B8926C1540A1DA8)

Blockchain Commons supports the open infrastructure of Tor by running its own exit node.

<center>
<img align="center" src="https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/tor-graph.png" width="100%">
  </center>

## How to Get Involved

_Want to become involved in Blockchain Commons' projects? Here's how!_

* **Participate in the Gordian Developer Community.** Join our [Developer Discussions on GitHub](https://github.com/BlockchainCommons/Gordian-Developer-Community/discussions). If you want more, [talk with us](mailto:team@blockchaincommons.com) to get access to our Gordian Signal group.
* **Contribute to Projects.** Submit Issues to Projects or (even better) PRs, offering clear improvements. We welcome them on all our repos!
* **Become a Sponsor.** Support Blockchain Commons by becoming a [GitHub Sponsor](https://github.com/sponsors/BlockchainCommons). We welcome all donations, as they allow us to continue our industry-supporting work. If you're a company interested in becoming more involved [talk with us](mailto:team@blockchaincommons.com) about becoming a Project Sponsor or a Sustaining Sponsor!
