---
cover: false
header:
  overlay_color: "#000"
  overlay_filter: "0.25"
  overlay_image: /images/qr-background.jpg
  og_image: /images/bcc-card.jpg
title: Welcome to Blockchain Commons
hide_description: true
classes:
  - wide
permalink: /home/
redirect_from: /index.html
sidebar:
  nav: sites
---

_Advocating for the creation of open, interoperable, secure &
compassionate digital infrastructure to enable people to control their
own digital destiny and to maintain their human dignity online_
{: .notice--info}

Blockchain Commons works with developer communities to design, build, and maintain secure & compassionate decentralized architectures & tools for digital assets & digital identity based on responsible key management; based on our [Gordian Principles](https://github.com/BlockchainCommons/Gordian#gordian-principles) of independence, privacy, resilience, and openness; and based on our [Self-Sovereign Identity Principles](https://github.com/WebOfTrustInfo/self-sovereign-identity/blob/master/self-sovereign-identity-principles.md). Our goal is to reclaim human dignity & authority in the digital world. We also strive to educate & grow the blockchain community through online courses and our work with legislators and regulators.

Blockchain Commons is proudly a “not-for-profit” social benefit corporation, domiciled in Wyoming but operating world-wide. We have a strong commitment to open source and a defensive patent strategy: anyone can use or improve our tools, and no one can take them away. 

_Read more about Blockchain Commons' [vision & objectives](vision.md)._

## News

<ul>
{% for post in site.posts limit: 7 %}
<li><b>{{ post.date | date: "%Y-%m-%d" }}:</b> <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>

See the _[complete posts archive](https://www.blockchaincommons.com/posts/)._

## Projects

This video overviews many of our specifications and other initiatives:

<p style="margin-left:50px">
<iframe width="400" height="225" src="https://www.youtube.com/embed/RYgOFSdUqWY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>

The Blockchain Commons projects are built atop the [Gordian
Architecture](https://www.blockchaincommons.com/projects.html#the-gordian-architecture),
the [Gordian
Specifications](https://www.blockchaincommons.com/projects.html#gordian-specifications),
and our [Gordian Use
Cases](https://www.blockchaincommons.com/projects.html#gordian-use-cases). They
include [developer
support](https://www.blockchaincommons.com/projects.html#gordian-developer-support)
and [reference
apps](https://www.blockchaincommons.com/projects.html#gordian-reference-apps), plus [events](https://www.blockchaincommons.com/projects.html#events), [educational projects](https://www.blockchaincommons.com/projects.html#events), [advocacy projects](https://www.blockchaincommons.com/projects.html#advocacy-projects), and [open infrastructure projects](https://www.blockchaincommons.com/projects.html#open-infrastructure-projects).

_See the complete list of Blockchain Commons' [projects](projects.html)._

## More Info

For more information, see our [Posts](https://www.blockchaincommons.com/posts/) and [GitHub](https://github.com/BlockchainCommons), including the following discussions areas:
* [**Gordian Developer Community**](https://github.com/BlockchainCommons/Gordian-Developer-Community/discussions). For standards and open-source developers who want to talk about interoperable wallet specifications, please use the Discussions area of the [Gordian Developer Community repo](https://github.com/BlockchainCommons/Gordian-Developer-Community/discussions). This is where you talk about Gordian specifications such as [Gordian Envelope](https://github.com/BlockchainCommons/Gordian/tree/master/Envelope#articles), [bc-shamir](https://github.com/BlockchainCommons/bc-shamir), [Sharded Secret Key Reconstruction](https://github.com/BlockchainCommons/bc-sskr), and [bc-ur](https://github.com/BlockchainCommons/bc-ur) as well as the larger [Gordian Architecture](https://github.com/BlockchainCommons/Gordian/blob/master/Architecture/README.md), its [Principles](https://github.com/BlockchainCommons/Gordian#gordian-principles) of independence, privacy, resilience, and openness, and its macro-architectural ideas such as functional partition (including airgapping, the original name of this community).
* [**Gordian User Community**](https://github.com/BlockchainCommons/Gordian/discussions). For users of the Gordian reference apps, including [Gordian Coordinator](https://github.com/BlockchainCommons/iOS-GordianCoordinator), [Gordian Seed Tool](https://github.com/BlockchainCommons/GordianSeedTool-iOS), [Gordian Server](https://github.com/BlockchainCommons/GordianServer-macOS), [Gordian Wallet](https://github.com/BlockchainCommons/GordianWallet-iOS), and [SpotBit](https://github.com/BlockchainCommons/spotbit) as well as our whole series of [CLI apps](https://github.com/BlockchainCommons/Gordian/blob/master/Architecture/Apps.md#cli-apps). This is a place to talk about bug reports and feature requests as well as to explore how our reference apps embody the [Gordian Principles](https://github.com/BlockchainCommons/Gordian#gordian-principles).
* [**Blockchain Commons Discussions**](https://github.com/BlockchainCommons/Community/discussions) — for developers, interns, and patrons of Blockchain Commons, please use the discussions area of the [Community repo](https://github.com/BlockchainCommons/Community) to talk about general Blockchain Commons issues, the intern program, or topics other than Gordian Development or Usage.

If you are interested in actively developing our interoperable specs such as Collaborative Seed Recovery and Gordian Envelope, please also join our [Signal groups or mailing lists](subscribe.html).

## Sustaining Sponsors

Thank you to the following companies who have become [sustaining sponsors](sponsors.html).

<figure class="third">
  <a href="https://bitmark.com/"><img src="/images/sponsors/bitmark-logo-black.png"></a>
  <a href="https://www.chia.net/"><img src="/images/sponsors/chia-logo.png"></a>
  <a href="https://www.crossbar-inc.com/"><img src="/images/sponsors/crossbar-black.png"></a>
  <a href="https://contract.design/"><img src="/images/sponsors/dcd-logo.png"></a>
  <a href="https://foundationdevices.com/"><img src="/images/sponsors/foundation-logo-black.png"></a>
  <a href="https://www.proxy.com/"><img src="/images/sponsors/proxy-black.png"></a>
  <a href="https://unchained-capital.com/"><img src="/images/sponsors/unchained-capital-black.png"></a>
</figure>

<br><br>

_Please support Blockchain Commons by becoming a [GitHub sponsor](https://github.com/sponsors/BlockchainCommons) or making a [BTCPay donation](https://btcpay.blockchaincommons.com/)._

## Organization Membership

We are a member of [COPA](https://open-patent.org/), the Crypto Open Patent Alliance. We believe in open software and open access to patents covering foundational cryptocurrency techniques.

<p align="center">
  <a href="https://www.opencrypto.org/"><img src="/images/copa-logo.png" width="33%" align="center"></a>
</p>
