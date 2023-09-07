---
header:
  overlay_color: "#00f"
  overlay_filter: "0.35"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "Help Shape the Future of Open Secure Chips"
title: "Musings of a Trust Architect: Open Silicon"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
tags:
  - Trust
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

> **ABSTRACT:** Drawing inspiration from Ken Thompson's seminal work, [Reflections on Trusting Trust](https://dl.acm.org/doi/pdf/10.1145/358198.358210), there are deep-rooted challenges in establishing trust in computing systems that require us to consider security down to the level of semiconductor design. Open silicon offers numerous benefits, however, the path to its adoption is fraught with challenges. Blockchain Commons' series of Silicon Salons fosters collaboration to address these challenges, advancing open and secure cryptographic semiconductor development.

<!--more-->

Trust architectures are more than skin deep. In his influential and ACM award-winning 1984 paper, "Reflections on Trusting Trust," Ken Thompson wrote about this dilemma. He noted that trusting an application necessitates trusting the code that underlies it, and in turn, trusting that code requires trusting the compiler that translates it into machine-readable instructions. However, Thompson goes further to reveal a profound vulnerability: you also have to trust the compiler for more than just faithful creation of machine code, because it could have been subverted to purposefully introduce invisiable malicious behaviors into the programs it compiles.

Thompson didn't explicitly discuss trust in microcode or in the fabrication process of chips, but that's the logical extrapolation of the concepts he introduced, and it adds even more layers to the problem. 

In other words, the architecture of trust is not a superficial matter but rather a deeply-rooted concern that spans the entire technological infrastructure from the applications, down into internet level, and even deeper to the security of individual chips from supply chains that we may not be able to easily trust.

## Open Silicon and Kerckhoffs' Law

Open silicon, or open-source hardware designs for cryptographic semiconductors, offers one solution to the lowest level of Thompson's trust dilemma. By opening up the design and development process of semiconductors, open silicon fosters collaboration, innovation, and transparency among developers, manufacturers, and researchers. This in turn creates trust, so that we can at least know the foundational level of our applications are secure.

The principles of open silicon are aligned with [Kerckhoffs' Principle](https://en.wikipedia.org/wiki/Kerckhoffs's_principle), a core tenet of cryptography which states that a cryptographic system's security should rely solely on the secrecy of the key, not on the obscurity of the algorithm or its implementation. By making the design and development process transparent and open to scrutiny, open silicon ensures that security is built on a robust foundation, not on the concealment of potential weaknesses.

The primary benefits of open silicon include:

* **Enhanced chip security.** Open-source designs  allow for thorough scrutiny by a wide range of experts, researchers, and stakeholders, leading to more secure chips overall.
* **Improved physical security.** Open silicon constrains the overall size and structure of the chip, making it more difficult for malicious actors to tamper with the hardware.
* **Efficient identification and resolution of hardware bugs.** Open-source RTL (register-transfer level) designs help developers to identify and resolve hardware bugs more efficiently because they can distinguish between unintentional vulnerabilities and deliberate backdoors. They can also mitigate risks associated with proprietary solutions.
* **Reduced software bugs.** Open hardware designs enable better analysis and understanding of the software layers, resulting in fewer software bugs and errors. 
* **Faster innovation and community-driven improvements.** Openness and transparency promote collaboration between designers, engineers, and other stakeholders, resulting in rapid exchange of ideas and continuous enhancements in the security and performance of silicon chips.
* **Better trust and credibility.** Open and transparent designs build trust among users and other stakeholders, as they can independently verify the security claims made by chip manufacturers, increasing adoption and acceptance of secure silicon chips across industries.
* **Reduced vendor lock-in.** Open designs reduce dependency on specific manufacturers, promote competition, and ensure that users have a choice between multiple secure silicon chips. This in turn encourages chip manufacturers to improve their offerings to stay competitive, leading to yet more community-driven enhancements.
* **Reduced costs.** Openly sharing designs and resources reduces the costs associated with research, development, and production of semiconductors, leading to more affordable secure silicon chips and promoting wider adoption.

## Challenges

Despite the numerous benefits of open silicon, the path to its adoption is not without challenges:

* **Balancing openness & security.** Striking a balance between open-source principles and the maintenance of a high level of security is a problem. Though I generally don't believe in security through obscurity, exposing inner workings potentially provides malicious actors with valuable information to exploit vulnerabilities.
* **Ensuring quality, avoiding fragmentation, and supporting standardization.** Coordinating contributions from diverse communities can create multiple problems. Maintaining high standards of performance and security can be difficult, as can achieving consensus among stakeholders on industry-wide standards and protocols to prevent fragmentation and ensure interoperability.
* **Ensuring that transistors match RTL designs.** Without access to detailed chip layouts, developers cannot fully guarantee the hardware matches the intended design, but once again, exposing those layouts can expose vulnerabilities.
* **Managing intellectual property, copyright concerns, and copyleft terms.** Applying open-source principles to hardware designs raises questions about copyrights, applicable licenses, the rights of various stakeholders, and the boundaries and implications of copyleft terms in the context of chip design.
* **Overcoming resistance to change.** Exposing proprietary technologies may lead to resistance from industry players fearing loss of control, revenue loss, or the need to adapt to new processes and standards.
* **Making initial investments.** Transitioning to open and transparent chip designs may require significant initial investments in research, development, and infrastructure, posing financial challenges for companies, especially in the short term.

## Overcoming Challenges

To tackle these challenges, collaboration is key. The Silicon Salon series, hosted by Blockchain Commons, fosters cooperation and knowledge sharing among stakeholders to drive open, secure cryptographic semiconductor development. By participating, attendees will actively shape best practices and strategies, bridging the gap between digital wallet developers and semiconductor manufacturers to enhance cryptographic security and trust. There a number of videos and presentations about the future of open silicon in the Silicon Salon [event archives](https://www.SiliconSalon.info/salons/).

Our next Silicon Salon will feature Mark Davis, CEO of Cranium Labs, who will delve into the intricacies of open silicon, exploring the history, challenges, and potential open solutions to the problems that his semiconductor design company has encountered. Following his resentation, a facilitated discussion among the participants of the Salon whill help to define best practices and strategies for bridging the gap between the requirements of digital wallet developers and the offerings of semiconductor manufacturers.

I cordially invite you to join us as an active participant in this conversation. Don't miss this opportunity to contribute to the advancement of cryptographic security and be part of an innovative community addressing crucial security topics.

Silicon Salon 4 is on Wednesday May 3rd at 9am PT. Tickets for the virtual event are available at Eventbrite:

https://www.eventbrite.com/e/silicon-salon-4-tickets-558196208887
