---
title: "Blockchain Commons Publishes 2026 Technology Overview"
excerpt_separator: "<!--more-->"
categories:
  - Videos
tags:
  - Video
classes:
  - wide
---


Over the last several years, Blockchain Commons has developed numerous technologies meant to improve the [independence, privacy, resilience, and openness](https://developer.blockchaincommons.com/principles/) of the internet, to allows users true self-sovereignty. The earliest technologies have been adopted by many third-parties, while many newer technologies are available for deployment now.

The brand-new [2026 Technology Overview](https://www.youtube.com/watch?v=f7MFW8RfcOE) from Blockchain Commons describes each of 24 different technologies, applications, and references in about a minute each, offering the most comprehensive and accessible look at Blockchain Commons technology to date.

{% include video id="f7MFW8RfcOE" provider="youtube" %}

Here's a quick look at the topics covered in the Overview:

## Data Encoding

_Our foundational methods for storing data in an interoperable format._

* **[dCBOR](https://developer.blockchaincommons.com/dcbor/).** An update to the CBOR data format that ensures that data is always encoded in the same way.
* **[Known Values](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2023-002-known-value.md).** Integers assigned to common concepts and recorded in a common registry.
* **[Uniform Resources (URs)](https://developer.blockchaincommons.com/ur/).** An encoding method for structuring binary data as plain text strings.
* **[Multipart URs (MURs)](https://github.com/BlockchainCommons/Research/blob/master/papers/bcr-2024-001-multipart-ur.md).** URs with large payloads split into fragments seen as Animated QR codes.

## Cryptographic Protections

_Technologies that protect, authenticate, and verify your data._

* **[FROST](https://developer.blockchaincommons.com/frost/).** A Schnorr-based threshold signing system.
* **[Provenance Marks](https://developer.blockchaincommons.com/provemark/).** A  forward commitment hash chain that is public verifiable, used to assess content authenticity.
* **[Sharded Secret Key Reconstruction (SSKR)](https://developer.blockchaincommons.com/sskr/).** A Shamir's Secret Sharing variant that includes two-level thresholds.

## Data Identification

_Aids that help humans to recognize complex binary and hex data._

* **[Bytewords](https://developer.blockchaincommons.com/bytewords/).** An encoding method that makes data human readable, also used by URs.
* **[LifeHash](https://developer.blockchaincommons.com/lifehash/).** A visual recognition system that  creates a unique visual icon for any data.
* **[Object Identity Blocks](https://developer.blockchaincommons.com/oib/).** An ID card for digital objects that improves recognition and reduces confusion.

## Gordian Envelope

_The core of our higher-level stack, used for safely storing and sharing data._

* **[Gordian Envelope](https://developer.blockchaincommons.com/envelope/).** A deterministic smart document system that supports elision, encryption, and permits.
* **[Gordian Sealed Transaction Protocol (GSTP)](https://developer.blockchaincommons.com/envelope/gstp/).** A transportation method for moving envelopes securely between parties.
* **[Encrypted State Continuations (ESC)](https://developer.blockchaincommons.com/envelope/esc/).** A method for storing client data as a black box in GSTP communications.

## Self Sovereign Identity

_Methods to control your own identity, built on Gordian Envelope._

* **[Extensible Identifier (XID)](https://developer.blockchaincommons.com/xid/).** A secure self-sovereign and self-certifying identifier.
* **[Gordian Clubs](https://developer.blockchaincommons.com/clubs/).** A self-contained cryptographic publication that you can distribute without infrastructure.

## Secure Data Transport

_Self-sovereignty can often be censored by the transport layer. These apps demo ways to avoid that._

* **[Garner](https://developer.blockchaincommons.com/garner/).** A Tor onion service that privately serves files using TorGaps.
* **[Hubert](https://developer.blockchaincommons.com/hubert/).** An automotable dead drop protocol that uses distributed storage networks for communication.

## Reference Apps

_All of our technologies are references. These apps show how many of them work._

* **[dCBOR-CLI](https://github.com/BlockchainCommons/bc-dcbor-cli).** An app for investigating dCBOR, including powerful dCBOR pattern expressions.
* **[envelope-CLI](https://github.com/BlockchainCommons/bc-envelope-cli-rust).** An app demonstrating extensive envelope and XID functionality.
* **[Seedtool-CLI](seedtool-cli-rust).** A command-line app that demonstrates data encoding and other low-level protocols.
* **[Gordian Seedtool](https://apps.apple.com/us/app/gordian-seed-tool/id1545088229).** An iOS seed vault that mirrors seedtool-CLI in a graphical environment.

## Information Repositories

_We want to help you learn about our technologies! Besides our [developer pages](https://developer.blockchaincommons.com/), the following resources also contain information._

* **[Gordian Dev Meetings](https://developer.blockchaincommons.com/meetings/).** Monthly or bimonthly meetings that discuss and demo technologies.
* **[Research Repo](https://github.com/BlockchainCommons/Research/blob/master/README.md).** The precise technical specifications for many of our technologies.
* **[YouTube](https://www.youtube.com/@blockchaincommons).** Videos of our meetings as well as other overviews and demos.

Besides our new [2026 Technology Overview](https://www.youtube.com/watch?v=f7MFW8RfcOE), you may also wish to watch our [2021 Technology Overview](https://www.youtube.com/watch?v=RYgOFSdUqWY), which contains more extensive discussions of our older (more widely adopted) technologies and also our two-part overview of Gordian Envelope.

<table width="100%">
  <tr>
    <td width="640px">
      <b>2021 Overview:</b>

      {% include video id="RYgOFSdUqWY" provider="youtube" %}
      
    </td>    
    <td width="640px">
      <b>Envelope Overview:</b>

      {% include video id="-vcLCFKQvik" provider="youtube" %}
      
    </td>    
    <td width="640px">
      <b>Envelope Extensions:</b>

      {% include video id="uFxStP3ATkw" provider="youtube" %}
      
    </td>    
  </tr>
</table>
