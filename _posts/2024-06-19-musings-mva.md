---
header:
  overlay_color: "#00f"
  overlay_filter: "0.35"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "The problems with MVP, and how MVA solves them."
title: "Musings of a Trust Architect: Minimum Viable Architecture (MVA)"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Gordian Architecture
tags:
  - Trust
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

> ABSTRACT: Minimum Viable Architecture (MVA) is an alternative to the Minimum Viable Product (MVP) approach, emphasizing the importance of a robust, scalable, and expandable architecture. The MVA methodology mitigates risks associated with reputation, competitiveness, and architectural deficiencies, and fosters collaboration among competitors. Real-world examples, such as SSL/TLS and the Gordian system, illustrate the successful implementation of MVA in software development.

A business methodology focused on producing a Minimum Viable Product blossomed in the 21st century. Unfortunately, it can set businesses up for future failure because it doesn't properly define the larger _architecture_ that is needed to evolve a product past its earliest, minimal state.

## The Old Methodology: Minimum Viable Product

A Minimum Viable Product (MVP) is a business methodology that advocates creating the simplest possible version of a product as a first release, to see if the market responds positively, or else to understand why it doesn't[^1]. If an MVP is successful, possibly through iterations of the initial work, the product can then be grown and ultimately find large-scale success in the market.

Twitter has long been used as an example of an MVP that did great, with Dropbox and Facebook being other examples of MVPs[^2] (to various extents). By the criteria of these companies, MVP would seem to be a win-win methodology.

However, they're not the full story.

### MVP Biases

<img src="https://www.blockchaincommons.com/images/Survivorship.png" width=350 style="float:right">

