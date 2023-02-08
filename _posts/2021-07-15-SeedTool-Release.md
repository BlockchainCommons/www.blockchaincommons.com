---
title: "Gordian Seed Tool Reveals the Foundations of Cryptography"
excerpt_separator: "<!--more-->"
categories:
  - Apps
tags:
  - Seed Tool
  - Gordian Architecture
classes:
  - wide
image: https://raw.githubusercontent.com/BlockchainCommons/GordianSeedTool-iOS/master/images/gg-list.jpg
---

<img src="https://raw.githubusercontent.com/BlockchainCommons/GordianSeedTool-iOS/master/images/logos/gordian-seedtool-logo-white.jpg" align=right width=250>

Blockchain Commons has released Gordian Seed Tool, a new iOS app that allows for the creation, storage, backup, and transformation of cryptographic seeds is now available on the [Apple appstore](https://apps.apple.com/us/app/gordian-seed-tool/id1545088229). It is an independent, private, and resilient vault, which can protect the most important underlying secret used by most cryptocurrencies: the cryptographic seed.

<!--more-->

Though most wallets focus on the private keys used to unlock their cryptocurrency transactions, Gordian Seed Tool takes a step back and allows you to manage the fundamentals upon which private keys are built: entropy and seeds. You can use coin flips, die rolls, card draws, or iOS randomness as the entropy to generate your seeds, or you can import them from other applications. Using those seeds, Gordian Seed Tool can then derive unique, non-correlatable public and private keys as you need them.

<img src="https://raw.githubusercontent.com/BlockchainCommons/GordianSeedTool-iOS/master/images/gg-list.jpg" align=right width=250>

The focus of Gordian Seed Tool is to protect your seeds. It does so by supporting new approaches to security such as QR-based airgaps, where you store your secrets on a closely held device that isn't fully networked, such as an offline device in airplane mode, or a strongly protected device like the secure enclave in Apple's iPhone and more modern Macinotoshes. You then communicate with that device primarily through QR codes or text that can easily be transmitted across that gap of air. Your seeds are thus protected by modern mobile-device security such as data encryption, trusted hardware, and biometric access protection.

That data encryption comes about through Apple's trusted encryption routines. Seed Tool then adds resilience through integration with iCloud. If your choose for your mobile iOS device to have a network connection, its seeds will be stored in iCloud using end-to-end encryption. If you lose your device, you can retrieve those seeds with a replacement device logged into the same Apple account. (If you prefer, you can also use a cellular networked device, such as an iPod Touch or wifi-only iPad, leveraging airplane mode, to entirely ensure that your seeds never leave your device.)

You'll be able to easily identify your seeds using the Blockchain Commons [object identity block](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2021-002-digest.md#object-identity-block), which includes a visual lifehash, a human-readable name, an icon, and an abbreviated digest. Put them together and you should be able to recognize each seed at a glance.

Besides generating seeds, storing them, and backing them up, Gordian Seed Tool can also transform your seeds. It can derive popular Bitcoin and Ethereum public and private keys from your seeds, answer requests for other derivations, encode seeds as bytewords, BIP39 words, or hex, or shard them into SSKR shares and save them to different locations or as social recovery with your family, friends and close colleagues. Your seed is the basis for a whole tree of secure data, and Gordian Seed Tool gives you access to all of it.

Gordian Seed Tool is just one of several Blockchain Commons apps that demonstrate the Gordian principles of independence, privacy, resilience, and openness. The [Gordian QR Tool](https://apps.apple.com/us/app/gordian-qr-tool/id1506851070) offers a way to store confidential QRs such as 2FA seeds, SSKR shares, and (for that matter) cryptoseeds. Our forthcoming _Gordian Cosigner_ will demonstrate how to easily manage Bitcoin transactions across an Airgap.

If you'd like to learn more about the libraries, specifications, and references being created by Blockchain Commons in coordination with our airgap wallet community, please visit our [discussion forums](https://github.com/BlockchainCommons/Airgapped-Wallet-Community/discussions), our [YouTube channel](https://www.youtube.com/channel/UCPQ9LtDWZAkfItMF4B5tztw) and our [research repo](https://github.com/BlockchainCommons/Research/blob/master/README.md). You can also support our work [as a patron](https://github.com/sponsors/BlockchainCommons).
