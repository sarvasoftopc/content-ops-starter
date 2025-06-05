---
type: PostLayout
title: "\U0001F510 JavaCard HMAC-SHA Challenge-Response Applet for Secure Authentication"
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
slug: case-study-5
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
> A cybersecurity-focused startup (under NDA) building next-gen secure elements needed a **JavaCard applet** that performs **HMAC-SHA1-based challenge-response authentication**. This applet would be used in programmable smartcards and NFC tokens for applications such as **two-factor authentication (2FA), terminal pairing, and mobile identity**.
>
> Their goal was to build a lightweight, reliable applet that could be deployed across multiple JavaCard platforms and interfaced easily with host apps via ISO 7816 APDUs.
>
> The startup’s engineering team had limited experience in low-level cryptographic JavaCard development and needed a **plug-and-play solution with clear APDU specs, full source code, and test scripts**.
>
>
>
> #### ❗ **The Challenge**
>
> Implementing HMAC-SHA1 on JavaCard involved multiple constraints:
>
> *   🧮 No built-in `HMAC` implementation in standard JavaCard libraries — it had to be **manually constructed** using the `MessageDigest` and `Signature` APIs.
>
> *   🧠 Manual key padding and block operations as per [RFC 2104]().
>
> *   ⚠️ Strict memory and performance limits: 1–4 KB RAM, 24 KB ROM for most cards.
>
> *   🧪 The applet needed to be **easily testable** from external tools like JCIDE, GPShell, or Android apps using `IsoDep`.
>
> *   🔐 Secure key loading and session key slot management.
>
> Most teams solve this with off-card processing, but the requirement here was **on-card computation** with secure key storage — suitable for offline, tamper-resistant use.
>
>
>
> #### 👨‍💻 **My Role**
>
> As the JavaCard specialist, I handled:
>
> *   🧱 Designing the APDU interface to support `LOAD KEY`, `CHALLENGE`, and `GET RESPONSE` commands.
>
> *   🔐 Implementing HMAC-SHA1 using raw `MessageDigest` and buffer manipulation logic.
>
> *   🗂️ Supporting 2 slots (e.g., SLOT 1, SLOT 2) for storing static or derived secret keys.
>
> *   🧪 Creating test cases in JCIDE for simulation and unit testing.
>
> *   📤 Writing documentation and demo scripts for host integration (e.g., Android, Python, Java).
>
>
>
> #### 💡 **The Solution**
>
> The result was a **lightweight JavaCard applet** that:
>
> *   🔑 Supports secure 20-byte key loading per slot using a proprietary or ISO 7816 APDU.
>
> *   🎯 Accepts an 8–32 byte random challenge input and responds with a 20-byte HMAC-SHA1 signature.
>
> *   🧩 Uses manual inner/outer pad (ipad/opad) logic and processes blocks in compliance with HMAC specification.
>
> *   🔁 Includes command chaining support for long inputs and script-based interaction.
>
> *   📓 Provides clear `CLA/INS` APDUs:
>
>     *   `0x80 0x10` → Load Key
>
>     *   `0x80 0x20` → Send Challenge
>
>     *   `0x80 0x30` → Get Response
>
>
>
> #### ✅ **The Outcome**
>
> *   📦 Deployed into thousands of secure elements, with downstream apps using it for offline 2FA and token pairing.
>
> *   ⚙️ Enabled faster onboarding for the client’s Android toolkit, reducing integration time by 50%.
>
> *   ✅ Validated against known RFC test vectors using JCIDE and external tools.
>
> *   🔄 Made portable across **JC2.2.2–JC3.0.5** cards with minimal changes.
>
>
>
> #### 🔧 **Tech Stack**
>
> *   **Platform:** JavaCard 2.2.2+, GlobalPlatform
>
> *   **Language:** JavaCard (CAP, JAR)
>
> *   **Crypto APIs:** `MessageDigest.ALG_SHA`, `Util.arrayCopy`, `RandomData`, Manual HMAC
>
> *   **APDU Tools:** JCIDE, GPShell, pyAPDU, Android IsoDep
>
> *   **Test Vectors:** RFC 2202 / RFC 4231 (HMAC)
>
> *   **Build Tools:** JCIDE, Eclipse JCWDE Simulator
>
> *   **Host Integration:** Java, Android (IsoDep), Python with pyscard

