# Github

#### **Client ID**

* **Description**: This identifier is unique to your OAUTH application on GitHub.
* **Instructions**:
  1. Navigate to your GitHub OAUTH application settings.
  2. Find and copy the Client ID.
  3. Paste the Client ID into the respective field on the integration page.

#### **Client Secret**

* **Description**: This is a confidential key associated with your GitHub OAUTH application.
* **Instructions**:
  1. In the GitHub OAUTH application settings, locate the Client Secret.
  2. Copy and paste the Client Secret into the designated field.

#### **App ID**

* **Description**: This is a numerical identifier specific to your GitHub OAUTH application.
* **Instructions**:
  1. In the GitHub OAUTH application settings, locate the App ID.
  2. Copy and insert the App ID in the provided space.

#### **App WebHook Secret**

* **Description**: This secret is used to validate the integrity of webhook requests from GitHub.
* **Instructions**:
  1. Within the GitHub OAUTH application settings, find the WebHook Secret.
  2. Copy and enter the WebHook Secret into the designated area.

***

#### **3. Setting the Scope**

* **Description**: The scope determines the access level and permissions that your OAUTH app will have on GitHub.
* **Instructions**:
  1. When setting up your GitHub OAUTH application, ensure you include the recommended scopes as listed.
  2. Input the scopes (e.g., **`user:email,read:org,repo`**) in the corresponding field on the integration page.

***

#### **4. Callback URL Configuration**

* **Description**: This URL is where GitHub redirects users after they grant or deny permission for your OAUTH application.
* **Instructions**:
  1. Set the Callback URL in your GitHub OAUTH application settings to match the example provided, ensuring a consistent path.
  2. The URL should adhere to the format: **`https://[your-domain].com/settings/integration-settings/github`**.
