---
title: "\U0001F510 EMV XDA & ODE Signature Ecosystem for JavaCard Smartcards"
slug: case-study-2
date: '2022-02-16'
excerpt: >-
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ante lorem,
  tincidunt ac leo efficitur, feugiat tempor odio. Curabitur at auctor sapien.
  Etiam at cursus enim. Suspendisse sed augue tortor. Nunc eu magna vitae lorem
  pellentesque fermentum. Sed in facilisis dui.
featuredImage:
  url: '/images/ChatGPT Image Jun 5, 2025 at 06_29_24 PM.png'
  altText: Case study 2
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
#### 🏢 **Background**

A global payment network operator (under NDA) needed to implement **EMV Book 2-compliant XDA (Static Data Authentication)** and **ODE (Offline Dynamic Signature)** mechanisms on JavaCard-based smartcards that lacked native ECC (Elliptic Curve Cryptography) support.

The solution had to support **secure offline authentication** using ECC-based digital signatures during EMV transactions, without depending on vendor-provided cryptographic APIs — ensuring maximum portability and control.

The implementation was aimed at enabling offline-capable smartcard products for regions with low connectivity and needed to pass stringent certification tests by an external lab before deployment.



#### ❗ **The Challenge**

Implementing EMV-compliant ECC on JavaCard with no built-in ECC libraries required overcoming multiple limitations:

*   ✅ Perform ECC-based signature generation and verification with **only basic JavaCard operations** (no BigInteger, no ECC primitives).

*   ✅ Fit all cryptographic operations into **severely constrained RAM and EEPROM** environments.

*   ✅ Achieve deterministic, certifiable behavior for **XDA and ODE** as required by EMV Book 2.

*   ✅ Support **lab-level testing and certification**, requiring exact signature reproducibility and EMV test case coverage.

*   ✅ Extend the ecosystem to work with the client’s existing test tools and deployment processes.

Most providers use native ECC libraries or move critical logic off-card — we delivered **100% on-card ECC**, from scratch.



#### 👨‍💻 **My Role**

As the sole architect and JavaCard developer, I:

*   🔬 **Engineered cryptographic primitives**: Created modular math functions (multiplication, subtraction, modular inverse, XOR, scalar multiplication) to simulate ECC point operations in JavaCard.

*   💻 **Developed a custom applet**: Built a secure, certifiable JavaCard applet supporting EMV XDA (static signature) and ODE (dynamic challenge-based signature).

*   🧪 **Upgraded test tooling**: Extended the client’s APDU test tool to auto-generate signature test vectors and verify correctness across different card batches.

*   🧰 **Optimized low-level logic**: Reduced memory footprint, improved speed, and avoided GC stalls and memory leaks in the absence of heap monitoring.

*   🏁 **Supported certification**: Collaborated with the lab to provide deterministic output and resolved test case issues that blocked certification.



#### 💡 **The Solution**

The final deliverable was a **portable and certifiable ECC signature engine** embedded within a JavaCard applet:

*   ✅ Fully compliant with EMV Book 2 XDA & ODE signature schemes.

*   ✅ Custom ECC signature generation using on-card arithmetic operations.

*   ✅ Offline dynamic response signing using internal card challenge logic.

*   ✅ Lab-testable with fixed seed values for predictable output.

*   ✅ Easily portable across JavaCard 3.x platforms, independent of vendor APIs.

The project also included a **simulator testing framework** for signing/verifying APDUs, and a **cryptographic math module** for use in future applets.



#### ✅ **The Outcome**

*   🏅 **Lab-certified** ECC signature ecosystem approved for EMV XDA and ODE.

*   🚀 Enabled deployment of offline-capable EMV JavaCards in low-connectivity regions.

*   🧩 Became the client's **reference cryptographic library** for internal JavaCard development.

*   🔒 Delivered a **vendor-agnostic** and **fully self-contained** JavaCard crypto stack.



#### 🔧 **Tech Stack**

*   **Platform:** JavaCard 3.x, GlobalPlatform 2.2.1

*   **Cryptography:** EMV Book 2, Custom ECC (no native support), Modular Math APIs

*   **Languages:** JavaCard (CAP files), APDU scripting

*   **Tools:** JCIDE, APDU Debuggers, Certification Lab Suite

*   **Other:** Lab certification support, simulator tool integration, deterministic testing framework

