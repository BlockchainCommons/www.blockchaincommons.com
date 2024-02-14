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
  nav: subpages
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


## Top Articles

The following blog posts are among our most important:

<ul>
{% assign top_posts = site.posts | where_exp: "post", "post.tags contains 'Top Articles'" %}
{% for post in top_posts limit:7 %}
<li><b>{{ post.date | date: "%Y-%m-%d" }}:</b> <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>

See the _[complete posts archive](https://www.blockchaincommons.com/posts/)._

## Major Projects

Current projects include:

* **Collaborative Seed Recovery.** [CSR](https://developer.blockchaincommons.com/csr/) was a major topic for our Gordian Developers community in 2023, and is now advancing with initial work on our [Depo server](https://github.com/BlockchainCommons/bc-depo-rust).
* **dCBOR.** We worked with the IETF and CBOR communities throughout 2023 to advance [dCBOR](https://developer.blockchaincommons.com/dcbor/) and are now finalizing a [draft](https://datatracker.ietf.org/doc/draft-mcnally-deterministic-cbor/).
* **FROST.** Our first [FROST Implementer's Round Table](https://developer.blockchaincommons.com/frost/meeting1/) was in late 2023, with more to come.
  
_See the complete list of Blockchain Commons' [projects](/projects/), its [Developer resources](https://developer.blockchaincommons.com) and our [Technology Overview video](https://www.youtube.com/embed/RYgOFSdUqWY) for more._

## More Info

For more information, see:
* [**Posts**](https://www.blockchaincommons.com/posts/) — News items and articles.
* [**Developers**](https://developer.blockchaincommons.com/) — Resources for our specifications.
* [**Repos**](https://github.com/BlockchainCommons) — Our code & document repos.
* [**Gordian Developer Community**](https://github.com/BlockchainCommons/Gordian-Developer-Community/discussions) — Discussions on our wallet specifications.
* [**Advocacy**](https://advocacy.blockchaincommons.com/) — Advocacy articles & testimony.

If you are interested in actively developing our interoperable specs such as Collaborative Seed Recovery and Gordian Envelope, please also join our [Signal groups or mailing lists](/subscribe/).

## Sustaining Sponsors

Thank you to the following companies who have become [sustaining sponsors](sponsors.html).

<figure class="third">
  <a href="https://bitmark.com/"><img src="/images/sponsors/bitmark-logo-black.png"></a>
  <a href="https://www.chia.net/"><img src="/images/sponsors/chia-logo.png"></a>
  <a href="https://www.crossbar-inc.com/"><img src="/images/sponsors/crossbar-black.png"></a>
  <a href="https://contract.design/"><img src="/images/sponsors/dcd-logo.png"></a>
  <a href="https://foundationdevices.com/"><img src="/images/sponsors/foundation-logo-black.png"></a>
  <a href="https://unchained-capital.com/"><img src="/images/sponsors/unchained-capital-black.png"></a>
</figure>

<br><br>

_Please support Blockchain Commons by becoming a [GitHub sponsor](https://github.com/sponsors/BlockchainCommons) or making a [BTCPay donation](https://btcpay.blockchaincommons.com/)._

## Organization Membership

We are a member of [COPA](https://open-patent.org/), the Crypto Open Patent Alliance. We believe in open software and open access to patents covering foundational cryptocurrency techniques.

<p align="center">
  <a href="https://www.opencrypto.org/"><img src="/images/copa-logo.png" width="33%" align="center"></a>
</p>
