# Azure

If you're looking to integrate with Azure DevOps:

**Client ID**

* **Description**: This is the unique identifier for your OAUTH application on Azure DevOps.
* **Instructions**:
  1. 1.Navigate to your Azure DevOps OAUTH application settings.
  2. 2.Locate and copy the Client ID.
  3. 3.Paste the Client ID into the provided field.

**Client Secret**

* **Description**: This is the secret key associated with your OAUTH application on Azure DevOps.
* **Instructions**:
  1. 1.Navigate to your Azure DevOps OAUTH application settings.
  2. 2.Locate and copy the Client Secret.
  3. 3.Paste the Client Secret into the provided field.

***

**3. Scope**

* **Description**: The scope defines the type of access and permissions the OAUTH app will have. This ensures that the application only accesses the specific capabilities that it has been granted.
* **Instructions**:
  1. 1.When creating or editing your OAUTH application on Azure, ensure you set the required and recommended scopes as displayed.
  2. 2.Paste the scopes, as mentioned in the provided field.

***

**4. Redirect URL**

* **Description**: This is the URL to which the user will be redirected after they grant/deny permission on Azure DevOps for your OAUTH app.
* **Instructions**:
  1. 1.In your Azure DevOps OAUTH application settings, set the Redirect URL to the provided example URL, ensuring the path is consistent.
  2. 2.Make sure that the URL matches the example format: **`https://[your-domain].com/settings/integration-settings/azure`**.
