---
header:
  overlay_color: "#00f"
  overlay_filter: "0.35"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "Why We Need Alternatives before It's Too Late"
title: "Musings of a Trust Architect: Problems of Cryptographic Agility"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
tags:
  - Trust
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

> **ABSTRACT:** Cryptographic agility was once seen as a desirable goal for computer security, but increasingly problems such as high costs, bad interactions, and downgrade attacks show the flaws of the methodology. We need to thoughtfully adopt alternatives such as cipher suites, methods, or just careful layering, to make sure that the new wave of digital identity and asset projects being released *now* doesn't repeat the mistakes of the past.

<!--more-->

Cryptographic Agility[^1], the idea that a system should be able to easily switch between different cryptographic algorithms and protocols, was once seen as a desirable goal by computer security professionals: after security issues with [MD5](https://eprint.iacr.org/2005/067) and [RC4](https://www.semanticscholar.org/paper/A-Class-of-Weak-Keys-in-the-RC-4-Stream-Cipher-Roos-Vironix/788c9474b2f74ff56253cdf799e71a3ef4d5f77c) in the 90s and 00s, developers decided that the ability to quickly adapt to new vulnerabilities and weaknesses that were discovered in specific algorithms could make systems more secure in the long run. More recently, cryptographic agility has been proposed to address challenges if Quantum Cryptography breaks existing cryptosystem.

Only in the last decade has there been pushback against the concept of cryptographic agility[^2]. In some communities, developers are now being advised to minimize the amount of agility they support, such as in some of the newest W3C Verifiable Credential work[^VC]
> "Cryptographic specification authors are advised to, if possible, further minimize the number of options and parameters to as few as possible to ensure cryptographic agility while also keeping the auditable security attack surface for downstream software libraries to a minimum."

That's the result of it becoming increasingly obvious to many that any security architecture that offers cryptographic agility comes with a large number of significant drawbacks.

Revisiting the concept of cryptographic agility is particularly important now because of the amount of innovation and advancement going on in the cryptography and identity spaces. Large scale cross-border identity work such as [GLEIF](https://www.gleif.org/en), and any number of other new takes on digital identity and digital assets, will need to determine their cryptographic foundations. We don't want them to simply adopt what we've been doing for the last few decades, such as COSE's adoption of JOSE-style cryptoagility [^cose].

As these new projects and standardization efforts come to a head, we instead need to ensure that they're dealing with cryptographic choices in secure, forward-looking ways. If we don't do it now, it'll quickly become too late as the newest wave of specifications mature.

## The Drawbacks of Cryptographic Agility

Some of the drawbacks of cryptographic agility that have been revealed in recent decades include: high costs; bad interactions; and downgrade attacks.

**High Costs.** One of the main issues with cryptographic agility is the cost of implementation and support. When a system is designed to support multiple algorithms, more code is required. This, in turn, leads to more bugs, a larger attack surface, and more potential vulnerabilities. As the number of cryptographic options increases, it also becomes increasingly difficult both to focus on any one particular algorithm or protocol and to properly test and review all of the code. 

**Bad Interactions.** Related is the opportunity for bad interactions, which quickly becomes exponential: as more combinations of algorithms and protocols are added to a system, the likelihood of a security vulnerability or weakness arising from an interaction between them increases. This can make it more difficult to detect and fix these issues and can ultimately lead to a less secure system. 

**Downgrade Attacks.** Finally, the support of cryptographic agility has also resulted in downgrade attacks, where an older and weaker version of a protocol is forced by an attacker to make it easier to break. I was shocked that as late as 2016 the [POODLE Attack](https://www.cisa.gov/uscert/ncas/alerts/TA14-290A) demonstrated that some implementations of Transport Layer Security (TLS) could be downgraded to SSL 3.0 from 1996! No one should have used those suites after 1999!

Together these problems constitute what I call the **"n-factorial problem"**: each new cryptographic option explodes the cost of implementation, the attack surface, and ultimately the chance of some sort of problem.

One of the best examples of the drawbacks of cryptographic agility can be found in the case of JSON Web Token (JWT)[^3][^4], which is a popular standard for securely transmitting information between parties. JWT agilely allows for the usage of multiple options — such as supporting either RSA or HMAC as a signing algorithm. This has led to the discovery of a number of vulnerabilities, as different algorithms have different security properties; in some cases, using a weaker algorithm can even result in a token being entirely compromised[^5]! Today JWT is more secure because it has a decade of addressing some of these these attacks, but because each fix has required a "hack" to resolve, they each have the potential of contributing new technical debt, which could have been avoided with a better architecture from the start.

## Alternatives to Cryptographic Agility

None of this suggests that we shouldn't offer options in our cryptographic technology. In fact, it's our job to offer valid options that work together and that can expand the breadth of a specification or application. However, asking developers without training to pick among those options — and worse, offering up sufficient options to muddle the whole — is not good design and ultimately makes products more vulnerable, not less.

Offering options that are nonetheless limited is the policy that we adopt with our own projects, such as our new [dCBOR libraries](https://github.com/BlockchainCommons/Gordian-Developer-Community/blob/master/meetings/2023/03-01/transcript-dcbor.md):

> So what's the point of determinism? ... [F]irst of all, it's to eliminate choices for how to serialize particular data. Why is that good? Well, we want the API to enforce these kinds of standards rather than have to give developers a lot of choices. Because when developers make choices, then that often brings up problems with interoperability. So we like the API to enforce these standards as much as possible.

Limiting options can also allow us to thoughtfully offer alternatives to full-on cryptographic agility.

One alternative is [cipher suites](https://en.wikipedia.org/wiki/Cipher_suite), which are collections of algorithms meant to work together to provide security, but which are limited to working in those suites, so that they don't require the review of huge numbers of pairwise combinations, as with full cryptographic agility. 

In the 90s, I supported the inclusion of cipher suites in early SSL/TLS, but only if they were severely limited. (I think I suggested five.) Unfortunately, that didn't last, which demonstrates one of the shortcomings of cipher suite strategy, which is that of constant growth. In the last decade my TLS 1.0 co-author, Tim Dierks, now a Director of Engineering at Google, shared with me that Google needed to support over a 100 suites in TLS to achieve their target of reaching 95% of the world.

I also wanted to limit cipher suites by incorporating expiration dates: both in early SSL/TLS design meetings and more recently for DID/VC architectures[^6]. Unfortunately, this approach has not been approved by any standards organization.

The DID/VC work actually demonstrated a close cousin of cipher suites, which is the "method", used to define DID methods, signing methods, and proof methods. Here, specifics are left up to implementors, who lay out a precise methodology for usage of a specification. Perhaps there is less opportunity for exponential growth as happened with TLS 1.0 Suites, because methods often create their own ecosystems, with their own security reviews, but I feel like more analysis would be needed to really differentiate the advantages and disadvantages of cipher suites vs. methods. Nonetheless, this is obviously a second alternative to full cryptographic agility.

A third alternative, albeit one that's weaker than cipher suites and methods, is the creation of clean and well-separated layers. Poor separation of layering can compound problems with cryptographic agility because it muddies the swapping of algorithms (even when cipher suites or methods or in use) and can also create technical debt because of bits and pieces of algorithms that got placed in the wrong layers. Strong layering can make sure everything is in its proper place, though it still offers the possibility for n-factorial review issues.

Granted, there are dangers to stepping back from full agility. In Blockchain Commons' recent work on [Gordian Envelope](https://www.blockchaincommons.com/introduction/Envelope-Intro/), we initially settled on BLAKE3 as our hash algorithm. Ultimately we decided that was a mistake because our use cases didn't need many of its future-looking features, such as its ease of use in streaming protocols; we instead had use cases that often involved constrained environments where BLAKE3 could not be easily supported. Backing out to SHA-256 has been a pain, requiring revisions of code, IETF draft proposals, use-case studies, and docs alike. We _could_ have avoided that if we'd supported a number of different hash algorithms via cryptographic agility, but I still think that would have been a mistake.

## A Modern Approach

Using a limited number of cipher suites or cleanly detailing methods for use in different ecosystems are ways to overcome the potential drawbacks of cryptographic agility while maintaining some of the benefits. 

In the last few years, newer protocols such as [WireGuard](https://www.wireguard.com) (a VPN security protocol) and the latest 1.3 version of the TLS protocol have pushed in this direction[^7]. WireGuard has a very limited number of cryptographic options, and only uses one algorithm for key exchange and one for encryption.[^8] Similarly, TLS 1.3 has limited the number of cryptographic suites, removing older, less secure options.[^9] This approach allows for more thorough testing and code review and reduces the risk of security vulnerabilities arising from interactions between different cryptographic options.[^10]

There are variants of cryptosuite design that are even more limited while still allowing for progressive advancement of the design, such as restricting a product to a single suite, but having a second one set aside for the future, to be deployed and used as necessary. (We plan to take this approach with Gordian Envelope).

There are also other options, such as making sure that protocols are very cleanly layered (which in my opinion is generally desirable). In this case, an algorithm could be seamlessly switched out by swapping a layer. But that, of course, depends on very careful design, which often is not pragmatic. This choice can also become a slippery slope like cipher suites became.

I feel like cryptoagility has been adopted without question for too long now; we need to accept its limitations and liabilities. Ultimately, I believe that instead supporting _constained_ choices and _opinionated_ choices can offer a better foundation — rather than the pure cryptoagility of recent decades.

----

## Inspirations

_This article was inspired by a recent post in the Credentials Community Group (CCG) by Manu Sporny: [https://lists.w3.org/Archives/Public/public-credentials/2023Jan/0092.html](https://lists.w3.org/Archives/Public/public-credentials/2023Jan/0092.html)_

> On Fri, Jan 27, 2023 at 4:24 PM Tomislav Markovski <tomislav@trinsic.id> wrote:
> > Side comment: I always wondered why data integrity signatures suites define the canonicalization algorithm in the suite as a constant, instead as a proof parameter using the "canonicalizationAlgorithm" term defined in the security vocab v1.
> 
> Providing optionality in cryptography libraries leads to code that's
more complex than necessary, very difficult (to impossible) to audit,
and creates foot guns for developers (who have proven to repeatedly
pick the wrong parameters in critical situations).
>
> The ideal number of cryptographic suites for your application is two,
with zero optionality. One cryptosuite to use today, and one
cryptosuite to use when your current cryptographic system is broken.
This is quite different from the old-and-busted philosophy used in the
2000s, some of which bled into the 2010s. Thankfully, more people are
speaking out against excessive optionality in cryptographic systems
today and doing something about it (the Data Integrity work  coupled
with no option cryptosuites being one such group... Wireguard in the
Linux kernel being another).
>
> You can see this updated approach playing out in critical software
systems today. For example, Wireguard in the Linux kernel has zero
agility and zero optionality and has been praised by Linus Torvalds as
better than the current cryptographic system in the Linux kernel.
Unsurprisingly some of the previous cryptography subsystem
implementers in the Linux kernel are taking it as an insult that their
code is being called "unsafe" and "overly complex", which completely
misses the point. Optionality leads to misuse as CVEs have
demonstrated over the years. Give developers a bad option in the name
of backward compatibility and they will use it without knowing the
dangers.
>
> There is an excellent presentation by the core kernel maintainer for
Wireguard that outlines why excessive optionality is being stripped
from systems like the Linux kernel here:
> 
> https://www.youtube.com/watch?v=eYztYCbV_8U
> 
> Key points above are made about auditability, reducing optionality,
and reducing agility around minute 3 and 16, though the entire
presentation (from 2016) is well worth the time.


## References

[^1]: ***Classic Definition:***<br/>[Cryptographic agility - Wikipedia](https://en.wikipedia.org/wiki/Cryptographic_agility)
[^2]: ***Other Criticism of Cryptographic Agility:***<br/>[Cryptographic Agility - Adam Langley](https://www.imperialviolet.org/2016/05/16/agility.html)
[^VC]: ***Warnings about Cryptographic Agility:***<br/>[Verifiable Credential Data Integrity 1.0 - W3C Working Draft](https://www.w3.org/TR/vc-data-integrity/#protecting-application-developers)
[^cose]: ***COSE & JOSE:***<br/> [RFC 8152 Introduction](https://www.rfc-editor.org/rfc/rfc8152#section-1)
[^3]: ***Criticisms of JWT:***<br/>[Should you use JWT/JOSE? - Neil Madden](https://neilmadden.blog/2017/03/15/should-you-use-jwt-jose/)
[^4]: ***Criticism of cryptographic agiility, and support for limited choices:***<br/>[Against Cipher Agility in Cryptography Protocols - Scott Arciszewski](https://paragonie.com/blog/2019/10/against-agility-in-cryptography-protocols)
[^5]: ***JWT vulnerabilities:***<br/>[Critical vulnerabilities in JSON Web Token libraries - Auth0](https://auth0.com/blog/critical-vulnerabilities-in-json-web-token-libraries/)
[^6]: ***Expiration dates for suites***:<br>"[W3C Public VC-WG List](https://github.com/w3c/vc-data-model/issues/253#issuecomment-474029947)"
[^7]: ***TLS Cipher Suites to Remove***:<br/>[Eliminating Obsolete Transport Layer Security (TLS) Protocol Configurations - National Security Administration](https://media.defense.gov/2021/Jan/05/2002560140/-1/-1/0/ELIMINATING_OBSOLETE_TLS_UOO197443-20.PDF)
[^8]: ***Wireguard's limited choices:***<br/>[WireGuard: The New Gold Standard for Encryption](https://www.perimeter81.com/blog/network/wireguard)
[^9]: ***This article even proposes no version numbers:***<br/>[Key-driven cryptographic agility - Neil Madden](https://neilmadden.blog/2018/09/30/key-driven-cryptographic-agility/)
[^10]: ***An article on risk assessment to integrate risks of cryptographic agility, however, it doesn't suggest the latest thought of just avoiding the problem. But it has some good risk modeling thoughts when we return to that:***<br/>[CARAF: Crypto Agility Risk Assessment Framework - Ma, Colen, et al](https://academic.oup.com/cybersecurity/article/7/1/tyab013/6289827)
