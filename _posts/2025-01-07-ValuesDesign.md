---
header:
  overlay_color: "#00f"
  overlay_filter: "0.35"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "The Design Pipeline, from Values to Deployment"
title: "Musings of a Trust Architect: How My Values Inform Design"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
tags:
  - Progressive Trust
  - Trust
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

  > **ABSTRACT:** By grounding technical decisions in ethical values, we can create compassionate digital architectures. This article examines how core human values such as dignity, autonomy, and human rights inform the design of trustworthy digital systems to enable progressive trust, safeguard privacy, promote individual choice, and build resilient systems resistant to coercion. 

![values-inform-design](/images/values-design.svg)

As we enter 2025, I'm reflecting on a journey of decades that has been dedicated to advancing privacy, security, and human autonomy in the digital age. My body of work dates back to the 1990s, which saw my early contributions with cryptographic pioneers and my co-authorship of the IETF TLS 1.0 standard. But this year marks the 10th anniversary of the first ["Rebooting Web of Trust" workshop](https://www.weboftrust.info/), which was a real milestone for my leadership role in shaping secure technologies such as [Self-Sovereign Identity](https://www.lifewithalacrity.com/article/the-path-to-self-soverereign-identity/) and the [W3C Decentralized Identifiers standard](https://www.w3.org/TR/did-core/). 

Over the past decade, my focus as a trust architect has sharpened on designing digital systems that empower individuals while respecting core values such as autonomy and human dignity. These designs play a critical role in how individuals express themselves, engage with communities, and pursue their aspirations in a world increasingly shaped by digital interactions.

Yet, this digital realm presents a dual reality. While it opens up unprecedented opportunities, it also makes us increasingly vulnerable to exploitation, coercion, and pervasive surveillance. This tension places a profound responsibility on architects of digital systems: we must ensure that technical designs are guided by deeply rooted human values and ethical principles.

Looking ahead to the next ten years, I reaffirm my commitment to these values, charting a course for the future that places human flourishing and trust at the center of technological progress. But to fulfill this commitment requires the complex answer to a simple question: _how can we design systems that uphold dignity, autonomy, and human rights?_

## The Core Values of Autonomy & Dignity

When we design digital systems, we're not just creating technical specifications. We're crafting spaces where people will live significant portions of their lives. To give them the ability to truly live and excel, we must give them automony: a digital system must empower individuals to control their own destinies within this digital realm. To do so, it must provide them with tools that:

* Protect their data.
* Exercise control over their digital presence.
* Ensure freedom from coercion.
* Cultivate trust through direct, transparent & efficient peer-to-peer interactions.
* Facilitate interactions built on trust and agency.
* Enable meaningful participation in the digital economy.
* Support engagement that aligns with their values and priorities.
* Foster resilience against systemic vulnerabilities.
* Operate seamlessly across jurisdictions and political boundaries 

(See my "Principles of Dignity, Autonomy, and Trust in Digital Systems" in the Appendix for a more extensive look at what I consider core values for digital system design.)

Providing individuals with digital autonomy is mirrored by the concept of digital dignity. A digital system that prioritizes dignity respects the individuality of its users and safeguards their right to privacy. It minimizes the data collected, provides clear and revocable consent mechanisms, and ensures that control remains in the hands of the user. A dignified system doesn't simply protect; it fosters agency and participation, allowing individuals to thrive without fear of surveillance, discrimination, or exploitation.

