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

Gordian Seed Tool is a new iOS app from Blockchain Commons that allows for the creation, storage, backup, and transformation of cryptographic seeds, now available on the [Apple appstore](https://apps.apple.com/us/app/gordian-seed-tool/id1545088229). It's an independent, private, and resilient vault meant to protect all of your cryptocurrency.

<div class="bold--excerpt--node">Read More</div>

<!--more-->

Though many people are familiar with the private keys used to unlock their cryptocurrency transactions, Gordian Seedtool takes a step back and allows you to manage the fundamentals upon which private keys are built: entropy and seeds. You can coin flips, die rolls, card draws, or iOS randomness as the entropy to generate the seeds, or you can import them. Afterward, you'll have the foundation of a whole hierarchy of private and public keys.

The fundamental goal of Gordian Seedtool is to protect your seeds. It does so by using Apple's trusted encryption routines to protect your cryptographic seeds on your closely held mobile device. Further resilience is added through integration with iCloud. If your mobile iOS device has a network connection, its seeds are stored in iCloud using end-to-end encryption. If you lose your device, you can then retrieve them on a replacement.

<img src="https://github.com/BlockchainCommons/GordianSeedTool-iOS/blob/master/images/gg-list.jpg" align=right width=250>

Gordian Seed Tool's protection is posited on the security of airgaps, where you store your secrets on a closely held device that isn't fully networked, such as a mobile phone, and then connect to it primarily via QR codes or text copies that can easily be transmitted across that gap of air. Your seeds are then protected by modern mobile security such as encrypted data and biometric access protections. If you prefer, you can also use an entirely non-networked device, such as an iPod Touch, to ensure that your seeds never leave your hands.

Besides generating seeds, storing them, and backing them up, you can also use Gordian Seedtool to transform your seeds. Besides being able to derive Bitcoin and Ethereum public and private keys from your seeds, you can also store your seeds as bytewords, BIP39 words, or hex, are shard them into SSKR shares. Your seed is the basis of the cryptographic protection for your digital assets, and Gordian Seed Tool gives you access to all of it.

Gordian Seedtool is just one of several Blockchain Commons apps that demonstrate the Gordian principles of independence, privacy, resilience, and openness. The [Gordian QR Tool](https://apps.apple.com/us/app/gordian-qr-tool/id1506851070) offers a way to store confidential QRs such as 2FA seeds, SSKR shares, and for that matter cryptoseeds. Our forthcoming _Gordian Cosigner_ demonstrates how to easily manage Bitcoin transactions across an Airgap.

If you'd like to learn more about the libraries, specifications, and references being created by Blockchain Commons in coordination with our airgap wallet community, please visit our [discussion forums](https://github.com/BlockchainCommons/Airgapped-Wallet-Community/discussions) and our [research repo](https://github.com/BlockchainCommons/Research/blob/master/README.md). You can also support our work [as a patron](https://github.com/sponsors/BlockchainCommons).
