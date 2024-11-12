# Server Setup

### Overview

CodeThreat SAST Center is an app that serves as a built-in platform offering source code scanning and integration features once installed on your operating system. This guide will walk you through the installation process.

### Supported Operating Systems

CodeThreat is compiled for major operating systems including:

* Windows
* Linux
* MacOS

Although specifically tailored for these operating systems, CodeThreat may also function correctly on similar or derivative systems. Please note that performance and compatibility on non-standard systems cannot be guaranteed, and support may be limited.

### Prerequisites

Before getting started, please ensure you meet the following requirements:

* One of the compatible operating systems mentioned above
* MongoDB

### Installation Steps

1. **Download the Product**: Use the provided download link to obtain the CodeThreat software compatible with your operating system.
2. **Extract the Files**: Once downloaded, extract the CodeThreat files to your designated machine.
3. **Install MongoDB**: CodeThreat requires MongoDB version 6+ or higher. Follow the installation guide for your system below:&#x20;
   * [MongoDB Installation for Windows](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-windows/)
   * [MongoDB Installation for Linux](https://www.mongodb.com/docs/manual/administration/install-on-linux/)
   * [MongoDB Installation for Mac](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-os-x/)
4. **Configure the System**: Navigate to the `config-example.json` file, copy it as  `config.json`and enter the appropriate details in the following fields:



```json
config.json

{
  "host": "localhost",
  "port": 8080,
  "certificate": "",
  "key": "",
  "update_url": "https://cloud.codethreat.com",
  "token": "",
  "mongo_url":  ""
}
```

```markdown
- `token`: If you wish to use automatic updates,
enter the token sent to you in this field. This will activate online updates.
- `mongo_url`: Enter the connection string of the intended MongoDB here.
```

### Security Considerations

Before proceeding, it is essential to review the following security measures:

* Ensure that your system is up to date with the latest security patches.
* Ensure that the MongoDB instance is securely configured and access is appropriately restricted.

### Next Steps

Once you have completed the above steps, you are ready to proceed to the next phase of the CodeThreat setup. Please refer to the next section of this guide for further instructions.

