---
description: https://github.com/CodeThreat/codethreat-gitlab-plugin
---

# Gitlab

Integrating CodeThreat with GitLab allows you to perform automatic security scans within your GitLab CI/CD workflows. This integration is configured via the **`.gitlab-ci.yml`** file, ensuring your project is continuously analyzed for security. Below is a detailed guide on how to configure CodeThreat integration for GitLab:

#### **CodeThreat Integration for GitLab**

#### **Setup Steps**

* **Creating the YAML File:** Begin by creating a **`.gitlab-ci.yml`** file in your projects. This file defines your GitLab CI/CD workflows.

```
include:

  - 'https://raw.githubusercontent.com/CodeThreat/codethreat-gitlab-plugin/main/templates/codethreat.gitlab-ci.yaml'

variables:
  GITLAB_ACCESS_TOKEN: "$GITLAB_ACCESS_TOKEN"
  GITLAB_USER_LOGIN: "$GITLAB_USER_LOGIN"
  GITLAB_BASE_URL: "https://gitlab.com"
  # Codethreat specific variables
  CT_BASE_URL: "$CT_BASE_URL" # SAST Center base URL  
  CT_TOKEN: "$CT_TOKEN"    # USER API token
  CT_ORGANIZATION: "codethreat" # Organization Name
  FAILED_ARGS: '{}'

```

This configuration automates your security scans using the CodeThreat GitLab Plugin. The **`include`** key incorporates a template file provided by CodeThreat into your project.

* **Configuring Variables:** In the **`variables`** section, define variables specific to GitLab and CodeThreat. These variables should be securely added in the Settings > CI / CD > Variables section of your GitLab group.

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

**Failure Conditions(FAILED\_ARGS)**

**Details of FAILED\_ARGS:** This JSON object determines when the workflow will be considered a failure based on the scan results. For instance, you can stop the workflow if a certain number of critical or high importance findings are detected or if specific types of vulnerabilities are found.

```
FAILED_ARGS: '{
  "max_number_of_critical":5,
  "max_number_of_high":4,
  "weakness_is":".*injection",
  "condition":"OR",
  "sync_scan":true,
  "policy_name":"Advanced Security",
  "sca_max_number_of_critical":5,
  "sca_max_number_of_high":4,
}'
```

**Max Number High/Critical:** max\_number\_of\_critical and max\_number\_of\_high, in SAST scans, this causes the workflow to fail if a certain number of critical or high importance findings are detected. sca\_max\_number\_of\_critical and sca\_max\_number\_of\_high, specifies the limits for the number of critical and high importance findings for SCA (Software Composition Analysis) findings. This works in a similar way to the criteria you set for SAST scans.

**Weakness Is:** Stops the workflow if weaknesses of a certain type are found. For example, “.\*injection” or ".\*injection,buffer.over.read,mass.assigment”

**Condition** : The AND or OR values determine how multiple fail\_args conditions are evaluated. AND requires all conditions to be met, while OR requires any one of them to be met to stop the workflow.

**Auto Merge** : If set to true and the process is triggered as a result of a merge request, the merge request is automatically accepted when the workflow is successful.

**— In addition**

**Sync Scan** : When set to false, the workflow continues without waiting for scan results. This can be useful, especially in situations where scan processes take a long time.

**Policy Name:** Determines under which security policy the scan will be conducted. The default is "Advanced Security," but different policies can also be selected.

This configuration and explanations offer a basic guide on how to set up integration with CodeThreat and GitLab CI/CD. This integration facilitates continuous security scanning of your projects, helping in the early detection of security vulnerabilities.
