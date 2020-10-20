---
cover: false
hide_description: true
permalink: /projects.html
---

Blockchain Commons is working on a large variety of projects all intended to improve the entirety of the community who is using blockchain technology and developing it.

## Open Infrastructure Projects

_Open infrastructure projects create resources that can be used by the entire internet community._

### Spotbit Server

**Onion Address:** h6zwwkcivy2hjys6xpinlnz2f74dsmvltzsd4xb42vinhlcaoe7fdeqd.onion<br>
**Related Repo:** [spotbit](https://github.com/BlockchainCommons/spotbit)

A instance of Blockchain Commons' Spotbit Bitcoin price-aggregation server, available for public usage.

### Testnet Public Node

### Tor Exit Node

## Self-sovereign Bitcoin Projects

_Self-sovereign Bitcoin projects give users more agency in their interactions with the Bitcoin blockchain, so that they're not dependent on anyone else._

### The Gordian System

**Repo:** [Gordian](https://github.com/BlockchainCommons/Gordian)<br>
**Status:** Varied

The Gordian system is a suite of powerful open-source tools that offers a self-sovereign solution for Bitcoin by using Tor and QuickConnect technology to link a protected GordianServer with a mobile GordianWallet so that you access full-node capabilities from a mobile device. (It's meant to cut through a traditionally knotty problem in Bitcoin development.)

Elements of the Gordian System include [GordianWallet-iOS](https://github.com/BlockchainCommons/GordianWallet-iOS), [GordianServer-MacOS](https://github.com/BlockchainCommons/GordianServer-macOS), and the alternative [Bitcoin Standup Linux Scripts](https://github.com/BlockchainCommons/Bitcoin-StandUp-Scripts), as well as the [QuickConnect API](https://github.com/BlockchainCommons/Gordian/blob/master/Docs/Quick-Connect-API.md) that links them all together. The newest member of the Gordian System is GordianSigner, which support PSBT signing and multisignatures. It's available for [Android](https://github.com/BlockchainCommons/GordianSigner-Android), [Catalyst](https://github.com/BlockchainCommons/GordianSigner-Catalyst), and [macOS](https://github.com/BlockchainCommons/GordianSigner-macOS).

### LetheKit

<a href="images/projects/lethekit.jpg"><img src="images/projects/lethekit.jpg" align="right" width="150"></a>
**Repo:** [bc-lethekit](https://github.com/BlockchainCommons/bc-lethekit)<br>
**Status:** Late Alpha

LetheKit is a do-it-youself platform for performing various sensitive cryptographic operations on an offline airgapped device. It uses no WiFi or Bluetooth which could leak information and contains no local storage, and when the device is turned off it forgets any sensitive data stored in RAM. Thus the name Lethe (lee-thee), from the mythological river of forgetfulness and oblivion.

### Spotbit

**Repo:** [spotbit](https://github.com/BlockchainCommons/spotbit)<br>
**Status:** Late Alpha

Spotbit is a portable Flask API for Bitcoin price data and candles. It can either be used as a repository of historical data that allows for more frequent API requests, or as a simple wrapper around exchange APIs that permits the user to collect information over Tor. It can aggregate data from over 100 exchanges and serve them from a single URL or using Tor as an onion hidden service. It's extremely flexible: the user can decide which base currencies to use (USDT, USD, EUR etc), which exchanges to keep data for, and how much data to keep.

## Developer Projects

_Developer projects create resources for use by engineers and programmers._

### C Libraries

### Keytool

### Seedtool

## Educational Projects

_Educational projects consist of books, tutorials, or courses, intended to teach the usage of blockchains to programmers and end users alike._

### Learning Bitcoin from the Command Line

<a href="images/projects/lbtc.png"><img src="images/projects/lbtc.png" align="right" width="150"></a>
**Repo:** [Learning-Bitcoin-from-the-Command-Line](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line)<br>
**Status:** v2.0 Complete (2020-10-20)

This is a complete nineteen-chapter course intended to teach system administrators, developers, and engineers who are already acquainted with the UNIX command line interface how to work with Bitcoin. It uses this methodology to teach the fundamentals of Bitcoin, from RPC communications to how transactions work and how scripts work. The majority of the course is focused on `bitcoin-cli`, but there's also information on scripting, on programming with the RPC interface, and on using other command-line programs, beginning with `lightning-cli`. 

### #SmartCustody

<a href="images/projects/sc.png"><img src="images/projects/sc.jpg" align="right" width="150"></a>
**PDF:** [#SC v1.01](https://bit.ly/SmartCustodyBookV101)<br>
**Repo:** [SmartCustodyBook](https://github.com/BlockchainCommons/SmartCustodyBook)<br>
**Status:** v1.01 Complete (2019-09-16)

_The Use of Advanced Cryptographic Tools to Improve the Care, Maintenance, Control, and Protection of Digital Assets._ This five-chapter (186-page) book is intended to make you rethink the security of your digital assets. It puts together a risk-modeling system with two additional building blocks: a cold-storage scenario for managing self-custody; and an extensively detailed list of potential adversaries. By working through the book, you can determine which adversaries are actually the most dangerous to your assets, and adjust your own self-custody scenario to accomodate them. Additional chapters talk about fiduciary duties with regard to digital assets. 

A v2.0 of this book is in the planning stage, to improve the accessibility of the course, to support additional hardware tools, and to introduce multi-signature scenarios.

