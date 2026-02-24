---
title: "Blockchain Commons Overviews Its Technology in New Video"
excerpt_separator: "<!--more-->"
categories:
  - Introduction
tags:
  - Video
  - Bytewords
  - UR
  - LifeHash
  - SSKR
  - Torgap
  - Airgap
classes:
  - wide
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/video-news-2.png
---

In the last year, Blockchain Commons has produced a large collection of specifications, reference libraries, architectures, and reference utilities meant to improve blockchain infrastructure by enabling interoperability among Bitcoin wallets — and in the future, other cryptocurrency applications, such as Ethereum wallets, and other cryptography programs, such as chat systems, key management programs, and more.

So, _what do Blockchain Commons' technologies do?_ We've just released [a Technology Overview video](https://www.youtube.com/watch?v=RYgOFSdUqWY) that discuses the concepts and foundations underlying our work and also highlights many of our most important technological releases.

<a href="https://www.youtube.com/watch?v=RYgOFSdUqWY"><img width="100%" src="https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/video-news-1.png" style="border:1px solid black;"></a>

<!--more-->

As the video notes, our work is built on a considerable volume of existing literature. We work with [entropy](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=2m56s), [seeds](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=2m39s), and [keys](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=4m45s) and use [airgaps](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=6m34s), [multisigs](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=5m12s), and [secure storage](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=4m6s) to ensure robust key creation, safe key usage, and responsible key management. We also build on crucial technological foundations such as [CBOR](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=11m13s), [CRC-32](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=11m37s), [Fountain Codes](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=14m53s), [QRs](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=8m15s), [SHA-256](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=12m55s), and [Shamir's Secret Sharing](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=13m36s).

This results in a number of core Blockchain Commons technologies:
<img width="30%" src="https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/video-news-2.png" style="border:1px solid black;" align="right">

- [Bytewords](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=16m21s) are a text-encoding method for binary data.
- [Uniform Resources](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=19m58s) support self-describing data that can be used interoperably.
- [LifeHash](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=24m55s) allows for graphical recognition of seeds, keys, and other data.
- [SSKR](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=26m52s) provides new libraries and methodologies for sharding secrets.
- The [Torgap](https://www.youtube.com/watch?v=RYgOFSdUqWY#t=28m46s) architecture creates security by partitioning blockchain services.

The [Technology Overview video](https://www.youtube.com/watch?v=RYgOFSdUqWY) discusses all of this and more.

We are also continuing to produce documents of use for the entire blockchain community, with our newest tutorials offering more depth on how to use the technologies highlighted in this video. That begins with some just-published developer-focused documents that expand on the overview of Uniform Resources (URs) found in the video. [Uniform Resources: An Overview](https://github.com/BlockchainCommons/crypto-commons/blob/master/Docs/ur-1-overview.md) explains how URs are put together, and then [A Guide to Using URs for Key Material](https://github.com/BlockchainCommons/crypto-commons/blob/master/Docs/ur-2-keys.md) looks at `ur:crypto-seed`, `ur:crypto-bip39`, and `ur:crypto-hdkey` as three different ways to transmit key material in a standardized, typed format. (We have more UR docs planned on SSKRs, PSBTs, and our new request and response system.)

The specifications, architectures, references, and documents that we're creating at Blockchain Commons are all meant to improve interoperability among many different vendors, to support the creation of wallets (and future cryptography applications) that enable independence, security, and resilience for their users. We've been working with an [Airgapped Wallet Community](https://github.com/BlockchainCommons/Airgapped-Wallet-Community/discussions) to create these various technologies. If you're designing blockchain applications of your own, we hope you'll view the [video](https://www.youtube.com/watch?v=RYgOFSdUqWY) to see how some of our technologies can help you.

You can also support the continued development of technologies like these, meant to support the entire community by becoming a [sponsor at GitHub](https://github.com/sponsors/BlockchainCommons) or by making a one-time donation [at our BTCPay](https://btcpay.blockchaincommons.com/).
