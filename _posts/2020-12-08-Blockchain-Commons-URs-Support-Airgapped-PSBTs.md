---
title: "Blockchain Commons' Uniform Resources (URs) Support Airgapped PSBTs & More"
excerpt_separator: "<!--more-->"
categories:
  - Specifications
tags:
  - AirGap
  - UR
classes:
  - wide
---

The [Uniform Resources specification](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2020-005-ur.md) is one of Blockchain Commons' most notable wallet enhancements of 2020: it enables airgapped PSBTs and is supported through a variety of reference libraries, including C++ and Swift implementations. Third parties have already ported the UR encoder to Python, Java, and Rust.

Uniform Resources, or URs, are a method for encoding binary data in plain text strings that are also well-formed URIs. They are simultaneously intended to address the challenges of QR codes, which are the main way that Bitcoin wallets transmit data across airgaps. While QR codes themselves are standard, the data encoded within QR codes is not, resulting in inconsistent usage among developers.

URs were created to resolve these interoperability issues by creating a standardized method for encoding binary data. They're built on CBOR, the Concise Binary Object Representation described in [IETF RFC 7049](https://tools.ietf.org/html/rfc7049). The CBOR data is encoded in a typed UR object, which creates a self-describing, structured binary representation. URs can be transmitted as text or encoded via other means, including QR codes. Once received, URs can be decoded by different apps on different machines without having to guess about the contents or the encoding methods.

<!--more-->

The tight size limitations of QRs, where version 40 QR codes max out at 2,953 bytes, are also resolved in the UR specification. The CBOR foundation supports sizes up to 2^32-1 bytes; the UR specification then describes how to sequence those large binary encodings into a multipart UR, which can be displayed across multiple QR codes.

<img src="https://raw.githubusercontent.com/BlockchainCommons/URDemo/master/Images/urdemo-animated.gif" align="right">

Thus far, the prime use of URs has been to allow the airgapped transmission of PSBTs, which frequently don't fit into a single QR code. Using URs, PSBTs can instead be transmitted as a animated sequence of QR codes, with each frame displaying one part of a UR sequence. Fountain codes allow the QR recording to start at any point and resolve problems with missing individual frames. This permits for the easy and intuitive transmission of partially signed transactions to airgapped devices for further signing: a user just needs to hold up a camera to scan the animated QR.

However, URs can do much more than that: they can support any airgapped Bitcoin function, as well as Blockchain Commons' unique [torgap architecture](https://github.com/BlockchainCommons/torgap/blob/master/Docs/FAQ.md). Definitions for seeds, keypaths, addresses, and accounts allow for all sorts of Bitcoin data to be transmitted in the efficient, self-describing format. In additions, URs can be sent not just as QR codes, but also as URLs or Signal Whispers. The possibilities go far beyond animated QRs for PSBTs.

As a creator of open infrastructure, Blockchain Commons is working to support wallet interoperability, helping end-users have many flexible choices among vendors. URs are one of our earliest and most successful open wallet projects. Our [bc-ur reference library](https://github.com/BlockchainCommons/bc-ur) supports URs in C++, while our [URKit](https://github.com/BlockchainCommons/URKit) does so in Swift. The specification has also been adopted by a number of third-party wallet developers:

- Foundation Devices, a company that focuses on open hardware for the decentralized internet, has created a [python implementation](https://github.com/Foundation-Devices/foundation-ur-py).
- Sparrow Wallet, a Bitcoin wallet for those who value financial self sovereignty, has created a [java implementation](https://github.com/sparrowwallet/hummingbird).
- Dominik Spicher has created a [rust implementation](https://github.com/dspicher/ur-rs).
  We expect to see URs deployed in more commercial wallets in the near future.

<table style="border:0px solid black;margin-left:auto;margin-right:auto;">
  <tr>
    <td>
      <a href="https://foundationdevices.com/"><img src="https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/airgap/foundation-logo.png"></a>
    </td>
    <td>
      <a href="https://sparrowwallet.com/"><img src="https://raw.githubusercontent.com/BlockchainCommons/www.blockchaincommons.com/master/images/airgap/sparrowwallet-logo-sm.png"></a>
    </td>
  </tr>
</table>

If you'd like to learn more about URs, please read our [research paper, BCR-2020-005](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2020-005-ur.md), and our [growing library of UR type definitions](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2020-006-urtypes.md). If you'd like to support Blockchain Commons' open infrastructure development, please become a [GitHub sponsor](https://github.com/sponsors/BlockchainCommons) or make a donation to our [BTCPay server](https://btcpay.blockchaincommons.com/). Blockchain Commons is funded entirely by patronage, donations, and collaborative partnerships with people like you.
