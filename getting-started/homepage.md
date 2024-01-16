# HomePage

This central hub offers a comprehensive view of the security posture across all your projects. At a glance, you can quickly assess the current number of unresolved security issues, the volume of codes scanned, and the number of projects under scrutiny. The dynamic Issue Trend graph provides insights into how security issues have evolved over time, letting you track the progress of resolutions. Additionally, the Risk Score offers a snapshot of the overall security health, and the Recent Scans list keeps you updated on the latest scanning activities. Dive into this dashboard to stay informed and proactive about your projects' security health.

#### **1. Open Security Issues**

This card displays the total number of unresolved security issues detected.

At a glance, users can understand the current state of security issues in the system.

#### **2. Total Scanned Codes**

Shows the volume of codes that have been scanned for potential vulnerabilities.

Helps in understanding the breadth of the scan. The larger the volume, the more comprehensive the scan.

#### **3. Total Projects**

Indicates the total number of projects which have undergone the security scan.

Provides a broader perspective on the number of projects monitored for security concerns.

#### **4. Total Scans**

Represents the number of times the system has conducted security scans.

An indicator of system activity, letting users know how frequently scans are being conducted.

#### **5. Risk Score**

A metric representing the overall security health of the system. It is typically graded from A (best) to F (worst).

Allows users to quickly gauge the overall security posture of the system.

The "Risk Score" is a composite metric that aims to quantify the potential security vulnerabilities and risks associated with a software application. Various factors, both structural and functional, contribute to this score. Here's a breakdown of the factors considered:

1. **Number of Sources:** This counts the points where data enters the system, possibly bringing in vulnerabilities if not sanitized correctly.
2. **Number of Sinks:** Points where data leaves the system or is used by the system. A higher number might indicate more potential points of failure.
3. **Number of Cryptographic Methods Used:** The more cryptographic methods in place, the more complex the security landscape becomes.
4. **Number of Try/Catch Blocks:** Excessive use can indicate potential error-handling vulnerabilities or areas of instability.
5. **Number of Executable Lines of Code:** Generally, more lines of code can introduce more potential points of vulnerability.
6. **Number of Lines for Logging:** Over-logging or under-logging can both be indicative of security concerns.
7. **Number of Session Add/Remove Statements:** Can be indicative of how user sessions are managed and potential misuse.
8. **Number of Access Control Methods/Libraries:** Indicates the complexity of access management in the software.
9. **Number of Third Party Libraries Used:** External libraries can introduce vulnerabilities if they're outdated or poorly maintained.
10. **Number of Source Code Files:** More files can mean more complexity and potential oversight in security checks.
11. **Number of Methods:** A higher count can indicate complexity and potential areas where vulnerabilities can hide.
12. **Number of Authentication API Calls:** Indicates the frequency and diversity of authentication attempts, which can be a significant area of concern.
13. **Number of Appsetting Params in Web.Config:** Parameters can sometimes store sensitive information and be a potential vulnerability.
14. **Number of Null Checks:** Indicates potential points where the system can fail or behave unpredictably.
15. **Number of Views (aspx, cshtml, etc):** More views might mean more points where data is rendered, possibly leading to vulnerabilities like XSS.
16. **Number of Financial & Privacy Related API Calls:** High sensitivity areas that, if compromised, can lead to significant breaches.

To determine the final "Risk Score," each of these factors is weighted based on its potential impact on security. The weighted scores are then combined, providing a holistic view of the application's security posture. It's vital to review and adjust the weights periodically based on evolving security standards and the application's unique context.

#### **6. Issue Trend Graph**

* **Description**: A graphical representation showing the trend of security issues over time. It differentiates between open and closed issues.
* **Usage**: Helps in tracking the progress of security issue resolution over time and can indicate if issues are increasing or decreasing.

#### **7. Recent Scans**

* **Description**: A list of the most recent scans, showcasing the project name and the status of the scan (e.g., "Scanning", "Successfully Finished", "In Queue").
* **Usage**: Provides users with a quick overview of the latest scanning activity. This can be especially useful to check the status of recent scans and to understand which projects have been recently evaluated.

***

**Note**: It's essential for users to regularly check the homepage to stay updated on the security posture of their projects. Regularly addressing open security issues and frequently scanning your codebase ensures a more secure environment.
