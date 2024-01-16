# Github

The "GitHub Integration" settings page allows users to connect and synchronize their GitHub account with the current system. This integration aids in seamless data exchange, task automation, and enhanced functionalities within the system by leveraging GitHub's features.

#### **1. Connect using OAuth v2:**

* **Description**: OAuth 2.0 is a protocol that allows applications to request user authorization and access tokens over HTTPS. It's widely adopted for user-authorized interactions with third-party APIs.
* **Steps**:
  1. Navigate to the "Connect using OAuth v2" section.
  2. In the "Access Token" field, enter the access token provided by GitHub upon successful authorization.
  3. Once the token is inputted, the system will automatically validate the token's authenticity.

#### **2. Connect using Personal Access Tokens (PAT):**

* **Description**: Personal Access Tokens (PAT) are an alternative to using passwords for authentication to GitHub when using the GitHub API or the command line. They're more secure and can be easily regenerated.
* **Steps**:
  1. Navigate to the "Connect using Personal Access Tokens (PAT)" section.
  2. You'll notice a note indicating, "A PAT has access to only a single organization in GitHub. Please make sure you enter the correct PAT here."
  3. In the "Personal Access Token (PAT)" field, provide your GitHub Personal Access Token.
  4. Click on the "Connect" button to establish the integration.

***

### **Tips:**

* Ensure you've generated the necessary tokens from your GitHub account settings before attempting the integration.
* Always keep your Access Tokens and PATs confidential. Avoid sharing them and regenerate if you suspect any unauthorized access.
* Regularly check the permissions associated with your tokens to ensure they have the right level of access for the tasks you want to perform.

***

### **Troubleshooting:**

* If you face any issues during the integration:
  1. Confirm the validity of your Access Token or PAT.
  2. Check the permissions and scope of your tokens on GitHub to ensure they match the requirements of the system.
  3. If issues persist, consider regenerating your tokens on GitHub and retrying the integration.
  4. Reach out to support for more specific help.
