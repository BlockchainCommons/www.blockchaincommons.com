---
header:
  overlay_color: "#00f"
  overlay_filter: "0.35"
  overlay_image: /images/blueprints.jpg
  og_image: /images/musings-card.jpg
  actions:
    - label: "See All Musings"
      url: /musings.html
tagline: "Why Schnorr is Ground-Breaking and How it Works"
title: "Musings of a Trust Architect: A Layperson's Intro to Schnorr"
author: "Christopher Allen"
excerpt_separator: "<!--more-->"
classes:
  - wide
categories:
  - Musings
tags:
  - Schnorr
  - Signatures
  - Top-Articles
image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/musings.png
---

> **ABSTRACT:** Schnorr signatures have been a long time coming, but now that [they're finally here](https://twitter.com/ChristopherA/status/1716919363729801494), they open up broad new cryptographic frontiers, including the improved privacy of signature aggregation and blind signatures, the improved power of threshold signatures and adapter signatures, and much more. This article explores some of those frontiers and also offers a simplified look at how Schnorr works.

<!--more-->

## What's Sigs Got To Do With It?

> _I was introduced to prime numbers in the third grade, when I “discovered” them accidentally, and a great teacher encouraged me to explore them further. Conversely, I learned about finite fields between my Junior and Senior years of High School, when I was offered the chance at taking a college course over the summer and had to find something that didn't depend on Calculus, which I hadn't yet taken._
>
> _I didn't know it at the time, but I was delving into the mathematical foundations of two powerful signature systems: RSA and Schnorr._

In the  world of digital communication, a pressing question often arises: how can we trust and authenticate digital messages? The answer is to use digital signatures.

Digital signatures function similarly to a seal of authenticity on a physical document, but for digital content. They assure the recipient of the message's integrity and the sender's authenticity. There are many methods for signatures, with RSA and Schnorr being the best known. They mostly rely on public-key cryptography: a signer uses his private key for a signature, which can then be verified with a public key.

## The Schnorr Legacy

> _I discovered RSA, which secures its signatures using prime numbers, in college. But it was when I later encountered Schnorr, built on finite fields, that I met the first cryptography that I truly fell in love with._

Claus-Peter Schnorr introduced Schnorr signatures in the early 1990s. They were not the first digital signature, but they had a strong mathematical foundation: they were provably secure under specific assumptions. They were invented later that other systems like RSA, but they provided a number of new benefits including:

* **Compactness** — Schnorr signatures are small, even when there are multiple signers.
* **Signature Aggregation** — Multiple signatures can be aggregated together and look exactly like a single signature.
* **Faster Verification** — Because of their small size (and the fact that aggregating multisigs doesn't increase that size), Schnorr signatures can be verified quickly.
* **Threshold Signatures** — Multisignatures requiring a certain quorum of participants are possible.
* **Blind Signatures** — Signatures can be made while hiding the content.
* **Adapter Signatures** — Signatures can be hidden by other values.

## Beyond the Fields We Know

> _Beyond all of their new benefits, I fell in love with Schnorr signatures because they were elegant. The aggregation of signatures was done with simple mathematical operations. You added two signatures together and they were aggregated! Or, you could subtract any signature from an aggregate sum! But perhaps I shouldn't say "simple" mathematical operations: Schnorr signatures depend on finite field math._

Think of finite fields as domains where numbers play by a unique set of rules. Each field is constrained to only contain certain numbers, usually defined by the letter `p`. The field then defines basic mathematical operations such as addition and multiplication such that if the operands are within the finite field, then the result of an operation on those operands will also lie within the finite field.

As it happens, the elliptic curves used for most modern cryptography are defined over finite fields. The finite fields act as a modulo to the curve, ensuring that the results of all operations on the curve fall within the field.

- Bitcoin's `secp256k1` works within the bounds of:
   - ``[ p = 2^{256} - 2^{32} - 977 ]``
- Curve25519, popular in key exchanges, operates around:
   - ``[ p = 2^{255} - 19 ]``
 
## Schnorr like an Eagle

> _When I was working as CTO of Certicom, I contacted the holders of the Schnorr patent about licensing it, but they wanted impossible terms. I assume it was the same for others who tried to use the cryptography at the time._
>
> _Those patent restrictions ultimately held back Schnorr signatures from broader acceptance until their expiration in 2008. Even afterward, there wasn't a quick move to Schnorr, despite its advantages, because ECDSA was mature, while there wasn't yet any good code for Schnorr. I sometimes wonder where we might be today if Bitcoin had mined its Genesis block four or five years after the expiration of the Schnorr patents, rather than a scant 11 months later._
> 
> _When I was working at Blockstream, following the expiration of the Schnorr patent, I pestered our engineers about Schnorr. I was happy to then be at the conference where the MuSig multiple-signature system was first rolled out, using Schnorr and a multi-stage signing system that addressed some of the challenges of the powerful signature technology. The security was quickly broken, but that was just a first step, before the release of next-generation Schnorr systems such as MuSig 2 and FROST._
>
> _It's taken a few decades, but due to their simplicity and robustness, we are at last in a future where Schnorr signatures are possible. We can at last implement the many possibilities that I couldn't even imagine when I first met finite fields, in that summer class years ago._

As a new technology, Schnorr has pitfalls and "footguns" that even now might not be fully understood. They need to carefully reviewed before the technology can be safely used.

Some of the earliest challenges of Schnorr have included:

- **Naive Aggregation**:
   Merging signatures without verification is risky. Combining known good signatures with an adversary's signature can actually nullify a signature as a whole because of the additive nature of Schnorr signatures. Advanced measures can prevent such issues.
- **Replay Attacks**:
   Without unique transaction data, a valid signature can be maliciously reused. The solution? Incorporate distinct transaction information within signatures.
- **Malleability**:
   An adversary might slightly alter a good signature while maintaining its validity. Contemporary protocols ensure signatures are consistent and resistant to changes.

Today, two major solutions address the challenges of Schnorr signatures, allowing users to take advantage of their many features:

- **MuSig2**: A scheme focusing on multi-signatures. It addresses the issue of naive aggregation by ensuring individual participants cannot manipulate the combined public key. It only requires two rounds of communication to be completed between the parties. However, it restricts itself to N-of-N signatures, disallowing threshold schemes (except perhaps in a variant that creates a Merkle tree of MuSigs). Major advantages includes accountability and  key generation being noninteractive.
- **FROST**: A versatile Schnorr threshold signature strategy, allowing a quorum to sign without revealing which members did so, increasing privacy and efficiency. It however, requires the completion of three rounds of communication by the parties before use. Major advantages include the ability to use Shamir protocols for refreshing shares, repairing lost shares, and enrollment and disenrollment of participants. The [Zcash Foundation implementation of FROST](https://frost.zfnd.org/) has recently received a successful [security assessment](https://research.nccgroup.com/2023/10/23/public-report-zcash-frost-security-assessment/). Their [Understanding FROST article](https://frost.zfnd.org/frost.html) is also a nice, brief overview of the technology.  

## Schnorr in a Nutshell (8 Bits)

The following examples offer a layman's explanation of Schnorr and its operations using an 8-bit model, which is to say an imaginary finite field that ranges from 0 to 255. This sort of finite field is easily managed by applying a modulo to all the operations. In this example, addition and subtraction operations would be finalized by applying "modulo 256", ensuring that the result remains within the field.

Obviously, practical cryptographic applications work with much larger numbers, which helps to ensure their security, but these small numbers can make examples much easier to read and understand.

### Generating Public Keys

For any signature, the first requirement is generating a public key from a secret private key. Here's a simplified 8-bit example:

1. **Private Key**: Start with a private key, for example, Alice's private key is `50`.
2. **Constant**: Multiply it by a constant number, say `5`.
3. **Public Key**: The result, (`50 x 5 = 250`), becomes Alice's public key.

Seems straightforward, right? The catch is that the mathematical definitions of the actual finite fields and the operations used by Schnorr ensure that division is almost impossible: if someone only has the public key (`250`) and the constant (`5`), working backwards to figure out our private key is more challenging than the reverse because of this special math. 

This difficulty to reverse is what makes this cryptography "asymmetric", which is crucial for security. It’s like baking a cake; once you have the final product, it's very difficult to determine the exact ingredients and their quantities.

### Creating Signatures

Imagine Alice wants to send Bob a secure message. Here’s how she would do it using the Schnorr signature system:

1. **Private Key**: Alice has a secret number, which she never shares with anyone. Let's say this number is `50`.
2. **Message**: Alice has a message. It could be anything, from a simple greeting to a bank transaction. In the digital world, this message can be represented as a number.
3. **Random Figure**: Alice picks a random number for each new message she wants to sign. Let's say she picks `20` for this particular message.
4. **Signature Calculation**: She then uses her private key, the random number, and her message to do some special math, which creates a unique signature for that message. In our 8-bit example, this math might lead to a signature like `150`. This signature is unique to the message and Alice's private key; even a small change in the message would produce a vastly different signature.
5. **Sending**: Alice sends her message and the signature (`150`) to Bob, but keeps her private key and random number secret.

#### Verifying Signatures

Now, let’s say Bob receives Alice's message and the signature she produced. To be certain that it's truly from Alice and hasn’t been tampered with, he needs to verify the signature:

1. **Public Key**: Everyone knows Alice's public key (like a public email address). In our example, this is `250`. Alice would've previously derived this public key from her private key using some more special math and made it publicly available.
2. **Verification**: Using the signature Alice sent (`150`), her public key (`250`), and the original message, Bob does his own math. (Though a private key can't be easily calculated from a public key, it *is* easy to determine that a signature matches a known public key using Schnorr's special math.) If Bob's calculations match the signature Alice sent, then he knows two things for sure: the message truly came from Alice (because she's the only one with the private key that matches the public key that Bob tested against); and the message hasn’t been tampered with (because the signature matched perfectly).
3. **Outcome**: Since Bob’s math using the public key and the message matched Alice's signature, he's assured of the message’s legitimacy.

In a nutshell, Alice uses her private key to "stamp" a message, and Bob uses her public key to verify that "stamp." The beauty of Schnorr signatures is that these calculations are simple (compared to other digital signature methods), yet remain secure, making them a favorite in many cryptographic applications.

### Creating Sequential Multisigs

Imagine a scenario where endorsements need to be made in a particular order, much like a relay race where one athlete passes the baton to the next. This is a simple form of multisignature that any signature system is likely to support.

1. **Initial Endorsement**: Alice wants to sign a document, let’s say a declaration. She does her special math with her private key and the message to produce a signature, which for simplicity, we'll say is `150`.
2. **Subsequent Endorsement**: Bob, having seen Alice's endorsement, decides he wants to endorse her action. He takes Alice's signed declaration and adds his signature to it. Bob's endorsement, perhaps, produces a signature of `75`.
3. **Sequential Result**: Now, the document carries both signatures, `150` from Alice followed by `75` from Bob, indicating a clear sequence: first Alice, then Bob.

### Creating Aggregate Multisigs

However, Schnorr signatures can be much more powerful than most traditional signature systems. They allow for aggregate signatures, where parties can sign in any order they want and jointly endorse a message.

1. **Individual Signatures**: Alice and Bob both want to co-sign a document. Alice, with her special math and private key, creates a signature, say `150`. Bob, independently, generates his signature, which might be `75`.
2. **Aggregation**: Using Schnorr's unique properties, these two signatures can be combined. Instead of appending one after the other, Schnorr adds the two together, possibly producing a single value of `225`.
3. **Aggregate Result**: The document now has one composite signature, `225`. Anyone verifying this knows both Alice and Bob endorsed it, but there’s no distinction about who signed first.

### Creating Threshold Signatures

In scenarios where a group decision is required, threshold signatures (or quorum signature aggregation) shines. It allows a subset of a larger group to sign a document, indicating a collective endorsement.

1. **Group Dynamics**: Imagine a council of five members. For some decisions, the endorsement of all members isn't necessary. Instead, only a majority, say three members, is sufficient.
2. **Individual Signatures**: Three members, Alice, Bob, and Carol decide to endorse a statement. Their signatures might be `150`, `75`, and `30` respectively.
3. **Aggregation**: With Schnorr, these signatures can be aggregated into a single composite signature, possibly `255`.
4. **Collective Result**: This single signature, `255`, stands testament that a quorum of the council endorsed the statement. Verifiers don't necessarily know which three members endorsed it, only that at least three did.

### Advanced Schnorr Techniques

Because of the power of Schnorr, there are even more possibilities:

1. **Blind Signatures**:
   Vital for preserving privacy. Bob wants Alice's signature without revealing the message (let's say `50`). By altering it slightly, like by adding `5`, he disguises it. Alice then signs this modified message (`55`), and Bob later extracts the initial signature.
2. **Key Aggregation**:
   Combines multiple public keys into one. With Alice's key at `250` and Bob's at `5`, the combined key might be `255`.
3. **Adapter Signatures**:
   This combines secret communication with validation. Alice holds a confidential number, say `20`. Bob communicates with her, and as she signs, she discloses her secret as part of the signature.

Even this just skims thes surface of possibilities. Further complexities include the use of hashes, commitments, challenges, and more complex threshold schemes. 

## Conclusion

Schnorr is an incredibly powerful toolbox. Techniques such as signature aggregation, collective multisigs, blind signatures, key aggregation, and adapter signatures demonstrate the flexibility of Schnorr while maintaining its ease of use and efficiency as well as the integrity and authenticity of the messages. The result is a wide variety of endorsement dynamics that will support many different use cases.

Now that MuSig and FROST are increasingly mature, these many dynamics and use cases, which have been waiting in the wings for more than 20 years, can finally be a reality.

I believe that it's truly a cryptographic revolution, as important as many of the ones that have come before.
