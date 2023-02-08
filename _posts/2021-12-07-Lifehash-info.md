---
title: "Blockchain Commons Launches LifeHash on the Web"
excerpt_separator: "<!--more-->"
categories:
  - Specifications
tags:
  - LifeHash
  - Airgap
  - Web Page
classes:
  - wide
image: http://www.blockchaincommons.com/images/lifehash-info.png
---

<a href="https://www.blockchaincommons.com/images/lifehash-info.png"><img src="https://www.blockchaincommons.com/images/lifehash-info.png" align="right" width=350></a>

Wolf McNally's [LifeHash](https://github.com/BlockchainCommons/bc-lifehash) is one of Blockchain Commons' interoperable specifications intended to make digital infrastructure open, interoperable, secure, and compassionate. A LifeHash takes a cryptographic objects such as a seed or a key (or really, any sort of data) and turns it into a beautiful and easily recognizable image. 

You can now play with LifeHashes at [LifeHash.info](http://lifehash.info/). This [C++ implementation compiled to WebAssembly](https://github.com/BlockchainCommons/lifehash-web/) allows you to enter an arbitrary text string or a SHA-256 digest and view the corresponding LifeHash — using one of a few different LifeHash variants. (We recommend v2 as the "official" LifeHash.) Because it's compiled into Webassembly, LifeHash.info does all the work in your browser, ensuring your secrets stay safe!

<!--more-->

A similar idea called [Blockies](https://www.npmjs.com/package/ethereum-blockies) already exists to identify Ethereum addresses. They're a great addition to the Ethereum ecosystem, but LifeHashes incorporate a few additional features. Because each one is built from an iteration of [Conway's Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life), they're more detailed. They also have been carefully formatted to display well on grayscale screens and low-resolution screens, with our [LetheKit offering a proof of concept](https://www.blockchaincommons.com/quarterlies/Q1-2021-Report/).

So why use LifeHashes? They ensure that any time that you see a key or seed in a different environment, you'll be able to recognize it through the visual hash (and now you can use [LifeHash.info](http://lifehash.info/) to display the LifeHash derived from the SHA-256 hash of an object, even if your app doesn't support LifeHashes). As an adjunct to existing computer and human examinations of digital hashes, LifeHashes can improve your security.
 
LifeHashes are particularly important for Blockchain Commons given our focus on resilient and independent airgapped architectures: a LifeHash allows for the easy comparison of a cryptographic object on either side of the gap, so that you know that you received what you were expecting. Transferred a seed? Asked to sign a PSBT for a specific account? LifeHashes can help you avoid costly errors.

Our explainer video talks more about LifeHash and demonstrates how it works:

<center>
<iframe width="560" height="315" src="https://www.youtube.com/embed/cu0K__KLxKo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>

Blockchain Commons is dedicated to improving the human aspects of the digital world; LifeHash does that by considering the human experience of cryptographic hashes and providing visual cues to replace (or at least supplement) the long strings of letters and numbers that we _can't_ easily differentiate.

If you'd like to support work of this sort to create a more human internet, please become a [Github Sponsor](https://github.com/sponsors/BlockchainCommons).
