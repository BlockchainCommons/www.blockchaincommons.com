---
header:
  overlay_color: "#00f"
  overlay_filter: "0.5"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Dispatches"
      url: /dispatches.html
tagline: "Martina Kolpondinos Takes on Coercive Patterns"
title: "Dispatches of a Trust Architect: Fighting Technology Paternalism"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Dispatches
tags:
  - Coercion
  - Self-Sovereign Identity
classes:
  - wide
---

In 2016, I chose the term "self-sovereign identity" to describe what identity systems should protect. But the community I helped to build has been [getting captured](/article/musings-gdc25/), as evidenced by [EU wallet regulations](/article/eidas/) and ISO standards that are consolidating around the same platform gatekeepers we set out to displace. I've been looking for the right word to describe the issues with what's happening to digital identity for a long time.

"Privacy" doesn't name the problem any more because it [means something different](/article/the-four-kinds-of-privacy/) to every regulator in the room. "Decentralization" became a buzzword, but it no longer prevents coercion due to compromises. "Interoperability" has been similarly corrupted by EUDI wallets that claim the term while depending on Apple and Google attestation infrastructures.

Martina Kolpondinos, who spent 15 months inside the Swiss federal eID team and is a co-editor on the WebVH spec, has just published a piece[^K2026] that may offer an answer by naming the pattern we keep running into: Technology Paternalism.

The term goes back to Spiekermann & Pallas[^SP2006], who argued that ubiquitous computing raises concerns beyond privacy: specifically, whether people can maintain control when systems decide for them. They proposed "the right for the last word": the ability to overrule autonomous system behavior. Unfortunately, twenty years later, things are worse, not better: 84% of organizations doubt they can even audit their AI agents[^CSA2026].

In my upcoming Architecture of Autonomy work, I've mapped how legal protections designed as shields against coercion get inverted in digital systems: property becomes privilege, contracts become coercion, due process becomes algorithmic absolutism, and exit becomes erasure. Kolpondinos shows how these same inversions manifest as paternalistic "features." She does so by building a four-part taxonomy for Technology Paternalism:

• **Design Paternalism.** The "quick setup" for systems is prominent, and "advanced" settings are buried. You aren't forced, but you are guided to a preferred usage pattern.

• **Algorithmic Paternalism.** Systems pre-select what you see. The defaults require no action, but choosing diversity requires effort.

• **Infrastructural Paternalism.** Your credentials, reputation, and relationships accumulate in a single ecosystem. Though you can leave, you leave empty-handed. This is what happens when the "interoperable" standard requires a specific device stack.

• **Protective Paternalism.** Restrictions are framed as safety. If you question them, you sound irresponsible. This is what silences objections in standards bodies. As discussed in the [replies to Martina's post](https://www.linkedin.com/posts/mkolpondinos_ssi-digitalidentity-sociotech-share-7439696404773707776-YS6E/), we ultimately want to annotate information, not censor it. This doesn't suppress contradicting claims, but instead holds them as attributable, visible, and resolvable. That's the kind of trust infrastructure we should be building: systems that make reasoning inspectable, not systems that decide for you.

Fundamentally, this paternalism is all coercion: it's taking away your choices and replacing them with the designer's choices. This is an increasing problem in technological spaces, and fighting coercion (through anti-coercion or coercion resistance) is definitely something that could replace our old buzzwords such as "privacy", "decentralization", and "interoperability".

Vitalik Buterin recently discussed the issues when he published the Ethereum Foundation mandate[^EF2026], three days before Martina's article. There, he frames Ethereum as "sanctuary technology", designed to "support technological self-sovereignty and allow cooperation without centralized coercion." His CROPS priority stack (Censorship resistance, Open source, Privacy, Security) tracks the same concerns from the protocol layer.

We've also been developing coercion-prevention lenses[^RSSI2026] in the Revisiting Self-Sovereign Identity initiative (revisitingssi.com). Kolpondinos's article is the first published output from a workshop participant, and it translates the identity community's coercion analysis into language the broader design community can use.

Ultimately, I think "technology paternalism" and "coercion resistance" work as a pair. Paternalism offers the diagnosis: it names an anti-pattern. Coercion-resistance then provides the treatment. Both do more work than "privacy" because they name the mechanism, not just the domain.

However, Technology Paternalism is harder to fight than outright ideology because it embeds moral choices in technical decisions and then presents them as neutral engineering. You could argue with someone if they were making an unvarnished moral claim, but you can't easily argue when they say "that's just how the protocol works."

But Kolpondinos' four countermeasures are a great response. She suggests tests that I wish every identity project would apply: Can you override the system's decision? Contest it? Inspect the reasoning? Leave without losing everything?

Apply that to any wallet architecture currently in standardization.

Read Martina's article, "Technology Paternalism Expands — A Case for Self-Sovereign Identity": https://www.kosmaconnect.net/interactionblog/technologypaternalism

## Citations

[^K2026]: _**Technology Paternalism: AI, Algorithms, Digital Identity, and the Role of Self-Sovereign Identity**_ (2026). [web article]. _Kolpondinos, Martina._ KosmaConnect, March 16, 2026. Retrieved 2026-03-17 from: <https://www.kosmaconnect.net/interactionblog/technologypaternalism>
    > "Four forms of technology paternalism and four countermeasures to restore user agency"

[^SP2006]: _**Technology Paternalism — Wider Implications of Ubiquitous Computing**_ (2006). [journal article]. _Spiekermann, Sarah; Pallas, Frank._ Poiesis & Praxis, 4, 6-18. DOI: 10.1007/s10202-005-0010-3. Available from: <https://link.springer.com/article/10.1007/s10202-005-0010-3>. Also available from SSRN: <https://papers.ssrn.com/sol3/papers.cfm?abstract_id=761111>
    > "The originating paper on technology paternalism and the right to the last word in ubiquitous computing"

[^CSA2026]: _**Securing Autonomous AI Agents Survey Report**_ (2026). [web article]. _Cloud Security Alliance; Strata Identity._ February 2026. Retrieved 2026-03-18 from: <https://cloudsecurityalliance.org/press-releases/2026/02/05/cloud-security-alliance-strata-survey-finds-that-enterprises-are-in-time-to-trust-phase-as-they-build-ai-autonomy-foundations>
    > "84% of organizations doubt they can audit their AI agents — empirical evidence of the governance gap"

[^EF2026]: _**Ethereum Foundation Mandate**_ (2026). [policy document]. _Ethereum Foundation._ March 2026. Retrieved 2026-03-18 from: <https://ethereum.foundation/ef-mandate.pdf>
    > "Ethereum as sanctuary technology — support technological self-sovereignty and allow cooperation without centralized coercion"

[^RSSI2026]: _**Coercion-Resistance Lenses**_ (2025–2026). [web resource]. _Revisiting Self-Sovereign Identity Initiative._ Retrieved 2026-03-18 from: <https://revisitingssi.com/lenses/briefs/coercion-resistance/>
    > "Coercion-prevention lenses and revised principles for the Self-Sovereign Identity 10th anniversary"

#DigitalIdentity #SelfSovereignIdentity #CoercionResistance #TechnologyPaternalism