Autonomy is also closely linked to the concept of trust. You must be able to know and trust your peers in order to truly have the autonomy to make meaningful decisions. This is where systems like [progressive trust](https://www.lifewithalacrity.com/article/progressive-trust/) come in.

A system built on autonomy, dignity, and trust ultimately treats individuals as more than their administrative identities; it recognizes that individuals possess an ineffable core of self that transcends digital representation. The first [principle of Self-Sovereign Identity](https://www.lifewithalacrity.com/article/the-path-to-self-soverereign-identity/#ten-principles-of-self-sovereign-identity), 'Existence,' upholds this kernel of individuality, affirming that any digital identity must respect and support the inherent worth of the person behind it.

To properly respect autonomy and dignity also requires careful attention to power dynamics and accountability. Distinct standards of transparency and privacy should address the power imbalances between individuals and institutions. Achieving this balance involves respecting individual privacy while enabling appropriate oversight of powerful institutions. We must protect the vulnerable while ensuring our larger administrative systems remain fair and just.

We must also address the crucial question: _how do we make privacy-preserving technology economically accessible to everyone?_ Any autonomy-enabling digital system must balance individual and collective interests by supporting sustainable development of digital infrastructure while fostering individual economic sovereignty and resilience. We must reward contributions to shared resources, uphold autonomy and self-determination, and ensure equitable access to rights-preserving technologies. By protecting individual freedoms and enabling fairness, privacy can ultimately be a tool that encourages participation regardless of economic means.

Decentralized identity wallets offer an example of how to embody the characteristics of autonomy, dignity, and trust, while also considering issues such as privacy, balance, and accessibility. They empower individuals to securely prove their credentials (such as educational achievements or professional certifications) directly to peers, without relying on central authorities that could arbitrarily deny their accomplishments. Consider Maria, a small business owner living in a vibrant but economically challenged _favela_ neighborhood in Buenos Aires, Argentina. Using a self-sovereign, decentralized identity wallet provided by the city, she is able to secure microloans without compromising her privacy, a triumph for both dignity and autonomy. 

As for how these core values transform into the design principles of decentralized identity wallets: that's the next question to address.

## From Values to Design Principles

The translation of the core values of autonomy,  dignity, and trust into concrete design principles shapes every aspect of trust architectures I build and guides me to specific technical choices:

- Cryptographically secure, self-certifying **identifiers** that operate independently of central authorities.
- Local or collaborative **key generation and management** to keep control in users' hands.
- **Peer-to-peer** protocols that resist centralized rent-seeking and walled gardens.
- **Offline-first** capabilities to prevent connectivity from becoming a point of coercion.
- **Data minimization** by default.
- Choices for **elision and redaction** to control what individuals share.
- Cryptographic **selective disclosure** to prevent unwanted correlation and tracking.
- **Revocable permissions** to ensure users retain ongoing control over their information.
- **Zero-knowledge proofs** or other systems that can balance privacy and accountability without enabling bad actors.
- **Decentralized architectures**, not as an ideological preference, but as a practical necessity.

The importance of these protections isn't theoretical. My work examining sensitive data &mdash; including [wellness](https://www.blockchaincommons.com/articles/Dangerous-Wellness-Data/), [educational credentials](https://www.blockchaincommons.com/articles/Dangerous-Educational-Credentials/), [financial transactions](https://developer.blockchaincommons.com/envelope/use-cases/summary/#financial-industry-use-cases), and identity documentation &mdash; has revealed how seemingly benign information can threaten human rights when misused. Health data can enable discrimination or coercion. Educational records can create permanent, unchangeable markers that limit opportunities. Financial and identity data can be weaponized to exploit or disenfranchise individuals.

A values-driven design can therefore be seen as not just an abstract focus on ideals such as autonomy, but protection against real-world harms. The rights to be forgotten, to correct errors, and to recover from systemic or administrative injustices ensure fairness in digital interactions. The ability for an individual to selectively share aspects of their identity protects from being reduced to digital records or confined to singular contexts. 

## From Design Principles to Education

Implementing human-centric design patterns reveals another challenge: helping developers to understand not just the technical complexity, but the human purpose behind each design choice. Developers must grasp not only how their systems operate but they must think critically about why their design decisions matter for privacy, autonomy, and dignity. 

While technical resources such as documentation and tutorials are indispensable for this education, true progress depends on fostering a compasionate culture where developers internalize value-driven imperatives. This has led me to prioritize the cultivation of decentralized developer ecosystems rooted in collaboration, open development standards, and shared learning. I've done this through a variety of means:

- **Workshops** that convene developers, policymakers, and advocates to share insights, collaborate, and explore innovative approaches.
- **Hackathons and Sprints** addressing pressing challenges in digital trust, enabling participants to co-create solutions in hands-on environments.
- **Regular Developer Meetups** for discussing current challenges, sharing practical experiences, and aligning on future roadmaps.
- **Peer Review and Collaboration Forums** to ensure transparency, accountability, and robust feedback in the development processes.
- **Cross-Organization Coordination** to facilitate collaborative projects, share resources, and distribute financial and time-related investments such as security reviews. 
- **Ecosystem Building** to design decentralized solutions that balance individual empowerment with collective benefit, ensuring that all contributors &mdash; users, developers, and communities &mdash; derive meaningful value and that mutual respect is cultivated through shared goals and open participation.
- **Mentorship Programs** to guide emerging developers in adopting values-driven approaches, fostering ethical practices from the outset of their careers. 
- **Advocacy Efforts** that include collaborating with policymakers and regulators to define a techno-social contract that upholds human dignity, ensures equitable and compassionate digital rights, and protects the interests of the vulnerable.

With this decentralized, collaborative approach to education, no single entity controls the evolution of these technologies. Instead, innovation is fostered across a diverse network of developers, building resilience into these systems and ensuring that solutions remain adaptable, inclusive, and accessible. This cooperative spirit reflects the very principles of autonomy, compassion, and inclusivity that underpin trustworthy digital systems.

## From Education to Implementation

As communities evolve from educational groups to implementation groups, forums and discussions continue to expand the community and allow us to address the broader societal implications of technical choices. Foundational principles should follow.

[The Ten Principles of Self-Sovereign Identity](https://www.lifewithalacrity.com/article/the-path-to-self-soverereign-identity/) is an example of a set of foundational principles that directly evolved from discussion at an educational workshop ([RWOT2](https://github.com/WebOfTrustInfo/rwot2-id2020/)). The [Gordian Principles](https://developer.blockchaincommons.com/principles/) and Privacy by Demand are other examples of core principles that evolved out of earlier discussions. Principles such as these form a bedrock for the values we will work to embed in actual implementations.

Code reviews and project evaluations should then include these principles &mdash; and more generally ethical alignment &mdash; as a key criterion. They're not just about technical correctness! By embedding values into every stage of development, we ensure that systems are designed to empower individuals, not exploit them.

_How can we manage the critical balance between transparency for accountability and privacy for individuals? How do we address power dynamics and ensure systems protect the rights of the vulnerable while holding powerful entities accountable? Ultimately, how do we prioritize both user autonomy and security in decisions around data storage, key management, or cryptographic algorithms?_ These are questions that should both arise and be addressed when considering a full education-to-implementation pipeline that is based on collaboration and the consideration of values.

Ultimately, implementing systems that respect dignity and autonomy demands a new kind of techno-social contract. This contract must bridge multiple realms:

- The *technical capabilities* that make solutions possible.
- The *cultural shifts* that make them acceptable.
- The *economic incentives* that make them sustainable.
- The *political will* that makes them viable.
- The *contractual & legislative agreements* that makes them durable.

This comprehensive approach will serve both individual autonomy and our collective commons. 

By ensuring that digital trust and human dignity remain at the core of technological progress, we build systems that serve as a foundation for a more equitable, humane, and resilient digital future. The result is implementations that transcend technical excellence by instilling a sense of stewardship among developers. They become not just the creators of secure systems but also champions of the communities these systems serve. 

## From Implementation to Deployment

Any framework to support values such as autonomy, dignity, and trust must be holistic in its approach. 

* Technical standards and specifications must harmonize with cultural norms and social expectations. 
* Economic models must simultaneously foster individual resilience and collective benefits, ensuring that privacy and autonomy remain accessible to everyone, and don't become luxuries available only to the wealthy. 
* Cultural norms and legislative efforts must go beyond surface-level privacy protections, addressing both the technical realities and human needs at stake. 
* Most importantly, technical and political discourse must evolve to recognize digital rights as fundamental human rights. This paradigm shift would enable policies that support compassionate decentralized approaches while holding powerful actors accountable to the communities they serve.

Nurturing the collaborative ecosystems plays a central role in this transformation. We must foster cultures of ethical awareness not just among developers but across society. This means supporting implementers and maintainers who understand not just the "how" of our systems, but the "why". It means engaging leaders who grasp both technical constraints and human needs and creating sustainable economic models that reward contributions to the commons while protecting individual rights. 

Legal deployment has always been one of the trickiest challenges in popularizing a system that supports individual autonomy, but the concept of [Principal Authority](https://www.blockchaincommons.com/articles/Principal-Authority/) presents a promising foundation, courtesy of Wyoming's digital identity law. It goes beyond the traditional frameworks of property and contract law, which, while useful, are insufficient in addressing the unique challenges of digital identity. 

Property law focuses on ownership and control and contract law governs agreements between parties, but neither fully captures the dynamic, relational nature of digital representations or the need for individual agency in decentralized systems. Principal Authority, grounded in Agency Law, functions much like the relationship between a principal and an agent in traditional legal contexts. For instance, just as an agent (like a lawyer or real estate agent) acts on behalf of a principal while preserving the principal's control, Wyoming’s digital identity law ensures that individuals retain ultimate authority over any actions or representations made on their behalf in the digital space. This legal framework acknowledges human agency &mdash; not mere ownership or contractual consent &mdash; as the primary source of legitimate authority. The result is a modern recognition of individual sovereignty, and therefore autonomy, that still fosters collaboration and commerce in the increasingly interconnected digital realm.

But, even if Principal Authority does prove a useful tool, it's just one tool in a whole toolkit that will be necessarily to successfully deploy rights-supporting software into society.

## Conclusion

My responsibility as a trust architect is not simply to build systems that work, but to build systems that work for humanity. This requires a steadfast commitment to values, a willingness to navigate difficult trade-offs, and a relentless focus on aligning design principles with human needs.

The technical challenges of implementing values-driven design are significant, but they're challenges worth solving. When we build systems that respect human rights and dignity, we create digital spaces that enhance rather than diminish human flourishing. 

As developers, policy makers, or advocates, we hold the power to embed human values into every line of code, every standard, and every policy. As we build tomorrow's digital ecosystems, we must therefore ask: _What can I do to make trust and dignity the foundation of our systems?_ 

To answer that question in a positive way will ultimately require a multi-stakeholder effort where technologists, policy makers, and civil society collaborate to uphold principles of equity, inclusion, and transparency in all aspects of digital architecture, down the entire linked chain from values to design to education to implementation to deployment. 

I hope you'll be part of that undertaking.

## Appendix 1: Principles of Dignity, Autonomy, and Trust in Digital Systems

While working on this article, I put together my own principles for dignity, autonomy, and trust in digital systems. As with my self-sovereign principles of a decade ago, I am offering these up for discussion in the community.

- **1. Human Dignity.** Design systems that prioritize and respect the inherent dignity of every individual. Embed privacy protections, minimize data collection, and provide clear, revocable consent mechanisms that align with user empowerment. Protect individuals from harm while fostering compassionate digital environments that promote trust, human flourishing, and technological progress aligned with human-centric values, actively considering potential societal impacts and unintended consequences.
- **2. Autonomy & Self-Determination:** Empower individuals to control their digital identities and make decisions free from coercion or undue influence. Enable them to manage their interactions, transact freely, preserve their sovereignty, act as peers not petitioners, and assert their rights through decentralized, compassionate, user-controlled systems.
- **3. Privacy by Design (& Default):** Embed robust privacy protections into every system, implementing data minimization, selective disclosure, anti-correlation, and cryptographic safeguards as default practices. This ensures that users retain control over their information and remain shielded from tracking, correlation, and coercion.
- **4. Resilience Against Exploitation:** Architect systems to withstand adversarial threats and systemic vulnerabilities. Leverage decentralization, cryptographic protections, and offline-first capabilities to empower users even in hostile and adversarial environments and to ensure autonomy remains intact under pressure.
- **5. Progressive Trust:** Design systems that reflect the natural evolution of trust, enabling selective and intentional information sharing. Foster trust gradually through mutual engagement, avoiding premature commitments, unnecessary reliance on intermediaries, or imposed full disclosure.
- **6. Transparency & Accountability:** Hold powerful institutions accountable while safeguarding individual privacy. Balance transparency with confidentiality to mitigate power imbalances, protect the vulnerable, and ensure justice and fairness in digital interactions. Ensure that innovation and system development prioritize fairness and compassionate considerations, holding powerful institutions accountable for societal impacts.
- **7. Interoperability:** Foster systems that are interoperable across cultural, legal, and jurisdictional boundaries. Promote inclusivity by prioritizing open standards, decentralized infrastructures, and accessible tools that serve diverse communities while avoiding exclusivity or centralized gatekeeping.
- **8. Adaptive Design:** Incorporate insights from Living Systems Theory, Ostrom's Commons, and other governance and design models to build architectures that are dynamic, resilient, and capable of evolving alongside societal and technological changes. Emphasize adaptability through iterative growth, collective stewardship, and interoperability, balancing stability with flexibility to support sustainable and inclusive digital ecosystems.
- **9. A Techno-Social Contract:** Bridge technical capabilities with cultural, economic, and legislative frameworks to create a sustainable, human and civil rights-preserving digital ecosystem. Recognize digital rights as fundamental human rights and align systems with shared values of autonomy, dignity, and collective benefit.
- **10. Ethics:** Cultivate a culture of ethical awareness, critical thinking, and collaboration among developers, policymakers, and users. Ensure technical decisions align with principles of trust and dignity by embedding education, mentorship, and a commitment to shared responsibility in the development process. Encourage innovation that is mindful of societal impacts, fostering a development ethos that prioritizes responsibility and safeguards against unintended consequences.

## Appendix 2: Use Cases for Values Designs

Values affect all of my designs. Following is some discussion of how it's influenced my work on self-sovereign identity and progressive trust.

## Self-Sovereign Identity

The conviction that technical designs must be built on human values came into sharp focus for me in 2016 when I authored the [10 Principles of Self-Sovereign Identity](https://www.lifewithalacrity.com/article/the-path-to-self-soverereign-identity/). These principles were not born from technical specifications alone but from a deep commitment to dignity, autonomy, and human rights. Over time, those values have guided the development of technologies such as Decentralized Identifiers (DIDs), Verifiable Credentials (VCs), and the DIDComm protocol for secure, private communication. They have also influenced broader thinking around cryptographic digital assets such as Bitcoin. I have come to see these values not as abstract ideals but as the very foundation of trust itself: principles that must underpin every digital system we create.

My principles of Self-Sovereign Identity also had a strong historical basis: they were built on [a deep historical and philosophical foundation](https://www.blockchaincommons.com/musings/origins-SSI/). The concept of sovereignty has evolved over centuries &mdash; from feudal lords to city-states to nations &mdash; consistently reflecting a balance between autonomy and interconnection. When I wrote about the principle of "Control", it was not about advocating absolute dominion but about framing sovereignty as the right to individual agency and prosperity, much like medieval cities, which preserved their independence while flourishing within broader networks of trade and diplomacy.

This understanding was deeply influenced by Living Systems Theory, which shows how every entity maintains its autonomy through selective boundaries while remaining part of a larger ecosystem. Just as a cell's membrane allows it to control what passes in and out while still participating in the larger organism, digital identity must enable both individual autonomy and collective participation. This biological metaphor directly informed principles such as "Existence" and "Persistence," which recognize that identity must be long-lived but also able to interact with its environment, and "Access" and "Portability", which define how identity information flows across boundaries.

The principles also reflect Ostrom's insights about managing common resources as well as feminist perspectives on sovereignty that emphasize agency over control. When I wrote about the principles of "Consent" and "Protection", I was describing the selective permeability of these digital boundaries—not walls that isolate, but membranes that enable controlled interaction. "Interoperability" and "Minimization" similarly emerged from understanding how sovereign entities must interact while maintaining their independence and protecting their core rights.

These concepts culminate in the final SSI Principles such as "Transparency," which balances individual autonomy with collective needs, and "Portability," which ensures that identities can move and evolve just as living systems do. Each principle reflects this interplay between values and technical implementation, creating a framework where digital sovereignty serves human dignity. They weren't meant to be an endpoint but rather a starting point for an evolving discussion about sovereignty in the digital age &mdash; one that continues to guide our work as we push the boundaries of what's possible in digital identity, ensuring our innovations prioritize human needs rather than subordinating them to technology.

The technical complexity required to implement such systems is significant, but it serves a deeply human purpose: the ability to build autonomy and trust. 

## Progressive Trust

Trust is not static; it evolves over time &mdash; a concept I describe as [progressive trust](https://developer.blockchaincommons.com/progressive-trust/). This principle reflects how trust naturally develops between people and organizations, both in the physical and digital worlds. Relationships are built incrementally, through selective and intentional disclosures, rather than being imposed upfront or dictated solely by third-party intermediaries. This gradual evolution is essential for fostering genuine connections while mitigating risks.

I discovered this concept through years of observing how people actually build relationships. For instance, when meeting someone at a conference, we don’t immediately share our life story. Instead, we begin with small exchanges, revealing more information as comfort, context, and mutual understanding grow. Digital systems must mirror this natural evolution of trust, creating environments that respect psychological needs and empower individual agency.

A well-designed system transforms these ideas about progressive trust into deployable systems by enabling users to disclose only what is necessary at each stage, while retaining the ability to refine or revoke permissions as relationships deepen, change, or dissolve. This flexibility demands advanced technical solutions, such as:

- Sophisticated cryptographic protocols that enable selective and intentional disclosure.
- Relationship-specific identifiers to ensure contextual privacy.
- Mechanisms to prevent unwanted tracking or correlation.
- Tools that balance transparency with security, safeguarding trust while avoiding vulnerabilities that could undermine it.

The technical complexity required to implement such systems is significant, but it serves a deeply human purpose: enabling individuals to build trust incrementally, naturally, and on their own terms. 

Knowing the values we are aligning with from the start helps to define this sort, even (as with progressive trust) when it's hard. The result is an architecture that not only reflects the organic nature of human relationships but also upholds autonomy, fosters confidence, and protects against coercion or exploitation.
