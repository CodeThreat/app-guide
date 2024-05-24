---
description: https://marketplace.visualstudio.com/items?itemName=CodeThreat.CodeThreat
---

# Azure

By integrating the [CodeThreat SAST](https://marketplace.visualstudio.com/items?itemName=CodeThreat.CodeThreat) application into your Azure DevOps environment, you can start managing your software development processes securely. Below, you will find steps and recommendations on how to make this process more understandable and effective:

**Installation of CodeThreat SAST Application**

**Adding the Application:** Find the CodeThreat SAST application on the Azure DevOps Marketplace and add it to your Azure DevOps environment. This is the first step in automating your security scans.

**Pipeline Configuration:** When creating a pipeline in Azure DevOps, search for the "CodeThreat Analysis - SAST" application in the "Task" section and add it to your pipeline. This step integrates CodeThreat's analysis capabilities into your project.

<figure><img src="../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

Configuration Settings: After adding the application, a window will open for you to make the necessary configurations. First, you need to configure the "CodeThreat Service Endpoint" setting. In Azure DevOps, follow the path Project Settings > Service connections > New Service Connection, search for "CodeThreat," and reach the related configuration window.

<figure><img src="../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

**Required Information:** Information such as the Server URL, username and password, or CodeThreat Token and Azure Token should be entered at this stage.

**Pipeline Configuration Details**

<figure><img src="../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

**Organization and Project Name:** You need to specify the organization name allocated for you in CodeThreat and the name of the project you want to scan. This information ensures the scan is performed within the correct scope.

**Failure Conditions**

**Max Number High/Critical:** These settings allow the pipeline to be considered failed based on the number of findings at a certain level of criticality. For example, 5 critical findings could cause the pipeline to stop.

**Weakness Is:** This setting stops the pipeline if weaknesses of a certain type are found. Multiple types of weaknesses can be specified, separated by commas. For example, “.\*injection” or ".\*injection,buffer.over.read,mass.assigment”

**Condition:** This setting determines how failure conditions are evaluated. The "AND" option requires all conditions to be met; "OR" indicates that meeting any one condition is sufficient.

**— In addition**

**Policy Name:** Determines under which security policy the scan will be conducted. The default is "Advanced Security," but different policies can also be selected.

**SyncScan:** When this option is active, the scan results are awaited, and the pipeline is marked as successful or failed accordingly. If not active, the pipeline moves to the next step immediately after the scan is initiated.

By following these steps, you can successfully install and configure the CodeThreat SAST application in your Azure DevOps environment. This integration allows you to automate security scans in your software development process and detect potential security vulnerabilities at an early stage.
