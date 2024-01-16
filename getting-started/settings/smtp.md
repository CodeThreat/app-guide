# SMTP

#### **1. Host Name**

* **Description:** This field represents the SMTP server's address that your application will use to send out emails.
* **Usage:** Enter the complete domain name of your SMTP server. Ensure it's accurate to allow successful email communications.

#### **2. Username**

* **Description:** This field is for specifying the authentication credentials, particularly the username, required to connect to the SMTP server.
* **Usage:** Provide the username associated with your SMTP server. It is often an email address, but always refer to your service provider for accurate details.

#### **3. Password**

* **Description:** Alongside the username, this field is used for authentication. It's the password associated with the provided username for the SMTP server.
* **Usage:** Carefully enter the password that corresponds to the provided username. Keep this information confidential to ensure email security.

#### **4. Port**

* **Description:** The SMTP server uses a specific port to listen for incoming requests. This field is to specify that port number.
* **Usage:** Input the port number designated by your SMTP service provider. Common port numbers are 25, 465, and 587, but always use the one recommended by your provider.

#### **5. TLS Enabled**

* **Description:** Transport Layer Security (TLS) is a protocol used for encrypting communications. When enabled, this ensures that emails are sent securely.
* **Usage:** Toggle this option based on your SMTP server's requirements. If your server supports and recommends using TLS, ensure this is enabled. If not, you can disable it.

#### **Test SMTP Connection**

* **Functionality:** This button allows you to test the current SMTP configuration. By clicking it, the system will attempt to establish a connection with the SMTP server using the provided settings. This helps in verifying if the settings are correct.
