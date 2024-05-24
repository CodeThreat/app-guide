# Jenkins

Jenkins is an open-source automation server used to automate continuous integration and continuous delivery (CI/CD) workflows. The CodeThreat Jenkins plugin allows you to easily perform security scans within your Jenkins environment. Below are the steps for installing and configuring the CodeThreat Jenkins plugin, along with an example pipeline configuration:



#### **CodeThreat Jenkins Plugin Installation**

* **Installing the Plugin:** Go to the Jenkins management panel, navigate to Manage Jenkins > Manage Plugins > Available tab, search for "CodeThreat" to find the CodeThreat plugin, and install it.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

Adding Credentials: To perform CodeThreat scans, you need to add your credentials to Jenkins. Go to Manage Jenkins > Manage Credentials and create a new credential using the "Username with password" option for your CodeThreat username and password, or the "Secret text" option for your CodeThreat access token. Assign an ID to the credential you create; this ID will be used in the pipeline configuration.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

Defining a Global Environment Variable: Define a global environment variable for the URL of the server where CodeThreat is running. Go to Manage Jenkins > Configure System, check the "Environment variables" option under "Global properties," and add a variable for the CodeThreat server URL (e.g., CT\_SERVER\_URL).

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

#### **Example Pipeline Configuration**

The following Jenkinsfile is an example of a Jenkins pipeline that includes a CodetThreat scan:

```
pipeline {
    agent any
    environment {
        CT_SERVER_URL = 'https://codethreat.example.com'
    }
    stages {
        stage('Clone') {
            steps {
                git url: 'https://github.com/exampleUser/exampleRepo.git', branch: 'main'
                sh 'zip -r example.zip .'
            }
        }
        stage('Scan') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'codethreat_credentials', usernameVariable: 'username', passwordVariable: 'password')]) {
                    script {
                        CodeThreatScan(
                            ctServer: "${CT_SERVER_URL}",
                            fileName: "example.zip",
                            project_name: "exampleProjectName",
                            credentialsId: "codethreat_credentials",
                            organization_name: "exampleOrganizationName",
                            maxNumberOfHigh: 10,
                            maxNumberOfCritical: 5,
                            weaknessIs: ".*injection,buffer.over.read,mass.assignment", 
                            condition: "OR",
                            policyName: "Advanced Security",
                            scaMaxNumberOfHigh: 10,
                            scaMaxNumberOfCritical: 5
                        )
                    }
                }
            }
        }
    }
}
```

If you want to use it with tokens

```
pipeline {
    agent any
    environment {
        CT_SERVER_URL = 'https://codethreat.example.com'
    }
    stages {
        stage('Clone') {
            steps {
                git url: 'https://github.com/exampleUser/exampleRepo.git', branch: 'main'
                sh 'zip -r example.zip .'
            }
        }
        stage('Scan') {
            steps {
                 withCredentials([string(credentialsId: 'codethreat_credentials_token', variable: 'accessTokenSecret')]) {
                    script {
                        CodeThreatScan(
                            ctServer: "${CT_SERVER_URL}",
                            fileName: "example.zip",
                            project_name: "exampleProjectName",
                            credentialsId: "codethreat_credentials",
                            organization_name: "exampleOrganizationName",
                            maxNumberOfHigh: 10,
                            maxNumberOfCritical: 5,
                            weaknessIs: ".*injection,buffer.over.read,mass.assignment", 
                            condition: "OR",
                            policyName: "Advanced Security",
                            scaMaxNumberOfHigh: 10,
                            scaMaxNumberOfCritical: 5
                        )
                    }
                }
            }
        }
    }
}
```

Among the above values, ctServer, fileName, project\_name, credentialsId, organization\_name are required. Other fields are not required. Now let's talk about those areas.

**Failure Conditions**

**Max Number High/Critical:** These settings allow the pipeline to be considered failed based on the number of findings at a certain level of criticality. For example, 5 critical findings could cause the pipeline to stop.

**Weakness Is:** This setting stops the pipeline if weaknesses of a certain type are found. Multiple types of weaknesses can be specified, separated by commas.

**Condition:** This setting determines how failure conditions are evaluated. The "AND" option requires all conditions to be met; "OR" indicates that meeting any one condition is sufficient.

**— In addition**

**Policy Name:** Determines under which security policy the scan will be conducted. The default is "Advanced Security," but different policies can also be selected.
