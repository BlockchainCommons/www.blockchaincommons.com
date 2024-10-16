---
header:
  overlay_color: "#00f"
  overlay_filter: "0.35"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "Modeling digital identity upon relationships."
title: "Musings of a Trust Architect: Edge Identifiers & Cliques"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
tags:
  - Cliques
  - Self-Sovereign Identity
  - Identity
  - Top Articles
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

_Since the mid-1990s, I’ve been advocating for the creation of secure digital infrastructures that protect human rights, civil liberties, and human dignity online. My mission has always been to decentralize power and give individuals control over their digital lives, from my early work co-authoring the TLS standard to my recent efforts supporting DIDs and Verifiable Credentials._

_We now stand at another crossroads in digital identity. The current paradigm, where an individual’s private key is the cornerstone of their identity, has served us well but it also has significant limitations—especially as we move toward a more interconnected, collaborative digital world. Fortunately, advances in cryptography allow us to rethink single-key self-sovereign identity systems, suggesting the possibility for new options such as edge identifiers and cryptographic cliques._

## The Single Signature Paradigm

Identity management has long  centered on the use of single-signature cryptographic keys. Operating on a straightforward principle, this "Single Signature Paradigm" requires the possession of a unique private key for cryptographic signatures, allowing actions such as authentication, data encryption, and transaction validation. 

<center>
  <img src="/images/cliques/cliques-0.png">
</center>

<br>

The security of this model hinges on the confidentiality of the private key: a compromise  of the key means a compromise of security. To reduce this threat, standards often require private keys be stored in specialized hardware, providing a fortified environment. This model is the cornerstone of security strategies endorsed and required by entities such as the National Institute of Standards and Technology (NIST), European Union government standards, and various international standards groups such as the Internet Engineering Task Force (IETF) and the World Wide Web Consortium (W3C).

There has been very limited success in strengthening this fundamental methodology through protocols such as key rotation. Meanwhile, the Single Signature Paradigm has many flaws, the most serious of which are Single Point of Compromise (where a key can be stolen) or Single Point of Failure (where a key can be lost). If anything, these problems are worsening, as demonstrated by recent side-channel attacks that can extract keys from older hardware. Other issues include scalability limitations, hardware dependency, operational inflexibility, and numerous legal, compliance, and regulatory issues.

There are fundamental limits to what can be achieved within the confines of a Single Signature Paradigm, making the need for evolution  clear.

## The Keys to Self-Sovereign Identity

The Single Signature Paradigm is problematic for many use cases surrounding digital assets, but particularly so for the management of digital identities, because identities are both central to our digital experience and largely irreplaceable. You can't just create a new identity to replace a compromised one without losing credentials and connections alike.

When I first conceived of my ideas for the personal control of digital identity, known today as self-sovereign identity, I didn't want to be limited by the Single Signature Paradigm. Instead, I modeled self-sovereign identity to be an identity that existed in a social context, not an isolated identity defined by singular keys. I wrote some on this in [The Origins of Self-Sovereign Identity](https://www.blockchaincommons.com/musings/origins-SSI/).

> One of the key principles of living systems theory is the concept of the membrane. This is not just a physical barrier but a selective boundary that controls the exchange of energy, matter, and information between the system and its environment. The membrane allows certain things to pass through while restricting others, thereby maintaining the system’s integrity and autonomy. It’s a delicate balancing act: the system must allow enough interaction with the environment to sustain itself while ensuring that it isn’t overwhelmed by external forces.


…

> Though I meant for it to be something that would protect the individual, self-sovereignty doesn’t mean that you are in complete control. It simply defines the borders within which you can make decisions and outside of which you negotiate with others as peers, not as a petitioner.

Implementing practical solutions that encapsulate this interconnectedness has historically been challenging due to the dominance of the Single Signature Paradigm. This has led to self-sovereign identity systems that actually adhere to the Single Signature Paradigm, which in turn causes the to overemphasize individualism, which was not my intent.

It's not the only way.

## Relational Edge Identity

Living systems theory suggests that identity isn't just about oneself, but about one's connections to the rest of society. 