Unfortunately, current literature about Minimum Viable Products suffers from [Survivorship Bias](https://en.wikipedia.org/wiki/Survivorship_bias). We hear about the success of companies that used MVPs, but we don't know that their doing so actually led to success. In fact, the successes that we see might just be a false signal.

How many hundreds or even thousands of companies pursuing MVPs failed for each Twitter or Facebook that succeeded? How many companies found that they couldn't scale their MVP, realized that they couldn't take commercial advantage of an otherwise successful MVP, or simply were beaten by competitors with even more viable products?

We can't measure the success of the MVP methodology by the anecdotal success of a few individual companies. 

> _Survivorship bias image by Martin Grandjean (vector), McGeddon (picture), Cameron Moll (concept). Released under [cc by-sa 4.0](https://creativecommons.org/licenses/by-sa/4.0/)._

### MVP Dangers

The MVP system also has other dangers.

Some of these are related to company brand. Though a new company doesn't have a reputation to damage, a series of unsuccessful MVPs could nonetheless curtail their future opportunities. Meanwhile, a more mature company might find their existing reputation blemished by a poor MVP. This is especially true today, as companies are increasingly saying that MVPs can be poor-quality releases[^3]. That didn't work out that well for _Cyberpunk 2077_, one of the highest profile and most controversial computer game releases of recent years, even though (like many modern-day computer games) it wasn't quite released as an MVP, but not in a fully complete form either[^cyberpunk2077].

There are also competitive dangers. Within a developmental niche, MVPs only work if everyone pursues them; otherwise, an MVP built on solid ideas could easily be out-competed by a firm who produced a slightly more mature prototype. Similarly, a company with more resources might be able to scoop up the ideas in a MVP and replicate them to their own advantage[^4].

However the biggest dangers of MVPs are probably architectural. By defining an MVP, a company can easily ignore the larger architecture issues that would have once been considered before starting work on any serious release. This can cause problems with scaling, with missing features that can't easily be added, and with locked-in decisions that become part of the final product. 

Twitter ("X"), for example, didn't finalize its network architecture design until 2010[^5], four years after its advent. It would have been easy for a better architected social-medium system to get in there first; the fact that no one did is one of the pieces of luck that led to Twitter's ultimate success. In fact, one of the developers at Twitter has noted this, saying: "In the end, Twitter barely made it, and product progress was slow for years due to post facto infrastructure investment."[^6]

The biases and dangers implicit in MVPs suggest the need to at least experiment with other methodologies for product releases. The huge problems implicit in the potential lack of architecture in an MVP also suggest what that alternative methodology should be: a Minimum Viable Architecture.

## A New Methodology: Minimum Viable Architecture

Minimum Viable Architecture (MVA)[^7] is a methodology that has been discussed in somewhat different forms over the last several years. It doesn't focus on the simplest product that can be released to consumers, but instead on the simplest architecture that can support future development within a product's technological ecosystem. 

The goal of an MVA is still to create a product that doesn't strain the resources of a company and that doesn't create a situation where a company's ultimate success or failure depends on that singular release. However, that simple product must be created with the understanding of a larger architecture that has enough flexibility[^mvahub] that designers can fill in gaps in that architecture in the future. It's just that the decisions for filling in those gaps are delayed as much as possible[^mvaca]. It's a melding of agile methodologies with architectural concerns. 

Though an MVA could be created with a full understanding of future expansions that may or may not be ultimately accomodated, it's more powerful to create an MVA that is modular and expandable — that doesn't depend on the architect thinking of everything, but instead future-proofs itself so that the architecture could include unthought-of elements in the future. As Jorge Lebrato says: "The architecture remains cohesive and each piece cooperates with the others, despite having had different rhythms." The best MVA is a compromise between entirely ignoring the architecture (as is likely in an MVP) and designing it entirely (which would likely result in time cost and waste)[^mediummva].

## MVA Examples

The following examples contain some real-world usages of MVA instead of MVP.

### SSL/TLS

When I co-authored the TLS spec in the '90s, I did my best to future-proof it by simultaneously constraining the design and giving it enough flexibility to be expanded in the future. This is an example of a Minimum Viable Architecture whose usefulness has proven itself: TLS is now the most deployed security system on the internet, at the heart of almost every shopping, financial, or banking transaction.

This future-proofing was thanks in part to our architecting elements that we suspected would be required in the future, but which couldn't be deployed in the then-present, primarily due to CPU limitations. Perfect forward secrecy[^8] is an example. Users were able to simply turn it on when its usage became viable on standard hardware platforms.

However, our more notable work in creating an MVA came from our inclusion of ciphersuites. These are powerful encryption and decryption rules that do the actual cryptographic work of TLS. By defining them as modular plug-ins, we supported the future innovation of TLS, even in ways that we could not envision. And, there was considerable innovation. TLS 1.2 had 37 ciphersuites, though that dropped back to five with TLS 1.3[^9].

### The Gordian System

<img src="https://www.blockchaincommons.com/images/projects/gordian-logo-white.png" width=350 style="float: right">

One of my most recent endeavors is Blockchain Commons' Gordian system[^10], which is a layered architecture for protecting digital assets and identity that has seen early successes with the protection of seeds with systems like SSKR[^sskr] and CSR[^csr] and that focuses on the Gordian Principles of independence, resilience, privacy, and openness.

> ***Blockchain Commons' Mission:*** _Advocating for the creation of open, interoperable, secure & compassionate digital infrastructure to enable people to control their own digital destiny and to maintain their human dignity online_

In order to create an MVA that future-proofs the Gordian products, the Gordian architecture identifies points of potential interoperability and breaks the architecture into discrete components across those interoperable interfaces, thus allowing individual elemetns to be replaced. This was done both at the large-scale application level and at the small-scale programmatic level. It's important everywhere.

At the large-scale application level, the Gordian system achieves interoperability by the careful architecting of both discrete applications and the ways that they can interact. Airgaps are a traditional methodology for introducing security into a digital asset system[^11], but the Gordian system has expanded that to include Torgaps[^12], which is a way for making transactions between connected applications both secure and non-correlatable. This modular approach is one way to enable future-proofing, and it's only strengthed by systems such as airgaps and torgaps that tightly constrain communications between the modules.

<center>
  <img src="https://developer.blockchaincommons.com/assets/images/appmap-black.png">
</center>

At the small-scall programmatic level, the Gordian system introduces a layered stack of specifications that together enable the private and secure transmission of sensitive data. This stack includes dCBOR[^dcbor], Bytewords[^bytewords], URs[^urs], Animated QRs[^aqrs], Envelope[^envelope], Gordian Transport Protocol[^gtp], and Gordian Sealed Transaction Protocol[^gstp]. Together these specifications allow for the deterministic storage of binary data (dCBOR), the alphabetic representation of binary data (Bytewords), the tagged display of that representation with functionality to support multipart data (URs), the QR display of multipart data (animated QRs), the structured & smart storage of content (Envelope), the communication of Envelopes (GTP), and the secure communication of Envelopes (GSTP). But we didn't know what all the layers would be when we got started: this is another example of future-proofing, and one that easily arises from carefully layered specifications.

Similarly, when Blockchain Commons creates its progressive use cases we focus first on the requirements without needing to know the technology. The technological specifics can be filled in by ourselves or individual vendors in the future.

By abstracting and separating architectural elements—whether they be large-scale components, layered specifications, or additional requirements found in progressive use cases—the Gordian system will be able to incorporate options that we are not even considering. The ultimate goal of _all_ of these designs is to ensure that our MVA architecture  does not limit itself, but instead remains flexible for the future.

{% include video id="S0deyIHXukk" provider="youtube" %}

### Other MVA Examples

This type of MVA thinking is a pattern that can be widely successful and that doesn't create some of the limitations that appear in MVP thinking. For example, when I was supporting the creation of the earliest specifications for Decentralized Identifiers (DIDs)[^dids], I was pleased to see us arrive at a compromise where core DID specifications were separated from specific DID methods and from signature suites. It's an architecture that allows for a lot of future expansion.

Similarly, some of my earliest Blockchain Commons work was with a company who was adapting the Gordian architecture. Even though they weren't planning to initially implement multi-sigs, I ensured that they don't make decisions that would lock them out of multi-sig usage in the future, because I was thinking of a MVA that went beyond the MVP they were focused on.

## Coda: The Benefits of Coopetition

It can be quite hard for a single company to figure out an MVA. Thus, it's great to work with other companies in your technology space. 

This is particularly true if your industry supports _coopetition_, where business competitors can work together for a mutually beneficial good. If an industry  supports interoperability, or one company adding services to another company's products, then it's a great candidate for coopetition—and thus MVAs are even more likely to be successful.

Blockchain Commons has been able to take advantage of this. A variety of companies have participated in the Gordian Developer Community community[^community], each contributing their own ideas and requirements for the Gordian architecture. In turn, they've then gone off and created open-source libraries that adapt the architecture[^libraries], before beginning work on their own wallets that use the MVA that we cooperatively designed. A not-for-profit organization can be a great support for MVA work of this type; that's what Blockchain Commons does.

## Conclusion

Hollowing out spaces in architectures for future development and creating flexibility for the future through modular designs are two of the most successful methods for turning an MVP into an MVA. They give you something that supports minimal investment and agile development, while simultaneously maximizing the ability to scale and expand in the future.

We don't always know the right solutions. We can't predict what will work best. So the best we can do is create architectures that won't lock us in to specific decisions about the future. By doing so, especially by working in coopetition to do so, we also ensure that no one company will lock us or our users into futures that we don't agree with. 

> _This article was originally drafted in 2021, and then back-burnered for various reasons. It's been great to see a real exposion in discussion of MVA in the years since by authors such as Ekaterina Novoseltseva [^mvahub], Jorge Labrato[^mediummva] and Murat Erder and Pierre Pureur[^mvaca], much of which reflects my own thoughts on MVA. Hopefully that means we're moving in this direction!_

[^cyberpunk2077]: Frank, Allegra. 2020. "How one of the biggest games of 2020 became one of the most controversial". _Vox_. https://www.vox.com/culture/22187377/cyberpunk-2077-criticism-ps4-xbox-one-bugs-glitches-refunds. 
[^1]: Various. Retrieved 2021. "Minimum Viable Product". _Wikipedia_. https://en.wikipedia.org/wiki/Minimum_viable_product. 
[^2]: Michael Sweeney. 2015, 2020. "5 Successful Startups That Began With an MVP". _Clearcode_. https://clearcode.cc/blog/successful-startups-minimum-viable-product/. 
[^3]: Allan Kelly. 2020. "The MVP is broken: It's time to restore the minimum viable product". _TechBeacon_. https://techbeacon.com/app-dev-testing/mvp-broken-its-time-restore-minimum-viable-product. 
[^4]: Andrea Contigiani. 2018. "The Downside of Applying Lean Startup Principles". _Knowledge at Wharton_.
[^5]: Mazdak Hashemi. 2017. "The Infrastructure behind Twitter: Scale". _Twitter blog_.
[^6]: Evan Weaver quoted by James Governor. 2017. "Minimum Viable Architecture – good enough is good enough in an enterprise". _James Governor's Microchips_. https://redmonk.com/jgovernor/2017/06/13/minimum-viable-architecture-good-enough-is-good-enough-in-an-enterprise/. 
[^7]: Deepak Karanth. 2016. "How to Create a Minimum Viable Architecture". _Dzone_. https://dzone.com/articles/minimum-viable-architecture. 
[^mvaca]: Pureur, Pierre. 2021. "Minimum Viable Architecture: How To Continuously Evolve an Architectural Design over Time". _Continuous Architecture in Practice_. https://continuousarchitecture.com/2021/12/21/minimum-viable-architecture-how-to-continuously-evolve-an-architectural-design-over-time/. 
[^mvahub]: Novoseltseva, Ekaterina. 2022. "Minimum Viable Architecture". _Apiumhub_. https://apiumhub.com/tech-blog-barcelona/minimum-viable-architecture/#. 
[^mediummva]: Lebrato, Jorge. 2022. "What is a Minimum Viable Architecture (MVA) and why an iPaaS such as Anypoint Platform can help you achieve it". _Medium: Another Integration Blog_. https://medium.com/another-integration-blog/what-is-a-minimum-viable-architecture-mva-and-why-an-ipaas-such-as-anypoint-platform-can-help-you-f54c9791f6c3. 
[^8]: Various. Retrieved 2021. "Forward Secrecy". _Wikipedia_. https://en.wikipedia.org/wiki/Forward_secrecy.
[^9]: Uncredited. 2020. "Cipher Suites and TLS Protocols". _SSLs.com Blog_. https://www.ssls.com/blog/cipher-suites-and-tls-protocols/. 
[^10]: Various. Retrieved 2024. "Blockchain Commons Developer pages". Blockchain Commons website. https://developer.blockchaincommons.com/. 
[^11]: Various. Retrieved 2024. "Air Gaps" Blockchain Commons website. https://developer.blockchaincommons.com/airgap/. 
[^12]: Various. Retrieved 2024. "Torgaps". Blockchain Commons website. https://developer.blockchaincommons.com/torgap/. 
[^sskr]: Various. Retrieved 2024. "SSKR: Sharded Secret Key Reconstruction". Blockchain Commons website. https://developer.blockchaincommons.com/sskr/. 
[^csr]: Various. Retrieved 2024. "CSR: Collaborative Seed Recovery". Blockchain Commons website. https://developer.blockchaincommons.com/csr/. 
[^dcbor]: Various. Retrieved 2024. "Deterministic CBOR (dCBOR)". Blockchain Commons website. https://developer.blockchaincommons.com/dcbor/.
[^bytewords]: Various. Retrieved 2024. "Bytewords". Blockchain Commons website. https://developer.blockchaincommons.com/bytewords/.
[^urs]: Various. Retrieved 2024. "Uniform Resources (URs)". Blockchain Commons website. https://developer.blockchaincommons.com/ur/.
[^aqrs]: Various. Retrieved 2024. "Animated QRs". Blockchain Commons website. https://developer.blockchaincommons.com/animated-qrs/. 
[^envelope]: Various. Retrieved 2024. "Gordian Envelope". Blockchain Commons website. https://developer.blockchaincommons.com/envelope/. 
[^gtp]: Appelcline, Shannon, Wolf McNally & Christopher Allen. 2024. "Gordian Transport Protocol / Envelope Request & Response Implementation Guide 📖". _GitHub_. https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2024-004-request.mdhttps://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2024-004-request.md. 
[^gstp]: McNally, Wolf & Christopher Allen. 2023. "Gordian Sealed Transaction Protocol (GSTP)". _GItHub_. https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2023-014-gstp.md. 
[^community]: Various. Retrieved 2024. "Gordian Developer Community". _GitHub_. https://github.com/BlockchainCommons/Gordian-Developer-Community
[^libraries]: Various. Retrieved 2024. "Blockchain Commons Libraries". Blockchain Commons website. https://developer.blockchaincommons.com/libraries/
[^dids]: Drummond Reed, Manu Sporny, Dave Longley, Christopher Allen, Ryan Grant, and Markus Sabadello. 2021. "Decentralized Identifiers (DIDs) v1.0". https://www.w3.org/TR/did-core/
