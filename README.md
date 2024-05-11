# Ethical-Hacking-Technical-Report
##### Client: Meta
##### Date: May 11, 2024
##### Prepared by: James Ivan B. Gabarda and Miko Andre C. San Miguel
##### Executive Summary: 
This report presents the technical findings of the ethical hacking assessment 
conducted for Meta. The assessment aimed to identify vulnerabilities within the 
organization's network infrastructure, applications, and systems. Through various testing methodologies, 
including penetration testing and vulnerability scanning, critical and high-risk issues were discovered. 
This report provides detailed descriptions of these findings, along with actionable recommendations for 
remediation.


1. Improper Implementation of View As Feature:
  - Critical: Inadequate Access Control (CVE-2024-ABCDE) in Facebook's "View As" feature allows unauthorized users to post stuff instead of just viewing profiles.
  - High: Lack of Input Validation (CVE-2024-FGHIJ) in the "View As" feature, allows attackers to insert malicious programs or scripts into the system.
2. Incorrect Generation of Access Token:
  - Critical: Access Token Flaw (CVE-2024-KLMNO) in Facebook's video uploader results in the generation of access tokens with excessive rights.
  - High: The lack of Token Verification (CVE-2024-PQRST) in the access token generation process results in tokens that can be utilized by unauthorized parties.
3. Access Token Generated for Wrong User:
  - Critical: User Context Vulnerability (CVE-2024-UVWXY) in Facebook's "View As" feature, resulting in access tokens being created for the incorrect user during profile views.
  - High: Token Leakage (CVE-2024-ZABCD): Access tokens were exposed in HTML code, possibly allowing unwanted access to user accounts.
4. Lack of Rate-Limiting in Meta Accounts Center:
  - Critical: The Meta Accounts Center does not have rate-limiting for entering 2FA codes, which gives hackers the ability to breach user accounts by performing brute-force assaults on SMS codes.
  - High: Inadequate security protocols, including weak password guidelines or the absence of multi-factor authentication, raise the possibility of account takeovers and illegal access.
5. Vulnerability in Facebook's Password Reset Process:
  - Critical: The password reset procedure on Facebook has a flaw that lets attackers take over any Facebook account by using the six-digit unique authorization number that is issued throughout the process.
  - High: The authorization code lacks sufficient security features, such as restricted validity or brute-force protection, increasing the danger of illegal access to user accounts.
6. **Cookie Theft Vulnerability:**
   - *Critical:* Malicious actors can intercept and copy authentication cookies to gain unauthorized access to Facebook user accounts, leading to account takeover and unauthorized data access.
   - *High:* Lack of proper encryption or token-based authentication mechanisms increases the risk of cookie theft attacks, potentially compromising user privacy and security.
7. **Cross-Site Scripting (XSS):**
   - *Critical:* Meta's platform may be vulnerable to XSS attacks, allowing attackers to inject malicious scripts into web pages viewed by other users, leading to account takeover and spreading malware.
   - *High:* Failure to properly sanitize user-generated content can result in the execution of arbitrary code in users' browsers, compromising their accounts and personal data.
8. **Data Breaches:**
   - *Critical:* Any breach of Meta's vast user data could lead to the exposure of sensitive information, including personal details, messages, and login credentials, resulting in severe privacy violations and reputational damage.
   - *High:* Weak access controls, inadequate encryption, or insider threats increase the likelihood of data breaches, exposing users to identity theft and financial fraud.
9. **OAuth Token Leakage:**
   - *Critical:* Improper handling of OAuth tokens could result in leakage, allowing attackers to access user accounts or impersonate them on other platforms, leading to unauthorized data access and misuse of user information.
   - *High:* Lack of token expiration policies, insufficient rate limiting, or inadequate monitoring of token usage increases the risk of OAuth token leakage, compromising user privacy and security.
10. **Privacy Violations:**
   - *Critical:* Flaws in privacy settings or data access controls could lead to unintended exposure of user information, violating privacy regulations and causing reputational damage to Meta.
   - *High:* Inadequate user consent mechanisms, excessive data collection practices, or insufficient transparency regarding data usage increase the risk of privacy violations, eroding user trust and loyalty.

##### Recommendations:
1. Improper Implementation of View As Feature:
  - Implement strict input validation and access restrictions to guarantee that users can only execute the required activities when using the "View As" feature.
  - Conduct regular security audits and code reviews to detect and resolve any possible vulnerabilities in the feature.
2. Incorrect Generation of Access Token:
  - Update the video uploader component to make sure that the right permissions are granted and that the access tokens are not granted too much.
  - Implement token expiration and revocation methods to mitigate the effect of compromised access tokens.
3. Access Token Generated for Wrong User:
  - Modify the "View As" features so that access tokens are produced for the viewer instead of the user being looked up.
  - Encrypt or conceal access tokens in HTML code to prevent unwanted use or theft.
4. Lack of Rate-Limiting in Meta Accounts Center:
  - Implement rate-limiting strategies in the Meta Accounts Center to restrict the number of tries to enter 2FA codes, resulting in lowering the danger of brute force attacks.
  - Implementing multi-factor authentication and maintaining strong password restrictions can improve overall security posture by providing additional protection against account breaches and unwanted access.
5. Vulnerability in Facebook's Password Reset Process:
  - Security administrators should ensure that all applications, databases, servers, and network devices are regularly hardened and properly configured.
  - Users are encouraged to make use of a password manager to create a unique and strong password for each site, and to use Multi-Factor Authentication (MFA) wherever possible.
  - System administrators must perform frequent backups and store them offline or on a different network.
6. **Cookie Theft Vulnerability:**
   - Implement secure cookie handling mechanisms, such as HTTPOnly and Secure flags, to prevent unauthorized access to authentication cookies.
   - Implement additional security measures, such as token-based authentication or session encryption, to mitigate the risk of cookie theft attacks.
7. **Cross-Site Scripting (XSS):**
   - Implement input validation and output encoding to sanitize user-generated content and prevent XSS attacks.
   - Regularly scan and audit web applications for security vulnerabilities, including XSS, using automated tools and manual testing.
8. **Data Breaches:**
   - Strengthen access controls and encryption mechanisms to protect sensitive user data stored by Meta.
   - Implement advanced threat detection and monitoring solutions to detect and respond to data breaches in real-time.
9. **OAuth Token Leakage:**
   - Enhance OAuth token management processes to prevent unauthorized access and leakage of tokens.
   - Implement rate limiting and monitoring for OAuth token usage to detect and mitigate suspicious activities.
10. **Privacy Violations:**
   - Conduct regular privacy assessments to identify and address gaps in privacy controls and data access permissions.
   - Provide users with more granular control over their privacy settings and data sharing options.
