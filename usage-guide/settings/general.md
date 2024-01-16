# General

#### 1.**Server URL**

* **Description:** This is the primary URL where your application communicates for remote access. It sets the foundation for where the application has been deployed, and how links within the application are interpreted.
* **Usage:** Enter the complete URL (including the **`https://`** or **`http://`** protocol) of the server. This URL will be used for all remote access operations and will override any previous URLs.

#### **2. Scan Process Hang Time (min)**

* **Description:** This setting is crucial for ensuring efficient scanning processes. If a scanning process does not progress (either it hangs or turns into a non-responsive state), this setting determines the maximum amount of time (in minutes) the system will wait before automatically terminating that process.
* **Usage:** Enter the desired time in minutes. The system will monitor scanning processes, and if any of them are unresponsive for the duration specified, they will be automatically terminated.

#### **3. Max Upload Limit (GB)**

* **Description:** To ensure that the system isn't overwhelmed with large uploads, this setting places a restriction on the maximum size of data that can be uploaded to the application.
* **Usage:** Specify the maximum upload limit in gigabytes (GB). This will be the upper limit for any data or files uploaded to the application.

#### **4. RabbitMQ Connection String**

* **Description:** RabbitMQ is a message-broker system. This setting is for specifying how the application connects to a RabbitMQ server. The connection string contains the necessary information to establish this connection.
* **Usage:** Enter the complete connection string for your RabbitMQ server. Ensure it's accurate to maintain a stable connection for message brokering.

#### **5. AzureBlob Connection String**

* **Description:** AzureBlob storage is a service for storing large amounts of unstructured data. This setting allows the application to connect to an AzureBlob storage account.
* **Usage:** Provide the connection string for your AzureBlob storage account. It's crucial for accessing and storing data in the Azure cloud.

#### **6. AzureBlob Container Name**

* **Description:** Within AzureBlob storage, data is stored in containers. This setting specifies the name of the container where the application should store its data.
* **Usage:** Enter the name of the AzureBlob container designated for the application's data storage.
