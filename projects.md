---
cover: false
hide_description: true
permalink: /projects.html
---

Blockchain Commons produces projects that fulfill its [Vision](https://www.blockchaincommons.com/vision.html). They're focused on decentralized systems that support independence, privacy, resilience, and openness and that encourage responsible key management.

{% include toc %}

<hr>

<a href="images/projects/gordian-logo-white.png"><img src="images/projects/gordian-logo-white.png" align="right" border="1" width="400"></a>
## The Gordian System

_The Gordian system is the heart of Blockchain Commons' work. It's intended to support the self-sovereign control of digital assets in a way that's safe, secure, and private by enabling responsible key management. It's built on a foundation of [Principles](https://github.com/BlockchainCommons/Gordian#gordian-principles) that have been fulfilled in an [Architecture](https://github.com/BlockchainCommons/Gordian#gordian-architecture) that is embodied in Reference Apps and supported by Reference Libraries._

### The Gordian Architecture

**Repo:** [Gordian](https://github.com/BlockchainCommons/Gordian)<br>
**Introduction:** [Gordian Architecture](https://github.com/BlockchainCommons/Gordian/blob/master/Docs/Overview-Architecture.md), [Roles](https://github.com/BlockchainCommons/Gordian/blob/master/Docs/Overview-Roles.md)

The Gordian Architecture puts the Gordian Principles into use through an overall design that covers everything that from the high-level architecture of a Gordian ecosystem through the specification and UX best practices that make it possible.

<center>
  <a href="https://raw.githubusercontent.com/BlockchainCommons/Gordian/master/Images/video-tech-overview.png"></a>
</center>

### Collaborative Seed Recovery

**Introduction:** [CSR Overview](https://github.com/BlockchainCommons/Gordian/blob/master/Docs/CSR.md)<br>
**Next Step:** [CKM Overview](https://github.com/BlockchainCommons/Gordian/blob/master/Docs/CKM.md)

Collaborative Seed Recovery, or CSR, is a new system intended to automate the recovery of seeds and other sensitive digital data in a way that is safe, secure, and simple to use. It is not a methodology to prevent compromise, but simply to add resilience to recovery in the case of failure or loss. It is an exemplar for how to introduce a key management role into a Gordian Architecture.

CSR is a step toward [Collaborative Key Management (CKM)](https://github.com/BlockchainCommons/Gordian/blob/master/Docs/CKM.md), which is expected to become an active project following the deployment of current CSR systems. Currently, CSR is planned for 2022 and CKM for 2023-2024.

### Gordian Reference App: Coordinator (iOS)

**Repo:** [Coordinator](https://github.com/BlockchainCommons/iOS-GordianCoordinator)

Gordian Coordinator is a Multisig Bitcoin transaction coordinator for iOS. It demonstrates the use of request and response envelopes to communicate when creating multisig transactions in a way that is both resilient and easy to use.

<a href="images/projects/Cosigner.png"><img src="images/projects/SeedTool.png" style="border: 1px solid black; float: left; margin-right: 1em" width="110"></a>
### Gordian Reference App: Seed Tool (iOS)

**Repo:** [Seed Tool](https://github.com/BlockchainCommons/GordianSeedTool-iOS)<br>
**Blog:** [Gordian Seed Tool Reveals the Foundations of Cryptography](https://www.blockchaincommons.com/apps/SeedTool-Release/) (7/15/21)

Gordian Seed Tool is Blockchain Commons' most fully featured reference app. It demonstrates independence and resilience by protecting your cryptographic seeds while also making them available for easy use. Using Seed Tool, you can generate seeds and store them securely on your device. You can then derive and share multi-signature signing and verification keys from those seeds or alternatively sign PSBTs directly from the app. Sophisticated backup procedures demonstrate the usage of Sharded Secret Key Reconstruction ([SSKR](https://github.com/BlockchainCommons/crypto-commons/blob/master/Docs/README.md#sharded-secret-key-reconstruction-sskr)) — which lets you split your seed into pieces and send them to trusted parties, who can send them back to you in an emergency for seed recovery. You can even use an entirely offline device (no internet access) to store your seeds and use QR codes to exchange necessary information with online devices running compatible wallet or signing software. A complete [manual](https://github.com/BlockchainCommons/GordianSeedTool-iOS/blob/master/Docs/MANUAL.md) details its functionality.

### Gordian Reference App: Server (MacOS)

**Repo:** [Gordian Server](https://github.com/BlockchainCommons/GordianServer-macOS)<br>

Gordian Server installs a self-sovereign Bitcoin Core server, protected by Tor, on your Mac computer. This gives you complete control over your Bitcoin destiny, and supports easy connectivity with [Gordian Wallet](https://github.com/BlockchainCommons/GordianWallet-iOS), [Fully Noded](https://apps.apple.com/us/app/fully-noded/id1436425586), and other wallets that support the [QuickConnect API](https://github.com/BlockchainCommons/Gordian/blob/master/Docs/Quick-Connect-API.md).

<a href="images/projects/lethekit.jpg"><img src="images/projects/lethekit.jpg" align="right" border="1" width="200"></a>
### Gordian Reference App: LetheKit (kit)

**Repo:** [lethekit](https://github.com/BlockchainCommons/lethekit)<br>
**Blog:** [Blockchain Commons Releases Feature-complete LetheKit](https://www.blockchaincommons.com/apps/Releasing-LetheKit/) (10/28/20)

LetheKit is a do-it-youself platform for performing various sensitive cryptographic operations on an offline airgapped device. It uses no WiFi or Bluetooth which could leak information and contains no local storage, and when the device is turned off it forgets any sensitive data stored in RAM. Thus the name Lethe (lee-thee), from the [mythological river](https://en.wikipedia.org/wiki/Lethe) of forgetfulness and oblivion.

### Gordian Reference App: Spotbit (web)

**Repo:** [spotbit](https://github.com/BlockchainCommons/spotbit)<br>

Spotbit is a portable Flask API for Bitcoin price data and candles. It can either be used as a repository of historical data that allows for more frequent API requests, or as a simple wrapper around exchange APIs that permits the user to collect information over Tor. It can aggregate data from over 100 exchanges and serve them from a single URL or using Tor as an onion hidden service. It's extremely flexible: the user can decide which base currencies to use (USDT, USD, EUR etc), which exchanges to keep data for, and how much data to keep.

### Other Gordian Reference Apps

**Legacy Repos:** [Cosigner iOS](https://github.com/BlockchainCommons/GordianCosigner-iOS), [Cosigner Android](https://github.com/BlockchainCommons/GordianSigner-Android), or [Cosigner macOS](https://github.com/BlockchainCommons/GordianSigner-macOS), [Wallet](https://github.com/BlockchainCommons/GordianWallet-iOS)<br>
**Research Repos:** [Mori-CLI](https://github.com/BlockchainCommons/mori-cli), [Sweeptool](https://github.com/BlockchainCommons/sweeptool-cli)

Several legacy reference apps were initially released to demonstrate specific Principles but have since become outdated or superceded by other applications. Several research reference apps have been written to test out new technologies and new ways to demonstrate our Vision, but haven't been upgraded to full reference status.

<hr>

## Gordian Reference Libraries

_The Gordian Reference Libraries adopt Gordian specifications for programming use. In addition, CLI apps and web apps offer other ways to demonstrate their application._

### Crypto Commons Libraries

**Repos:** [Crypto Commons](https://github.com/BlockchainCommons/crypto-commons#gordian-reference-libraries)

All of the Gordian reference libraries can be found linked from the Crypto Commons repo. Libraries are originally coded in C or C++, but the repo also contains implementations of some libraries for Java, Python, Swift, or other languages.

### Gordian Reference CLI Apps

**CLI Repos:** [bytewords-cli](https://github.com/BlockchainCommons/bytewords-cli), [envelope-CLI](https://github.com/BlockchainCommons/envelope-cli-swift), [keytool-cli](https://github.com/BlockchainCommons/keytool-cli), [LifeHashTool](https://github.com/BlockchainCommons/LifeHashTool), [Musign-CLI](https://github.com/BlockchainCommons/musign-cli), [seedtool-cli](https://github.com/BlockchainCommons/seedtool-cli)

Blockchain Commons also provides many references apps that are meant to be run from the command line, explicitly exercising and demonstrating our reference libraries.

<center><a href="images/projects/keytool.png"><img src="images/projects/keytool.png" align="right" border="1" width="500"></a></center>

### Gordian Web Apps

**LifeHash Demo:** [Lifehash Demo](https://lifehash.info/), [Lifehash Repo](https://github.com/BlockchainCommons/lifehash.info)
**Seedtool Demo:** [Seedtool Demo](https://seedtool.info/), [Seedtool Repo](https://github.com/BlockchainCommons/seedtool.info)

Some Blockchain Commons apps have also been converted to web demos.

<hr>

## Gordian Specifications

The Gordian architecture is ultimately built on specifications that empower our [Vision](https://www.blockchaincommons.com/vision.html).

### Research Papers

**Repo:** [Research](https://github.com/BlockchainCommons/Research)<br>
**Video:** [Overview](https://www.youtube.com/watch?v=RYgOFSdUqWY)

Much of Blockchain Commons' work on specifications begins with Research papers, which describe and detail the use of a new, interoperable specification for blockchain and Bitcoin.

### Envelope Specification

**Repo:** [Secure Components](https://github.com/BlockchainCommons/BCSwiftSecureComponents), [Envelope-CLI](https://github.com/BlockchainCommons/envelope-cli-swift) <br>
**Introduction:** [Docs](https://github.com/BlockchainCommons/BCSwiftSecureComponents/tree/master/Docs)

 The Secure Components suite provides tools for easily implementing encryption (symmetric or public key), signing, and sharding of messages, and representation of knowledge graphs, including serialization to and from CBOR and UR formats. The core of the Secure Components capability suite is the Envelope. This is a smart-document structure that supports the storage, backup, encryption & authentication of data, with explicit support for Merkle-based selective disclosure.
 
<a href="https://raw.githubusercontent.com/BlockchainCommons/LifeHash/master/images/lifehash-grayscale-v2.png"><img src="https://raw.githubusercontent.com/BlockchainCommons/LifeHash/master/images/lifehash-grayscale-v2.png" align="right" border="1" width="400"></a>
### Lifehash Specification

**Repo:** [Overview & Web Demo](https://github.com/BlockchainCommons/lifehash-web)<br>
**Video:** [Explainer Video](https://www.youtube.com/watch?v=cu0K__KLxKo)

LifeHash is a method of hash visualization based on Conway's Game of Life that creates beautiful icons that are deterministic, yet distinct and unique given the input data. The basic concept is to take a SHA256 hash of the input data (which can be any data including another hash) and then use the 256-bit digest as a 16x16 pixel "seed" for running Conway’s Game of Life.

LifeHash is used by Blockchain Commons to create distinct and unique visual representations for your seeds and keys, so that you can recognize them at a glance.

### SSKR Specification

**Paper:** [UR Type Definition for Sharded Secret Key Reconstruction (SSKR)](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2020-011-sskr.md)<br>
**Security Review:** [2021 Review](https://github.com/BlockchainCommons/bc-sskr/blob/master/SECURITY-REVIEW.md)<br>
**Documents:** [SSKR Overview](https://github.com/BlockchainCommons/crypto-commons/blob/master/Docs/sskr-overview.md), [SSKR Share Scenarios](https://github.com/BlockchainCommons/SmartCustody/blob/master/Docs/SSKR-Sharing.md), [SSKR Dangers](https://github.com/BlockchainCommons/SmartCustody/blob/master/Docs/SSKR-Dangers.md)

Blockchain Commons SSKR is an implementation of Sharded Secret Key Reconstruction (SSKR) for use in Blockchain Commons Software Projects. It currently implements Shamir's Secret Sharing, allowing for sharding and reconstruction of a key, to improve Resilience.

### Uniform Resource (UR) Specification

**Papers:** [Uniform Resources (URs)](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2020-005-ur.md), [Registry of UR Types](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2020-006-urtypes.md), [UR Type Definitions for Transactions Between Airgapped Devices](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2021-001-request.md), and others<br>
**Documents:** [UR Overview](https://github.com/BlockchainCommons/crypto-commons/blob/master/Docs/ur-overview.md), [UR Introduction](https://github.com/BlockchainCommons/crypto-commons/blob/master/Docs/ur-1-overview.md)<br>
**Blog:** [Blockchain Commons’ Uniform Resources (URs) Support Airgapped PSBTs & More](https://www.blockchaincommons.com/specifications/Blockchain-Commons-URs-Support-Airgapped-PSBTs/) (12/8/20)<br>
**Test Vectors:** [crypto-request](https://github.com/BlockchainCommons/crypto-commons/blob/master/Docs/crypto-request-test-vectors.md), [crypto-seed](https://github.com/BlockchainCommons/crypto-commons/blob/master/Docs/crypto-seed-test-vectors.md), [SSKR](https://github.com/BlockchainCommons/crypto-commons/blob/master/Docs/sskr-test-vector.md)

UR stands for Uniform Resources, a method for encoding structured binary data in plain-text strings that are also well-formed URIs. It's an interoperability specification that allows for the reliable, typed transfer of data and was designed in particular to allow for reliable transmission of crypto-seeds, crypto-keys, PSBTs, and other data related to cryptocurrency.

One of the particular advantages of UR is careful integration with QR codes, a prime method for transmitting data across airgaps. URs are built to be efficient when encoded as QRs. In addition, multi-part URs allow for the creation of animated QRs, overall containing more information than any single QR could have.

<hr>

## Educational Projects

_Educational projects consist of books, tutorials, or courses, intended to teach the usage of blockchains to programmers and end users alike._

<a href="images/projects/lbtc.png"><img src="images/projects/lbtc.png" align="right" border="1" width="500"></a>
### Learning Bitcoin from the Command Line

**Repo:** [Learning-Bitcoin-from-the-Command-Line](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line)<br>
**Future:** [Topics for v3.0](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line/blob/master/TODO-30.md)<br>
**Blog:** [Learning Bitcoin Upgrades to v2](https://www.blockchaincommons.com/courses/Learning-Bitcoin-Upgrades-to-v2/) (10/30/20)

This is a complete twenty-chapter course intended to teach system administrators, developers, and engineers who are already acquainted with the UNIX command line interface how to work with Bitcoin. It uses this methodology to teach the fundamentals of Bitcoin, from RPC communications to how transactions work and how scripts work. The majority of the course is focused on `bitcoin-cli`, but there's also information on scripting, on programming with the RPC interface, and on using other command-line programs, beginning with `lightning-cli`. Translations are now available for [Portuguese](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line/blob/master/pt/README.md), with the final iteration of [Spanish](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line/tree/spanish-translation/es) pending.

<a href="images/projects/sc.png"><img src="images/projects/sc.jpg" align="right" border="1" width="200"></a>  
### #SmartCustody

**PDF:** [#SC v1.01](https://bit.ly/SmartCustodyBookV101)<br>
**Book Site:** [WWW Site](https://www.smartcustody.com/)
**New Scenarios:** [Multisig Scenario](https://github.com/BlockchainCommons/SmartCustody/blob/master/Docs/Scenario-Multisig.md)
**New Technologies:** [Articles](https://github.com/BlockchainCommons/SmartCustody#smartcustody-tools)
**Case Studies:** [Overview](https://github.com/BlockchainCommons/SmartCustody/blob/master/Docs/Case-Studies-Overview.md)
**Repo:** [SmartCustody Repo](https://github.com/BlockchainCommons/SmartCustody), [SmartCustodyBook](https://github.com/BlockchainCommons/SmartCustodyBook)<br>
**Future:** [Outline for v2.0](https://github.com/BlockchainCommons/SmartCustodyBook/blob/master/TODO.md)<br>
**Blog:** [June TweetStorms on #SmartCustody Adversaries, 1-on-1 Advice, Supporting Smart Custody Book v2](https://www.smartcustody.com/2020-06-03-June-Tweetstorm/) (6/3/20)

_The Use of Advanced Cryptographic Tools to Improve the Care, Maintenance, Control, and Protection of Digital Assets._ This five-chapter (186-page) book is intended to make you rethink the security of your digital assets. It puts together a risk-modeling system with two additional building blocks: a cold-storage scenario for managing self-custody; and an extensively detailed list of potential adversaries. By working through the book, you can determine which adversaries are actually the most dangerous to your assets, and adjust your own self-custody scenario to accomodate them. Additional chapters talk about fiduciary duties with regard to digital assets. 

A v2.0 of this book is in the planning stage, to improve the accessibility of the course, to support additional hardware tools, and to introduce multi-signature scenarios. Our [multisig design article](https://github.com/BlockchainCommons/Gordian/blob/master/Docs/Multisig.md), our [sharding design article](https://github.com/BlockchainCommons/SmartCustody/blob/master/Docs/SSKR-Sharing.md), our [SSKR Dangers article](https://github.com/BlockchainCommons/SmartCustody/blob/master/Docs/SSKR-Dangers.md), [Timelock exploration article](https://github.com/BlockchainCommons/SmartCustody/blob/master/Docs/Timelocks.md), and our [multisig scenario](https://github.com/BlockchainCommons/SmartCustody/blob/master/Docs/Scenario-Multisig.md) will all be incorporated into #SC 2.0 in some form, per our [#SC 2.0 outline](https://github.com/BlockchainCommons/SmartCustodyBook/blob/master/TODO.md).

<hr>

## Advocacy Projects

_Blockchain Commons isn't just about technological development. It also works to ensure that there's a solid legal foundation for our blockchain technologies. That's where Advocacy comes in_.

### Law & Advocacy

**Repo:** [Law & Advocacy Repo](https://github.com/BlockchainCommons/law-and-advocacy)<br>
**Articles:** [Principal Authority](https://www.blockchaincommons.com/articles/Principal-Authority/), [Private Key Disclosure](https://www.blockchaincommons.com/articles/Private-Key-Disclosure/)

Our Law & Advocacy repo includes both research that we've done on the current state of the law and advocacy that we've done to _change_ that status. 

### Testimony

**Repo:** [Testimony Repo](https://github.com/BlockchainCommons/Testimony)

Blockchain Commons has regularly provided testimony to various agencies and instutions. Much of our work has occurred in Wyoming, because they are on the cutting edge of support for blockchains and other digital technologies. This repo theoretically contains links to much of our testimony, but at the moment includes just a few of our links and needs to be filled in.

<hr>

## Events

_One of the prime goals of Blockchain Commons is to bring together different parties to educate and to create consensus on the future development of our technologies and specifications. This happens through events._

<a href="https://raw.githubusercontent.com/BlockchainCommons/siliconsalon.info/master/assets/silicon-salon-1/images/silicon-salon.jpg"><img src="https://raw.githubusercontent.com/BlockchainCommons/siliconsalon.info/master/assets/silicon-salon-1/images/silicon-salon.jpg" border=1 width=300 align="right"></a>
### Silicon Salon

**Website:** [Siliconsalon.info](https://www.siliconsalon.info/)

The Silicon Salon seeks to create semiconductor solutions for cryptography by bringing together semiconductor manufacturers who are interested in creating silicon solutions specifically intended for cryptography with wallet creators and other cryptographic principals. Each event to date has included presentations from principles in the area and discussion among attendees. Our web site includes the presentations and summarizes the discussions.

### Rebooting the Web of Trust

**Website:** [weboftrust.info](https://www.weboftrust.info/)<br>
**GitHub Repos:** [WebofTrust Repos](https://github.com/WebofTrustInfo)

Rebooting the Web of Trust is a semiannual design workshop that was founded by Christopher Allen prior to the foundation of Blockchain Commons; many of its ideas in turn became the heart of our initial work. We continue to attend and support the workshops.

<hr>

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

A instance of Blockchain Commons' Spotbit Bitcoin price-aggregation server, available for public usage.

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
