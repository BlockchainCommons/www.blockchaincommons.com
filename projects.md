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



### Spotbit

**Repo:** [spotbit](https://github.com/BlockchainCommons/spotbit)<br>
**Status:** Late Alpha

Spotbit is a portable Flask API for Bitcoin price data and candles. It can either be used as a repository of historical data that allows for more frequent API requests, or as a simple wrapper around exchange APIs that permits the user to collect information over Tor. It can aggregate data from over 100 exchanges and serve them from a single URL or using Tor as an onion hidden service. It's extremely flexible: the user can decide which base currencies to use (USDT, USD, EUR etc), which exchanges to keep data for, and how much data to keep.

## Developer Projects

_Developer projects create resources for use by engineers and programmers._

### C Libraries

**Repos:** [bc-crypto-base](https://github.com/BlockchainCommons/bc-crypto-base), [bc-shamir](https://github.com/blockchainCommons/bc-shamir/), [bc-sskr](https://github.com/BlockchainCommons/bc-sskr), [bc-bip39](https://github.com/BlockchainCommons/bc-bip39), and [bc-ur](https://github.com/BlockchainCommons/bc-ur)<br>
**Status:** Feature-complete beta

Blockchain Commons offers a variety of C-language cryptographic libraries focuses largely on wallet design, which can be used in your own projects. The currently libraries include 
reference implementations of [BIP39](https://github.com/BlockchainCommons/bc-bip39), [Shamir Secret Sharing](https://github.com/blockchainCommons/bc-shamir/), [Shamir Secret Key Recovery](https://github.com/BlockchainCommons/bc-sskr), and [Uniform Resources](https://github.com/BlockchainCommons/bc-ur). The usage of these libraries is also demonstrated in [the keytool app](https://github.com/blockchainCommons/bc-keytool-cli) and the [seedtool app](https://github.com/blockchainCommons/bc-seedtool-cli).

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
