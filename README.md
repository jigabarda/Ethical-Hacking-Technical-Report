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
