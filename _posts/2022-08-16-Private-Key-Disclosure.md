---
title: "Private Key Disclosure: A Needless Threat to Rights and Assets"
excerpt_separator: "<!--more-->"
categories:
  - Articles
tags:
  - Advocacy
  - Legislation
  - Self-Sovereign Identity
classes:
  - wide
header:
  og_image: https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/posts/legislation.jpeg
---

***UPDATE 2023-02-16: This bill has passed the Wyoming Assembly 41-13, a day after the Wyoming Senate passed it by a vote of 31-0. If Wyoming Governor Mark Gordon signs the bill, it will go into effect on 1 July. Details of the current bill are at [wyoleg.gov tracker](https://wyoleg.gov/Legislation/2023/HB0086). If you have questions, ask at the [Twitter thread](https://twitter.com/ChristopherA/status/1626243594364526592).***

> **ABSTRACT:** Digital assets are only as safe as their private keys. Securing private keys through responsible key management has thus been a major focus at Blockchain Commons, under our [#SmartCustody](https://www.smartcustody.com/) initiative. Unfortunately, securing keys ultimately isn't just a logistical problem or a technical problem. It's also a legal problem because US courts have inserted themselves into the process by demanding keys, often as a part of discovery.
>
> Turning over keys to courts not only introduces major threats to the digital assets controlled by the keys, but it also fundamentally misunderstands the purpose and use of private keys. There are better tools for court-based discovery, public keys prime among them. There are better, more traditional ways to enforce the turn over of assets. Requiring the disclosure of private keys instead is a needless threat not just to digital assets, but to our rights as well.

<hr>

Increasingly, attorneys in the United States are asking courts to force the disclosure of private keys as part of discovery or other pre-trial motions, and increasingly courts are acceding to those demands. Though this is a relatively recent phenomenon, it's part of a larger problem of law enforcement seeking back doors to cryptography that goes back at least to the U.S. government's [failed introduction of the Clipper Chip](https://www.eff.org/deeplinks/2015/04/clipper-chips-birthday-looking-back-22-years-key-escrow-failures) in 1993.

![](/images/posts/sink-clipper.jpg)

Unfortunately, today's attacks on private keys in the courtroom have been more successful, creating an existential threat to digital assets, data, and other information protected by digital keys. That danger arises from a fundamental disconnect between this practice and the realities of technologies that leverage public-key cryptography for security: private-key disclosure can cause irreparable harm, including the loss of funds and the distortion of digital identities.

As a result, we need to support legislation that will protect digital keys while allowing courts to access information and assets in a way that better recognizes those realities. The private-key disclosure law [currently being considered in Wyoming](https://youtu.be/61c3sYGqO-E?t=1063) is an excellent example of the sort of legislation that we could put forth and advocate for in order to maintain the proper protection for our digital assets and identities.

<!--more-->

[Wyoming Senate Filing 2021-0105](https://wyoleg.gov/Legislation/2021/SF0105):
<blockquote>
    No person shall be compelled to produce a private key or make a private key known to any other person in any civil, administrative, legislative or other proceeding in this state that relates to a digital asset, other interest or right to which the private key provides access unless a public key is unavailable or unable to disclose the requisite information with respect to the digital asset, other interest or right. This paragraph shall not be interpreted to prohibit any lawful proceeding that compels a person to produce or disclose a digital asset, other interest or right to which a private key provides access, or to disclose information about the digital asset, other interest or right, provided that the proceeding does not require production or disclosure of the private key.
</blockquote>
 
## The Realities of Private Keys

The forced disclosure of private keys is deeply harmful because it fundamentally runs at odds with how private keys work. Attorneys (and courts) are usually trying to force the disclosure of information or (later) the relinquishment of assets, but they're treating private keys just like they're physical keys that they could demand, use, and give back.  

Private keys do not match any of these realities. As Wyoming State Legislature Senate Minority Leader [Chris Rothfuss](https://wyoleg.gov/Legislators///1971) says:
> <img src="https://www.blockchaincommons.com/images/quote-rothfuss.jpeg" alt="Sen. Chris Rothfuss" style="float: right;" width="75" >"There is no perfect analog for a modern cryptographic private key in existing statute or case law; it is unique in its form and function. As we build a policy framework around digital assets, it is essential that we appropriately recognize and reflect the characteristics of the underlying public / private key and cryptographic technologies. Without clear, unambiguous legal protection for the sanctity of the private key, it is impossible to ensure the integrity of the associated digital assets, information, smart contracts and identities."


That appropriation recognition and reflection requires us to understand that:

*1. Private keys are not assets.*

Private keys are fundamentally the way we exert authority in the digital space, an interface between our physical reality and the digital reality. They may give us the ability to control a digital asset: to store it, to send it, or to use it. Similarly, they may give us the ability to decrypt protected data or to verify a digital identity. However, they are not the assets, the data, nor the identity themselves.

It's the obvious difference between your car and your electronic key fob. The one is an asset, while the other lets you control that asset. 

As Jon Callas, Director of Technology Projects at the EFF, says:
><img src="https://www.blockchaincommons.com/images/quote-callas.jpeg" alt="Jon Callas, EFF Director Technology Projects" style="float: right;" width="75" >  "They don't even want the key, they want the data; asking for the key is like asking for the filing cabinet rather than the file.”

*2. Private keys are not the proper tool for discovery.*

Treating private keys as a tool to ensure the discovery of information fundamentally misunderstands their purpose. Private keys are not how we see something in digital space, but instead ***how we exert authority in digital space***!

Turning back to comparisons, it's the difference between a ledger and a pen. If you wanted accounting information, you'd ask for the ledger; you wouldn't ask for the pen, especially not if it was a pen that allowed you to write undetectably in the handwriting of the accountant!

Former Federal Prosecutor Mary Beth Buchanan, when offering [testimony](https://diyhpl.us/wiki/transcripts/wyoming-select-committee/private-key-disclosure-buchanan/) in favor of Wyoming's private-key disclosure law, said:

><img src="https://www.blockchaincommons.com/images/quote-buchanan.jpeg" alt="Mary Beth Buchanan" style="float: right;" width="75" >  "the court could order a disclosure or an accounting of all the digital assets that are held, and then those assets could be disclosed and the location of whether they are held across different platforms or even different wallets. But giving the key is actually giving access to those assets. That is the difference."

Fortunately, there is an electronic tool that meets the needs of discovery: public keys. Wyoming has recognized that in their [legislation](https://wyoleg.gov/InterimCommittee/2022/S19-2022061423LSO-0058v0.2.pdf), saying that a private key should never be required if a public key would do the job (and they parenthetically noting at hearings that their current understanding is that a public key will _always_ do the job). If our concern is revealing information that will help to catch and prosecute criminals, then public keys are the answer.

*3. Private keys are not physical.*

Electronic private keys and physical keys are very different. A physical key could pass through many hands and there could be the expectation that it was very likely not duplicated (especially if it were a special key, such as a safety-deposit-box key), and that when the key was returned to the original holder, they would once again have control of all of the linked assets. The same is not true for a private key, which could be easily duplicated by any of the many hands it passed through, with no way to ascertain that had happened.

Returning to the example of a car's key fob, it would not be appropriate to force the disclosure of the unique serial number stored within a car fob for the same reason it's not appropriate to force the disclosure of a private key. Doing so, would give _anyone_ who gets that serial number the ability to create a new fob and steal your car!

*4. Private keys serve many purposes.*

Finally, private keys are likely to have a lot more purposes than physical keys, especially if a court decides to go after not just a specific private key, but the root key from an HD wallet or a seed phrase. Root keys (and seeds) might be used to protect a wide variety of assets as well as private data. They may also be used to control identities and to offer irrefutable proof that the owner agreed to something through digital signatures.

The authoritative uses of private keys are so wide and all-encompassing that it's hard to come up with a physical equivalent. The closest analogy, which was brought up by Blockchain Commons' Christopher Allen at one of the Wyoming hearings, would be if a court demanded access to a hotel room by requiring the hotel's master key, which can provide access to _all_ rooms. But, a private key is more than that, so it would be as if the court also required that someone with signatory powers at the hotel sign a bunch of blank contracts _and_ blank checks. The potential for harm with the disclosure of a private key is just that high for someone who is using it for a variety of purposes — and there will be more and more people doing so as the importance of the digital world continues to increase.

## The Realities of Courts

Going beyond the fact that a private key is the wrong tool for courts and that it's often being used in the wrong way, there are a number of other problematic realities related to the courts themselves and how and when they're trying to access private keys.

*5. Courts are not prepared to protect private keys.*

To start with, courts don't have the experience needed to protect private keys. This danger is made worse by the fact that a single private key is likely to pass through the hands of many different court staff over time. 

But, this isn't just about courts. The problem of creating safe ways to transfer public keys is far bigger. It's something that the cryptographic field as a whole does not have good answers for. Blockchain Commons' Christopher Allen attested in his  testimony in Wyoming that the "immense difficulties of transferring a private key are a risk that allows bearing of false witness." Putting courts, without crypto-expertise, in the middle of the problem could be catastrophic.

Perhaps cryptographers will resolve these issues in time, and perhaps someday courts will be able to share in that expertise if they decide doing so is a good use of their time and resources, but we need to consider keys whose disclosures are being forced _now_.

*6. Courts are requiring premature disclosure.*

The current situation with key disclosure is even more problematic because it's occurring as part of discovery or other pre-trial motions. Discovery rulings are [almost impossible to appeal](https://www.resolvingdiscoverydisputes.com/appeals/obtaining-review-of-discovery-rulings/), which means that in today's environment key holders have almost no recourse for protecting the token of their own authority in digital space.

*7. Courts are more demanding of digital assets than physical assets.*

We recognize that courts should be able to require the _usage_ of a key. Compelling usage is nothing new, but the private key is not required for that, simply a court order.

If someone refuses to use their private key in a way compelled by a court, that's nothing new either. The physical world already has plenty of examples of people refusing such orders, such as by hiding assets or just refusing to pay judgements. They are handled with sanctions such as contempt of court.

Asking for more from the electronic world is an overreach of traditional judgements that also creates much greater repercussions.

## The Repercussions of Disclosure

Using the wrong tool for the wrong reasons and putting it in hands not ready to deal with it will have calamitous results. Here are some of the most obvious repercussions.

*1. Asset Theft*

Obviously, there is a danger of the assets being stolen, as a private key gives total control over those assets. These assets could go far beyond the specifics of what a court is interested in, because of the multitude of uses for keys.

*2. Asset Loss*

Beyond the problem of purposeful theft, keys could be lost, and with them digital assets. Former federal prosecutor Mary Beth Buchanan raised this concern in her [testimony](https://diyhpl.us/wiki/transcripts/wyoming-select-committee/private-key-disclosure-buchanan/), saying: 

><img src="https://www.blockchaincommons.com/images/quote-buchanan.jpeg" alt="Mary Beth Buchanan" style="float: right;" width="75" >"Evidence is lost all the time." If that evidence was a private key, which might hold a variety of assets, information, and proofs of identity, the loss could be tremendous.

Wyoming State Legislature Majority Whip [Jared Olsen](https://wyoleg.gov/Legislators///2035) agreed with this concern at a recent Wyoming hearing, noting that a judicial assistant could delete a key and cause a loss of $8 billion dollars in Bitcoin when there was only a judgment for $100,000. He said he was "concerned about just simply handling it".

*3. Collateral Damage*

Thefts or losses resulting from the disclosure of a private key could also go far beyond an individual before the court. Increasingly, assets are being held in multisignatures, which may grant multiple people control over the same assets. By requiring the disclosure of a key, a court could negatively impact people entirely unrelated to the proceedings.

*4. Identity Theft.*

Because private keys might also protect the identifier for digital identity, their loss, theft, or misuse could put someone's entire digital life at risk. If a key was copied, someone else could pretend to be the holder and even make digital signatures that are legally binding for them. 

## Support This Legislation

Protecting private keys is one of the most important things that Blockchain Commons has ever worked on. As Blockchain Commons' founder Christopher Allen said:
> <img src="https://www.blockchaincommons.com/images/quote-allen.jpeg" alt="Christopher Allen" style="float: right;" width="75" >"I find the protections of this Private Key Disclosure bill crucial for the future of digital rights."

Wyoming State Legislature Senate Minority Leader Chris Rothfuss affirmed this, adding:
><img src="https://www.blockchaincommons.com/images/quote-rothfuss.jpeg" alt="Sen. Chris Rothfuss" style="float: right;" width="75" >" Christopher Allen has been an invaluable member of our blockchain policy community, bringing a lifetime of technical expertise to advise our committee work and inform our legislative drafting. Mr. Allen has emphasized the particular importance of protecting private keys from any form of compulsory disclosure."

We need your help to make it a reality.

If you're an experienced member of the cryptocurrency or digital asset field or a human-rights activist, please submit your own testimony in support to the [Wyoming Select Committee on Blockchain, Financial Technology and Digital Innovation Technology](https://wyoleg.gov/Committees/2022/S19). The bill will be coming up for further discussion on September 19-20 in Laramie, Wyoming.

But, Wyoming is just the start. They are doing an excellent job of leading the way, but we need other states and countries to follow. If you have connections to another legislature, please suggest they introduce [similar language to Wyoming's bill](https://wyoleg.gov/InterimCommittee/2022/S19-2022061423LSO-0058v0.2.pdf).

Even if you don't feel comfortable talking with a legislature, you can help by advocating for the protection of private keys as something different than assets.

Ultimately, our new world of digital assets and digital information will succeed or fail based upon how we lay its foundations today. It could become a safe space for us or a dangerous wild west. 

Properly protecting private keys (and using public keys and other tools for legitimate judicial needs) is a keystone that will help us to build a sturdy edifice.

_This article was also published by [Bitcoin Magazine as "Saving Private Keys from the Courts"](https://bitcoinmagazine.com/legal/saving-bitcoin-private-keys-from-courts)._
