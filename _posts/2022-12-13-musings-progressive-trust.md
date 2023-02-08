---
header:
  overlay_color: "#00f"
  overlay_filter: "0.35"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "A New Approach to Building Trust in Decentralized Systems"
title: "Musings of a Trust Architect: Progressive Trust"
excerpt_separator: "<!--more-->"
categories:
  - Musings
tags:
  - Trust
classes:
  - wide
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

### A New Approach to Building Trust in Decentralized Systems

#### by Christopher Allen

_Musings of a Trust Architect is a series of articles by [Life with Alacrity author](http://www.lifewithalacrity.com/) and Blockchain Commons founder Christopher Allen that lays out some of the foundational ideas and philosophies behind the technology of Blockchain Commons._

> ABSTRACT: Progressive trust is the concept of gradually building trust over time. It differs from classical models of trust, which rely on authentication mechanisms and centralization; and zero-trust models, which assume that trust should never be relied upon or which mandate the use of "trust frameworks" or "trust registries". Progressive trust is based on the idea that trust is not a binary state but instead a dynamic and evolving process involving gradually learning about your partners through successful interactions. It's how trust works in the real world, between people and groups. This architecture is critical for protecting human rights and dignity, as it allows individuals to defend against coercion and violations of their privacy, autonomy, agency, and control. To support a progressive trust architecture, capabilities such as data minimization, elision/redaction, escrowed encryption, and cryptographic selective disclosure must be used. 

<!--more-->

<a href="/musings.html"><img src="https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png" width=200 height=200 style="border: 1px solid black; float: right;"></a>

I first wrote about progressive trust back in 2004[^1]. There, I suggested that software should "better serve our needs and the needs of the groups that we are involved in" and that to do so, "we need to figure out how to apply an understanding of how human groups behave and work." Recently, that concept has finally been gaining traction: in the world of decentralized systems, it can be used as a new approach for modeling and building trust.

The basic idea behind progressive trust is to model how trust works in the real world, between real people, groups, and businesses, rather than solely relying on mathematical or cryptographic trust. To explain this concept, I often use the example of meeting someone at a conference.

When we meet at a conference, we spend time listening to and understanding each other. We do this because being at the same conference has allowed us to create a simple credential for each other: that we are both interested in the same things. We continue to talk and exchange information, such as people we know in common, shared interests, and meaningful ideas. As our conversation progresses, we may unconsciously check to see if others are listening and adjust our conversation or location accordingly.

If we decide to meet again to continue our discussion, we may authenticate some of the credentials we have been given to ensure that we are comfortable with the level of trust we have in each other. As our collaboration grows, we may seek out more credentials and endorsements and engage in more tests of our mutual trust. Eventually, we may bring in third parties to witness and enforce our mutual obligations.

This is the way human trust works. It is also similar to how groups function and how businesses manage risk. It allows us to build trust and collaboration in a more natural and effective way. A progressive trust architecture thus permits us to support this gradual building of trust over time algorithmically.

The traditional algorithmic mechanism for building trust is to verify every interaction or transaction as "trusted." This is often done through authentication mechanisms such as passwords or digital certificates and/or by identifying interactions as being inside a trusted firewall or VPN. However, these mechanisms can be easily compromised and do not adequately capture the dynamic and evolving nature of trust between people and groups.

More modern zero-trust architectures instead assume that trust should never be relied upon by any system or network. They mandate the use of a centralized third-party, or more recently a "trust framework"[^2] or "trust registry"[^3], to manage and enforce the trust relationships. All parties must consult that registry to determine who is a trusted issuer. 

While this approach has the advantage of removing the need for individual parties to trust each other, it has numerous shortcomings:

Trust registries create new risks of centralization and vulnerability to coercion. In addition, trust registries may not be able to capture the dynamics of trust-building over time, which can be vital to building trust in complex or evolving systems. Further, trust registries can become outdated or irrelevant as requirements and details change for each party, resulting in gaps that make it difficult to determine the authenticity and reliability of new data with a privacy-breaking "phone home." Finally, trust registries must rely on a third party to hold and update the registry. This highlights some of the flaws of centralization, such as the trust registry not treating the risks of all parties equally, or focusing on mitigating the risks of those parties with more power to influence the registry, or creating a dependence that is likely to be expensive and only benefits the few.

The problems with trust registries highlight the importance of using architectures that support the autonomy and agency of all parties. Progressive trust offers this alternative through its model of how trust is built and maintained in the real world. It is based on the idea that trust is not a binary state but rather a dynamic and evolving process. As a result, trust is built gradually over time through a series of interactions and transactions that allow parties to test and verify each other's credentials and capabilities.

This progressive trust architecture protects human rights and dignity in a way that traditional models do not. Unlike traditional models of trust, progressive trust instead focuses on the choices of each party, allowing individuals to defend against coercion, financial and data loss, and violations of their privacy and authority. With progressive trust, individuals can do all of this, as the architecture is designed to support the autonomy and agency of each party. 

Specific technical capabilities must be in place to support a progressive trust architecture. These include data minimization, elision/redaction, escrowed encryption, and various cryptographic selective disclosure techniques. Data minimization, for example, involves limiting the amount of shared data to the minimum necessary to protect privacy and reduce the risk of data loss or harm. Elision/redaction allows parties to decide what information to share, removing or masking portions to give them greater control over managing their own risks. Cryptographic selective disclosure enables parties to prevent future data correlation, and escrowed encryption allows information and promises to be enforced in the future. Fundamentally, these are all techniques that we use in real-life when progressively increasing trust with someone else; they just need to be modeled in digital space.

In terms of design principles, progressive trust architectures must be flexible and scalable to adapt to changing trust requirements over time. This means leveraging modular and atomic credentials, claims, and proofs that can be combined and updated as needed. It also requires using various cryptographic tools such as cryptographic inclusion proofs and zero-knowledge protocols and leveraging data models that express how the various sub-credentials are connected, allow for gaps, and minimize undue correlation.

One of the key challenges in building a progressive trust architecture is that trust is not binary; instead, it includes more gray areas. Trust is also not universal: each party will have a different view about it. For example, in a decentralized system, not all parties may be willing or able to share sensitive information, leading to gaps in the data. Additionally, as new information is added and existing data gaps are updated, the level of trust may change, making it difficult to evaluate the authenticity of a piece of information with certainty. These challenges require verifiers to understand their own business risks and choices and apply them instead of relying on third parties to make these decisions.

Ultimately, mechanisms must be put in place to ensure that the progressive trust architecture is secure and resilient. Robust software security development techniques and practices must be used, including requiring proper cryptographic security reviews and developing decentralized governance models that can support the decision-making processes necessary for building and maintaining trust in the system.

Progressive trust offers an important new alternative to traditional and zero-trust models for online trust. By understanding and applying the principles of how human trust and collaboration work in real life, we can build trust and collaboration more naturally and effectively. Progressive trust supports each party's autonomy and agency and allows trust to evolve and adapt to changing requirements and information. As more organizations and individuals begin to explore decentralized systems, progressive trust architecture usage will only continue to grow.

[^1]: Allen, Christopher (2004). **Progressive Trust**. [online] _Life With Alacrity_ (blog). Available at: <http://www.lifewithalacrity.com/2004/08/progressive_tru.html> [Accessed 8 December 2022]

[^2]: MATTR (2021) **Trust Frameworks** _MATTR Inc._ (website) Available at: <https://learn.mattr.global/docs/concepts/trust-frameworks> [Accessed 8 December 2022]

[^3]: Johnson, Anna (2022) **Trinsic Basics: What Is a Trust Registry?** _Trinsic Inc._ (website). Available at <https://trinsic.id/trinsic-basics-what-is-a-trust-registry/> [Accessed 8 December 2022]
