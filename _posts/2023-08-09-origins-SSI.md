---
header:
  overlay_color: "#00f"
  overlay_filter: "0.35"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "Feudalism, Ostrom, Living Systems Theory, and More"
title: "Musings of a Trust Architect: The Origins of Self-Sovereign Identity"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
redirect_from:
  - /Origins-SSI
  - /origins-ssi
tags:
  - Self-Sovereign Identity
  - RWOT
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

> ***ABSTRACT:*** The idea of Self-Sovereign Identity emerged in 2016, but it has inspirations dating back centuries. This article explores the historic evolution of sovereignty and demonstrates how it can be modeled using approaches from other disciplines, including Living Systems Theory and Ostrom's Principles. It then dovetails that with the topic of human rights to demonstrate many of the goals of the original advocacy for Self-Sovereign Identity. These are goals that we must reconsider today, to shape a digital future rooted in individual autonomy and human rights.

_Christopher Allen is a futurist whose work on the internet highlighting personal agency and privacy dates back to his co-authorship of the TLS spec. He popularized the the term "self-sovereign identity" through his publication of ["The Path to Self-Sovereign Identity"](https://www.coindesk.com/markets/2016/04/27/the-path-to-self-sovereign-identity/) and has continued to support it through the [Rebooting the Web of Trust workshops](https://www.weboftrust.info/) and articles such as ["Self-Sovereign Identity, Five Years On"](https://www.coindesk.com/policy/2021/04/26/self-sovereign-identity-5-years-on/). It's now seven years on: here's the latest._

# The Origins of Self-Sovereign Identity

Throughout my professional career, themes of collaboration and trust have remained constant pillars that inform my ventures in the digital world. As a technologist, I have been involved with the development of collaboration and security tools since the inception of the internet and became deeply invested in how these digital spaces can both bolster and challenge traditional systems. My fascination as a software architect with trust has guided me toward understanding the ways in which some concepts of sovereignty, particularly self-sovereignty, unfold within both our physical and digital identities. The convergence of collaboration, trust, and self-sovereignty led to my formulation of [10 Principles of Self-sovereign Identity](http://www.lifewithalacrity.com/2016/04/the-path-to-self-soverereign-identity.html) in 2016.

However, I feel that over time some of my original intents for self-sovereign identity have been lost. Though I meant for it to be something that would protect the individual, self-sovereignty doesn’t mean that you are in complete control. It simply defines the borders within which you can make decisions and outside of which you negotiate with others as peers, not as a petitioner.

To help to clarify some of the original goals of self-sovereign identity, I thought that it would be helpful to delve into the origins of those principles and to examine the array of influences that shaped them. 

This includes five major areas:

* **History**, which reveals how the idea of sovereignty has evolved.
* **Living Systems Theory**, which describes how membranes allow different systems to interact.
* **Ostrom's Principles**, which further define the boundaries of common resources.
* **Feminist Perspectives**, which redefine sovereignty as agency, not control.
* **Human Rights & The Governance of the Commons**, which detail the intersection between self-sovereign systems and the UN Declaration of Human Rights.

Through this exploration, I aim to describe some of the original goals underlying the self-sovereign principles and to illuminate the importance of self-sovereign identity in our interconnected, digital world.

## A History of Sovereignty

Any look at the recent concept of self-sovereignty must begin with a look at historic sovereignty, dating back to even before the state-centric model we are familiar with today. It has changed and evolved over time.

During the early Middle Ages, the concept of sovereignty was embodied by lords, who wielded power to give them control over their domains. However, these lords did not exist in isolation; they were part of a complex network of feudal relationships, where power and authority were often negotiated rather than absolute. Vassals pledged fealty to their lords, yet even these bonds were based on mutual obligations. The lord promised protection, and in return, the vassal provided military service and counsel. It was a symbiotic relationship.

As societies underwent transformation, so too did the concept of sovereignty. The rise of cities during the late Middle Ages challenged the power dynamics that had previously been centered around lords and their domains. Independent cities, often organized as city-states, started to emerge as powerful entities. Their sovereignty was asserted not through isolated power but through commerce, diplomacy, and alliances with other cities. Networks of cities created dynamic trade relationships, with goods and information flowing between these different powers.

Jean Bodin wrote about sovereignty in 1576. He saw it as "absolute" and "indivisible", but nonetheless recognized that it could be passed from one person to another for a limited time. This concept was the foundation of the Peace of Westphalia, which ended the Thirty Years' War in 1648. 

The treaty was a major shift in sovereignty from cities to nations that established the modern concepts of the nation-state and state sovereignty. It marked this significant transition by formalizing the idea of territoriality and non-interference, establishing that each nation was sovereign within its borders. Yet, even then, nations needed to negotiate with each other, reflecting the historical roots of sovereignty in reciprocity and interconnectedness: sovereignty was fluid, rooted in the balance of power between peers with power. It was less about rigid boundaries and more about negotiations and relationships.

This evolution of sovereignty — from lords to cities to nations — offers a historical lens through which we can better understand the principles of self-sovereign identity and its own interconnected world view.

## Living Systems Theory

The evolution of my ideas for self-sovereign identity goes beyond the traditional context. That began with [Living Systems Theory (1978)](https://en.wikipedia.org/wiki/Living_systems), which struck a deep chord with me from the moment I was first introduced to it, in the mid-80s. It provides a great model for extracting some of the design patterns seen in historic sovereignty.

Living systems theory is a framework that sees the world as an interconnected network of systems. Each living system (such as a single cell, an organism, a social organization, or an ecosystem) is part of a larger system (its environment), and, in turn, is composed of smaller systems (its subsystems). The beauty of this theory lies in its capacity to draw parallels between different levels of organization, making it applicable across a diverse range of fields.

One of the key principles of living systems theory is the concept of the membrane. This is not just a physical barrier but a selective boundary that controls the exchange of energy, matter, and information between the system and its environment. The membrane allows certain things to pass through while restricting others, thereby maintaining the system's integrity and autonomy. It's a delicate balancing act: the system must allow enough interaction with the environment to sustain itself while ensuring that it isn't overwhelmed by external forces.

The concept of the selective membrane is not static; rather, it's a dynamic entity, constantly adapting and responding to the system's internal and external changes. This theory is particularly resonant in today's world, which is characterized by interconnectedness and the continuous negotiation and redefining of boundaries.

It also has obvious parallels to the historic evolution of sovereignty. The symbiotic relationships of peers, cities, or nations all reflect the interdependent relationships in a living system, while the flow of goods that evolved out of the mercantile city-state period demonstrates the movement of objects out of and through the membranes of these independent entities.

More importantly, living systems theory reveals the conception of a _sovereign self_: a sovereign entity (whether an individual or collective) that like a living systems navigates the balance between maintaining its autonomy and engaging with its environment, including its peers. This is the central foundation of self-sovereign identity.

## Ostrom's Principles & Living Systems

Elinor Ostrom's groundbreaking work on managing common-pool resources was another non-traditional look at sovereignty that offered additional valuable insights to shape my emerging understanding of self-sovereign identity. As the first woman to receive the Nobel Prize in Economic Sciences, in 2009, Ostrom challenged conventional wisdom by showing how local property can be successfully managed by local communities.

Ostrom's [eight principles](http://www.lifewithalacrity.com/2015/11/a-revised-ostroms-design-principles-for-collective-governance-of-the-commons-.html) for managing a commons provide a blueprint for effective, sustainable communal resource management. They demonstrate that with the right systems in place, communities can manage shared resources equitably and sustainably, without the need for centralized control or privatization.

Her first principle was particularly notable for my self-sovereign work. I paraphrase it as:

* **Authorized Use.** The community of those who have the right to use the common resource is clearly defined.
* **Commons Boundaries.** The boundaries of the commons are clearly defined so as to separate the usage rules from the larger environment.

Much like the selective membrane in living systems theory, Ostrom's principles delineate the boundaries of a common resource, establishing clear rules on who can use the resource and how much they can use. They also call for collective-choice arrangements that allow most resource appropriators to participate in the decision-making process, responding dynamically to their environment through the membrane of their living system.

Further, Ostrom's principles recognize the need for effective monitoring, conflict resolution mechanisms, and graduated sanctions for rule violators. These elements can be seen as analogous to the regulatory mechanisms within a living system, ensuring its continued functionality and survival.

Finally, Ostrom's principles suggest that resource governance activities are organized in multiple layers of nested enterprises. This reflects the hierarchical organization seen in living systems, where smaller systems exist within larger ones, and each layer is interconnected and interdependent.

In this light, Ostrom's principles and the living systems theory converge towards a shared understanding: that complex systems, whether they be biological, social, or digital, can effectively self-regulate and sustain themselves when guided by fundamentals that respect their autonomy, uphold their integrity, and recognize their interconnectivity.

## Sovereignty from a Feminist Lens

One of the important elements of Ostrom's principles is that they approached sovereignty from a different, more cooperative viewpoint. Ostrom wasn't alone in that conception. The idea was in the zeitgeist when I was teaching at Bainbridge Graduate Institute in the early '10s, just before I began writing about self-sovereign identity. More recently, it's been articulated in a few published articles.

In ["Exploring Sovereignty through a Feminist Lens"](https://www.gendersecurityproject.com/post/exploring-sovereignty-through-a-feminist-lens), Vaishnavi Pallapothu advocates for more inclusive understandings of sovereignty and for a transition from rigid hierarchical systems to more interconnected and equitable structures — ones that cleave closer to the ideals of a sovereign self.

> “Sovereignty would move beyond the implication of sovereignty as domination, towards sovereignty as the right to individual agency and prosperity.” – [Vaishnavi Pallapothu](https://www.gendersecurityproject.com/post/exploring-sovereignty-through-a-feminist-lens)

This feminist interpretation of sovereignty fundamentally disrupts the power dynamics traditionally associated with sovereignty. Instead of seeing sovereignty as a tool of domination and control, Pallapothu reframes sovereignty as a means of affirming individual agency and prosperity. Moreover, Pallapothu introduces a sense of fluidity and inclusivity to sovereignty, emphasizing the necessity for cooperation and mutual respect between entities, whether they be individuals, communities, or nations. 

This focus on the significance of individual agency within a larger system resonates deeply with the principles of self-sovereign identity and also aligns with the dynamics of living systems and with Ostrom's principles, which stress interdependence and balance rather than domination. 

Pallapothu isn't the only one to offer a more diverse look at sovereignty. Bethany Webster does so too in ["The 13 Elements of Sovereignty"](https://www.bethanywebster.com/blog/what-is-sovereignty-13-elements/), which talks about women's sovereignty rather than digital sovereignty, but nonetheless is another great additional to the discussion.

These radical departures from traditional writings on sovereignty, by Pallapothu, Ostrom, Webster, and others demonstrate the importance of including women and marginalized groups (and their too-often overlooked contributions) in the discourse around sovereignty. 

Building upon all of these insights, my journey into self-sovereign identity began to take shape, giving rise to principles that mirrored this understanding but were adapted to the unique challenges of the digital age.

## The Sovereignty of Self and Human Rights

The concept of the sovereign self, championed by the feminist viewpoint, intrinsic to living systems theory, and revealed by Ostrom's principles, connects to a fundamental pillar of human rights. The [Universal Declaration of Human Rights](https://www.un.org/en/about-us/universal-declaration-of-human-rights), adopted by the United Nations in 1948, underlines the inherent dignity and equal and inalienable rights of all individuals. This aligns with the concept of self-sovereignty, underscoring the individual's inherent right to autonomy and self-determination.

However, the concept of self-sovereignty is not merely about autonomy; per the Declaration's promise of "dignity", self-sovereign identity is also about the recognition of each individual's unique identity and experiences. It empowers individuals to freely express themselves, to make choices without coercion, and to be treated with respect. Such principles echo the most basic tenets of human rights, promoting equality, freedom, and justice.

These ideals of autonomy, self-determination, dignity, and respect do not exist in isolation. As we've seen in living systems theory, every entity is part of a broader network of relationships and exchanges. Likewise, self-sovereignty operates within a societal context, requiring an environment that respects individual agency and fosters mutual respect among all individuals.

> "Human rights are not only violated by terrorism, repression or assassination, but also by unfair economic structures that create huge inequalities." - Pope Francis (from [2013](https://www.theguardian.com/world/2013/mar/13/jorge-mario-bergoglio-pope-poverty))

Thus, self-sovereignty is closely linked to the broader quest for social justice and equality. It calls for the transformation of societal structures that perpetuate inequality and injustice, highlighting the imperative to ensure that every individual can exercise their right to self-sovereignty.

It is in this societal and human rights context that the importance of self-sovereign identity becomes even more salient. That's because self-sovereign identity offers a critical framework for asserting individual autonomy and dignity in an increasingly digital world.

It was also within this context that the idea of self-sovereign identity evolved. "The Path to Self-Sovereign Identity" was written just in advance of [RWOT2](https://www.weboftrust.info/events/#rwot-2-id2020-2016), which was held in coordination with the [ID2020 Summit](https://id2020.org/) at the United Nations. Many of the concepts of self-sovereign identity and many of the original discussions focused on ID2020's requirement that everyone in the world have the ability to prove their identity. This human-rights approach thus remains a vital component of self-sovereign identity.

## Sovereignty in the Digital Era

Together, all of these philosophies, histories, and other ideas offered a strong foundation for the ideas of self-sovereign identity, but there was also a precipitating event: a change in the internet.

In the early internet era, personal sovereignty was a growing power, supported by developments such as self-hosted UUCP emails, personal domains, and individual blogs. These innovations demonstrated interconnectivity, with information being exchanged across personally controlled digital borders. It challenged the notion of absolute state sovereignty. 

But by the start of the '10s, globalization was rising, and digital services and platforms were being consolidated. The nature of digital sovereignty began to shift: not only did states with "sovereign power" take increased control of the digital world, but so did corporate giants and global digital platforms, which are sometimes called [post-sovereignty](https://lawexplores.com/sovereignty-or-post-sovereignty-a-social-systems-theoretical-perspective/)

When the once-impermeable membranes of state sovereignty added new non-state parties to their ecosystems, individuals did not have a voice in this renegotiation of terms. Instead, the new parties only negotiated with the older state sovereigns. This resulted in insufficient mutual obligations being offered to individuals — or only obligations under property law. We once again become "serfs".

People had already been attacking this problem for a while. I participated in the collaborative event that led to the [ASN white paper](https://firstmonday.org/ojs/index.php/fm/article/view/1068/988) and that in turn led to the user-centric models that I wrote about in ["The Path to Self-Sovereign Identity"](https://www.lifewithalacrity.com/2016/04/the-path-to-self-soverereign-identity.html), but as I was poking my head back into the identity field starting at IIW 2014, I felt that these approaches had failed because they'd been co-opted by those with centralized power. We needed better answers.

Consequently, I identified a need for sovereignty to manifest at the individual level not only in the real world, but also online. Digital rights needed a model where individuals, much like living systems, had personal boundaries serving as membranes. Individuals needed to become sovereigns too, so that they could negotiate as peers. Human beings needed identity.

> "As digital systems create representations of us, a free society demands that we be given a voice in deciding how those representations are created and used. Not because we own that data, but because individual human beings are the ONLY valid source for that moral authority. Human dignity demands that individuals be treated with respect no matter which system they interact with, face-to-face or online. Without that, we become nothing but data in the machine — entries in a ledger to be managed, problems to be solved, digital serfs. We are not." – Christopher Allen (2020)

This is where my knowledge of all those scattered philosophies and ideas began to merge into my early thoughts on self-sovereign identity: individuals are seen as living systems, intertwined with each other and with other layers of systems, each with permeable boundaries serving as their membranes. As in living systems theory, my principles needed to highlight the need for a balance between maintaining individual autonomy and engaging in an interconnected digital world; as in Ostrom's principles, that balance would be based on strong boundaries and clear rules; and as in the Universal Declaration of Human Rights, those rules needed to protect agency and human dignity.

Together all of these ideas shaped my perspective, deeply informed my original ten principles, and influenced my choice to use the term "self-sovereign identity" as a name for them in 2016. But, some of these origins and influences have been lost, and if there is a desire to return to the original intent behind the self-sovereign principles, we must return to these influences as well.

## Join Me in the Conversation

As we look forward, it's clear that we must strive for balance: maintaining personal and collective autonomy while also encouraging connection in an increasingly interconnected world. By upholding the principles of self-sovereign identity, and their original intents and influences, I believe we can shape a future that respects and values every individual's rights and dignity.

In the seven years since their inception, the original ten principles of self-sovereign identity have been widely accepted. However, these principles were never meant to be an endpoint. Rather, they were written as a starting point for a larger discussion on the essence of self-sovereignty and human rights in the digital world. Back in 2016, I wrote that I saw these principles as a "departure point to provoke a discussion about what's truly important." Furthermore, I sought assistance in evolving these principles to the next level.

Today, it is apparent that as self-sovereign systems are being deployed in the EU and elsewhere, there's an urgent need to delve deeper into these principles, to correct misunderstandings and acknowledge legitimate criticisms. This is not about regressing to past ideas but about reconnecting with the foundational spirit that informed them in the first place. It is crucial to learn from both the triumphs and the setbacks of the early adopters of these principles to guide the development of the next generation of self-sovereign identity technologies. The problem is large: we thus need people from a large number of disciplines to ensure that we do self-sovereign technology right and with the humility required for such a massive and important undertaking.

The upcoming Rebooting Web of Trust conference in [Cologne, Germany](https://www.weboftrust.info/events/rwot12/), starting September 18th, presents an excellent platform for this undertaking. I urge you to [contribute advance readings](https://github.com/WebOfTrustInfo/rwot12-cologne/blob/main/advance-readings/advance-reading-primer.md) with your own perspectives on self-sovereign idenity or your own constructive questions. These will allow you to participate in the discussions during an event where we can refine and expand the self-sovereign identity principles.

This is my call to action: let's collaborate together to ensure that the digital future we're building is rooted in respecting individual sovereignty and the fundamental human rights of all individuals.
