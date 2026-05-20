---
header:
  overlay_color: "#00f"
  overlay_filter: "0.5"
  overlay_image: /images/blueprints-letters.jpg
  og_image: /images/dispatches-card.jpg
  actions:
    - label: "See All Dispatches"
      url: /dispatches/
tagline: "How Do Sanctuary Tech and Exodus Protocols Compare?"
title: "Dispatches of a Trust Architect: Sanctuary and Exodus"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Dispatches
tags:
  - Exodus Protocol
  - Self-Sovereign Identity
classes:
  - wide
---

On March 3, Vitalik Buterin posted a manifesto on X[^V2026a]. It introduced a new term: *sanctuary technologies*. Ten days later, the Ethereum Foundation made it official with a 38-page mandate document, which they described  as "part constitution, part manifesto."[^EF2026]

I noted this briefly in my recent [Dispatch on Technology Paternalism](https://www.lifewithalacrity.com/article/dispatches-technology-paternalism/), but the new mandate deserves its own treatment. When Vitalik talks about working to "preserve technological self-sovereignty" and "enable cooperation without coercion, domination or rugpulling,"[^V2026mandate] something is happening that those of us working on Exodus Protocols, Architectures of Autonomy, and [coercion-resistance lenses](https://revisitingssi.com/lenses/briefs/coercion-resistance/) of Self-Sovereigh Identity should pay attention to.

This Dispatch is about what Vitalik and the Ethereum Foundation are saying, where it overlaps with what I've been saying, and where the work goes from here.

## What Vitalik Said

Vitalik's March 3 posting introduced the idea of sanctuary technologies:

> "Ethereum should conceptualize ourselves as being part of an ecosystem building 'sanctuary technologies': free open-source technologies that let people live, work, talk to each other, manage risk and build wealth, and collaborate on shared goals, in a way that optimizes for robustness to outside pressures."[^V2026a]

He added to that framing by talking about the creation of a collaborative space:

> "Ethereum's role is to create 'digital space' where different entities can cooperate and interact."[^V2026a]

Instead of trying to compete with Apple or Google, his goal is "de-totalization":

> "Do not try to be Apple or Google, seeing crypto as a tech sector that enables efficiency or shininess."[^V2026a]

> "[instead] reduce the stakes of the war in heaven, by preventing the winner from having total victory."[^V2026a]

When Vitalik announced the EF mandate on March 13, he repeated his framing, saying that
Ethereum is to be "a sanctuary technology, to preserve technological self-sovereignty, to enable cooperation without coercion, domination or rugpulling," ensuring "no single person, organization or ideology's victory in cyberspace can be total."[^V2026mandate] 

This is not isolated to Vitalik. Bastian Aue, whose appointment as Co-Executive Director was announced in February, said it more bluntly in his own statement at the time:

> "The mandate of the EF is to make sure that real permissionless infrastructure, cypherpunk at its core, is what gets built."[^Aue2026]

As for the mandate itself? It makes a lot of the self-sovereign ideas that Vitalik talks about in his personal posts concrete by requiring Ethereum to have the property of CROPS[^V2026b]: Censorship Resistance; Open Source and Free, as in Freedom; Privacy; and Security. It also emphasizes long-duration survival by highlighting a *walkaway test*: could Ethereum continue to function without the Ethereum Foundation?[^EF2026] 

All together, this is a pretty big commitment to self-sovereign ideals, and one worth talking more about.

## Where Sanctuary Meets Exodus

I've been talking about self-sovereignty since I introduced the term in "The Path to Self-Sovereign Identity"[^AllenSSI], the principals of which I've been updating through the Revisiting SSI project[^AllenRSSI]. Recently, I wrote about self-sovereignty from the perspective of Exodus Protocols[^AllenExodus]. I define them as "systems that free us from the control of external sources (like Google or Yahoo! or Sony) by creating infrastructure that doesn’t require infrastructure." Bitcoin is my prime example of a working Exodus Protocol. 

My discussion of freedom from external control is a good match for Vitalik's discussion of optimization "for robustness to outside pressures." Generally, I feel like his Sanctuary Technologies match a lot of my Exodus Protocol patterns for creating autonomous infrastructure[^AllenExodus]:

1. Operate Without External Dependencies. 
2. Encode Rules in Mathematics, Not Policy. 
3. Make Constraints Load-Bearing.
4. Preserve Exit Through Portability. 
5. Work Offline and Across Time. 

Vitalik's call for "technological self-sovereignty" aligns with patterns one and two while the discussion of survivability mirrors points from patterns four and five. The CROPS priority stack reveals the reason for many of these patterns, something I discuss further in [Revisiting SSI lenses](https://revisitingssi.com/lenses/briefs/) such as ["Coercion Resistance"](https://revisitingssi.com/lenses/briefs/coercion-resistance/), ["Self-Coercion"](https://revisitingssi.com/lenses/briefs/self-coercion/), ["Choice Architecture & Exit Rights"](https://revisitingssi.com/lenses/briefs/choice-architecture/), and ["Binding Commitments"](https://revisitingssi.com/lenses/briefs/binding-commitments/). Vitalk even reaches for the term "tech enshittification / corposlop"[^V2026a] — which is Cory Doctorow's term that I have also used in describing why our digital infrastructure is built on sand.

I do feel like there's one major difference, however: **Sanctuary Tech is a goal while Exodus Protocols are an architecture.**

Vitalik's test for Sanctuary Tech is functional: *robustness to outside pressures.* By that test, his examples include Starlink, locally-running open-weight LLMs, Signal, and Community Notes.[^V2026a] These are good things, and at the present moment they meaningfully expand human autonomy. But Starlink is centrally owned by a single corporation. By [my Five Patterns](https://www.lifewithalacrity.com/article/musings-exodus.protocol/), Starlink fails Pattern 1 (Operate Without External Dependencies) and Pattern 2 (Encode Rules in Mathematics, Not Policy). It is liberating today, but it's not architecturally resilient against the day whoever owns it changes their mind. Similarly, Signal has a dependence on access to a cell phone with a cell number.

The EF Mandate's test is sharper than the X post. *Walkaway* resistance and long-duration survival are closer to the Exodus framing. But the gap remains: Sanctuary Tech describes what we want, while Exodus Protocols describe what is needed to deliver it.

This is the same gap I've been working in the [Architecture of Autonomy](https://drive.google.com/drive/folders/1BmIN7VTKczpzN3ZFiifMqboDHFptkwCT) and the [Revisiting SSI coercion-resistance lenses](https://revisitingssi.com/lenses/briefs/coercion-resistance/): the difference between *naming* a value (privacy, decentralization, sanctuary) and *engineering* it as a load-bearing constraint that holds when the political wind changes.

## What's the Next Step

The Ethereum Foundation has named the right goal. The work now is the architecture.

Concretely, three things would help:

**1. Cross-pollinate the conversations.** The identity community has spent ten years working through the failure modes of sovereignty claims, including [our own](https://www.blockchaincommons.com/musings/musings-ssi-bankruptcy/). The Ethereum Foundation has spent ten years building the most credibly-neutral programmable infrastructure on the planet. The lessons translate in both directions. The work has been siloed for too long, and the [Revisiting SSI](https://revisitingssi.com/) initiative is one venue where that cross-pollination can happen.

**2. Test Sanctuary Tech candidates against the Five Patterns.** Starlink does not pass. Signal does not pass. Some Ethereum protocol-layer mechanisms, such as FOCIL for inclusion lists, encrypted-mempool proposals, and account abstraction at the right layer, plausibly do. The LEAN Ethereum roadmap and the post-quantum work the EF has named are candidates that deserve to be examined as Exodus Protocols, not merely as performance or security improvements. The Five Patterns work as a checklist.

**3. Apply coercion-resistance lenses to wallet and L2 architectures.** Finally, we can revisit the RSSI lenses for coercion and apply them to wallets. Though they were built for identity, they're agnostic about which stack they analyze, and Ethereum's wallet layer deserves the same scrutiny that we have brought to digital identity wallets. Unfortunately, we already know that many "sanctuary technology" candidates, especially wallets, currently ride on the same Apple/Google attestation infrastructures that we identified as compromised in EUDI wallets.

We are at an unusual moment. An institution with the resources, talent, and protocol surface area of the Ethereum Foundation has just declared, in writing, that it considers itself in the business of building infrastructure that can't be taken away. That alignment with the Exodus Protocol thesis is rare. It is also fragile: the EF's executive leadership has turned over twice in the last twelve months[^DLNews2026], and institutional resolve in technology rarely outlasts the people who first articulated it. Wo we need to take advantage of this opportunity now.

If you are building anything you would call a Sanctuary Technology or an Exodus Protocol, I would like to talk. My [Architecture of Autonomy draft](https://drive.google.com/drive/folders/1BmIN7VTKczpzN3ZFiifMqboDHFptkwCT) is open for community comments, the [Revisiting SSI lenses](https://revisitingssi.com/lenses/briefs/) are open, and the [Exodus Protocol patterns](https://www.lifewithalacrity.com/article/musings-exodus.protocol/#five-patterns-for-creating-autonomous-infrastructure) are public. The Ethereum Foundation has named the goal. 

We must use that opportunity to build a foundation that won't fall.

## Citations

[^V2026a]: ***Sanctuary Technologies thread*** (2026). \[X post\]. *Buterin, Vitalik.* @VitalikButerin, March 3, 2026. Retrieved 2026-05-08 from: <https://x.com/VitalikButerin/status/2028913738057957433>

    > "Ethereum should conceptualize ourselves as being part of an ecosystem building 'sanctuary technologies': free open-source technologies that let people live, work, talk to each other, manage risk and build wealth, and collaborate on shared goals, in a way that optimizes for robustness to outside pressures."

[^V2026b]: ***Core properties (CROPS) post*** (2026). \[X post\]. *Buterin, Vitalik.* @VitalikButerin, March 5, 2026. Retrieved 2026-05-08 from: <https://x.com/VitalikButerin/status/2029662920318275935>

    > "We should not compromise on core properties: censorship resistance, open source, privacy, security (CROPS)."
    
[^V2026mandate]: ***Mandate announcement*** (2026). \[X post\]. *Buterin, Vitalik.* @VitalikButerin, March 13, 2026. Retrieved 2026-05-19 from: <https://x.com/VitalikButerin/status/2032469755614179700>

    > "Ethereum is a unique object and has a unique role in the world. Its  role is to be a sanctuary technology, to preserve technological  self-sovereignty, to enable cooperation without coercion, domination or rugpulling, and to provide an escape hatch, to ensure that no single  person, organization or ideology's victory in cyberspace can be total."

[^EF2026]: ***The Promise of Ethereum: Introducing the EF Mandate*** (2026). \[blog post and policy document\]. *Ethereum Foundation Board.* Ethereum Foundation Blog, March 13, 2026. Retrieved 2026-05-08 from: <https://blog.ethereum.org/2026/03/13/ef-mandate>. PDF available at: <https://ethereum.foundation/ef-mandate.pdf>

    > "Today we are publishing the EF Mandate, a document that serves as part constitution, part manifesto, and part guide for the Ethereum Foundation. … We are here to uncapture the individual, and to entrench their freedoms of association."

[^Aue2026]: ***co-ED Announcement*** (2026). \[X post\]. *Aue, Bastian.* @aerugoettinea, February 13, 2026. Retrieved 2026-05-19 from: <https://x.com/aerugoettinea/status/2022318885047779576>

    > "The mandate of the EF is to make sure that real permissionless infrastructure, cypherpunk at its core, is what gets built." — Bastian Aue, on his appointment as Co-Executive Director.

[^AllenExodus]: ***The Exodus Protocol*** (2025). \[blog post\]. *Allen, Christopher.* Life with Alacrity, October 28, 2025. Retrieved 2026-05-19 from: https://www.lifewithalacrity.com/article/musings-exodus.protocol/. 

    > "An Exodus Protocol is only successful if it’s designed to actually empower through autonomous service. We don’t want to just create a new digital prison. To design for success requires five architectural principles that help to create the architecture of autonomy itself."
    
[^AllenRSSI]: ***Revisiting SSI*** (2025-2026). \[web site\]. Retrieved 2026-05-19 from: https://revisitingssi.com/.

    > "In the decade since their publication, SSI has evolved from a provocative idea into infrastructure deployed by governments, companies, communities, and open protocols. At the same time, the sociotechnical environment around identity has been transformed by new technologies and new platform models that challenge the assumptions of 2016."

[^AllenSSI]: ***The Path to Self-Sovereign Identity*** (2016). \[blog post\]. *Allen, Christopher.* Life with Alacrity, April 26, 2016. Retrieved 2026-05-19 from: https://www.lifewithalacrity.com/article/the-path-to-self-soverereign-identity/. 

    > "Self-sovereign identity is the next step beyond user-centric identity and that means it begins at the same place: the user must be central to the administration of identity. That requires not just the interoperability of a user’s identity across multiple locations, with the user’s consent, but also true user control of that digital identity, creating user autonomy. To accomplish this, a self-sovereign identity must be transportable; it can’t be locked down to one site or locale."

[^Walkaway2026]: ***Ethereum Foundation Codifies Its Own Obsolescence in New Mandate*** (2026). \[news article\]. *Unchained Daily.* Unchained, March 16, 2026. Retrieved 2026-05-08 from: <https://unchainedcrypto.com/ethereum-foundation-publishes-crops-mandate-for-network-stewardship/>

    > "The 'EF Mandate' … codifies what co-founder Vitalik Buterin calls the 'walkaway test': the idea that Ethereum should function perfectly even if the Foundation and its current developers vanished tomorrow."

[^Defiant2026]: ***Ethereum Foundation Publishes EF Mandate*** (2026). \[news article\]. *The Defiant.* March 16, 2026. Retrieved 2026-05-08 from: <https://thedefiant.io/news/blockchains/ethereum-foundation-publishes-ef-mandate-a-constitution-for-the-world-computer>

    > "The 38-page document … aims to articulate the 'promise of Ethereum,' as well as the EF's role in the ecosystem. Per the Mandate, the EF defines its role not as Ethereum's owner or ruler, but as a steward with one core mission: ensuring Ethereum becomes and stays a decentralized, resilient tool for user self-sovereignty."

[^DLNews2026]: ***Ethereum Foundation co-director resigns to focus on AI*** (2026). \[news article\]. *Gilbert, Aleks.* DL News, February 13, 2026. Retrieved 2026-05-08 from: <https://www.dlnews.com/articles/defi/ethereum-foundation-co-director-resigns/>

    > "Tomasz Stańczak, a co-director of the Ethereum Foundation, will resign at the end of the month. … He will be replaced by Bastian Aue, a member of the Foundation's leadership team. Hsiao-Wei Wang will remain as the Foundation's other executive director."
