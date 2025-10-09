---
header:
  overlay_color: "#00f"
  overlay_filter: "0.5"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "Preserving Agency When Infrastructure Fails"
title: "Musings of a Trust Architect: The Gordian Club"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
tags:
  - clubs
  - Standards
  - Top Articles
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

___Imagine:___ A reporter maintains a list of sources and the information they provided for an article critical of the federal government. This is a requirement for fact-checking any serious news story or for later defending it in a court of law. But the federal government illegally seizes the list and jails the sources.

___Imagine:___ A protest group uses a supposedly secure messaging app to coordinate, but the government threatens the app store, who substitutes a version that records all of the information that should be encrypted. The government then begin arresting participants at home, before the protests even begin.

___Imagine:___ An immigrant flees a totalitarian regime. They carry with them a digital cache of their identity credentials, which will be necessary to immigrate elsewhere. But a border patrol catches them exiting their country and confiscates their records. The government uses their control of internet infrastructure to block future attempts to verify the credentials, which all [phone home](https://www.blockchaincommons.com/news/No-Phone-Home/). The emigrant is let go, but now not only cannot immigrate, but will also have problems proving their identity in their own country.

These stories are unfortunately no longer restricted to problematic countries on the edge of global democratic society: authoritarianism is spreading across the entire world. In the United States alone, unwarranted searches and seizures, violations of free speech rights, and illegal use of military forces for domestic peacekeeping are  on the rise. As a result: unencrypted data is no long safe, because we can't be certain it won't be illegally seized; centralized services are no longer trustworthy, because they have shown that they will bow to dictatorial whims; and centralized servers are no longer reliable, because their usage could be censored through infrastructural control.

Protecting data, especially in a world of services that profit off of user content, is a serious problem that I've long struggled with. Unfortunately, the problem is coming to a head. In a globally connected society, we can no longer trust data, servers, or services that are outside of our personal control. New solutions are required, not just to ensure our human rights, but to ensure our personal safety.

## The Rise of Autonomy

Fortunately, Bitcoin trailblazed the path for another way. Bitcoin protects a user's assets (and their ability to transact) with decentralized protocols that depend on math rather than the fiat of whatever entity controls a server or service. But Bitcoin is largely limited to protecting "value transfer." There's a lot more ground to cover.

That's where Blockchain Commons' newest technology comes into play: the _autonomous cryptographic object_ (ACO). It can protect many other sorts of digital interactions, and it pretty much does what it says on the label.

**The Power of Autonomy:** Autonomy means the ability to make your own choices: self-government. It's a word that should be right up there with _privacy_ and _self-sovereignty_ as a fundamental digital right. But to truly maintain self-control requires you not to be dependent on external entities. That's the core of the "A" in ACO.

This might be the most important part of an ACO because it creates a number of fundamental advantages:

* **Unblockable Access.** No server or platform dependencies.
* **Perfect Privacy.** No logs or tracking.
* **Disaster Resilience.** Available during infrastructure failure.
* **Censorship Resistance.** No fiat controlling access.

**The Power of Cryptography:** Meanwhile, cryptography is the math. The "C" in ACO says that your autonomous control of the object is dependent upon set mathematical rules rather the arbitrary decision of some external force. It's what allows you to escape the fragility of centralized servers: math doesn't bow to authoritarian dictates.

**The Power of Objects:** Finally, the "O" in ACO isn't just a neutral descriptor. It says that an ACO is a discrete (and, yes, autonomous) thing that can be stored or passed around as users see fit, without the need for a specific network. Calling it an object differentiates it from a client or a server or something else dependent on a global communication infrastructure.

Using ACOs is a paradigm shift. Traditionally, access control was at the whim of administrators. With ACOs, access control (and the information they protect) is determined by the pure math of cryptography instead. It's a change from the serfdom of asking "Mother, May I?" to the agency of saying "Yes, I Can." It creates infrastructure that you control, rather than infastructure that controls you.

## Join the Gordian Club

I don't want ACOs to just be a theory, so I've been working in recent months to create a working example of an ACO at Blockchain Commons: the [Gordian Club](https://developer.blockchaincommons.com/clubs/).

A Gordian Club is an ACO built on [Gordian Envelope](https://developer.blockchaincommons.com/envelope/) (along with the rest of the [Gordian Stack](https://developer.blockchaincommons.com/clubs/technology/)). It allows for the storage of credentials, data, or other information in an organized and protected way. Access control is managed by Permits.

* **Envelope.** Gordian Envelope allows for the “smart” storage of information as a recursive set of semantic triplets.
* **Permit.** Envelopes can be encrypted, with permits allowing for the decryption of that data in a variety of ways.

A Gordian Club's permits allow the encoding of either read or write permissions. These permissions can be simultaneously linked to public keys, to [XIDs](https://developer.blockchaincommons.com/xid/), and to secret shares, because envelope permits can enable different means of access to the same data. Permission can also be [delegated](https://developer.blockchaincommons.com/clubs/ocaps/), using cryptographic ocaps made possible by the Schnorr signatures at the heart of Gordian Clubs.

The permissions and data are published in an initial Edition of the Gordian Club. But that's just the first step. Thanks to the write permissions, a Club can later be updated in new Editions that might contain slight or wholesale changes to the data and permissions found in the previous Edition. A [provenance mark](https://developer.blockchaincommons.com/provemark/) validates the linkage of multiple Editions. 

Because of its autonomous design, Gordian Clubs are entirely transport neutral. Though you could send an Edition over the internet, you don't have to. You could send it via messaging. You could put it on an NFC card or thumb drive, then mail it. You could print it as a QR code and publish it in a newspaper. You could distribute it via Blockstream Satellite. The transport doesn't even have to be near-term: a Gordian Club Edition could be stored away for archival and used years down the road. This is true autonomy: not beholden to servers or services, but not beholden to a stable network either.

Here's how a Gordian Club might look in those real-life examples of modern-day authoritarianism:

**Journalism:** A journalist stores a list of sources and their information in a Gordian Club. One permit allows him to open it with his private key. He also sends the Club and [SSKR](https://developer.blockchaincommons.com/sskr/) shares to the five board members for his newspaper. Any three of them together can open it, which they might need to do in the case of a lawsuit over an article. The journalist can later issue new Editions of the Club when he updates his information cache or when the members of the board change. The information is encrypted, which means it's protected even in the case of an illegal seizure. Freedom of press has become a mathematical right: the government would have to coerce either the journalist or multiple board members to access it.

**Protest:** A protest group passes around a Gordian Club that contains information on upcoming protests. Updated Editions are published whenever new protests are planned, which can be done by agreement of a FROST quorum of protest organizers. Alongside its data, the Gordian Club contains a list of allowed readers, which was determined by the FROST quorum of organizers. However, any reader can also delegate read permissions to another reader. These delegated permissions only remain valid for that Edition of the Gordian Club; if there was a compromise due to delegation, it wouldn't extend to future Editions.

**Credentials:** An immigrant stores their credentials as a Gordian Club, which they send to a human rights organization in the country they are immigrating to. It is locked with the organization's public key and with a stretched password, which corresponds to a line from the immigrant's favorite song, which is long enough to be largely unbreakable, yet memorable to the immigrant. If the immigrant is seized before they leave their country, the border patrol can only go on what the emigrant self-reports. Even if the border patrol learns who the immigrant is, they can't block their credentials, because they're all self-sovereign, without phone-home requirements, and stored in that Gordian Club. Alternatively, if the immigrant reaches a safe haven, the human rights organization will provide the Gordian Club; either they can unlock it with their key or the immigrant can do so with their own password.

There are many other use cases that go beyond that increasing authoritarianism of modern countries. This includes use cases where the internet is not available or where a longer timeframe is required.

**Emergencies:** A category 5 hurricane devastates the Eastern Seaboard. The internet is largely down, though cell phone access remains available for emergency use. An unencrypted Gordian Club is created with all the emergency resource information and passed from user to user via messaging. Signatures verify its authenticity, even as Editions are updated, which helps users to steer away from the scammers that inevitably come out during these times of tragedy.

**Archival:** The patriarch of a family writes his last will and testament in a Gordian Club, accessible by his private key, by his lawyer's private key, or by three out of five shares given to his heirs. The information in it stays private until his passing, with the quantum-resistant cryptography available in Gordian Envelope ensuring privacy until that sad date. But afterward, it's easily accessible by heirs or the lawyer. The provenance marks clearly note which version of the will is the newest. 

### Five Principles For Autonomy

Gordian Clubs make ACOs concrete by following five principles that I've developed for autonomous systems.

1. **Operate Without External Dependencies.** Everything you need is within the Gordian Club: data and permissions truly operate autonomously.
2. **Encode Rules in Mathematics, Not Policy.** Permits are accessed through mathematical (cryptographic) constructs such as private keys or secret shares.
3. **Make Constraints Load-Bearing.** Members can't be removed from a Gordian Club Edition, but that also means permissions can't be unilaterally revoked. Gordon Clubs don't have live interactivity, but that means they can't be censored by a network.
4. **Preserve Exit Through Portability.** An ACO that can be freely passed around without network infrastructure is the definition of portability.
5. **Work Offline and Across Time.** Gordian Clubs are meant to be used offline; archival is a major use case, allowing access across a large span of time.

I'll have more on these principles, how I derived them, and what the Exodus Protocol Pattern is in a future Musings.

### Credit Where Credit is Due

Gordian Clubs were inspired by the Clubs feature of [Project Xanadu](https://www.xanadu.net/), which was the world's first hypertext project: it could have been a world wide web of tightly interconnected information before there was a World Wide Web. 

Project Xanadu was built around "Clubs," which could be individuals or organizations and which could be recursively created: a Club (or individual) could be a member of a Club (or individual) ... etc. Each Club could have read or write permissions to itself or to other clubs, and those rights could also be passed down through a hierarchy.

The problem with Clubs was that they required centralized administration. When I became peripherally involved with Project Xanadu in the early '90s, I suggested the use of cryptography to turn that human-based administration into math-based administration. But cryptography wasn't up to the requirements at the time.

Now it is, thanks in large part to the release and development of Schnorr signatures, allowing for the creation of Gordian Clubs.

## Gordian Clubs Are a Reality!

None of this is just a theory. I have a working [library](https://github.com/BlockchainCommons/clubs-rust) and [CLI](https://github.com/BlockchainCommons/clubs-cli-rust) for Gordian Clubs. A demo is available on YouTube:

{% include video id="bqxW7iDk4QI" provider="youtube" %}

There's also a full [log of the demo](https://github.com/BlockchainCommons/clubs-cli-rust/blob/master/demo-log.md), which you can use to follow along, using the `clubs-cli-rust` app.

Take a look, but more importantly let me know _how will you use Gordian clubs?_ What use cases will be served by ACOs? And are Gordian Clubs the right answer or do you need something more (or less)? I'd love to get your feedback as we continue work on this crucial new technology.

For more on Gordian Clubs, take a look at our developer pages:

* [Gordina Clubs Overview](https://developer.blockchaincommons.com/clubs/)
* [The Power of Autonomy](https://developer.blockchaincommons.com/clubs/autonomy/)
* [Gordian Technology](https://developer.blockchaincommons.com/clubs/technology/)
* [ocaps and Delegation](https://developer.blockchaincommons.com/clubs/ocaps/)
* [Project Xanadu History](https://developer.blockchaincommons.com/clubs/history/)
