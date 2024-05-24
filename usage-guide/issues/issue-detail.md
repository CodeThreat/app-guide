# Issue Detail

On the Issue Detail Page, vulnerabilities that have been detected are listed. This interactive interface allows you to deeply inspect each vulnerability, view the associated code block, trace the vulnerability steps, and manage its status.

<figure><img src="../../.gitbook/assets/image (3) (1).png" alt="" width="375"><figcaption></figcaption></figure>

On the left-hand side:

* **Detected vulnerabilities** are categorized and listed.
* Each category might represent a programming language or platform like **`Javascript`**, **`Csharp`**, etc.
* Click on any vulnerability to get more insights.

<figure><img src="../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

Upon selecting a vulnerability:

* The center panel displays the **code block** associated with the detected vulnerability.
* Here, you can review the code that is potentially vulnerable.

On the right side:

* The **Issue Trace** section displays the trace of the vulnerability, showing steps from the sink to the source.
* By clicking on any of the steps (e.g., Invocation, Variable), the corresponding part of the code block will be highlighted, offering a clearer understanding of the vulnerability's flow within the code.

<figure><img src="../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>



* **Description**: Represents vulnerabilities that have moderate impact and/or exploitability. While they aren't immediate threats, they can serve as entry points for more sophisticated attacks.
* **Action**: Prioritize and rectify based on the available resources and the overall security posture of your system.

#### **4. Low**

* **Description**: These are minor threats, often with limited impact and harder exploitability. However, in certain scenarios, especially when combined with other vulnerabilities, they might still pose risks.
* **Action**: Address when feasible. While they might not require immediate attention, it's still advisable to fix them to maintain a robust security posture.
*

Next to the severity dropdown:

* Use the status button to assign a current status to the vulnerability.
* Available statuses are **`Hidden`**, **`Open`**, **`Closed`**, **`Accepted`**, **`ReCheck`**, and **`FalsePositive`**.

For actions on multiple vulnerabilities:

* Use the checkboxes on the left side of the vulnerabilities list to select multiple entries.
* Once selected, you can perform bulk operations, such as changing the status for all selected vulnerabilities.

### **Status Options**

#### **1. Hidden**

* **Description**: This status means the vulnerability is currently hidden from the main view, possibly because it's deemed as non-essential or is being reviewed separately.

#### **2. Open**

* **Description**: The vulnerability is currently active, unaddressed, and requires attention.

#### **3. Closed**

* **Description**: This indicates that the vulnerability has been addressed and resolved.

#### **4. Accepted**

* **Description**: This status signifies that the vulnerability is acknowledged but might not be fixed immediately due to certain reasons, such as it being an intended feature or having mitigating controls in place.

#### **5. ReCheck**

* **Description**: This status is for vulnerabilities that need to be revisited and re-evaluated. Maybe due to some changes in the code or environment or a new patch has been applied, and its effectiveness needs to be checked.

#### **6. FalsePositive**

* **Description**: Upon review, it's determined that the detected vulnerability is a false alarm and doesn't pose any real threat.

#### **Description**

The "Description" section provides a comprehensive explanation of the identified vulnerability, along with relevant code snippets. It aims to give the user a clear understanding of the nature and potential impact of the issue at hand. By offering contextual examples, this section educates the user on the specific problem areas within the code that can be exploited.

<figure><img src="../../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

#### **Mitigation**

The "Mitigation" segment suggests remedies and preventive measures for the identified vulnerabilities. It presents both a description of the solution and sample code that rectifies the problem. This is essential for developers, allowing them to quickly address the issue and ensure the security of their software. It's a go-to guide for patching the vulnerabilities.

<figure><img src="../../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

#### **Audit**

In the "Audit" section, users have the capability to assign the vulnerability to specific individuals or teams for further review or action. Additionally, if a connection to Jira has been established in the settings page, there's an option to automatically create a task in Jira regarding the vulnerability. This integration ensures seamless workflow and prompt attention to critical issues.

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

#### **History**

The "History" tab retains a chronological record of actions and status changes related to the vulnerability. Users can track when the vulnerability was first detected, when it was addressed, and any other relevant status updates. This provides transparency and can be instrumental in audits and reviews, helping teams understand the lifecycle of an issue.

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

#### **Details**

The "Details" section displays more granular information about the vulnerability, including:

* **Fix Cost**: An estimate of the effort or resources required to address the vulnerability.
* **Trust Level**: Indicates the confidence in the vulnerability detection, possibly based on the method used for identification.
* **Impacts**: Describes the potential consequences if the vulnerability were to be exploited.
* **Root Causes**: Highlights the fundamental reasons or code practices leading to the vulnerability.
* **Standards**: References to coding or security standards that the vulnerability may be violating.

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>



AI Assistant

The AI Assistant is an innovative feature within the "codethreat / Issues" interface that leverages advanced machine learning algorithms to provide insights, recommendations, and scenarios related to detected vulnerabilities. By tapping the "AI Assistant" button, users can get an in-depth understanding of the vulnerability, potential remediation strategies, a summarized flow of the issue, and possible attack scenarios.

**Remediation Suggestions**:

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

* The AI Assistant generates and provides specific recommendations on how to address the detected vulnerability.
* This is particularly useful for developers who might not be well-versed in security practices, giving them a straightforward guide to patch the vulnerability.
* The suggestions also come with sample code or configuration adjustments, making the remediation process smoother.

**Issue Flow Summarization**:

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

* Provides a concise overview of the vulnerability, simplifying the technical details into an easy-to-understand summary.
* This is beneficial for both technical and non-technical stakeholders, allowing them to quickly grasp the nature and severity of the issue without diving deep into the code.

**Possible Attack Scenarios**:

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

* The AI Assistant outlines potential exploitation scenarios, helping the user understand the real-world implications of the vulnerability.
* This provides context on why the vulnerability is critical and what could happen if it's left unaddressed.
* By visualizing potential threats, teams can prioritize which vulnerabilities need immediate attention.
