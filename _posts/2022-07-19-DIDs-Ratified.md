---
title: "Seven Years Later: DIDs Have Been Ratified!"
excerpt_separator: "<!--more-->"
categories:
  - News
  - Specifications
tags:
  - DID
  - W3C
classes:
  - wide
---
Congratulations to W3C on the ratification of [DID v1.0](https://www.w3.org/TR/did-core/) as a W3C standard!

![](/images/did-image-1.svg)

Though Blockchain Commons has only lightly touched upon DIDs to date, they nonetheless are a crucial part of our history. In addition, their ratification today as an international standard demonstrates the ability of a cooperative commons to incubate ideas that will eventually be adopted as standards to be used widely by governments, corporations, and individuals.

<!--more-->

Blockchain Commons' Christopher Allen began experiments with decentralized identifiers in late 2014 when he built on his previous work as the co-author of the TLS spec by suggesting a [hack to TLS](https://github.com/ChristopherA/revocable-self-signed-tls-certificates-hack) that associated X.509 certificates with Bitcoin addresses and then allowed revocation of those certs by spending the Bitcoin. It was a decentralized solution to the centralized problem of certificate authorities. Around the same time, Dave Longley and Manu Sporny were exploring similar ideas around identifiers and decentralization in the [W3C Web Payments Community Group](https://web-payments.org/minutes/2014-05-07/). Then, in 2015, Christopher began work with Drummond Reed and others from Respect Network as part of the XDI Registry Working Group, whose goal was to explore possibilities for a decentralized and rootless registry of identifiers; a strawman was presented at [IIW 21](https://iiw.idcommons.net/A_Registry_Directory_~_based_on_BLOCKCHAIN_that_is_ROOTless_%26_NOT_Centralized).

That presentation led to interest from Anil John of the Science and Technical Directorate at the Department of Homeland Security, who was looking for alternative identifiers to the US Social Security Number that also provided clear differentiation between identifier and authenticator functions. Christopher helped to coordinate a community effort that led to both Drummond Reed at Respect Network and Manu Sporny at Digital Bazaar submitting proposals to the Identity Management and Data Privacy R&D Program. The goal was to show wide community interest in decentralized identity. Not only did both companies receive a grant, but they also both received additional funds through round two of the program.

Much of the community's support for DIDs then occurred through the [Rebooting the Web of Trust design workshop](https://www.weboftrust.info/) that Christopher founded in November 2015 to mark the upcoming 25th anniversary of PGP. One of the five papers that were published following that first workshop was the massive [Decentralized Public Key Infrastructure paper](https://github.com/WebOfTrustInfo/rwot1-sf/blob/master/final-documents/dpki.pdf), which included as one of its design principles that "each principal must be in complete control of their current identifier/public-key binding", but had not yet settled on questions such as whether decentralized identifiers should be usernames or UUIDs.

DIDs themselves saw their first major workshopping at RWOT 2, which was run in conjunction with the [ID2020 conference](https://medium.com/id2020/id2020-holds-inaugural-summit-at-the-united-nations-7112014add5e) at the United Nations in May 2016. Drummond Reed and Les Chasen of Respect Network produced the initial paper on the [Requirements for DIDs](https://github.com/WebOfTrustInfo/rwot2-id2020/blob/master/final-documents/requirements-for-dids.pdf), supported by that US Department of Homeland Security grant. That was also the workshop that brought in Manu Sporny's work on [Verifiable Credentials](https://www.w3.org/TR/vc-data-model/), which required an identifier to work with, and so was quickly dovetailed into the project.

Christopher has been constantly involved with the iterations of the DID specification that followed, beginning with the [DID Data Model and Generic Syntax Implementer's Draft 01](https://github.com/WebOfTrustInfo/rwot3-sf/blob/master/final-documents/did-implementer-draft-10.pdf) that was written at RWOT 3 in San Francisco, where he worked with Drummond and Les as well as Ryan Grant. More designs followed across the subsequent Rebooting the Web of Trust events, including a massive DID breakout room at RWOT 5 in Boston, which spent the length of the conference refining the growing spec. Many, many more people contributed to the evolution of the design, among them: Daniel Buchner, who spearheaded Microsoft's support of DIDs and with Microsoft's backing created the Decentralized Identity Foundation (DIF); and Joe Andrieu, who led the work on the [DID Method Rubric](https://www.w3.org/TR/did-rubric/), a way to evaluate DID methods, as well as foundational use cases and engagement models for decentralized identity such as [Joram](https://github.com/WebOfTrustInfo/rwot3-sf/blob/master/final-documents/joram-engagement-model.pdf) and [Amira](https://github.com/WebOfTrustInfo/rwot5-boston/blob/master/final-documents/amira.pdf) and the [Use Cases and Requirements for Decentralized Identifiers document](https://www.w3.org/TR/did-use-cases/).

As part of his work on the preliminary DID spec, Christopher became one of the co-chairs of the W3C Credentials Community Group alongside Joe Andrieu and Kim Hamilton Duffy. There, he co-authored and co-architected the DID spec to be presented to the W3C. He has also been an invited expert at the DID Working Group since its advent in September 2019. Today, July 19, 2022, that Working Group's work became a "W3C Recommendation" and thus an official international standard. Our congratulations to DID Working Group chairs Daniel Burnett and Brent Zundel, to DID editors Manu Sporny, Amy Guy, Markus Sabadello, and Drummond Reed, and to everyone who has spent the last seven years working on turning the ideas incubated in New York, San Francisco, Boston, and elsewhere into a real specification that can change the world by giving people control over their digital identifiers.

![](/images/did-image-2.svg)

Besides his work on the DID spec itself, Christopher is also one of the architects alongside Kim Hamilton Duffy, Ryan Grant, and Dan Pape, behind [the BTCR DID method](https://w3c-ccg.github.io/didm-btcr/), which has been dubbed the ["granddaddy of DIDs"](https://the-rubric.castos.com/podcasts/23899/episodes/the-granddaddy-of-dids-didbtcr). This DID method anchors decentralized identifiers on the Bitcoin blockchain, very similar to the X.509 cert revocation that Christopher was advocating back in 2014.

Blockchain Commons was founded in 2018 to support the ideas and community that came out of Rebooting the Web of Trust. Though Blockchain Commons proper has not published much on DIDs, except as an educational topic for our interns, it continues to be a future focus for us, with the idea of decentralized identifiers being a crucial assumption for our Gordian architecture. Christopher also continues to be an invited expert on Verifiable Credentials 2.0 and has advocated for the DID spec throughout its ratification process. Our expertise with DIDs and with BTCR leaves this all as an open opportunity for Blockchain Commons. If you've considered becoming a [sponsor](https://github.com/sponsors/BlockchainCommons) of Blockchain Commons and are interested in DID work, please [drop us a line](mailto:team@blockchaincommons.com) to discuss the topic!

_Illustrations drawn from [DID v1.0 spec](https://www.w3.org/TR/did-core/)._
