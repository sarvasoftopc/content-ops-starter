---
title: "\U0001F4F1 iOS Contactless SDK for Card Data Activation and Tokenisation"
slug: case-study-3
date: '2021-11-18'
excerpt: >-
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ante lorem,
  tincidunt ac leo efficitur, feugiat tempor odio. Curabitur at auctor sapien.
  Etiam at cursus enim. Suspendisse sed augue tortor. Nunc eu magna vitae lorem
  pellentesque fermentum. Sed in facilisis dui.
featuredImage:
  url: /images/img-placeholder.svg
  altText: Case study 3
  styles:
    self:
      borderRadius: x-large
  type: ImageBlock
bottomSections:
  - title: Divider
    colors: bg-light-fg-dark
    styles:
      self:
        padding:
          - pt-7
          - pl-7
          - pb-7
          - pr-7
    type: DividerSection
  - items:
      - title: About Company
        tagline: This is the tagline
        subtitle: >-
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ante
          lorem, tincidunt ac leo efficitur, feugiat tempor odio. Curabitur at
          auctor sapien.
        image:
          url: /images/telus-logo.svg
          altText: Company logo
          styles:
            self:
              margin:
                - ml-3
          type: ImageBlock
        colors: bg-light-fg-dark
        styles:
          self:
            padding:
              - pt-6
              - pl-6
              - pb-6
              - pr-6
            textAlign: left
            borderColor: border-neutralAlt
            borderStyle: none
            borderWidth: 0
            borderRadius: none
            flexDirection: row
        type: FeaturedItem
    variant: small-list
    colors: bg-light-fg-dark
    styles:
      self:
        margin:
          - mb-20
        padding:
          - pt-0
          - pl-0
          - pb-0
          - pr-0
        justifyContent: center
      subtitle:
        textAlign: center
    type: FeaturedItemsSection
isFeatured: true
colors: bg-light-fg-dark
styles:
  self:
    padding:
      - pt-5
      - pl-5
      - pb-5
      - pr-5
    textAlign: center
    borderColor: border-light
    borderStyle: none
    borderWidth: 0
    borderRadius: none
    flexDirection: col
type: PostLayout
---
> #### 🏢 **Background**
>
> A mobile security vendor (under NDA), specializing in contactless and token-based card provisioning, partnered with me to develop a **lightweight iOS SDK** to handle **contactless card activation, token lifecycle management, and APDU communication** using Apple devices with NFC capabilities.
>
> The SDK was intended to be integrated into a secure Mobile app that could **activate and** **provision virtual cards**, manage tokenised **credentials**, and initiate **contactless payments** via secure element or HCE-like environments on iOS.
>
> The client's primary market was in regions adopting mobile-first financial services, where **over-the-air activation and local secure personalization** of card data was a competitive necessity.
>
>
>
> #### ❗ **The Challenge**
>
> Creating an NFC and tokenization SDK on iOS came with platform-specific and business-critical hurdles:
>
> *   🚫 Apple’s iOS provides **limited and restrictive access to NFC**, especially for low-level ISO 7816 APDU communication.
>
> *   🔐 Card activation had to be **cryptographically secure**, including dynamic challenge-response authentication with back-end.
>
> *   🔄 The SDK had to manage **token lifecycle events** — activate, update, suspend, resume, delete — with secure persistence.
>
> *   🛡️ Ensuring **data protection** through encryption at rest, in transit, and during in-app operations.
>
> *   ⏱️ All this had to be built **under tight regulatory constraints**, while maintaining a minimal SDK footprint and seamless developer experience.
>
> Unlike Android, where HCE and JavaCard APIs are available, iOS required clever design using **Core NFC** and **background secure services**.
>
>
>
> #### 👨‍💻 **My Role**
>
> As the lead SDK developer and security engineer:
>
> *   🧱 **Architected the SDK** to expose clean interfaces for card provisioning, APDU exchange, and token updates.
>
> *   📲 **Integrated with Core NFC** to enable ISO 7816 APDU command exchange with compliant cards and terminals.
>
> *   🔐 **Implemented secure session management** with token request, storage, and invalidation via iOS Secure Enclave and Keychain.
>
> *   🌐 **Built support for OTA personalization**, handling secure certificate exchange and key derivation using ECC-based schemes.
>
> *   📦 **Wrapped everything** in a compact, developer-friendly SDK distributed via Swift Package Manager (SPM) and CocoaPods.
>
>
>
> #### 💡 **The Solution**
>
> The final product was a **Swift-based iOS SDK** that enabled:
>
> *   📲 **Secure card activation** via NFC by sending APDU command sequences to the card chip.
>
> *   🔄 Full **token lifecycle management**, with authenticated API calls to back-end systems.
>
> *   🔐 Support for **ECC-based mutual authentication** using certificates and challenge-response flow.
>
> *   📥 **Encrypted storage** of tokens using Apple Keychain with biometric protection options.
>
> *   🧩 Modular API interfaces for easy integration by fintech app developers.
>
> *   📘 Included full developer documentation, usage samples, and testing suite.
>
>
>
> #### ✅ **The Outcome**
>
> *   🔐 SDK successfully integrated into the client's fintech and wallet apps with **millions of downloads**.
>
> *   🌍 Enabled **secure mobile provisioning and contactless activation** in under 30 seconds.
>
> *   ✅ Compliant with PCI and payment scheme tokenization guidelines.
>
> *   🧰 Became the **foundation layer** for the client’s iOS payment suite used across digital banking and transit partners.
>
> *   🛠️ Reduced development and integration time for partners by 80% thanks to clean APIs and full documentation.
>
>
>
> #### 🔧 **Tech Stack**
>
> *   **Platform:** iOS 13+
>
> *   **Languages:** Swift, Objective-C (bridging)
>
> *   **NFC:** Core NFC (ISO 7816 APDU support)
>
> *   **Security:** ECC, Apple Keychain, Secure Enclave, HTTPS (TLS 1.3), JWT
>
> *   **Tools:** Xcode, Swift Package Manager, CocoaPods
>
> *   **Other:** ISO 7816, Tokenisation APIs, APDU scripting framework,

