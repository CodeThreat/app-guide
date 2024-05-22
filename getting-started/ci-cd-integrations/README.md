# CI-CD Integrations

In today's software development processes, Continuous Integration and Continuous Deployment (CI/CD) play a crucial role. CodeThreat offers plugins that integrate with various CI/CD platforms, making these processes more secure and efficient. Compatible with CI/CD tools such as Azure, Jenkins, Bamboo, GitLab, and GitHub Actions, these plugins allow you to incorporate CodeThreat's robust security analysis features directly into your software development workflow.

Before starting the integration process, there are some prerequisites that need to be met to ensure the plugins work smoothly:

**Access to CodeThreat Server:** The first step in integration is having a URL where CodeThreat is running. This is typically provided through CodeThreat's cloud-based service at [cloud.codethreat.com](http://cloud.codethreat.com). This URL serves as a central point where the plugins can send analysis results.

**CodeThreat Account:** Another requirement for integration is having a valid CodeThreat account. This account is used to manage and access your analysis results. The CI/CD plugins use your username and password or a more secure option, a personal access token, to access this account.

**Special Integration Tokens:** Some CI/CD platforms may require special security or access tokens during integration. For example, services like Azure or GitLab may require these tokens to be specified in the plugin configuration. These tokens enhance the security of the integration and ensure seamless communication between the CodeThreat plugins and the respective CI/CD platform.

Once these prerequisites are met, CodeThreat plugins can add valuable security analyses to your software development process, enabling safer development and deployment of your applications. Detailed setup and configuration steps for each CI/CD platform are explained in the respective integration guides.