Consider the process of a child's identity formation. They may be named "Joshua" upon birth, suggesting a unique, nodal form of identity. But, there are many Joshuas in the world. To truly define the child's identity requires [linked local names](https://github.com/WebOfTrustInfo/rwot1-sf/blob/master/topics-and-advance-readings/linked-local-names.md) (or [pet names](https://github.com/WebOfTrustInfo/rwot6-santabarbara/blob/master/topics-and-advance-readings/petnames.md)) that define relationships. The father and mother say "my child", attesting to the relationship between each of them and the child. A sibling says, "My brother's child" and a grandparent says "my grandchild". 

<center>
  <img src="/images/cliques/cliques-1a.png" width="60%" height="60%">
</center>

<br>

Though unidirectional descriptors are useful to help identify someone, each link is actually bidirectional, creating an edge between two individual nodes of identity:

<center>
  <img src="/images/cliques/cliques-1b.png" width="60%" height="60%">
</center>

<br>

At this point we must ask: does the node really define identity or is it the edges? The most complete answer is probably that an identity is defined by an _aggregation_ of edges sufficient to identify within the current graph context: "Joshua, who is filially linked with Mary, who is filially linked with Anna."

## Relational Edge Keys

We can model the interconnectedness of edge-based relationships in an identity system by using [Schnorr-based](https://www.blockchaincommons.com/musings/Schnorr-Intro/) aggregatable multisig systems that support Multi-Party Computing (MPC), such as MuSig2 or FROST (see the Appendix in the next article for more on the technology and the differences between the two systems). Schnorr-based systems are an excellent match for edge identity because their peer-based key construction technique matches the peer-based model of an identity graph: two users come together to create a joint private key.

To create a relational edge key, the two identities (nodes) connected by an edge each generate a private commitment. These commitments are combined in a cryptographic ceremony to form the edge's private key. The associated public key then effectively becomes an identifier for this two-person group, indiscernible from a single user's public key thanks to Schnorr.

<center>
  <img src="/images/cliques/cliques-2.png" width="60%" height="60%">
</center>

<br>

Leveraging the Multi-Party Computation (MPC) of MuSig2 or FROST allows for the creation of a private key that doesn't exist on a single device. It exists only in a distributed cryptographic construct, colloquially called a "fog". Through unanimous consent, users can use this "fog" to sign collectively, allowing (even requiring) joint agreement for joint actions.

This relational-edge identity model begins to resolve the issues with current self-sovereign identity models by recognizing identity as being about more than just a single self-sovereign person. It also offers substantial benefits including better security, trust, resilience, and verification due to full keys existing only in this distributed cryptographic "fog". Finally, it allows relationships to dynamically grow and change over time through the addition or removal of edges in a graph.

## Clique Identity

Edge identity is just the first step in creating a new model for identity that recognizes tthat personal digital identity is founded in relationships. The next step is to expand pairwise relationships by forming a clique, specifically a triadic clique.

A clique in graph theory is "a fully connected subgraph where every node is adjacent to every other node." Thus, in a complete graph, no node remains isolated; each is an integral part of an interconnected network. This concept is core to understanding the transition from simple pairwise relationships to more complex, interconnected group dynamics. 

In our example, there is an obvious triadic clique: the nuclear family of Mary, Bob, and Joshua.

<center>
  <img src="/images/cliques/cliques-3.png" width="40%" height="40%">
</center>

<br>

Remember that the term "nuclear family" comes from the word "nucleus".That's a great metaphor for a tight, strongly connected group [of this type](https://www.lifewithalacrity.com/article/dyads-triads-the-smallest-teams/). A triadic clique fosters strong social cohesion and supports a  robust, tightly-knit network. 

Cryptographically, we form a triadic clique by generating a relational edge key for each pair of participants in the group. This represents the pair's joint decision-making capability. Once these pairwise connections are in place, the trio _of edges_ participates in a cryptographic ceremony to create a shared private key for the whole group, which in turn creates a clique identifier: the public key. This identifier represents not just an individual or a pair but the collective identity of the entire triadic group (and, once more, their decision-making capability).

Although my examples so far suggest that nodes in a clique are all people, that doesn't have to be the case: I'll talk about cliques of devices as one of three variations of this basic formula in my next article.

## Why Cliques of Edges?

As noted, a clique is formed by the pairwise edges jointly creating a key, not by the original participants doing so. There are a number of advantages to this.

Most importantly, it builds on the concept of identity being formed by relationships. Call it the Relationship Signature Paradigm (or the Edge Signature Paradigm). We're saying that a group is defined not by the individuals, but by the relationships between the individuals. This is a powerful new concept that has applicability at all levels of identity work.

Individually, we might use the Relationship Signature Paradigm to create an individual identity based on edge-based relationships. My relationship to my friends, my relationship to my company, my relationship to my coworkers, my verifiable credentials (which are themselves relationships between myself and other entities), and my relationship to my published works together define the "clique" that is me. Crucially, this identity is built upon the relationship with other participants, _not the participants themselves_.

At a higher-level, we can also use this paradigm to form a clique of cliques, where each member is not a participant or even an edge, but instead a clique itself! Because we already recognized cliques as being formed by relational groups when we defined a first-order clique as a collection of edges, we can similarly define a clique as a collection of cliques (or even a collection of edges and cliques), creating a fully recursive paradigm for identity.

<center>
  <img src="/images/cliques/cliques-3a.png" width="60%" height="60%">
</center>

<br>

There is one clique-based design where the Relationship Signature Paradigm can't be used: fuzzy cliques, which is another variation of clique identity. But more on that in the next article.

## Higher Order Graphs

There is no reason to limit cryptographic cliques to three edges. However, the larger the group is, the harder it is to close the graph: as the number of nodes (n) in a clique increases, the number of edges grows following the formula `(n*n-1)/2`, which is the number of unique edges possible between `n` nodes. 

A "4-Clique" (or K4), for example, is a complete graph comprising 4 nodes, where each node is interconnected with every other node, resulting in a total of `(4*3)/2 = 6` edges. 

<center>
  <img src="/images/cliques/cliques-4.png" width="40%" height="40%">
</center>
<br>


This pattern continues with larger cliques: 
* K5 = `(5*4)/2 = 10` edges; 
* K6 = `(6*5)/2 = 15` edges; 
* K7 = `(7*6)/2 = 21` edges; etc.

In practice, as the number of nodes in a clique increases, the complexity of forming and maintaining these fully connected networks also escalates: each additional connection requires its own key-creation ceremony with every existing member of the graph.

Complete graphs, or closed cliques, have valuable applications across various disciplines, from computer science to anthropology, but they aren't the only solution for cryptographic cliques. I'll talk more about the alternative of open cliques as another variation of the clique identity model in my follow-up article next week. 

## Conclusion

The Single Signature Paradigm has been at the heart of the digital world since the start. It's always had its limitations, but those limitations are growing even more problematic with the rise of digital identity. 

Relational edge keys and closed cliques offer a next step, modeling how identity is actually based on relationships and that many social decisions are made through the edges defined by those relationships.

Other advantages of using clique-based keys and identities include:

1. **Decentralized Identity Management**. Peer-based edge and clique identifiers are created collaboratively, bypassing third-party involvement, thus supporting self-sovereign control and improving anonymity.
1. **Identity Validation**. Peer-based identifiers help to authenticate social identities, creating trust.
1. **Resilience Against Single Points of Failure**: Distributing control among multiple parties in a clique guards against single points of failure.
1. **Secure Group Decision Making**. Relations or groups can securely and irrevocably made decisions together.
1. **Enhanced Privacy in Group Interactions**. Aggregatable Schnorr-based signatures keep the identities of the members of a relationship or a clique private.

Cliques can be quite useful for a number of specific fields:

1. **Blockchains**. The use of aggregatable signatures creates smaller transactions on blockchains. 
1. **Collaborative Projects**. Collaborative projects and joint ventures can use clique keys to authenticate shared resource usage and other decisions.
1. **Financial Fields.** Dual-key control is often required in financial fields, and that's an implicit element of relational edge keys. 
1. **Internet of Things (IoT) & Other Smart Networks.** Relational edge keys can ensure secure and efficient communication among diverse devices that have paired together.
1. **Medicine & Other Sensitive Data.** When data is sensitive, cliques can ensure all parties have agreed to the data sharing terms, maintaining both security and collaboration integrity.

By leveraging cryptographic cliques for group identification and decision-making, we open a wide array of opportunities. These are just the beginning: open cliques, fuzzy cliques, and cliques of devices can offer even more opportunities, as I discuss in my next article in this series (which also talks a little bit about the cryptography behind this).
