---
title: "Gordian QR Tool Supports Vaccine Records, 2FAs, Cryptoseeds, and More"
excerpt_separator: "<!--more-->"
categories:
  - Apps
tags:
  - QR Tool
  - Gordian Architecture
classes:
  - wide
image: https://raw.githubusercontent.com/BlockchainCommons/GordianQRTool-iOS/master/images/ca-digital-vaccine-record.png
---

The state of California recently [announced their Digital COVID-19 Vaccine Record system](https://cdt.ca.gov/news/california-launches-new-digital-tool-giving-residents-convenient-access-to-their-covid-19-vaccine-record/). It allows Californians to access a digital copy of their vaccine records, rather than having to depend entirely on their physical copy. The main entry point is a QR code containing a rudimentary Verifiable Claim (VC), which makes for great ease of use. However, Blockchain Commons has concerns over how the user experience (UX) design might negatively affect both privacy and security; we are working to address these with our new [Gordian QR Tool](https://apps.apple.com/us/app/gordian-qr-tool/id1506851070) for the iPhone, Blockchain Commons' first Apple appstore release.

<!--more-->

<img src="https://raw.githubusercontent.com/BlockchainCommons/GordianQRTool-iOS/master/images/ca-digital-vaccine-record.png" align="right" width=300>
For a while now, increasingly personal information has been getting encoded as QRs. During the pandemic, COVID tests were  often stored as QRs. There has also been extensive use of QR codes to transmit secure information across an airgap. Many people first saw this use of QRs when they read a QR code for a two-factor authentication seed into their phone's Authenticator app. At Blockchain Commons, we similarly use QR codes as an encoding method to transmit seeds and keys.

Some possible architectural issues arise from using QR codes for confidential data, such as the fact that you're actually transmitting the data (not a proof of the data), that the QRs tend to contain all of the data (not just a selection), and that there's no way to rescind a QR or expire it. Those issues will have to be dealt with at a foundational level as we figure out what can safely be encoded as a QR — and more importantly how to offer restricted proofs rather than complete information.

However, there are also security & privacy UX issues related to the storage of QR codes that need to be resolved no matter what is encoded. The state of California itself demonstrated the bad habits that we're already developing when they said in [their official press release](https://cdt.ca.gov/news/california-launches-new-digital-tool-giving-residents-convenient-access-to-their-covid-19-vaccine-record/): "individuals are encouraged to screenshot the information and save it to their phone files or camera roll".

Now, storing QRs as photos on a phone does meet some minimal security requirements. Most phones are closely held and protected by a PIN, a thumbprint, or a faceprint. They're often backed up to a cloud service and that cloud data is mostly secured as well. Still, there are numerous opportunities for problems.

That's in large part due to the fact that photos are built to be shared. It's very easy to send a photo to a friend or a social network, which is great for photos, but less so for your QR codes. In addition, photos are built to be synced. Though your data might be relatively safe if it's synced to the cloud, it's not that secure when synced to your desktop computer, which is vulnerable to malware and other attacks.

Photos also aren't built to be searched and their categorization systems are usually rudimentary. Even if your QR code was safe, you might not be able to easily find it.

<img src="https://raw.githubusercontent.com/BlockchainCommons/GordianQRTool-iOS/master/images/qr-list-2.jpeg" align="right" width=250>
That's where Blockchain Commons' [Gordian QR Tool](https://apps.apple.com/us/app/gordian-qr-tool/id1506851070) for the iPhone comes in. Though we can only make sure that our own uses of QR codes are architecturally secure, we can definitely provide better ways to store QR codes, and that's what QR Tool does.

QR Tool lets you scan any QR code into an encrypted vault. It then protects your code with two-factor authentication: you initilally log in with your Apple login and password, and then anytime you want to view your codes, you additionally must use a biometric authentication, such as a fingerprint. Unlike your semi-porous camera roll, QR Tool was built to keep confidential information secure.

QR Tool also provides proof that your codes weren't changed. Using [Lifehash](https://github.com/BlockchainCommons/LifeHash) technology, QR Tool links each code to a unique, evocative, and unchanging graphical color representation. This will prove particularly useful when the Lifehash specification is adopted by other companies, so that you can transfer a QR code between applications and verify immediately that it's the same — something that's difficult with the QR code alone.

Finally, QR Tool resolves the problem of categorization by automatically recognizing a wide variety of QR codes and giving you the opportunity to change those categorizations as you see fit.

If the future we hope to see more fully featured [Verifiable Credentials](https://www.w3.org/TR/vc-data-model/), but there's no doubt that QRs are with us for the moment, and we need to make sure that they remain secure and easy to use. This is why we released QR Tool. It's a reference implementation for the Gordian Principles, demonstrating how to store confidential data in a way that's independent, private, resilient, and open: QR Tool ensures that you hold your own QRs, that they're safe, and that you can easily transmit them to other services.

If you've got QRs of your own to secure, you can purchase QR Tool from the [Apple Store](https://apps.apple.com/us/app/gordian-qr-tool/id1506851070) or you can compile it directly from the source code found at the [QR Tool repo](https://github.com/BlockchainCommons/GordianQRTool-iOS) on GitHub.
