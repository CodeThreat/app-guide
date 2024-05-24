# GitHub Actions

Integrating CodeThreat with GitHub Actions allows you to automatically analyze the security of your projects hosted on GitHub. To set up this integration, you need to create a YAML file within the .github/workflows directory in the root directory of your project. If the .github or workflows directory does not exist, you should create them.

**Example YAML File**

```
run-name: CodeThreat Scan Task

on:
  # Trigger scan when pushing in master or pull requests, and when creating
  # a pull request.
  push:
        branches:
        - main
        - master
  pull_request:
        branches:
        - main
        - master
jobs:
  codethreat_scanner:
    runs-on: ubuntu-latest
    name: Codethreat Scan
    steps:
      - name: Check Out Source Code
        uses: actions/checkout@v3
      - name: Install Node.js
        uses: actions/setup-node@v1
      - name: CodeThreat Github Action Scanner
        uses: CodeThreat/codethreat-scan-action@master

        env:
           ACCESS_TOKEN: ${{ secrets.ACCESS_TOKEN }}
           GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
           CT_SERVER: ${{ secrets.CT_SERVER }}
           ORGNAME: ${{ secrets.ORGNAME }}
        with: 
            FAILED_ARGS: |
                 - max_number_of_critical: 15
                 - max_number_of_high: 15
                 - weakness_is: ".*injection"
                 - condition: 'OR'
                 - automerge: false
                 - sync_scan: true
                 - policy_name: 'Advanced Security'
```

**Explanation of Parameters in the YAML File** Under ‘steps’, the 'CodeThreat GitHub Action Scanner': This step is necessary to initiate the CodeThreat scan. The CodeThreat GitHub Action is added to your project with the specified ‘uses’ part, CodeThreat/codethreat-scan-action@master

Values under ‘env’: These are the values required to start the CodeThreat scan. These values should be securely entered in your project's Settings > Secrets and variables > Actions section.

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

There is no need to add GITHUB\_TOKEN as it is automatically provided by GitHub. Using USERNAME and PASSWORD instead of CT\_TOKEN is also possible.

**Failure Conditions(FAILED\_ARGS)** **Max Number High/Critical:** max\_number\_of\_critical and max\_number\_of\_high, in SAST scans, this causes the workflow to fail if a certain number of critical or high importance findings are detected. ‘sca\_max\_number\_of\_critical’ and ‘sca\_max\_number\_of\_high’, specifies the limits for the number of critical and high importance findings for SCA (Software Composition Analysis) findings. This works in a similar way to the criteria you set for SAST scans.

**Weakness Is:** Stops the workflow if weaknesses of a certain type are found. For example, “.\*injection” or ".\*injection,buffer.over.read,mass.assigment”

**Condition** : The AND or OR values determine how multiple fail\_args conditions are evaluated. AND requires all conditions to be met, while OR requires any one of them to be met to stop the workflow.

**Auto Merge** : If set to true and the process is triggered as a result of a merge request, the merge request is automatically accepted when the workflow is successful.

**— In addition**

**Sync Scan** : When set to false, the workflow continues without waiting for scan results. This can be useful, especially in situations where scan processes take a long time.

**Policy Name:** Determines under which security policy the scan will be conducted. The default is "Advanced Security," but different policies can also be selected.

This configuration and explanations provide a basic guide on how to configure integration with CodeThreat and GitHub Actions. This integration helps you to continuously scan your projects for security, aiding in the early detection of security vulnerabilities.
