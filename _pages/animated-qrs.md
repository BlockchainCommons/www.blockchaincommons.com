---
cover: false
header:
  overlay_color: "#000"
  overlay_filter: "0.25"
  overlay_image: /images/qr-background.jpg
  og_image: /images/bcc-card.jpg
title: Animated QRs
hide_description: true
classes:
  - wide
permalink: /devs/animated-qrs.html
---

{% include video id="HsFF5HPKQIk" provider="youtube" %}

**Animated QRs** are an interoperable specification for transmitting data that allows for the transmission of relatively large amounts of data (compared to standard QRs). They were created with the following goals:

* To Allow for the Transmission of Data Across Airgaps.
* To Support the Conveyance of More Data than Allowed by a Static QR.
* To Especially Enable PSBT Signing That is Done on an Unconnected Device.
* To Ensure Interoperability among Many Vendors by the Use of Uniform Resources.
* To Resolve [The NASCAR Problem](https://indieweb.org/NASCAR_problem) in Wallets.

## Airgap Usage

<img src="https://raw.githubusercontent.com/BlockchainCommons/Gordian/master/Images/airgap.png" align="right" width=100px>

QRs came into use in the digital-asset community because they could be used in airgap architectures. This allows for the storage of sensitive data (such as seeds and keys) in a device not directly connected to the internet, such as a hardware wallet or (to a lesser extent) a phone. A coordinator that is linked to the internet can then communicate with the disconnected device by QRs, without any sort of direct connection.

One of the earliest use cases for airgaps was Partially Signed Bitcoin Transactions (PSBTs). A networked coordinator could create a PSBT and then send it to the disconnected device for signing. After a PSBT was totally signed it could be returned to the networked coordinator for transmission to the Bitcoin network.

_Why Airgaps?_ Airgaps allow users to keep critical data in a location that's not connected to the internet, protecting them from most sorts of theft and hacking, which tend to rely on internet-connected devices. By usings QRs to constrain communication with the airgapped device, security is greatly improved, and even if some overflow were possible, the requirement for a user to carry data back and forth across the airgap would greatly reduce the choice of an exploit. This means that even if a device coordinating a transaction were corrupted, the keys wouldn't be, and even if a transaction were produced incorrectly, a user could see this on their signing device.

_Why PSBTs?_ PSBTs are a perfect complement to airgaps because they allow transactions to be created on an internet-connected device (which knows about UTXOs) but signed on an airgapped device (which knows about keys). They also become more important as multisigs are increasingly used to protect digital assets, because PSBTs allow for individual key holders to each sign on their own device, at their own convenience.

## Size Problems

Unfortunately, QRs can only contain limited amounts of information. Technically, they can hold up to 7089 numeric characters, 4296 alphanumeric characters, or 2953 bytes of binary data. The reality is often lower than that, especially because large QRs pack their data so tightly that they can easily become unreadable on consumer devices such as phones or computer cameras. 

This proved problematic for PSBTs because they often require the transmission of larger amounts of information, particularly as more signers were added. Solving this problem required a new type of QR: the animated QR, which transmits several QR frames that together comprise the entirity of a large set of digital data, such as a PSBT.

## UR Interoperability

Blockchain Commons' Animated QRs are built atop the [Uniform Resource (UR) specification](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2020-005-ur.md) to ensure their interoperability among many wallets. URs are fundamentally a self-describing data encoding, but they can also be fragmented and sequenced. This allows a much larger data set to be broken into smaller segments and later to be recombined, all in a carefully specified way. To create Animated QRs, fragments are created that are each small enough to be encoded in a QR that will be readable by average consumer devices.

## Fountain Code Tech

<img src="https://raw.githubusercontent.com/BlockchainCommons/URDemo/master/Images/urdemo-animated.gif" align="right" width=200px>

Blockchain Commons' multipart Animated QRs are built from URs using [Luby transform codes](https://en.wikipedia.org/wiki/Luby_transform_code) (fountain codes). This rateless encoding method allows for the receipt of an animated QR to begin at any frame and for the transmission to overcome issues with missing frames.

This process is detailed in our references: [URKit](https://github.com/BlockchainCommons/URKit), a reference framework that allows for the encoding and decoding of URs in Swift; and [URDemo](https://github.com/BlockchainCommons/URDemo), an iOS demo that shows how Animated QRs built on URs can be sent and received. A variety of [UR libraries](https://github.com/BlockchainCommons/crypto-commons#bc-ur) in additional languages such as Java, Python, and Rust are available thanks to our community.

The use of an interoperable specification for encoding, fragmenting, sequencing, transmitting, recombining, and decoding data is what allows Animated QRs to defeat the NASCAR problem. Already, software wallets are building up huge menus of hardware devices, with different interactions required for each. Wallets using the UR standard can instead present a unified communication methodology, making interaction with other devices effortless.

## Wide Adoption

Prior to Blockchain Commons' release of URs and Animated QRs, PSBTs could not be reliably transmitted using QR codes. As a result of this need, Blockchain Commons' Animated QRs have seen [wide adoption](https://github.com/BlockchainCommons/Gordian-Developer-Community#urs) in the wallet developer community. 

<center>
<img src="https://www.blockchaincommons.com/images/ur-adopters-bg.jpg" width="75%" style="border: 2px solid #699EA0">
</center>

However, URs can do much more than just allow the transmission of PSBTs. They were built to allow for the transmission of a [wide variety](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2020-006-urtypes.md) of data types in a way that is both self-describing and interoperable. They support the transmission of seeds, keys, envelopes, and other data between a wide variety of parties and increase the resilience of that valuable data because the self-describing tags ensure that it can be recovered by anyone at a later time.

See our [UR docs](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2020-006-urtypes.md) for more information on the foundational data format that allows for the creation of animated QRs.

## Supporting Interoperability

If you're a **Bitcoin User** who values the safety and resilience of your digital assets, don't take any chances with their safety. Use a wallet that supports interoperability specifications such as Animated QRs for PSBTs (and other future interoperability standards from Blockchain Commons). This not only increases the _convenience_ of your assets, because you can use them across multiple wallets and devices, but also their _resilience_, because you can use one of those alternative wallets if your main wallet's vendor goes out of business or suffers a catastrophic failure.

If you're a **Wallet Developer** who wants to to support their users in this way, and also to take advantage of the innovations of Blockchain Commons and its members, join our Gordian Developer Community. Sign up for our [announcements list](https://www.blockchaincommons.com/subscribe.html#gordian-developers) or join our [Signal channel](https://www.blockchaincommons.com/subscribe.html#gordian-developers). Even better, join us on [GitHub](https://github.com/blockchaincommons) where we welcome your input on projects!

## Links

* [Blockchain Commons Repos](https://github.com/blockchaincommons)
* [UR Overview](https://github.com/BlockchainCommons/crypto-commons/edit/master/Docs/ur-1-overview.md)
* [UR Specification](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2020-005-ur.md)
* [UR Data Type Registry](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2020-006-urtypes.md)
* [UR Adoption](https://github.com/BlockchainCommons/Gordian-Developer-Community#urs)
* [URKit](https://github.com/BlockchainCommons/URKit)
* [URDemo](https://github.com/BlockchainCommons/URDemo)
