---
header:
  overlay_color: "#00f"
  overlay_filter: "0.5"
  overlay_image: /images/blueprints-linked.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "ZCash & The Advantages of Interoperability"
title: "Musings of a Trust Architect:<br>Interop, What Is It Good For?"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
tags:
  - Zcash
  - Standards
  - Top Articles
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

> _In early 2025, Blockchain Commons architected and engineered a major project for the Zcash blockchain: the ZeWIF specification that allows all of its wallets to interoperate._
>
> _Interoperability is something that I consider vitally important for a technological ecosystem, so I was thrilled that Blockchain Commons could improve interoperability for Zcash. Here's a bit more on why, what Blockchain Commons did for Zcash, and what I'd like to do for other technological communities._

## The Limits of Interop

Obviously, some level of interop is necessary for any ecosystem, or it just wouldn't work. There was a white paper and there are BIPs for Bitcoin; without them, no one could agree on how the blockchain works. We similarly have specifications, RFCs, and standards for everything from email to graphics file formats.

Unfortunately, there are limits to interop. Standards tend to cover the things that are required for the broadest level of intercommunication within an ecosystem. But when companies begin to work on their own apps, their work often turns proprietary—sometimes aggressively so—and that limits a technological ecosystem's ability to continue to grow. 

As an example, email has standards such as [RFC 5322](https://www.rfc-editor.org/rfc/rfc5322) for how mail servers communicate with each other. When mailers begin storing their mail, things become somewhat more balkanized: you might use a classic `mbox` format or a single-message `eml` format or a proprietary format such as Microsoft Outlook's `msg`. Finally, there's no consistency at all for how mailers might algorithmically filter messages: it's hard to control whether a message ends up in the "Important", "Everything Else", or even "Spam" category of Gmail, even if a mailer adopts newer standards such as DKIM, DMARC, and SPF. 

Yet, all of these types of interactions are important. If a mail ends up in a Spam folder, that's almost as bad as it not being delivered at all; if mail can't be restored from a proprietary mailbox, it's lost as well. That's why interop is important.

## The Power of Interop

I developed four core architectural fundamentals for Blockchain Commons that I call the [Gordian Principles](https://developer.blockchaincommons.com/principles/). Of them, ***Privacy*** is only peripherally related to the question of interoperability, but the other three highlight why interop is important for the health of any technological ecosystem.

* ***Independence*** is a user-focused principle. It says that users should be free from external control. This is the heart of my ideas of [self-sovereign identity](https://www.lifewithalacrity.com/article/the-path-to-self-soverereign-identity/), and it's the heart of interoperability too. With the ability to export or exchange data in an interoperable way, users don't get locked into a single platform. Instead, they can choose among a variety of options to find an application, service, or pricing structure that meets their precise needs.
* ***Resilience*** is a data-focused principle. It says that data should be protected from loss. When data output and exchange formats are standardized for interoperability, they become widely used and widely understood. That ensures that they can be recovered far into the future. If you've ever tried to recover an old ClarisWorks or WordStar file, you've seen how much a non-interoperated file format can damage resilience. In comparison, `.rtf` files will never be lost and even `.docx` is pretty good—both because Microsoft Word has an enormous install base and because it's an XML-based output format.
* ***Openness*** is a creator-focused principle. It says that infrastructure should be open so that new creators can join the ecosystem. When communication is standardized, anyone can develop in accordance with the standards, including newcomers. But, this isn't just beneficial to creators, it's also beneficial to users. Without new entrants, an ecosystem can become staid and stagnant. With new entrants, an ecosystem is constantly innovating and expanding. It creates an atmosphere of _coopetition_: members of the ecosystem cooperate to interoperate, but then compete to offer the best products within those standards.

In other words, interoperability is beneficial for the vast majority of members of the ecosystem: users get more options, more innovations, and freedom of choice; creators get the ability to fairly participate and compete; and data gets strong protections far into the future.

## What We Did for Zcash

I was thrilled when members of the Zcash community started talking with me about their needs, because it showed a strong, ecosystem-wide understanding of the need for inteoperability.

But there was also a strong inciting incident that led to the Zcash work: the older [zcashd server was being deprecated](https://z.cash/support/zcashd-deprecation/) and so there was a need to migrate digital-asset data from its wallet to others. This also reflected a longer-term issue. Digital assets had sometimes been [lost during previous migrations](https://forum.zcashcommunity.com/t/shifting-from-zeclite-to-zashi/47756) due to differences or even bugs in different wallets.

Obviously, a one-off migrator could have been created, likely linking zcashd with its replacement wallet, [zallet](https://github.com/zcash/wallet). But I approached things from an architectural point of view: I wanted to create an extensible Wallet Interchange Format (that's the "eWIF" in "ZeWIF") that would not just enable the zcashd migration, but also allow any migration from one wallet to another within the Zcash ecosystem. I wanted to take the immediate needs and political will and turn it into something that could benefit the community for years to come.

That was the [ZeWIF proposal](https://github.com/ZcashCommunityGrants/zcashcommunitygrants/issues/3) that we put forth. It called for one month of studying Zcash wallet data as it currently exists, then another two months of developing the spec and writing libraries to convert among different wallets using that spec. (That timeline turned out to be a bit ambitious, but we're closing out the initial design with a fourth month of work.)

As we release ZeWIF into the ecosystem, we should see advancements in accordance with the Gordian principles:

* ***Independence.*** Users will be able to move their funds easily among Zcash wallets.
* ***Resilience.*** Translation of keys and seeds should be more reliable, and if conversion is done using our [best practices](https://github.com/BlockchainCommons/zmigrate/blob/master/docs/bestpractices.md), there should be clear warnings if anything wansn't converted.
* ***Openness.*** New wallets can join the ecosystem. If they have innovative features, they can easily pick up new users if they support ZeWIF as an import format.

I've been thrilled to have strong support from wallet makers in the Zcash community. That type of buy-in is required to make interoperability work. [Zingo Labs](https://zingolabs.org/), the makers of the Zingo wallet, introduced us to the opportunity and have worked closely with us to fulfill our vision. Meanwhile, [ECC](https://z.cash/ecosystem/electric-coin-company/) has been our next testbed, since they're using ZeWIF to manage conversions between zcashd and zallet. Other principals have been involved as well, and just as importantly we didn't receive any pushback from anyone who refused to use the format. (Not everyone has adopted it yet, but we're just finalizing the complete ZeWIF draft at this point.)

We were fortunate, because that's not always the case.

## What We Did for Bitcoin

This isn't Blockchain Commons' first rodeo. Creating interoperability has been Blockchain Commons' goal since the start, and we've done most of our interop work to date with Bitcoin.

Our two biggest successes for Bitcoin have been [Animated QRs](https://developer.blockchaincommons.com/animated-qrs/) and [SSKR](https://developer.blockchaincommons.com/sskr/). Animated QRs are a standardized way to move large files across airgaps. That's the exact sort of intercommunication that has always required interoperability. SSKR is a standardized way to shard a secret, currently focused on Shamir's Secret Sharing. Because it isn't just about intercommunication, getting a variety of companies to use it was a bigger victory, because it ensures those secrets will remain accessible and resilient into the far future. Both technologies are integrated with our [Uniform Resources](https://developer.blockchaincommons.com/ur/), which have been implemented by [more than a dozen companies](https://developer.blockchaincommons.com/ur/implementations/), offering true interoperability.

But these successes have unfortunately been piecemeal. There's just one company that I'm aware of that's adopted a pretty wide swath of Blockchain Commons' Gordian specifications, and that's our long-time sponsor, [Foundation](https://foundation.xyz/). We  most recently worked with them to support [QuantumLink](https://community.foundation.xyz/t/quantumlink/291), a Post-Quantum-Cryptopgraphy (PQC) method of Bluetooth communication that's in their new [Passport Prime device](https://foundation.xyz/buy-passport-prime/), but they've also implemented URs, Animated QRs, SSKR, and other Blockchain Commons interop specs. As a result, they've got well-studied, mature specifications that they didn't roll themselves and that should be resilient and reliable far into the future. I think that adding in a variety of linked interop specs like this has a multiplicative effect.

I'd love to see more of this in the Bitcoin community, but a lot of people are resistant.

## Why People Fight Interoperability

The primary reason that we see people fight interoperability is market dominance. The Bitcoin ecosystem has grown large enough that some of the bigger players have stepped back from inteoperability

I was sad to see ColdCard go this way, after they themselves built on Trezor and other open-source libraries. At least they've remained source-verifiable (meaning you can view their code in their repo), at least until you get now to the proprietary chip, but they were once one of maybe three hardware wallets that were fully open-source,and so fully interoperable.

But I think the recent release of Ledger Recover was even more of a tragedy. Here they were offering a big innovation: a way to recover seeds by splitting them up and distributing them off device, similar to Blockchain Commons' own [Collaborative Seed Recovery (CSR)](https://z.cash/ecosystem/electric-coin-company/). But by keeping their protocol for distributing and recovering seed shares non-interoperable, they kept anyone else from offering seed vaults of their own, instead locking their users into their choices—which were very unpopular due to  privacy-busting requirements for KYC information.

The exact opposite approach is taken by another of Blockchain Commons' long-time developer partners, Craig Raw of the [Sparrow wallet](https://sparrowwallet.com/). He's working hard to make Sparrow compatible with everything out there, but the difficulty he faces underlines the issues with the semi-interoperable state of most blockchains. He has to make [NASCAR-like lists](https://indieweb.org/NASCAR_problem) of otherwise incompatible products and introduce secret sauce to interoperate with each of them. We're very luck to have the Sparrow wallet working with all of these different devices, but it's something that would never happen if there weren't someone as dedicated as Craig working on the project.

For smaller companies, interoperability is a way in. Obviously, you should do it!

For bigger companies, interoperability means both trusting your engineers to provide the best experience and trusting your customers to recognize it. That's a leap of faith, but one that I'd hope to see most companies make in our industry. After all the idea of personal control is likely one of the reasons that your customers are working with digital assets in the first place!

## The Potential for Other Blockchains

I hope that our work with Zcash (and before that with Bitcoin) is just a first step. I'd like to take that experience to other blockchains and offer new interoperability to grow those ecosystems as well.

Even after the work we've already done, Bitcoin may still need this sort of work the most, because it's gotten so big. How could we make migration between wallets easier? Or just the migration of seeds or keys? How could we more widely standardize the backup of seeds with a methodology like Ledger Recover or our own CSR? How could we inteoperate third-party services such as pricing and fee lookups? Every one of these elements of interoperability would improve the ecosystem, but they require a dedication to inteoperability itself.

The same is true for other ecosystems that have gotten large enough to see multiple companies working on projects. Big changes could be the incentive for this, such as Monero's move to Seraphis. But even without big changes on the horizon, big ecosystems grow to the point where interoperability becomes a requirement: Ethereum has a huge infrastructure built around WalletConnect, but we've talked with people in the ecosystem who think there's real room for improvement. I hope that many chains (and other ecosystems) beyond Monero and Ethereum will see the advantages of improving interoperability for all the reasons I've laid out here, particular independence for users, resilience for data, and openness for developers.

Are you a leader working in a digital-asset ecosystem? Would you like to work with me to take lessons learned from the Zcash project to create interoperable wallet formats, data-exchange formats, service formats, or something else? Drop me a line at <a href="mailto:team@blockchaincommons.com">team@blockchaincommons.com</a>. I'd love to talk about how we can expand your ecosystem as well.
