# Access Token

The Access Token page is designed to facilitate the generation and management of access tokens. These tokens grant secure access to specific API endpoints. As a crucial security measure, once generated, these tokens cannot be retrieved, so users are encouraged to store them securely.

1. **Generating a New Token:**
   * **Description:** This functionality allows users to create new access tokens.
   * **Usage:** Click on the "+ New Token" button to generate a new token. Upon generation, make sure to copy and store the token in a secure location, as it won't be retrievable in the future.
2. **Token List:**
   * **Description:** A list of all the generated tokens, along with their associated details.
   * **Usage:**
     * **Name**: A user-defined name or label for the token to quickly identify its purpose or associated project.
     * **Token**: A partial view of the token. The complete token is hidden for security reasons.
     * **Created Date**: The date on which the token was generated.
     * **Last Used**: The most recent date the token was used to access an API endpoint. If it hasn't been used, it will display "Never".
     * **Action Button (represented by a bin icon)**: Allows users to delete the token if it's no longer needed or if it's suspected to be compromised.

#### **Interacting with Access Tokens:**

1. **Storing a Token**: After generating a new token, always ensure it's saved securely as the platform does not provide a retrieval option.
2. **Token Management**: Regularly review the "Last Used" column to monitor token activity. If there's any suspicion of unauthorized use, consider deleting the token and generating a new one.
3. **Deleting a Token**: Use the action button (bin icon) next to the token you wish to remove. Confirm the deletion in any subsequent prompts. Be cautious, as deleting a token will revoke access to any API endpoint associated with that token.

#### **Best Practices:**

* Do not share tokens publicly or with unauthorized personnel.
* Regularly monitor token usage and activity.
* Rotate tokens periodically for enhanced security.
* Always store tokens in a secure and encrypted location, such as a password manager or secure vault.
