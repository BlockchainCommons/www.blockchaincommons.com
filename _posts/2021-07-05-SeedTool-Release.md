---
title: "Gordian Seed Tool Reveals the Foundations of Cryptography"
excerpt_separator: "<!--more-->"
categories:
  - Projects
tags:
  - Apps
  - SeedTool
  - Gordian
  - Projects
---

<img src="https://github.com/BlockchainCommons/GordianSeedTool-iOS/blob/master/images/logos/gordian-seedtool-logo-white.jpg" align=right width=250>

Blockchain Commons has released Gordian Seed Tool — a new iOS app that allows for the creation, storage, backup, and transformation of cryptographic seeds — on the [Apple appstore](https://apps.apple.com/us/app/gordian-seed-tool/id1545088229). It's an independent, private, and resilient vault meant to protect all of your cryptocurrency.

<div class="bold--excerpt--node">Read More</div>

<!--more-->

Though many people are familiar with the private keys used to unlock their cryptocurrency transactions, Gordian Seedtool takes a step back and allows you to manage the fundamentals upon which private keys are built: entropy and seeds. You can use coin flips, die rolls, card draws, or iOS randomness as the entropy to generate the seeds, or you can import them. Afterward, you'll have the foundation of a whole hierarchy of private and public keys.

The fundamental goal of Gordian Seedtool is to protect your seeds. It does so by using Apple's trusted encryption routines to encode your cryptographic seeds on your closely held mobile device. Further resilience is added through integration with iCloud. If your mobile iOS device has a network connection, its seeds are stored in iCloud using end-to-end encryption. If you lose your device, you can then retrieve them with a replacement device logged into the same Apple account.

You'll also be able to easily identify your seeds using the Blockchain Commons [object identity block](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2021-002-digest.md#object-identity-block), which includes a visual lifehash, a human-readable name, an icon, and an abbrviated digest. Put them together and you should be able to recognize each seed at a glance.

<img src="https://github.com/BlockchainCommons/GordianSeedTool-iOS/blob/master/images/gg-list.jpg" align=right width=250>

Gordian Seed Tool's protection is posited on the security of airgaps, where you store your secrets on a closely held device that isn't fully networked, such as a mobile phone, and then communicate with it primarily through QR codes or text that can easily be transmitted across that gap of air. Your seeds are thus protected by modern mobile-device security such as data encryption and biometric access protection. (If you prefer, you can also use an entirely non-networked device, such as an iPod Touch, to ensure that your seeds never leave your device.)

Besides generating seeds, storing them, and backing them up, Gordian Seedtool can also transform your seeds. It can derive Bitcoin and Ethereum public and private keys from your seeds,  encode your seeds as bytewords, BIP39 words, or hex, or shard them into SSKR shares. Your seed is the basis for a whole tree of data, and Gordian Seed Tool gives you access to all of it.

Gordian Seedtool is just one of several Blockchain Commons apps that demonstrate the Gordian principles of independence, privacy, resilience, and openness. The [Gordian QR Tool](https://apps.apple.com/us/app/gordian-qr-tool/id1506851070) offers a way to store confidential QRs such as 2FA seeds, SSKR shares, and (for that matter) cryptoseeds. Our forthcoming _Gordian Cosigner_ will demonstrate how to easily manage Bitcoin transactions across an Airgap.

If you'd like to learn more about the libraries, specifications, and references being created by Blockchain Commons in coordination with our airgap wallet community, please visit our [discussion forums](https://github.com/BlockchainCommons/Airgapped-Wallet-Community/discussions) and our [research repo](https://github.com/BlockchainCommons/Research/blob/master/README.md). You can also support our work [as a patron](https://github.com/sponsors/BlockchainCommons).
