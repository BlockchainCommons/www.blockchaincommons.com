---
header:
  overlay_color: "#00f"
  overlay_filter: "0.35"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "Managing Permissions, Authority, and Data Access"
title: "Musings of a Trust Architect: Least & Necessary Design Patterns"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
tags:
  - Self-Sovereign Identity
  - Verifiable Credentials
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

> ***ABSTRACT:*** The principles of least privilege and least authority are core computer security principles that can minimize attacks. Not only can they be extended to the realm of digital data with a new principle of least access, but they can also be flipped on their heads, to address what privilege and authority (and access) are required.

While the roots of computer security can be traced back to the military and intelligence communities, where the focus was on protecting information and assets from enemies and adversaries, I prioritize the protection of individuals, who are uniquely due respect and dignity, and who are likely to be more vulnerable and less resilient than groups such as tribes, corporations and goverments.

I've already written about design patterns such as [Data Minimization and Selective Disclosure](https://www.blockchaincommons.com/musings/musings-data-minimization/) that protect those individuals, but I want to share some thoughts on related design patterns that talk not about what data to release, but instead what permissions to grant. And moreso, I want to talk about how those design patterns can provide even more insight into protecting the data of indvidiuals when we _turn them inside out_.

So let me introduce the ___least___ design patterns followed by their reverse, the ___necessary___ design patterns.

## The Principle of Least Privilege

