---
type: PostLayout
title: "\U0001F4F2 Android NFC APDU Toolkit for ISO 7816 Command Testing"
date: '2021-11-18'
excerpt: >-
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ante lorem,
  tincidunt ac leo efficitur, feugiat tempor odio. Curabitur at auctor sapien.
  Etiam at cursus enim. Suspendisse sed augue tortor. Nunc eu magna vitae lorem
  pellentesque fermentum. Sed in facilisis dui.
featuredImage:
  type: ImageBlock
  url: /images/img-placeholder.svg
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
slug: case-study-4
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
> A mobile security company (under NDA) needed a **developer-friendly Android app** to simulate and test **ISO 7816 APDU command-response flows** with smartcards, JavaCards, and secure elements via NFC.
>
> The client wanted a customizable Android toolkit to send low-level commands to NFC-enabled cards and analyze responses, aimed at their QA teams, card applet developers, and integration partners. The tool had to support scripting, hex-level editing, and structured logs to aid in debugging cryptographic and protocol issues.
>
> Their internal teams were spending excessive time debugging contactless issues manually using physical test benches — this app was meant to **bring all testing to an Android phone**.
>
>
>
> #### ❗ **The Challenge**
>
> Building a low-level testing tool for NFC cards meant addressing:
>
> *   ⚙️ Full ISO 7816-4 APDU support with CLA/INS/P1/P2/P3 formatting and dynamic payload editing.
>
> *   📲 Reliable NFC communication across fragmented Android devices and versions.
>
> *   💬 Real-time command sending and response parsing, including status word (SW1/SW2) decoding.
>
> *   📜 User-defined command scripts with conditional flows and result logging.
>
> *   🔐 Optional secure transmission for testing encrypted payloads and authentication flows.
>
> Most NFC apps are tailored for consumers (e.g., transit, tap-to-pay). This needed to be a **developer-grade utility** with full control over the protocol layer — something rarely available on Android.
>
>
>
> #### 👨‍💻 **My Role**
>
> As the sole developer, I was responsible for:
>
> *   🔧 Designing the command editor UI for composing, saving, and replaying APDU scripts.
>
> *   📲 Implementing the ISO 7816 protocol stack over Android’s NFC APIs (IsoDep).
>
> *   🔍 Adding smart parsing of status words, response data, and hex dumps.
>
> *   📚 Enabling script loading from JSON/text files for repeatable test cases.
>
> *   📤 Providing options to export logs and APDU traces for external validation.
>
> I also built internal testing capabilities for stress testing command sequences and measuring card response times.
>
>
>
> #### 💡 **The Solution**
>
> I delivered a fully functional **Android NFC APDU Toolkit** app that:
>
> *   ✍️ Allows real-time APDU command editing with hex validation and templates.
>
> *   🔁 Supports multi-command script execution with delays, conditions, and comments.
>
> *   📟 Displays parsed response data with live decoding of standard TLVs and SW codes.
>
> *   🧪 Enables QA and developers to validate card applets without specialized equipment.
>
> *   📂 Supports script import/export and session log archiving for audit and sharing.
>
> *   📱 Compatible with most Android devices having NFC (Android 7+).
>
>
>
> #### ✅ **The Outcome**
>
> *   🚀 Rolled out across the client's internal and partner QA teams with **over 1,000 daily test runs**.
>
> *   🛠️ Cut down card applet debugging time by 60% during certification and OTA integration phases.
>
> *   📲 Became a preferred tool for onboarding new card partners and verifying OTA personalization logic.
>
> *   🔄 Provided the foundation for future enhancements including secure channel testing and real card emulation.
>
>
>
> #### 🔧 **Tech Stack**
>
> *   **Platform:** Android (7.0+)
>
> *   **Languages:** Java, Kotlin
>
> *   **NFC API:** `android.nfc.tech.IsoDep`
>
> *   **UI:** Material Design (XML-based), ViewModels
>
> *   **Parsing:** TLV parser, Status Word decoder, Hex utils
>
> *   **Tools:** Android Studio, ADB Logcat, Postman (backend testing), JSON templates
>
> *   **Other:** ISO 7816-4, APDU Scripting Engine, File-based script loading

