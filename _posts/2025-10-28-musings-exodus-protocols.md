---
header:
  overlay_color: "#00f"
  overlay_filter: "0.5"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "Five Patterns for Creating Autonomous Infrastructures"
title: "Musings of a Trust Architect: The Exodus Protocol"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
tags:
  - clubs
  - exodus protocol
  - Top Articles
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

It's 2025. Digital infrastructure has become the heart of not just our economy, but our culture. 

But it can be taken from  us in a heart beat.

Those of us in the decentralized space have warned against this future for a long time, but it first hit me in a truly visceral way a decade ago when I was teaching technology leadership at Bainbridge Graduate Institute. I supported my students with a powerful coordination system that tied together del.icio.us bookmarks, Google Reader, and Google Docs. My students could discover information through RSS feeds, collaboratively bookmark and annotate it, and then work with their peers using that shared data. It was an effective tool for both learning and cooperative action that was soon adopted by the whole school.

But then Yahoo sold del.icio.us and Google shut down Reader. Without warning, without a chance to migrate, our learning community's entire digital infrastructure collapsed. A generation of learners was quietly deplatformed from the tools that had empowered them to think, share, synthesize and learn together.

By now, everyone probably has a story of digital infrastructural loss. How they lost their Google+ circles. How their internet radio turned off forever one day. How their digitally stored MP3s disappeared into the ether. It's a pattern that's encouraged by the perverse incentives of capitalism. A useful service becomes essential infrastructure. Companies move in to collect rent on the technology. Then, they exert their power by reducing features and increasing distractions. Eventually, it becomes non-profitable and they kill it. (Cory Doctorow calls this pattern [enshittification](https://pluralistic.net/2022/11/28/enshittification/).)

Which leads to the question that haunts me: _how can we create digital infrastructure that can't be taken from us?_

## Enter the Exodus

To resolve this problem, we need what I call **Exodus Protocols**. These are systems that free us from the control of external sources (like Google or Yahoo! or Sony) by creating infrastructure that doesn't require infrastructure. 

_What in the world do I mean by that?_

There's actually a well-known Exodus Protocol: Bitcoin. It provides financial infrastructure, allowing users to transfer value among themselves, but it does so without enshrining permanent infrastructure or empowering centralized authorities.

Miners can come and go. Full nodes can exist as services, but you can also spin them up locally. Some type of network is important for miners to collect transactions and form them into blocks, but the average user doesn't need that: they can create their own transactions air-gapped and transfer them using QR codes. It's generally hard to censor Bitcoin, and it would be unthinkable for the entirety of it to disappear in any short amount of time.

Bitcoin demonstrated something profound: *that fundamental capabilities can exist as mathematical rights rather than centralized privileges.* When your ability to transact depends on a bank's approval, it's not a right, it's permission. Bitcoin restored transaction as a right through autonomous infrastructure. That's an Exodus Protocol.

Unfortunately, Bitcoin only creates an Exodus Protocol for a small (but important) corner of what we do on the internet: value transfer. It does have some cousins, such as IPFS for data storage, but there aren't great Exodus Protocols for the vast majority of what we do within the digital sphere. We need more Exodus Protocols, to free us from dependency on centralized services, so that our carefully constructed infrastructures don't suddenly disappear, as happened for my students at BGI. We need to empower coordination (whether it be for my students or a board of directors), collaboration (at a forum or on a shared artists' whiteboard), and identity (to correct the [missteps made by the self-sovereign identity movement](https://www.blockchaincommons.com/musings/musings-ssi-bankruptcy/)).

## Five Patterns for Creating Autonomous Infrastructure

An Exodus Protocol is only successful if it's designed to actually empower through autonomous service. We don't want to just create a new digital prison. To design for success requires five architectural principles that help to create the architecture of autonomy itself.

**An Exodus Protocol must ...**

### 1. Operate Without External Dependencies

If something requires permission to operate, it's not autonomous. If it stops working when a company fails or a government objects, it's infrastructure built on sand. 

We instead need truly independent architecture. This can be accomplished either through objects that are self-contained, with everything needed for operation either within the object or derivable through math (e.g., autonomous cryptographic objects such as [Gordian Clubs](https://developer.blockchaincommons.com/clubs/)); or through distributed operations without centralization, where any operator can be replaced.

> **₿ — Bitcoin's approach:** Bitcoin took the distributed approach, with validation, verification, and recording of value transfers done by hundreds of thousands of replaceable independent nodes. There's no central server or authority.

### 2. Encode Rules in Mathematics, Not Policy

Policy means that someone else decides how a service works. They can make arbitrary or biased decisions. They can succumb to coercion, and they can censor.

In contrast, math doesn't discriminate, doesn't take sides, and doesn't change its mind under pressure. Replacing policy rules with mathematical rules means introducing cryptographic proofs such as private keys and signatures. They make verification deterministic: the same inputs always produce the same outputs.

> **₿ — Bitcoin's approach:** With Bitcoin, the control of value is ultimately determined by who holds a private key. Sophisticated systems such as threshold signatures and secret sharding offer more nuanced control.

### 3. Make Constraints Load-Bearing

Constraints make systems less flexible. But, that's not necessarily a bad thing. We just need to ensure that those constraints serve dual purposes by also supporting a system's autonomy.

We must be aware of what constraints mean: how they're helpful and how they're harmful. Then we must design constraints that create the autonomous infrastructure that we want. As an example: if a credential can't expire, then it works forever. Similarly, if it can't be revoked, then it offers perfect access to past content. 

> **₿ — Bitcoin's approach:** Bitcoin offers a number of constraints that strengthen its autonomy largely by building upon mathematics rather than arbitrary policy. Transactions can't be reversed, which means: 🟥 that you can't walk back a mistake; but also that 🟢 your funds can't be seized by fiat. Rules changes require consensus, which means: 🟥 that important updates can require months or years of coordination; but also that 🟢 your funds can't be threatened by an arbitrary increase of supplies.

### 4. Preserve Exit Through Portability

Centralized systems lock you in, which is the opposite of sovereignty. True autonomy requires not just the ability to leave, but the ability to take everything with you. Without the ability to walk away, consent collapses into coercion.

Escaping lock in requires interoperability and open standards. Data and credentials must be portable across implementations without proprietary formats that trap users.

> **₿ — Bitcoin's approach:** Bitcoin keys work in any wallet. Standards for the use of seeds to generate HD keys and the use of wallet descriptors further this interoperability.

### 5. Work Offline and Across Time

Infrastructure that requires connectivity can be denied connectivity. Infrastructure that requires specific platforms can be denied those platforms. 

True autonomy works with whatever channels remain available when coercion attempts to deny others. It requires asynchronous operations, creating services that work during outages and across decades regardless of infrastructural changes.

> **₿ — Bitcoin's approach:** Bitcoin transactions can be signed offline and broadcast later. The protocol doesn't care about internet connectivity for core operations.

## Foundation, Not Fiat

Not every digital service needs to be an Exodus Protocol. In fact, there are definitely services where you want centralization. You want more vulnerable people to be able to recover their funds in case of fraud. You want parents to be able to act as guardians for their children.

But there are services that are irreplaceable and so would benefit from Exodus. These are digital services that store data, create identity, and manage assets that would be difficult to replace. And there are times when Exodus Protocols become more important than ever: when we're under threat, under siege, or just struggling to survive.

We still want to offer the ease of access and usability of centralized services in those situations where they're appropriate, but we want to build those centralized services upon a strong, unwavering foundation of Exodus. If the centralized services fail, there must still be foundations that cannot fall.

## Exodus Technology

Early in the month, I introduced [Gordian Clubs](https://www.blockchaincommons.com/musings/musings-clubs/). They're another example of the Exodus Protocols that I discuss in this article.

Here's how Gordian Clubs, which are Autonomous Cryptographic Objects (ACOs) that can be used to coordinate (by sharing data) and collaborate (by updating data), fulfill the five patterns. 

(This is a repeat of a list from the Gordian Clubs article.)

**Gordian Clubs ...**

1. **Operate Without External Dependencies.** Everything you need is within the Gordian Club: data and permissions truly operate autonomously.
2. **Encode Rules in Mathematics, Not Policy.** Permits are accessed through mathematical (cryptographic) constructs such as private keys or secret shares.
3. **Make Constraints Load-Bearing.** Members can’t be removed from a Gordian Club Edition, but that also means permissions can’t be unilaterally revoked. Gordon Clubs don’t have live interactivity, but that means they can’t be censored by a network.
4. **Preserve Exit Through Portability.** An ACO that can be freely passed around without network infrastructure is the definition of portability.
5. **Work Offline and Across Time.** Gordian Clubs are meant to be used offline; archival is a major use case, allowing access across a large span of time.

There are numerous other technologies that can enable Exodus Protocols. Many of them are puzzle pieces that could be adopted into larger scale solutions. These include:

* **QR Codes.** Data that can be printed or displayed on air-gapped devices and that can be automatically read into other systems.
* **Bluetooth.** Another method for transmitting data when networks are down.
* **Threshold Signatures.** A method of coordination (signing) that typically does not require live interactivity.

Though we haven't previously used the term, Blockchain Commons technologies are often built as Exodus Protocols:

* [**Animated QRs.**](https://developer.blockchaincommons.com/animated-qrs/) Animation extends QRs to allow the automated transmission and reading of larger quantities of data. 
* [**Gordian Envelope.**](https://developer.blockchaincommons.com/envelope/) Envelopes are built to allow selective disclosure of information without a network. They're the foundation of Gordian Clubs.
* [**XID.**](https://developer.blockchaincommons.com/xid/) Also built atop Gordian Envelope, XIDs (eXtensible IDentifiers) are decentralized identifiers that are truly autonomous, avoiding the [failures of the SSI ecosystem](https://www.blockchaincommons.com/musings/musings-ssi-bankruptcy/).

## From Five Patterns to Six Inversions

The threat of our digital infrastructure being taken away from us is part of a larger issue that I call "The Six Inversions." It's the systematic  transformation of rights into revokable privileges in the digital world.

In the physical world, we have property rights that assure us of access to infrastructure, but in the digital world, centralized entities can take away that infrastructure at any time for any reason. We have no rights to property, to justice, to transparency, or to exit. Our contractual power is neutered, and our identity is sold. As a result, digital infrastructure is unstable, which is why we need to create infrastructure without infrastructure, in the form of Exodus Protocols.

I'll write more about the Six Inversions in the future, but for the moment I wanted to point it out as an underlying philosophy for why digital infrastructure is unreliable and must be reimagined. 

It's because we don't have the rights that we expect from the physical world.

## Conclusion

As I said, Exodus Protocols aren't for everyone or everything, but there are situations and services where they're critical.

When we've identified these cases, we can then deploy Exodous Protocol patterns: operating without dependencies, encoding rules in mathematics, making constraints load-bearing, preserving exit through portability, and working offline across time. This creates a blueprint for infrastructure that holds when everything else fails. 

What is your critical infrastructure? What have you spent years building and would be hurt without? What infrastructure's loss would damage your ability to identify yourself, to communicate, to cooperate, or to collaborate? I'd love to hear what they are and to work with you to design the next generation of autonomous infrastructure.

Bitcoin is just the beginning.
