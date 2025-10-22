---
header:
  overlay_color: "#00f"
  overlay_filter: "0.5"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "Solutions for Swiss e-ID and Other Digital Identity Systems"
title: "Musings of a Trust Architect: Five Anchors to Preserve Autonomy & Sovereignty"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
tags:
  - Advocacy
  - Self-Sovereign Identity
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

> **ABSTRACT:** How do you protect autonomy and democratic sovereignty in digital identity systems? This article suggests five foundations: protecting choice by design; building for an extended future; maintaining platform independence; requiring duties; and implementing institutional safeguards.

On September 28, 2025, Switzerland adopted the use of "electronic proof of identity," or e-IDs, to be issued and administered by the Swiss government. 

Use of the e-ID is meant to be voluntary and free of charge. However, there's still real concern about the use of e-ID in Switzerland. The vote passed with just 50.4% of the voters in agreement. A previous vote on the same subject failed in 2021. 

And, I think there's real cause for concern.

Fortunately, I was able to talk directly about these concerns: thanks to previous work that I'd presented on "The Architecture of Autonomy" (which I'll talk more about here in the future), I was invited to present at a meeting on October 2 for hundreds of people interested in (or concerned about) e-ID, incuding members of Swiss government and businesses.

The [video of my talk](https://www.youtube.com/watch?v=Tgu5kQuClOU&t=5447s) is available, but what follows is a synopsis of my major points, focusing on how to keep digital identity systems safe.

## The Unique Advantages of Switzerland

Swiss e-ID is ultimately a governmental digital identity system. That means it's not self-sovereign: the government controls issuance and maintains the system. But, that's not disqualifying. Though I'd (obviously) prefer a [self-sovereign identity system](https://www.blockchaincommons.com/tags/#self-sovereign-identity), I hope that Swiss e-ID will put us on the path to eventually produce a LESS (Legally-Enabled Self Sovereign) system.

But for now, I think Switzerland is a place where these first steps can be reasonably taken by the government. Switzerland has a strong culture of individual autonomy. They have a constitutional principle that sovereignty resides in the people. That's exactly what's required if you must trust a centralized governmental entity with your identity.

So why the concern? Despite the best intentions of the Swiss government, it'd be quite easy for their new e-ID system to be subverted, [much as has happened with self-sovereign identity](https://www.lifewithalacrity.com/article/ssi-bankruptcy/). When I talked at the October 2 meeting, my goal was therefore to present solutions that would help to avoid potential subversion, both in Switzerland and for other governments who adopt Swiss policies and technologies without having the same philosophies of autonomy at the heart of their democracy.

I did this by presenting five "anchors" that I believe must be considered when designing digital identity system if we want to preserve both personal autonomy and democractic sovereignty. (And of course, ensuring autonomy and sovereignty ultimately puts us on [the path to self-sovereign identity](https://www.lifewithalacrity.com/article/the-path-to-self-soverereign-identity/).)

## 1. Preserve Choice by Design

> _Choice disappears when alternatives become second-class._

Though the Swiss e-ID promises to be "voluntary and free of charge," this is the first place that things could go very wrong, because voluntary-in-theory doesn't necessarily mean voluntary-in-practice: it's possible to follow the technical requirements of such a precept without folowing its intent. If the use of a digital identity system is incentivized, or if critical systems become digital-only, its usage effectively becomes mandatory. But that's not the only place that individual choice can be subverted within digital identity: the very identity system can do so too if it's too rigid in saying what individual elements of data a user can share.

To solve the first problem requires the issuer of the digital identity (in this case the Swiss government) to ensure that practices concerning the identity system aren't coercive, and that nothing is denied to people who don't (or can't!) use the digital system. The second problem requires the creation of a technical architecture focused on user agency, so that a user can choose what to share, with whom, and when. That user agency must then be supported by a great UX that makes choosing to share only what's absolutely required the simplest answer.

## 2. Build a 20-Year Architecture, Not 2-Year Product

> _MVP thinking optimizes for shipping, not decades of democratic evolution_

When I co-authored TLS, I knew there were issues in the spec that needed to be addressed. I expected that to happen in 3-5 years, but it took 20! That sort of extensive bureaucratic delay isn't unusual in the world of international standardization. This is why any digital identity system needs to make sure it's ready for the next 20 years! Fundamentally, we need to design for the future, not for a short-term shipping deadline.

To solve this requires focusing on two critical issues: data minimization and resilience. Data minimization ensures that a system always sends out the least amount of data required for a specific need. It's important for the long-term health of a system because it ensures we have variability: we can adjust what's sent out as new democratic rules come into play, without having to redesign the system from scratch. (It also answers the second issue of choice, mentioned above.) Resilience means ensuring that digital identies will survive under a variety of adverse conditions, including total network failure. It readies us for changing conditions in the future. 

## 3. Maintain Platform Independence

> _Platforms profit from lock-in, not user autonomy._

Though Swiss e-ID is being created by the Swiss government, it's ultimately going to be dependent upon platform vendors such as Apple and Google and their app stores. Depending on how a digital identity is administered, platforms might be able to surveil its usage, block its usage, or engage in other anti-democratic actions. A creator of digital identity must avoid this to maintain _technical sovereignty_.

Addressing this problem requires asserting Swiss jurisdiction (or more generally, the jurisdiction of the organizations creating the identity system) over the platforms. Not only must anti-democratic actions be bluntly forbidden, but there also must be independent oversight with enforcement power. Those enforcement powers must be very strong, as we've already seen that platforms are willing to pay hundreds of millions of dollars to avoid following similar rules such as GDPR.

## 4. Require Duties for Non-Governmental Parties

> _The bigger risk isn't government surveillance, it's commercial profiling._

Ultimately, a digital ID system is going to be beholden not just to the platforms that enable it, but also to the parties that utilize it, and most of those are going to be commercial entities. Those commercial entities could misuse a user's data after they acquire it. This can damage _commercial sovereignty._

To prevent this abuse requires setting duties on entities that use a digital ID system such as e-ID. These duties should include: purpose limitation, restricting use to specific needs; verify and forget, forbidding the storage of e-ID data; and unlinkability, preventing tracking data across services or silently "pinging" some log when usage occurs. Generally, entities using a digital identity system must recognize a duty to the user as the principal holder of the identity. Again, strong enforcement will be required.

## 5. Implement Institutional Safeguards
Democratic oversight of digital power

> _Swiss democracy requires both empowering government to protect citizens from private sector abuse AND constraining government overreach._

As I said in the introduction to these anchors, I think that Switzerland has a government that is actually trustworthy to manage digital identity. However, there's a big _but_. That might not be true for other governments that adopt their systems. In addition, the extreme regime changes we've seen in the United States over the last decade suggest that we must also be concerned about future governments. To ensure _institutional sovereignty_ requires that any digital identity system protect itself not just from platforms and businesses, but also from the very entity that's administering it!

Addressing this issue requires a number of things. First, the digital identity must remain politically independent. If it's governmental, like Swiss e-ID, that requires things like cross-party appointments and fixed terms for directors as well as data governance being totally separated from politics. Second, it requires that the identity governance have duties to the users such as transparent enforcement, guaranteed human review, and service-level commitments. Third, it requires real care taken be taken with revocation, as that might be the area of a digital identity where corruption could do the most damage. This should include more duties such as two-party authorization, guaranteed quick court review, and restoration of revoked identity pending appeal.

## The Ultimate Vision

What does success ultimately look like for a digital identity system like Swiss e-ID?

These five anchors provide a checklist for success:

* ☑️ **Real Choice:** Digital and physical options remain equivalent.
* ☑️ **Sustainable Architecture:** Design is dynamic, supporting a 20-year future.
* ☑️ **Technical Sovereignty:** Platforms have democratic oversight.
* ☑️ **Commercial Sovereignty:** Businesses follow strict duties to users.
* ☑️ **Institutional Sovereignty:** Digital ID system ensures oversight of itself as well.

These goals help to ensure that agency over our digital identity remains with us, the people who are [the principals behind those identities](https://www.blockchaincommons.com/articles/Principal-Authority/), and that's my ultimate goal, whether a system is fully self-sovereign or, like Swiss e-ID, a government deployment.

If you are a member of the Swiss civil service working with e-ID, or another interested party, please feel free to <a href="mailto:team@blockchaincommons.com">mail me directly</a> for a personal presentation and/or to answer questions on these topics.

For more, you can see my videos and slides from the  October 2 presentation:

<table width="100%">
  <tr>
    <td width="640px">
      <b>Swiss e-ID Meeting:</b>

<a href="https://www.youtube.com/watch?v=Tgu5kQuClOU&t=5447s"><img src="https://img.youtube.com/vi/Tgu5kQuClOU/hqdefault.jpg"></a>

    </td>
    <td width="640px">
      <b>Slides:</b>

<a href="https://developer.blockchaincommons.com/assets/pdfs/2025-10-swisseid-noannotations.pdf"><img src="https://developer.blockchaincommons.com/assets/pdfs/2025-10-swisseid.jpg" style="border:2px solid white"></a>

    </td>
    <td width="640px">
      <b>Slides w/Annotations:</b>

<a href="https://developer.blockchaincommons.com/assets/pdfs/2025-10-swisseid.pdf"><img src="https://developer.blockchaincommons.com/assets/pdfs/2025-10-swisseid.jpg" style="border:2px solid white"></a>

    </td>
  </tr>
</table>
