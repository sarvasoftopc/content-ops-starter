---
type: PostLayout
title: "\U0001F4B3 JavaCard AEIPS and Expresspay Applet for C4/C8 Kernels"
date: '2021-11-18'
excerpt: >-
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ante lorem,
  tincidunt ac leo efficitur, feugiat tempor odio. Curabitur at auctor sapien.
  Etiam at cursus enim. Suspendisse sed augue tortor. Nunc eu magna vitae lorem
  pellentesque fermentum. Sed in facilisis dui.
featuredImage:
  type: ImageBlock
  url: /images/Credit Card Security Flat.jpg
  altText: Case study 3
  styles:
    self:
      borderRadius: x-large
bottomSections:
  - type: DividerSection
    title: Divider
    colors: bg-light-fg-dark
    styles:
      self:
        padding:
          - pt-7
          - pl-7
          - pb-7
          - pr-7
  - type: FeaturedItemsSection
    items:
      - type: FeaturedItem
        title: About Company
        tagline: This is the tagline
        subtitle: >-
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ante
          lorem, tincidunt ac leo efficitur, feugiat tempor odio. Curabitur at
          auctor sapien.
        image:
          type: ImageBlock
          url: /images/telus-logo.svg
          altText: Company logo
          styles:
            self:
              margin:
                - ml-3
        actions: []
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
    actions: []
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
slug: case-study-6
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
---
> #### 🏢 **Background**
>
> A **leading global payment network operator** (under NDA) engaged me to design and develop **JavaCard applets implementing AEIPS and Expresspay specifications**. These applets were to be deployed across C4 and C8 kernel platforms as part of the client's certified contactless payment product line.
>
> The client needed platform-optimized, EMV-compliant applets that would interoperate seamlessly across thousands of terminals globally. Given their plans to scale contactless payment issuance, these applets needed to be **secure, modular, and certification-ready**.
>
>
>
> #### ❗ **The Challenge**
>
> Delivering secure JavaCard applets for AEIPS and Expresspay with EMV compliance involved significant challenges:
>
> *   🧠 Understanding and translating AEIPS and Expresspay specs into **low-level JavaCard logic**, including transaction lifecycle, CVM processing, and cryptographic verification.
>
> *   🧩 Supporting **C4 and C8 kernel-specific flows**, each with its own command timing, APDU sequencing, and performance characteristics.
>
> *   🧪 Meeting rigorous **payment brand certification requirements**, including personalization scripting and cryptographic test vectors.
>
> *   ⚙️ Optimizing applet performance and memory usage for **production-grade smart cards** with limited RAM and EEPROM.
>
> These specifications are typically implemented by large vendor teams — but here, the client wanted an **independent JavaCard expert** to deliver both AEIPS and Expresspay in a lean, secure, and testable way.
>
>
>
> #### 👨‍💻 **My Role**
>
> As the dedicated JavaCard engineer, I led the entire technical effort:
>
> *   🧱 Designed separate but reusable JavaCard architectures for AEIPS and Expresspay flows.
>
> *   🔐 Implemented EMV-compliant commands including `SELECT`, `GET PROCESSING OPTIONS`, `READ RECORD`, `GENERATE AC`, and `GET DATA`.
>
> *   ⚙️ Integrated EMV cryptographic elements such as ARQC generation, issuer authentication, dynamic data signing, and key diversification.
>
> *   🧪 Provided exhaustive unit tests and personalization scripts tailored for C4 and C8 kernel simulators.
>
> *   📄 Delivered technical documentation for the client's internal validation and future maintenance teams.
>
> *   🤝 Coordinated with the client’s certification and security teams to meet internal and external validation standards.
>
>
>
> #### 💡 **The Solution**
>
> The final deliverables included **two modular and secure JavaCard applets** for AEIPS and Expresspay, each customized for their respective kernel platforms:
>
> *   🧩 AEIPS Applet:
>
>     *   Full EMV transaction state machine for **contactless Magstripe and EMV modes**.
>
>     *   Dynamic data authentication using EMV-CDA/SDDA with tag filtering.
>
>     *   Support for **terminal risk management** and outcome parameter set generation.
>
> *   💠 Expresspay Applet:
>
>     *   Built-in flow for contactless **qVSDC and MSD modes**, configurable via profile.
>
>     *   Kernel-specific behavior matching C4/C8 terminal requirements.
>
>     *   Selective CVM enforcement and proprietary data tag handling.
>
> *   🔐 Both applets supported:
>
>     *   Secure personalization via GlobalPlatform secure channel.
>
>     *   Offline and online cryptogram generation.
>
>     *   **Memory-efficient design** with optimized buffer reuse and APDU parsing logic.
>
>
>
> #### ✅ **The Outcome**
>
> *   🏁 **Certified and deployed** across the client’s global smartcard portfolio.
>
> *   🌍 Enabled **secure and interoperable contactless transactions** with millions of POS terminals worldwide.
>
> *   ⚙️ Strengthened the client's ability to deploy across **multiple kernel types**, reducing reliance on third-party vendors.
>
> *   ⏱️ **Accelerated time-to-market** for new card products by providing reusable codebase and compliance documentation.
>
>
>
> #### 🔧 **Tech Stack**
>
> *   **Platform:** JavaCard 3.x, GlobalPlatform 2.1.1+
>
> *   **Specs:** AEIPS, Expresspay, EMV 4.3+
>
> *   **Kernels:** C4, C8
>
> *   **Protocols:** ISO 7816-4, EMV Contactless Book C
>
> *   **Crypto:** Static/Dynamic Data Authentication, ARQC/TC/ARPC processing
>
> *   **Tools:** JCIDE, GP Tools, EMVCo-certified test tools, personalization script engines

