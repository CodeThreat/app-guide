# Jira

The "Jira Integration" settings page offers users the capability to connect and synchronize their Jira account with the current platform. With this integration, users can ensure a smooth flow of data, benefit from task automation, and make the most out of both Jira's and the platform's functionalities.

#### **Connect using API Token:**

* **Description**: API tokens are a secure and efficient method to connect applications without the necessity of revealing user credentials. With the token, third-party platforms can interact with Jira, creating an integrated experience.
* **Steps**:
  1. Navigate to the "Connect using API Token" section.
  2. Read the instruction: "You can use Jira's API token to connect your application. For more info, click here." This link can provide detailed guidance on generating and using Jira API tokens.
  3. A reminder is given: "An API Token has access to only a single organization in Jira. Please make sure you enter the correct API Token here."
  4. Enter your generated Jira API Token into the "API Token" field.
  5. For the "Protocol" dropdown, select the protocol your Jira instance uses. This is typically "HTTP" or "HTTPS."
  6. In the "Hostname" field, provide the domain name or IP address of your Jira server or cloud instance (e.g., **`yourcompany.atlassian.net`**).
  7. Fill in the "User Email" field with the email address associated with your Jira account.
  8. Click on the "Connect" button to complete the integration process.

***

### **Tips:**

* Prior to initiating the integration, ensure you have your Jira API token ready. You can generate this from your Jira account settings.
* API tokens should be treated with utmost confidentiality. Refrain from disclosing them, and regenerate immediately if there's a suspicion of any unauthorized access.
* Periodically, review the permissions linked to your API token in Jira to confirm it possesses the required rights for your operations.

***

### **Troubleshooting:**

* If you encounter difficulties during the integration:
  1. Confirm that your API Token is active and valid.
  2. Check the permissions and scope of your API token within Jira to ensure compatibility with platform requirements.
  3. If problems persist, consider regenerating your API token in Jira and attempting integration anew.
  4. Always feel free to reach out to support for specialized guidance.
