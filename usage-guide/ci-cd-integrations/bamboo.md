# Bamboo

Bamboo is a continuous integration and continuous delivery (CI/CD) tool developed by Atlassian. The CodeThreat Bamboo plugin allows you to add security scans to your Bamboo CI/CD workflows. This integration enhances the security of your projects by helping to detect vulnerabilities at an early stage. Below are the steps for installing and configuring the Codethreat Bamboo plugin, along with an example task configuration:



#### **CodeThreat Bamboo Plugin Installation**

* **Installing the Plugin:** Upload the CodeThreat Bamboo plugin to your Bamboo server. This is typically done through Bamboo's Manage Apps or Add-ons section.
* **Creating a Task within a Plan:** Navigate to an existing or new Bamboo plan and click on the Tasks tab. From there, use the Add task option to add a CodeThreat Scan Task to your plan.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

#### **Task Configuration**

After adding the task, you will encounter a configuration window like the one below. There are some mandatory fields in this window that you need to fill out:

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

* **Base URL:** The URL of the server where CodeThreat is running. For example,[https://codethreat.example.com](https://codethreat.example.com).
* **Username and Password or Token:** The username and password or access token for your CodeThreat account. These details are used to authorize CodeThreat scans.
* **Organization Name:** The name of your organization registered in CodeThreat.
* **Project Name:** The name of the project you want to scan, which will be created on CodeThreat.

**Failure Conditions**

**Max Number High/Critical:** These settings allow the pipeline to be considered failed based on the number of findings at a certain level of criticality. For example, 5 critical findings could cause the pipeline to stop.

**Weaknesses:** This setting stops the pipeline if weaknesses of a certain type are found. Multiple types of weaknesses can be specified, separated by commas. For example, “.\*injection” or ".\*injection,buffer.over.read,mass.assigment”

**Condition:** This setting determines how failure conditions are evaluated. The "AND" option requires all conditions to be met; "OR" indicates that meeting any one condition is sufficient.

**— In addition**

**Policy Name:** Determines under which security policy the scan will be conducted. The default is "Advanced Security," but different policies can also be selected.
