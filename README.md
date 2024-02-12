---
description: >-
  Introducing SARIF reporting, AI integration for on-premises, and new analyzers
  for PHP and Swift languages
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

# v2402 GenAI, Sarif and New Language Supports

{% hint style="info" %}
&#x20; In this update, we primarily focused on enhancing CodeThreat's integration with various CI/CD environments' security features through the implementation of SARIF output.&#x20;

&#x20; Additionally, by enabling the use of AI-generated outputs in on-premises environments, we aim to simplify the resolution of outputs produced by CodeThreat, facilitating a more comprehensive analysis of a repository's security across all layers.&#x20;

&#x20; Furthermore, we'd like to express our gratitude for the interest shown in our cloud environment. The feedback received from our user base, which was achieved without any promotions, has been overwhelmingly positive.
{% endhint %}

## 🌟 **Latest Update:** v2402

### **🌐 Custom LLM Integration for AI-Driven Vulnerability Fix**

* Users can now integrate Large Language Models (LLMs) from Azure OpenAI, OpenAI, Anthropic, and Ollama into their development environments.
* Supports selecting the preferred LLM provider, tailored to project needs and workflows.
* For on-premises requirements, Ollama provides a fully compatible AI capability, ensuring comprehensive support without external dependencies.

<figure><img src=".gitbook/assets/image (38).png" alt=""><figcaption><p>You can also develop custom models and integrate them into CodeThreat for more accurate outcomes!</p></figcaption></figure>

{% hint style="info" %}
&#x20; We've observed a recurring challenge where vulnerability resolution recommendations can take upwards of 4-5 hours, often leading to bottlenecks that slow down the entire process. \
\
&#x20; However, the integration of AI has shown promising results in accelerating these processes. Specifically, when GenAI is tailored to provide recommendations directly relevant to the code in question, we've seen resolutions that could be achieved in as little as 5-10 minutes.



&#x20; Another trend we've noted is the manner in which organizations attempt to manage various tools, which, in attempting to streamline operations, can inadvertently lead to more problems, thus reducing AppSec accessibility over time.

\
&#x20; Our goal is to enhance the accessibility and efficiency of AppSec processes, ensuring that security measures are not just thorough but also seamlessly integrated and expedient, leveraging AI to bridge the gap between complex security requirements and practical, timely solutions.
{% endhint %}

### 🔍  **SARIF Format**

* SARIF (Static Analysis Results Interchange Format) output reports are now available, facilitating integration with services like GitHub Vulnerability Alerts.
* Users can include SARIF output in their action YAML, enabling automated vulnerability reporting within GitHub’s development cycles.
* The feature also supports tools like Microsoft’s sarif-tools CLI for custom logic implementation in CI/CD pipelines and services.
* Sarif Report Generation is available in Project's Overview, Report Section!



Add CodeQL's Upload Sarif Job in your workflow action yaml to use **Github Vulnerability Alerts**

```yaml
on:
  pull_request:
      branches:
        - main
  push: 
        branches:
        - main
jobs:
  codethreat_scanner:
    runs-on: ubuntu-latest
    name: Codethreat Github Actions
    steps:
      - name: Check Out Source Code
        uses: actions/checkout@v3
      - name: Install Node.js
        uses: actions/setup-node@v1
      - name: CodeThreat Scanner
        uses: CodeThreat/codethreat-scan-action@master
        env:
           ACCESS_TOKEN: ${{ secrets.ACCESS_TOKEN }}
           GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
           CT_SERVER: ${{ secrets.CT_SERVER }}
           USERNAME: ${{ secrets.USERNAME }}
           PASSWORD: ${{ secrets.PASSWORD }}
           ORGNAME: ${{ secrets.ORGNAME }}
        with: 
            FAILED_ARGS: |
                 - max_number_of_critical: 4
                 - max_number_of_high: 20
                 - weakness_is: ".*injection,buffer.over.read,mass.assigment"
                 - condition: 'OR'
                 - automerge: true
                 - sync_scan: true
      - name: Upload SARIF file
        uses: github/codeql-action/upload-sarif@v2
        with:
          sarif_file: codethreat.sarif.json
```

<figure><img src=".gitbook/assets/image (39).png" alt=""><figcaption><p>The Code Scanning Alerts feature in GitHub is beneficial for handling code issues if you utilize GitHub Services.</p></figcaption></figure>

### 🚀 New Language Supports <mark style="color:yellow;">(Beta)</mark>

#### Introducing PHP and Swift Analyzers

<figure><img src=".gitbook/assets/image (40).png" alt=""><figcaption><p>KStore serves as CodeThreat's hub of knowledge, where users can explore the capabilities of the analyzer in its latest version.</p></figcaption></figure>

* We have introduced analyzers for PHP and Swift, currently in beta testing.
* PHP support includes 25 new specialized rulesets for frameworks such as Laravel, Symfony, and WordPress, accessible within the KStore.
* Swift support includes 10 new specialized rulesets for Weak Crypto-Keychain, Sql Query injection type vulnerabilities. The full list of current ruleset can be seen in KStore within the codethreat platform.

{% hint style="warning" %}
We plan to provide additional rulesets and support for new frameworks in future releases, and we welcome user feedback on these beta analyzers to guide their development and refinement.
{% endhint %}



## 🐛 **Stability Updates**

* Addressed issues related to hardcoded information searches. It is recommended for users with on-premises deployments to update their knowledge bases to benefit from these fixes.

\


