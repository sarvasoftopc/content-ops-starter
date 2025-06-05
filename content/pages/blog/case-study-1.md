---
title: Enabling EMV Contactless Payments on Android POS for EU Market
slug: case-study-1
date: '2025-05-25'
excerpt: >-
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ante lorem,
  tincidunt ac leo efficitur, feugiat tempor odio. Curabitur at auctor sapien.
  Etiam at cursus enim. Suspendisse sed augue tortor. Nunc eu magna vitae lorem
  pellentesque fermentum. Sed in facilisis dui.
featuredImage:
  url: /images/9564770.jpg
  altText: Case study 1
  styles:
    self:
      borderRadius: large
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
isFeatured: false
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
### 🏢 Background

A European payment solutions provider (under NDA) approached me to develop a **NEXO-compliant, EMV-certified Point of Sale (POS) application** from the ground up. The client specializes in Android-based payment terminals and needed a **fast, reliable**, and **fully certifiable POS app** for the European market that adhered to **NEXO Fast specifications** and passed **CFCF.eu certification**.

Their goal was to deploy the solution across thousands of Newland and Sunmi Android terminals used by merchants in retail and hospitality environments.


### ❗ The Challenge

Building a POS app for the European market that adheres to **NEXO 4 and 5 protocols** is no small feat. The system had to:

*   Support **contactless EMV transactions**, including secure kernel communication.

*   Comply with **NEXO Fast Application Layer Protocol**, which demands rigid adherence to ISO 20022 messaging.

*   Pass **certification through CFCF.eu**, requiring strict protocol and functional conformity.

*   Be efficient and modular enough to run on low-power Android POS terminals.

*   Be delivered by a single developer within tight deadlines.

Most providers solve this with a large team — but the client wanted an **efficient, expert-led solution** without compromising quality or certification requirements.

### 👨‍💻 My Role

As the **sole engineer and architect** from my OPC company, I led the entire lifecycle:

*   **System Architecture**: Designed a modular and testable Android POS framework.

*   **Protocol Implementation**: Implemented the full NEXO Fast stack and EMV Level 2 kernel interface.

*   **Secure Integration**: Handled transaction flows, card communication, and response parsing.

*   **Debugging & Certification Prep**: Simulated test cases, resolved certification issues, and worked closely with the lab for CFCF approval.

*   **Deployment Support**: Optimized the APK for Sunmi and Newland hardware and delivered production-ready builds.

### 💡 The Solution

I developed a **fully compliant Android POS app** using Kotlin that:

*   Seamlessly integrates with **EMV Level 2 kernels** for contact and contactless transactions.

*   Implements **NEXO Fast v4/v5 protocol stack**, handling messaging, status words, and session control.

*   Offers a dynamic merchant interface for transaction display and receipt printing.

*   Supports fallback and retry mechanisms for real-world payment conditions.

*   Includes secure configuration loading and transaction logging as per NEXO mandates.

This solution was tailored for **Sunmi and Newland terminals**, ensuring compatibility with their printer modules, NFC readers, and secure elements.

### ✅ The Outcome

*   **Successfully certified** under **CFCF.eu**, passing all protocol, functional, and security test cases.

*   Deployed across **10,000+ terminals** in production within the EU.

*   Reduced client’s go-to-market time by **over 6 months** compared to outsourcing to a large team.

*   Delivered an app that is **modular**, **future-proof**, and **easily maintainable**.



### 🔧 Tech Stack

*   **Language**: Kotlin, Java

*   **Platform**: Android (Sunmi, Newland)

*   **Protocols**: EMV Level 2 Kernel, NEXO Fast v4/v5, ISO 20022

*   **Tools**: Android Studio, CFCF Certification Suite, Terminal Simulators

*   **Other**: SQLite, Secure Print Modules, Logcat Analysis Tools



### 🎯 Why It Matters

This case demonstrates that **a single-expert company** can deliver highly regulated, complex fintech software with agility, quality, and certification readiness. By deeply understanding both the **protocols** and the **business landscape**, I was able to offer a **faster and more cost-effective solution** than larger development houses.

