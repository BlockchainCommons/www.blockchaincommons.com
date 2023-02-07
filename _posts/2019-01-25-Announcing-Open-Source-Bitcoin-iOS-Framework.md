---
title: "Announcing Open Source Bitcoin Framework for iOS"
excerpt_separator: "<!--more-->"
categories:
  - Libraries
tags:
  - Bitcoin Framework
  - iOS Libraries
classes:
  - wide
---

### Building on Libbitcoin

Today we are announcing the availability of the open source [Bitcoin framework for iOS](https://github.com/BlockchainCommons/iOS-Bitcoin). We have been working with veteran iOS developer [Wolf McNally](https://wolfmcnally.com/125/announcing-open-source-bitcoin-framework-for-ios/) on wallet apps for iOS that will support airgapped transaction signing and [BTCR Decentralized Identity (DID)](https://w3c-ccg.github.io/didm-btcr/). As part of this effort we chose to build on the open source [libbitcoin](https://libbitcoin.org/) library.

<!--more-->

### From C++ to Swift

Libbitcoin is written in C++. This poses a problem for incorporating it into native iOS apps: there is no straightforward way to import C++ code into Swift. Swift does interface fairly easily to straight C, however. So to bridge the gap we wrote two frameworks: [CBitcoin](https://github.com/BlockchainCommons/iOS-CBitcoin), which exports a C-based interface from libbitcoin, and [Bitcoin](https://github.com/BlockchainCommons/iOS-Bitcoin), which builds on CBitcoin to export a clean Swift interface to libbitcoin.

Since the purpose of these two frameworks is primarily to facilitate building cryptocurrency wallets on iOS, we haven't (so far) had a need to export parts of libbitcoin that are useful primarily to Bitcoin nodes. Pull requests are welcome!

Building libbitcoin for iOS is no simple task. It has two other dependencies: [libsecp256k1](https://github.com/bitcoin-core/secp256k1), which handles the [elliptic curve cryptography](https://en.wikipedia.org/wiki/Elliptic-curve_cryptography) and [libboost](https://www.boost.org/), which is a large toolkit for writing better C++. These and libbitcoin itself have to be built as fat binaries for two ARM architectures for running on the iPhone, native MacOS, and another version for running on MacOS under the iOS simulator. For this we built on the open source work of [Airbitz](https://en.bitcoin.it/wiki/Airbitz).

Once the binaries are built, they have to be combined into fat binaries and then bundled into frameworks. We provide a [Bash shell script to coordinate these steps](https://github.com/BlockchainCommons/iOS-CBitcoin/blob/master/build_frameworks.sh). The build takes over half an hour on a Mac Pro, so to save others the time my script zips up the resulting frameworks and checks them into GitHub too. _However_, the zipped frameworks exceed GitHub's file size limit, but it turns out they also have a solution: [Git Large File Storage](https://git-lfs.github.com/).

### Use Now with Cocoapods

The final frameworks are deployed as [Cocoapods](https://cocoapods.org/), and the Bitcoin framework is the only one you need to reference directly in your iOS app, by including:

```ruby
pod 'Bitcoin'
```

in your `Podfile`, and:

```swift
import Bitcoin
```

in your `.swift` files.

Unit tests are in the Bitcoin framework `Example` target. All the detailed instructions are in the `README.md` for the [Bitcoin framework](https://github.com/BlockchainCommons/iOS-Bitcoin).
