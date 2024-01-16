# Scan Policy

The Policy Management page offers users the flexibility to customize and manage scan policies for CodeThreat. This ensures that your scans are tailored to specific requirements, allowing for a more focused and efficient assessment.

1. **Scan Policies:**
   * **Description:** Scan policies define the parameters and settings for the CodeThreat scans.
   * **Usage:** You can tweak various settings, such as scan speed, targeted weaknesses, and compliance standards.
2. **Select Default Policy:**
   * **Description:** This dropdown menu allows you to set a default scanning policy.
   * **Usage:** Click on the dropdown and select from the available policies. The chosen policy will be used as the default for subsequent scans unless changed.
3.  **Generate New Scan Policy:**

    * **Description:** This feature allows you to create new, custom scan policies.
    * **Usage:**
      * **Policy Name**: Enter a unique name for your custom policy. This helps in differentiating between multiple policies.
      * **Description**: Provide a brief description of the policy. This can include its purpose, key settings, or any other relevant details.



Default Policies

**OWASP Top 10 Focus**: A scan tailored towards the most critical web application security risks as recognized by OWASP.

**Advanced Security**: Scans that look into deeper security issues that might not be part of the standard OWASP list.

**API Security**: Focuses on vulnerabilities specific to web APIs. This would look into areas such as JWT, CORS, and HTTP specific issues.

**Code Quality & Best Practices**: Scans that are not just about security but about the general quality and best practices in code.

**Data & Privacy Protection**: Concerned with data leaks, privacy violations, and database-related vulnerabilities.

**Mobile Security**: Focuses on vulnerabilities specific to mobile applications, including Android specific issues, geolocation, and SMS related vulnerabilities.

**Cryptography & Authentication**: Scans centered around issues related to encryption, hashing, signatures, and general authentication and session management flaws.

**File & Resource Management**: Concerned with issues like file uploads, directory traversal, and resource injection.

**Web Client-Side Security**: This would include vulnerabilities like XSS, HTML issues, and anything client-side related.

**Sensitive Information Exposure:** Scans focused on uncovering hardcoded credentials, tokens, and secrets. This includes checking configuration files, code repositories, and anywhere sensitive data might inadvertently be hardcoded or exposed.

#### **Creating a New Scan Policy:**

1. Navigate to the 'Policy Name' field and enter a name for your new policy.
2. In the 'Description' field, provide a brief summary of what this policy entails.
3. Adjust the specific scan settings as per your requirements.
4. Once satisfied with your settings, click 'Save' to store this policy. It will now be available in the "Select Default Policy" dropdown.

#### **Best Practices:**

* Regularly review and update your policies to ensure they align with evolving security requirements.
* When creating a new policy, ensure that its name and description are clear, so team members can easily understand its purpose.
* While the flexibility to customize is available, always ensure that the policy adheres to industry standards and best practices to maintain the security integrity of your scans.
