# Report

The "report" tab provides an interface for users to generate detailed reports based on the most recent scan of a given project. The comprehensive set of filters allows users to tailor the results to their specific needs, ensuring that they receive only the most relevant information. The generated reports can be exported in two formats: HTML and PDF.

1. **Saved Filters**: This section allows users to save their custom filter configurations. Once saved, these configurations can be quickly loaded in future scans, streamlining the report generation process. It's a time-saving feature for those who regularly require specific types of reports.
2. **Scan Scope**: This section determines the scope of the generated report.
   * **Severities**: Filters vulnerabilities based on their severity levels. Options range from informational (info) to critical, ensuring users can focus on threats relevant to their needs.
   * **Fix Costs**: Helps to prioritize issues based on the estimated resources required to address them. Users can filter results by low, medium, and high fix costs.
   * **Standards**: Defines the security standards against which the scan was conducted. Options include well-known standards like HIPAA, CWE, PCI DSS, OWASP Top 10, NIST800-53R4, and ISO27001.
3. **Status**: This filter categorizes vulnerabilities based on their current status, such as Hidden, Open, Closed, Accepted, ReCheck, and FalsePositive.
4. **Platforms**: Identifies the platforms or programming languages relevant to the scan. It's essential for teams working across multiple tech stacks.
5. **Impacts**: This section categorizes vulnerabilities based on the potential impacts they could have if exploited. Examples include client-side code execution, remote code execution, insecure configuration bypassing, and more.
6. **Root Causes**: Determines the underlying causes or weaknesses leading to the vulnerabilities. This filter helps teams understand and address the root of the problem.
7. **Labels**: Additional categorization based on specific characteristics or traits of the vulnerabilities, like credential, configuration, password, and more.
