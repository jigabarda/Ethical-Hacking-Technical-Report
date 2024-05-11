# Ethical-Hacking-Technical-Report
##### Client: Meta/Facebook
##### Date: May 11, 2024
##### Prepared by: James Ivan B. Gabarda and Miko Andre C. San Miguel
##### Executive Summary: 
This report presents the technical findings of the ethical hacking assessment 
conducted for [Company Name or Website]. The assessment aimed to identify vulnerabilities within the 
organization's network infrastructure, applications, and systems. Through various testing methodologies, 
including penetration testing and vulnerability scanning, critical and high-risk issues were discovered. 
This report provides detailed descriptions of these findings, along with actionable recommendations for 
remediation.


1. Improper Implementation of View As Feature:
  - Critical: Inadequate Access Control (CVE-2024-ABCDE) in Facebook's "View As" feature, allowing unauthorized users to post content instead of just viewing profiles.
  - High: Lack of Input Validation (CVE-2024-FGHIJ) in the "View As" feature, enabling attackers to inject malicious code or scripts into the system.
2. Incorrect Generation of Access Token:
  - Critical: Access Token Flaw (CVE-2024-KLMNO) in Facebook's video uploader, resulting in the generation of access tokens with excessive permissions.
  - High: Lack of Token Verification (CVE-2024-PQRST) in the access token generation process, leading to tokens that can be used by unauthorized parties.
3. Access Token Generated for Wrong User:
  - Critical: User Context Vulnerability (CVE-2024-UVWXY) in Facebook's "View As" feature, causing access tokens to be generated for the wrong user during profile views.
  - High: Token Leakage (CVE-2024-ZABCD) due to access tokens being exposed in HTML code, potentially leading to unauthorized access to user accounts.
##### Recommendations:
1. Improper Implementation of View As Feature:
  - Implement strict input validation and access controls to ensure that users can only perform intended actions within the "View As" feature.
  - Conduct regular security audits and code reviews to identify and fix any potential vulnerabilities in the feature.
2. Incorrect Generation of Access Token:
  - Update the video uploader component to ensure that access tokens are generated with the correct permissions and are not overly permissive.
  - Implement token expiration and revocation mechanisms to limit the impact of compromised access tokens.
3. Access Token Generated for Wrong User:
  - Modify the "View As" feature to ensure that access tokens are generated for the viewer and not for the user being looked up.
  - Encrypt or obfuscate access tokens in HTML code to prevent unauthorized access or token theft.
