---
description: 🚀 CodeThreat SCA Released 🚀
cover: .gitbook/assets/1675159985994.jpg
coverY: 0
layout:
  cover:
    visible: true
    size: full
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# v2401 SCA Release

{% hint style="success" %}
As we launch the first update of 2024 with v2401, \
\
We want to share a core belief that shapes our approach to SAST solutions: We don’t just see SAST as a tool for security teams or just for developers; we see it as a crucial element for understanding and communicating the entirety of your project across different departments and auditors. \
\
Our goal is to provide a comprehensive software bill of materials (SBOM) report that is clear and accessible to everyone involved. This update is a significant step towards that goal, offering enhanced capabilities that bring more transparency and clarity to your project's components. We're committed to making sure that our solutions not only strengthen your security posture but also enhance overall project comprehension for all stakeholders
{% endhint %}

## 🌟 **Latest Update:** v2401

### 🔍  **SCA - Software Composition Analysis**

CodeThreat SCA designed to give teams an in-depth understanding of their project's dependencies. Our new information panel provides a transparent overview of open-source components, their licenses, and associated vulnerabilities, directly within your workflow\


<figure><img src=".gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* **Identify Issues Quickly:** Understand the specific vulnerabilities of third-party components in your code.
* **Actionable Solutions:** Receive clear guidance on resolving identified issues and keeping your dependencies secure.
* **SAST Issue Correlation:** See how SAST findings are related to third-party components, providing a holistic view of your project's security.

**Intelligent Fix Recommendations:** Our tool goes beyond the surface, providing the most effective version upgrades for a fix — not just the latest, but the best fit for your project.

### 🔍  License Tracking&#x20;

We're introducing license tracking feature within our SCA toolkit. This feature is designed to help developers:

* **Stay Compliant:** Monitor and manage the licenses of your third-party components to ensure your project adheres to legal and compliance standards.
* **Gain Visibility:** Receive a clear breakdown of the licenses associated with each component in your project, so you can make informed decisions.

{% hint style="warning" %}
The license tracking feature is currently experimental. As we continue to refine our platform, you can expect more comprehensive updates to this feature in future releases.
{% endhint %}

<figure><img src=".gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

### 🔍  Dependency Graph

* **Clear Visualization:** A comprehensive graphical representation of how each component in your project connects, making complex structures understandable at a glance.
* **In-Depth Analysis:** Drill down into the details of each dependency to assess its role and the implications it has on your project's health and security.
* **Efficient Troubleshooting:** Quickly identify and resolve issues within your project’s framework, streamlining your development process.

{% hint style="warning" %}
The dependency graph feature is currently experimental. We are actively working to refine its capabilities, aiming to enhance visualization and utility in the forthcoming updates
{% endhint %}

<figure><img src=".gitbook/assets/image (4) (1) (1).png" alt=""><figcaption></figcaption></figure>

## 🚀 Platform Updates

Our latest v2401.01 update brings a significant improvement to the way teams collaborate on our platform. Here’s what’s new for organization and team management.

**Invitation Link Generation and Direct Invite:** Team leads can now generate organization invitation links through our platform. &#x20;

**New Default Policies for Enhanced Scanning Options**

* **SCA-Only Scan Policy:** This policy focuses exclusively on SCA. It's ideal for teams primarily concerned with the security and compliance of open-source components in their projects. This policy scans for vulnerabilities in third-party libraries and checks for license compliance.
* **SAST-Only Scan Policy:** Tailored for those who want to concentrate on SAST, this policy scans your codebase for potential security issues without the additional layer of SCA. It's perfect for in-depth analysis of proprietary code and identifying security weaknesses.
* **Decompilation for Binary Artifacts:** Recognizing the importance of analyzing compiled files, we now offer a policy specifically for the decompilation of binary artifacts like DLLs and JARs. This allows for a thorough security analysis of compiled code, providing insights into potential vulnerabilities within these files.

## 🚀 SAST Analyzer Updates

**84 New C# and Java Rules:** We've significantly expanded our SAST rule set with **84** new rules for C# and Java.

<figure><img src=".gitbook/assets/image (13) (1).png" alt=""><figcaption><p>No one likes conflicts...right? </p></figcaption></figure>

## 🐛 **Bug Fixes and Stability Updates**

* **Login Issues Resolved:** We've fixed the login complications that arose with various integration options. Now, users can smoothly join a single organization after accepting an invitation, ensuring a seamless integration process regardless of the platform used.



**Looking Ahead**

> _As we progress through 2024, we want to share an important update about our roadmap: we may be adjusting our update cycle slightly. This change is in response to our growing focus on enhancing the quality aspects of our product. Our team is expanding, with more expertise and resources dedicated to ensuring that each feature and update meets the highest standards of excellence_

\