The concept of "least privilege" has been around in computer security for several decades. Though its origins are not entirely clear, the design pattern was popularized in the mid-1970s by Jerry Saltzer and Michael Schroeder in their influential paper, ["The Protection of Information in Computer Systems"](https://bitstreamllc.com/assets/documents/the-protection-of-information-in-computer-systems-saltzer-schroeder.pdf). Since then, the "Principle of Least Privilege" has become a cornerstone of modern computer security design.

At its core, the principle of least privilege is all about limiting the damage that can be caused by a security breach. This principle stipulates that each user, program, or system component should have only the minimum set of permissions required to perform their respective functions. In other words, if a user does not need access to a particular file, system resource, or network device to perform their job, then they should not have access to it. By limiting the access of each user or component to only what is necessary, the system as a whole becomes more resilient to attack.

"It also reduces the number of potential interactions among privileged programs to the minimum for correct operation, so
that unintentional, unwanted, or improper uses of privilege are less likely to occur. Thus, if a question arises related
to misuse of a privilege, the number of programs that must be audited is minimized."<br>[—Jerry Saltzer & Michael Schroeder, "The Protection of Information in Computer Systems"](https://bitstreamllc.com/assets/documents/the-protection-of-information-in-computer-systems-saltzer-schroeder.pdf)
{: .notice--info}

The principle of least privilege can be applied to a wide range of security domains, including access control, network security, and application security. In access control, for example, least privilege means that each user should be granted only the permissions necessary to perform their job functions, and no more. In network security, least privilege means that each network device should be configured to only allow the traffic that is necessary for its specific function, and no more. In application security, least privilege means that each application should be designed to only access the resources and data that are necessary to perform its intended function, and no more.

## Principle of Least Authority

The principle of least privilege has evolved and grown over the decades. In particular, it has been refined as the principle of least authority, which expands on how a user (or device) might gain access to a resource. It is perhaps best described in Chapter 8 of Mark S. Miller's dissertation, ["Robust Composition: Towards a Unified Approach to Access Control and Concurrency Control"](http://www.erights.org/talks/thesis/markm-thesis.pdf). Whereas least privilege focuses on individual permissions granted to a user, least authority instead recognizes that a user and a resource are part of a larger ecosystem that can include _transitive authority_: even if a user doesn't have the _privilege_ to access a resource, he might have the _privilege_ to access a program (or some other object) that itself has the _privilege_ to access the resource. It's a recognition that privileges are part of a larger web, which when seen together becomes _authority_.

"It is unclear whether Saltzer and Schroeder’s Principle of Least Privilege [SS75] is best interpreted as 'least permission' or 'least authority.' As we will see, there is an enormous difference between the two."<br>[—Mark S. Miller, "Robust Composition:
Towards a Unified Approach to Access Control and Concurrency Control"](http://www.erights.org/talks/thesis/markm-thesis.pdf)

The concept of least authority has become a standard principle in many modern security designs. In a least privilege system, a user might have been granted privileges to access a file or to utilize a database program; but a least authority system is more likely to additionally consider the access to files that the user might receive through access to the database.

Many modern discussions of least privilege conflate it entirely with least authority, but that should only be done if least privilege has been expanded to incorporate the larger ecosystem of interwoven privileges recognized in Miller's paper.

## A New Principle of Least Access

The least privilege and least access design patterns focus on the permission to do things, which is the standard for security on computing systems. However within the world of self-sovereign identity (SSI) and verifiable credentials, we instead need to focus on data access.

The ["data minimization" and "selective disclosure"](https://www.blockchaincommons.com/musings/musings-data-minimization/) design patterns already outline methods for reducing access to data. Combining that with "least privilege" and "least authority" reveals a larger, related design pattern that we can apply more specifically to digital data: "least access".

> "Data Minimization is the practice of limiting the amount of shared data to the minimum necessary: just enough for parties to successfully transact, accomplish a task, or otherwise meet a goal with each other, while minimizing risks to all parties by omitting unnecessary content."<br>[—Christopher Allen, "Musings of a Trust Architect: Data Minimization & Selective Disclosure"](https://www.blockchaincommons.com/musings/musings-data-minimization/)
{: .notice--info}

> "Data minimization mitigates the following threats: surveillance, stored data compromise, correlation, identification, secondary use, and disclosure."<br>[—IETF RFC 6973](https://datatracker.ietf.org/doc/rfc6973/)
{: .notice--info}

Rather than just minimizing data, least access minimizes data access. We can state the principle as follows: _In order to protect privacy, respect individual entitlements, and maintain human dignity, only the minimum amount of data **access** necessary to achieve a specific goal should be granted._ 

In practical terms, this new "least access" principle can be applied in a variety of contexts. For example, in the case of online transactions, this principle would go beyond the idea of data minimization, which says that only the minimum identifying data necessary to complete the transaction should be collected, and no more, to say that a merchant should not have any ability to access data he shouldn't have — and perhaps even that a datastore shouldn't be able to reveal data that the merchant shouldn't have access to. Consider a more coerceive situation where an LEO might demand personal data from a citizen: if the citizen's datastore refuses to grant the LEO access to information that they shouldn't have, then the threat of coercion is negated.

To further enhance privacy and security, a "least access" principle should be extended to minimize opportunities for correlation. This refers to the process of linking different pieces of data together to identify an individual, even if that data was collected separately. Limiting access to data through the Principle of Least Access (and especially through the Principle of Least Authority that it's built upon) should help to minimize data more than just selective disclosure alone, because it looks at the whole data ecosystem. This in turn can help protect individuals' privacy and prevent the misuse of their personal data.

## Turning Design Patterns Inside Out

Once I discover a useful design pattern, I often find utility in turning it inside out. This results in a different mindset that can provide new insights into security design.

For instance, selective disclosure is a part of my architectural tool box, and also a goal and byproduct of least access. Turning it inside out creates the idea of "selective correlation" instead: you think about what to purposefully disclose to enable correlation, rather than what to minimize to avoid correlation. It's built on the idea that correlation is not always a bad thing, and that in some cases it is necessary to achieve specific security goals.

Thus, with the inside-out design pattern of selective correlation, you: identify the specific pieces of data that need to be correlated in order to achieve a particular security objective; and then design systems and applications that allow for this correlation to occur while minimizing the risk of privacy violations.

A similar methodology can be applied to the "Least" design patterns.

## Necessary Privilege, Authority, and Access

To turn the design patterns of "least privilege", "least authority", and "least access" inside out, we focus on the positive aspects of granting access to resources and data in a way that enables effective and efficient operation, rather than simply limiting access. We could call this "necessary privilege". The idea actually goes back to Saltzer's original design for least privilege in ["Protection and Control of Information Sharing in Multics"](https://bitstreamllc.com/assets/documents/protection-control-info-sharing-multics-saltzer.pdf) when he said: "Protection mechanisms should be based on permission rather than exclusion." 

Fundamentally, necessary privilege and necessary authority systems should focus from the start on what will be _necessary_ for a user to do their job, rather than just how to limit them. This allows for the boundaries of design for a project to be reset. Rather than trying to tamp down all possible abuses, which is potentially an endless task, it instead concentrates a designer's attention on the positive. Once a designer fully understands the boundaries for what are necessary, their design task becomes easier and their work more proficient.

If this job is done well, then designers can create systems and applications that scale and that are more flexible and adaptable to changing user needs, because everything is proactively flagged for usage, rather than being negatively limited, with access then added after the fact. This approach may also help to minimize the burden on system administrators by reducing the need for constant permission updates and access control changes. And it's all done while still maintaining a high level of security. 

Besides improving administrator workload, the system can also create better user experiences: if a user prooactively has access to everything that they need, they'll never bump up against barriers in a system. This can help to reduce the risk of human error and increase user satisfaction by empowering users with the authority they need to perform their tasks effectively. It creates a more "humane" and thus more resilient system.

A necessary access system can extend these necessary privilege and necessary authority advantages to digital data. It does so by defining what data each system needs to operate rather than what data each individual is willing to release. Now perhaps a user won't be willing to release the data in question, but this creates the foundation needed for a negotiation, where a user can decide whether he wants to use a system or not. It also ensures that the user knows what data he's releasing, thanks to the improved user experience of the positvely oriented system. Since this sort of negotiation is crucial for credential systems, necessary access offers the potential of improving the whole space.

## A Summary in Brief

The differences between these six design patterns can be subtle. Here's how each one offers a slightly different way to consider computer security:

* **Least Privilege.** Minimize permissions to what's necessary for a task.
* **Least Authority.** Minimize permissions, but consider transitive authority.
* **Least Access.** Minimize data access to what's necessary for a task, considering transitive authority.
* **Necessary Privilege.** Provide permissions necessary for a task.
* **Necessary Authority.** Provide permissions and consider transitive authority.
* **Necessary Access.** Provide data access necessary for a task, considering transitive authority.

## One Last Flip-Flop

Turning design patterns inside out forces us to think differently and creates new insights into how to solve security problems.

Turning the "least" design patterns inside-out involves a shift in focus from limiting access and authority to enabling access and authority in a controlled and strategic way. It allows us to identify the specific needs of users and applications and to grant access and authority accordingly, creating security designs that are more effective, efficient, and user-friendly.

