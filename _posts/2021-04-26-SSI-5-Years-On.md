---
header:
  overlay_color: "#00f"
  overlay_filter: "0.35"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "The Initial Design, Development, and Deployment of SSI"
title: "Self-Sovereign Identity: 5 Years On"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
tags:
  - Self-Sovereign Identity
  - RWOT
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

_Musings of a Trust Architect is a series of articles by [Life with Alacrity author](http://www.lifewithalacrity.com/) and Blockchain Commons founder Christopher Allen that lays out some of the foundational ideas and philosophies behind the technology of Blockchain Commons._

> ABSTRACT: On April 26, 2016, Christopher released ["The Path to Self-Sovereign Identity"](http://www.lifewithalacrity.com/2016/04/the-path-to-self-soverereign-identity.html), a foundational article on SSI. Five years on, self-sovereign identity has become a dynamic part of the internet ecosystem. These are Christopher's thoughts on how the field has advanced in that time period, and what challenges it still faces.

<!--more-->

<a href="/musings.html"><img src="https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png" width=200 height=200 style="border: 1px solid black; float: right;"></a>

It was five years ago today that I wrote <a href="http://www.lifewithalacrity.com/2016/04/the-path-to-self-soverereign-identity.html">"The Path to Self-Sovereign Identity"</a>, my foundational article discussing the history of digital identity and laying out principles for creating a new sort of identity, based on individual control and human rights. (They're not the only set of potential principles! Bethany Webster offers her own [13 Elements of Sovereignty](https://www.bethanywebster.com/blog/what-is-sovereignty-13-elements/), which focus on women's sovereignty rather than digital sovereignty, but is the exact sort of differing perspective that we need to successfully deploy digital identities that will be useful for a diverse population.)

"The Path to Self-Sovereign Identity" was written to address a problem that was growing year by year: Facebook was increasingly controlling our access to the online world, and Google was increasingly correlating all of the information about us. Meanwhile, the refugee crisis in Europe was highlighting the problem that <a href="https://id2020.org/digital-identity">1.1 billion people in the world were living without digital identity at all</a>, denying them crucial access to financial, political and social systems.

How could we square the circle, widening access to digital identity, while making sure it was something that was controlled by us, not by huge megacorps? My answer was <a href="http://www.lifewithalacrity.com/2016/04/the-path-to-self-soverereign-identity.html">self-sovereign identity</a>.

My article was very much written from atop the shoulders of giants. <a href="https://www.openpgp.org/">PGP’s Web of Trust</a> was one of the first architectures to show a different way, where identity could be supported by peers rather than by centralized authorities. The <a href="https://internetidentityworkshop.com/">Internet Identity Workshop (IIW)</a> had already done a decade worth of lauded design of user-centric identity, including work with <a href="https://openid.net/">OpenID</a> and other emerging standards. Devon Loffreto was one of the first to talk about “sovereign source authority” in <a href="https://web.archive.org/web/20200309135642/https://www.moxytongue.com/2012/02/what-is-sovereign-source-authority.html#!https://web.archive.org/web/20210420234237/https://www.moxytongue.com/2012/02/what-is-sovereign-source-authority.html">Project VRM</a>. I am happy to have contributed to that stream of design, and I have been elated to see support grow for my own self-sovereign identity approaches over the last five years.

I feel like the principles were the most important element of my original article. They were intended as a draft that I thought would need more community input and evolve over time, but instead they resonated immediately. I have been able to talk about them with legislators and civil servants in Taiwan, Holland and Wyoming; they speak to all of those people about the need for human dignity and control of identity on the internet. The 10 principles of self-sovereign identity have become a part of our conversation.

<figure><img src="https://www.blockchaincommons.com/images/ssi-principles-jolocom.jpeg"><figcaption tabindex="0">Icons by <a href="https://dribbble.com/shots/5103877-Jolocom-selected-Icons">Ira Nezhynska</a>, used courtesy a community contribution from <a href="https://jolocom.io/">Jolocom</a>.</figcaption></figure>

There’s been a bit more resistance over the name of self-sovereign identity. There was always concern that it would get intellectually conflated with the <a href="https://www.splcenter.org/fighting-hate/extremist-files/ideology/sovereign-citizens-movement">sovereign citizen movement</a> in the United States, to which it has zero relation, but there was also concern whether it would cause unease with governments. Personally, I put the latter concern aside in May 2016 when I attended the ID2020 Summit at the United Nations and heard global ambassadors and leaders perfectly willing to use the new term.

Today, the language of self-sovereignty had spread far beyond its beginnings as a type of identity to users of many sorts of digital assets, such as cryptocurrency. Digital-asset holders speak of it as something that gives them the autonomy to make their own decisions about those assets, without any interference from third parties or other gatekeepers. So, even if there is still some question about the “self-sovereign” nomenclature in the digital-identity ecosystem, it seems to be increasingly accepted by the digital-assets community.

I think Google may actually best point to the success of the term: I remember back in 2016, people interested in my original article were told to just search for “self-sovereign” and they could find it at the top of the results, but now it’s a few pages back in the searches! That reflects progress in the field: The search results are now full of articles discussing self-sovereign identity and of companies offering solutions.

![](https://www.blockchaincommons.com/images/ssi-interest.png)

I think these are the two most crucial successes to mark on this fifth anniversary: that we are all acknowledged to be people on the internet, deserving dignity and holding human rights and that the idea of self-sovereignty has become a part of the vocabulary. It speaks to a change in our view of personhood in the 21st century that I feel is crucial. But, of course, that’s been backed up by an astounding amount of technological innovation during the last five years as well.

I’m proud that a lot of that initial movement came through work on two crucial technologies, Decentralized Identifiers (DIDs) and Verifiable Credentials (VCs), at the <a href="https://www.weboftrust.info/">Rebooting Web of Trust (RWOT) workshops</a> that I host. The work was done by a huge array of experts, leading off with Drummond Reed, Les Chasen, and Manu Sporny. Five years later, VCs are a full <a href="https://www.w3.org/TR/vc-data-model/">Recommendation at W3C</a> as an official international standard, and DIDs are a <a href="https://www.w3.org/TR/did-core/">Candidate Recommendation at W3C</a> and thus almost there. That’s the heart of the self-sovereign identity architecture: an identifier and the ability to make claims.

> ***What does a DID look like?*** A DID is a digital identifier such as `did:example:123` that represents you (or really, any entity) in some context. In a sense, it’s like a Social Security number or driver’s license number, except that it is controlled by you and non-identifying. A link to a DID document can provide authentication information and references to Verifiable Credentials. That allows you to make claims without forcing you to reveal a real-world identity first.

> ***How does a DID work?*** A user can use a secret (usually a large number) to prove that they own a DID and thus the claims made for that DID through Verifiable Credentials. These Verifiable Credentials might give them electronic privileges, such as access to a website, or they might provide real-world details, such as date of birth, college degrees, or work history. Other entities can validate the claims by signing them. The essential point is the identifier is separate from the claims about that identifier, and thus offers better security and privacy.

> ***How do DIDs meet the requirements of self-sovereign identity?*** DIDs address many of the principles of self-sovereign identity, but particularly control, access, and portability. A user has personal authority over their identity, and in fact can create multiple, contextual identities to avoid correlation; a user knows all the data associated with the DID; and a user can use the DID in different contexts as they see fit. That is a big change from something like Facebook Connect, where a third-party could suddenly and arbitrarily remove a user’s access to a variety of websites. DIDs built upon the full set of self-sovereign identity principles can go far beyond that, allowing a user total understanding of the identity they are putting forth and what information it provides to other people.

There are now any number of companies advancing these ideas: Self-sovereign identity is becoming a large industry. There are so many that the best way to talk about them is simply through an overview of the largest communities. A variety of companies are closely aligning to the W3C specs, including members of the <a href="https://www.w3.org/community/credentials/"">W3C-CCG (Credential Community Group)</a> such as Digital Bazaar, which has persistently supported the work of Rebooting the Web of Trust; the <a href="https://identity.foundation/">Decentralized Identity Foundation</a> is also working on creating a decentralized identity ecosystem, with leadership from Microsoft and Consensys; and the Linux Foundation is working on <a href="https://www.hyperledger.org/use/hyperledger-indy">Hyperledger Indy</a> with companies such as International Business Machines and Evernym. It’s not just a large ecosystem, but a healthy one, with a number of different voices each suggesting different ways forward and with many new voices emerging.

Mind you, I think there’s still room for improvement.

I have always thought it was premature to tie DIDs too tightly to a methodology, especially to a specific ledger approach. That has become a point of contention as blockchain-based ledger technologies such as Bitcoin and Ethereum have been criticized for their transaction costs, energy usage, and financial volatility. Fortunately, there’s already work being done to address that, via a rubric for evaluating the <a href="https://www.w3.org/TR/did-rubric/">decentralization of DID methods</a>.

I am also a little unsettled to see so much attention paid to Legally-Enabled Self Sovereign (LESS) Identity, and not nearly enough to Trust Minimized Identity, as I said in <a href="https://docs.google.com/presentation/d/1BbkBX-tUgifiS_VKcqCZYRTQAGF5pK-JEYQwmHYbMcI/edit">a talk</a> just before the pandemic. LESS Identity is focused on high-trust environments with real-world identity verification and is positioned for government acceptance; while Trust Minimized Identity is focused on defending human rights against powerful actors, and so has additional requirements for anonymity and is more likely to be built around peer-to-peer authentication.

![](https://www.blockchaincommons.com/images/ssi-less-trust.jpg)

It’s somewhat understandable that LESS Identity has received the most attention because it’s what businesses are more likely to need, and it still satisfies crucial self-sovereign principles such as enabling user control and allowing for minimum disclosure. But Trust Minimized Identity was one of our major concerns when we first started talking about self-sovereign identity: Supporting the human rights of refugees, no matter where they are in the world, was one of our first and most crucial use cases, and LESS Identity won’t get us there.

In other words, there’s still a need for Trust Minimized Identity, and we must make sure that we don’t lock it out as an option as we progress on LESS Identity systems. We are doing a bit of trust-minimized work at <a href="https://www.blockchaincommons.com/">Blockchain Commons</a> with our <a href="https://github.com/BlockchainCommons/did-method-onion">did:onion method</a>, but we have had the same trouble prioritizing it that everyone does – money is available for the LESS Identity approaches that are supported by progressive national governments, but not necessarily for trust-minimized solutions needed elsewhere.

Finally, we should remember that though DIDs and VCs may be a foundational architectural requirement to support many of the principles of self-sovereign identity, they are not themselves sufficient. Technology can make it easier to manage electronic identity morally, but in order to ensure that principled foundation, we need to build privacy and the guarantee of human rights atop it, using cryptographic technologies such as blinding, selective disclosure, de-anonymization resistance and zero-knowledge proofs.

This is becoming particularly important today, when we are seeing DIDs and VCs being considered as the basis of vaccine credentials (aka “Immunity Passports”). The use of DID and VC technologies alone <i>does not</i> ensure that vaccine credentials fulfill the principles of self-sovereign identity; careful scrutiny is required to balance the needs of public health with the risks of those credentials being used for other, unintended purposes.

I became involved in the identity field in large part because I believe that identity can be a double-edged sword, usable for both beneficial and maleficent purposes. To remain beneficial to its participants, an identity system must balance transparency, fairness and support of the common good with protection for the individual. Even with the use of DIDs and VCs, we must remain vigilant.

Despite these qualms, I am thrilled by how far self-sovereign identity has come in five years. I’m thrilled to have advocated for the term and to have suggested some principles and that these have found acceptance in our communities. I’m thrilled to have worked with folks from <a href="https://www.weboftrust.info/">Rebooting the Web of Trust</a>, from <a href="https://internetidentityworkshop.com/">IIW</a>, from <a href="https://www.w3.org/">W3C</a>, from <a href="https://identity.foundation/">DIF</a>, from <a href="https://www.hyperledger.org/use/hyperledger-indy">Hyperledger Indy</a>, and from any number of companies to advance these foundational ideas into a real industry, and I’m thrilled to see what comes next!
