---
cover: false
header:
  overlay_color: "#000"
  overlay_filter: "0.25"
  overlay_image: /images/qr-background.jpg
title: Welcome to Blockchain Commons
hide_description: true
classes:
  - wide
permalink: /index.html
---

_Advocating for the creation of open, interoperable, secure &
compassionate digital infrastructure to enable people to control their
own digital destiny and to maintain their human dignity online_
{: .notice--info}

Blockchain Commons works with developer communities to design, build, and maintain secure & compassionate decentralized architectures & tools for digital assets & digital identity based on responsible key management; based on our [Gordian Principles](https://github.com/BlockchainCommons/Gordian#gordian-principles) of independence, privacy, resilience, and openness; and based on our [Self-Sovereign Identity Principles](https://github.com/WebOfTrustInfo/self-sovereign-identity/blob/master/self-sovereign-identity-principles.md). Our goal is to reclaim human dignity & authority in the digital world. We also strive to educate & grow the blockchain community through online courses and our work with legislators and regulators.

Blockchain Commons is proudly a “not-for-profit” social benefit corporation, domiciled in Wyoming but operating world-wide. We have a strong commitment to open source and a defensive patent strategy: anyone can use or improve our tools, and no one can take them away. 

_Read more about Blockchain Commons' [vision & objectives](vision.md)._

## News

See the _[Complete Posts Archive](https://www.blockchaincommons.com/posts/)._

<ul>
{% for post in site.posts limit: 7 %}
<li><b>{{ post.date | date: "%Y-%m-%d" }}:</b> <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>

## Projects

Our current projects include:

* [Gordian Products & Technologies](https://github.com/BlockchainCommons/Gordian) — reference apps that demonstrate the [Gordian Principles](https://github.com/BlockchainCommons/Gordian#gordian-principles).
   * [Gordian Seed Tool](https://github.com/BlockchainCommons/GordianSeedTool-iOS) — our premiere reference app, demonstrating how to closely hold a seed and still use it for active management of keys.
* Web demos — demonstrations of specs and apps such as [Lifehash](https://lifehash.info/) and [Seedtool](https://seedtool.info/).
* [Research](https://github.com/BlockchainCommons/Research) — Technical descriptions and docs for our interoperable and open infrastructural and architectural specifications, such as [Uniform Resources (URs)](https://github.com/BlockchainCommons/crypto-commons/blob/master/Docs/ur-1-overview.md), [Sharded Secret Key Reconstruction (SSKR)](https://github.com/BlockchainCommons/crypto-commons/blob/master/Docs/sskr-developers.md), [Bytewords](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2020-012-bytewords.md), and [Lifehash](https://github.com/BlockchainCommons/lifehash.info).
* [Crypto Commons Libraries](https://github.com/BlockchainCommons/crypto-commons) — reference libraries providing access to interoperable and open infrastructural and architectural specifications, including [Shamir's Secret Sharing](https://github.com/BlockchainCommons/bc-shamir), [Sharded Secret Key Reconstruction (SSKR)](https://github.com/BlockchainCommons/bc-sskr), [Uniform Resources (URs)](https://github.com/BlockchainCommons/bc-ur), [Lifehash](https://github.com/BlockchainCommons/bc-lifehash), [Bytewords](https://github.com/BlockchainCommons/bc-bytewords), and more.
* [Learning Bitcoin from the Command Line](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line) — our educational course introducing blockchains and Bitcoin development.
* [#SmartCustody](https://www.smartcustody.com/) — our educational course laying out the foundation of responsible key management.
* [**Non-partisan Advocacy**](https://github.com/BlockchainCommons/Testimony/blob/master/README.md) — promotion of legislation protecting technology & digital civil rights to ensure secure & compassionate digital infrastructure.

This video overviews many of our specifications and other initiatives:

<p style="margin-left:50px">
<iframe width="400" height="225" src="https://www.youtube.com/embed/RYgOFSdUqWY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>

We also offer services to the improve the security and infrastructure of the larger blockchain ecosystem:

* Infrastructure — support of Tor exit nodes and other blockchain infrastructure & software.
* Security Reviews — risk-based assessments of custody methodologies, operational security procedures, and layer-2 protocols such as payment channels.
* Project Support — contractual support of our open-source projects such as Gordian Seed Tool and for our specs and libraries.

If you are interested in working with us directly on a Security Review or Support for using a project with your business, please [contact us](mailto:team@blockchaincommons.com).

These are just the beginning! Blockchain Commons is also working on other cryptographic research, cryptographic & privacy protocol implementations, architecture & code reviews, industry standards, and documentation. Our more future-looking research includes work on identity wallets, social-recovery techniques, zero-knowledge curve-operation proofs, advanced cryptographic primitives such as Schnorr, MuSig, and scriptless scripts, and in general establishing multi- and cross-blockchain standards.

If you support the goals and projects of Blockchain Commons, please consider becoming a [Sponsor](https://www.blockchaincommons.com/sponsors.html).

## More Info

For more information, see our [Posts](https://www.blockchaincommons.com/posts/) and [GitHub](https://github.com/BlockchainCommons), including the following discussions areas:
* [**Gordian Developer Community**](https://github.com/BlockchainCommons/Gordian-Developer-Community/discussions). For standards and open-source developers who want to talk about interoperable wallet specifications, please use the Discussions area of the [Gordian Developer Community repo](https://github.com/BlockchainCommons/Gordian-Developer-Community/discussions). This is where you talk about Gordian specifications such as [Gordian Envelope](https://github.com/BlockchainCommons/Gordian/tree/master/Envelope#articles), [bc-shamir](https://github.com/BlockchainCommons/bc-shamir), [Sharded Secret Key Reconstruction](https://github.com/BlockchainCommons/bc-sskr), and [bc-ur](https://github.com/BlockchainCommons/bc-ur) as well as the larger [Gordian Architecture](https://github.com/BlockchainCommons/Gordian/blob/master/Architecture/README.md), its [Principles](https://github.com/BlockchainCommons/Gordian#gordian-principles) of independence, privacy, resilience, and openness, and its macro-architectural ideas such as functional partition (including airgapping, the original name of this community).
* [**Gordian User Community**](https://github.com/BlockchainCommons/Gordian/discussions). For users of the Gordian reference apps, including [Gordian Coordinator](https://github.com/BlockchainCommons/iOS-GordianCoordinator), [Gordian Seed Tool](https://github.com/BlockchainCommons/GordianSeedTool-iOS), [Gordian Server](https://github.com/BlockchainCommons/GordianServer-macOS), [Gordian Wallet](https://github.com/BlockchainCommons/GordianWallet-iOS), and [SpotBit](https://github.com/BlockchainCommons/spotbit) as well as our whole series of [CLI apps](https://github.com/BlockchainCommons/Gordian/blob/master/Architecture/Apps.md#cli-apps). This is a place to talk about bug reports and feature requests as well as to explore how our reference apps embody the [Gordian Principles](https://github.com/BlockchainCommons/Gordian#gordian-principles).
* [**Blockchain Commons Discussions**](https://github.com/BlockchainCommons/Community/discussions) — for developers, interns, and patrons of Blockchain Commons, please use the discussions area of the [Community repo](https://github.com/BlockchainCommons/Community) to talk about general Blockchain Commons issues, the intern program, or topics other than Gordian Development or Usage.

## Sustaining Sponsors

Thank you to the following sponsors who have become [sustaining sponsors](https://github.com/sponsors/BlockchainCommons) of Blockchain Commons.
  
[<img src="images/sponsors/bitmark-logo.png" width="30%" align="center">](https://bitmark.com/)
[<img src="images/sponsors/blockchainbird.png" width="30%" align="center">](https://github.com/blockchainbird/bird)
[<img src="images/sponsors/chia-logo.png" width="30%" align="center">](https://www.chia.net/)

[<img src="images/sponsors/crossbar.png" width="30%" align="center">](https://www.crossbar-inc.com/)
[<img src="images/sponsors/foundation-logo.png" width="30%" align="center">](https://foundationdevices.com/)
[<img src="images/sponsors/proxy.png" width="30%" align="center">](https://www.proxy.com/)

[<img src="images/sponsors/unchained-capital.png" width="30%" align="center">](https://unchained-capital.com/)

<br clear="all">[*Learn more about them.*](sponsors)

Please support Blockchain Commons by becoming a [GitHub sponsor](https://github.com/sponsors/BlockchainCommons) or making a [BTCPay donation](https://btcpay.blockchaincommons.com/).

## Organization Membership

We are a member of [COPA](https://open-patent.org/) , the Crypto Open Patent Alliance. We believe in open software and open access to patents covering foundational cryptocurrency techniques.

<p align="center">
  <a href="https://www.opencrypto.org/"><img src="images/copa-logo.png" width="33%" align="center"></a>
</p>
