# Bug-Bounty-Hunting-On-OpenBugBounty
It is a security-focused initiative aimed at identifying and reporting vulnerabilities on websites listed on the Open Bug Bounty platform and  maintaining the integrity of online services and promoting a safer digital environment.

## Team Member:
DEEPAK MOHANTY, G PREETAM KUMAR, SALMAN DUDEKULA, GORLA BHARGAV REDDY, LASHKAR VARUNESH, DEVARASETTI KAYALN, C.SUDHEER KUMAR REDDY

## Introducation:
The rapid growth of digital techonologies has transformed the way we live, work and communicate. However, it has also increased the risk of cyber threats such as hacking, data breaches, and identify theft. As a result, there  is a growing need for enchanced online security measures to protect individuals and organizations from these risks.

The Bug hunting on any target of openbugbounty aims to address this need by identifying and reporting vulnerabilities on websites listed on the Open Bug Bounty platform. Open Bug Bounty is a non-profit organization that facilitates coordinated disclosure of website security vulnerabilities by connecting security researchers with website owners. The platform enables researchers to identify vulnerabilities and report them to the website owner, allowing them to take necessary measures to address the issues.

## Testing Methodology:
- Choose a target from openbugbounty platform
- Manual Testing
- Exploitation
- Reporting
- Verification

## Choose a target from openbugbounty platform
1. First create an account on openbugbounty in order to participate in their bug bounty program.
2. Now, here we are choosing https://lescontamines.net/ that was listed on OpenBugBounty as a target for our bug hunting.
   
![Screenshot 2024-02-07 151806](https://github.com/ItsDeepakgit/Bug-Bounty-Hunting-On-OpenBugBounty/assets/91217911/3a02e8a8-7551-4a73-a9fe-fd928fe26f82)

## Manual Testing
3. Next, conduct manual testing to identify vulnerabilities.
   
##### Vulnerable found: CWE-79: Cross-site scripting (XSS)
##### Type: Critical

**XSS:** 

Cross-site scripting (also known as XSS) is a web security vulnerability that allows an attacker to compromise the interactions that users have with a vulnerable application. It allows an attacker to circumvent the same origin policy, which is designed to segregate different websites from each other. Cross-site scripting vulnerabilities normally allow an attacker to masquerade as a victim user, to carry out any actions that the user is able to perform, and to access any of the user's data. 

![Screenshot 2024-02-07 152308](https://github.com/ItsDeepakgit/Bug-Bounty-Hunting-On-OpenBugBounty/assets/91217911/253e521d-f17d-4e96-834a-73bfa852382f)

## Exploitation:
4. Exploit the vulnerability by injecting the following script into the URL: `"><script>alert(document.cookie)</script>`.

![Screenshot 2024-02-07 153006](https://github.com/ItsDeepakgit/Bug-Bounty-Hunting-On-OpenBugBounty/assets/91217911/20191158-9032-4fc1-b8f2-9ac17e61c2a6)

5. Observe the page triggered with on XSS.

![Screenshot 2024-02-07 153339](https://github.com/ItsDeepakgit/Bug-Bounty-Hunting-On-OpenBugBounty/assets/91217911/73321f43-b864-4110-be8f-2bf117382f8c)

![Screenshot 2024-02-07 153409](https://github.com/ItsDeepakgit/Bug-Bounty-Hunting-On-OpenBugBounty/assets/91217911/2cf40054-01ad-49e3-b4de-8c3a423b65b6)

## Reporting:
6. Next, Reporting XSS vulnerability to the website owner through the OpenBugBounty platform.

![Screenshot 2024-02-07 150435](https://github.com/ItsDeepakgit/Bug-Bounty-Hunting-On-OpenBugBounty/assets/91217911/c58f86cb-ed9e-4bd2-a92d-dabf1872336c)

### Report in Proper Document:
We are finding a critical security vulnerability on website, https://lescontamines.net/, specifically related to CWE-79: Cross-Site Scripting (XSS). This vulnerability exposes users to the risk of having their private information, including session cookies, compromised by malicious actors.
#### **Vulnerability Details:**
Vulnerability Type: CWE-79: Cross-site Scripting(XSS)

Affected URL: https://lescontamines.net/?Tp=%22%3E%3Cscript%3Ealert(document.cookie)%3C/script%3E

#### **Steps to Reproduce:**
1. Navigate to the website https://lescontamines.net/.
2. Exploit the vulnerability by injecting the following script into the URL: `"><script>alert(document.cookie)</script>`.
3. Observe the triggered XSS on the page.

#### **Impact:**
The identified XSS vulnerability allows an attacker to:
- **Impersonate or Masquerade as the Victim User:** The attacker can assume the identity of a legitimate user.
- **Read Any Data Accessible to the User:** Access sensitive user information.
- **Capture User Login Credentials:** Obtain login credentials, compromising user accounts.
- **Perform Unauthorized Actions:** Execute actions on behalf of the user, potentially causing harm.
The actual impact of an XSS attack generally depends on the nature of the application, its functionality and data, and the status of the compromised user. 

#### **Recommendations (Mitigation):**
- **Input Validation:** Implement thorough input validation mechanisms to sanitize and validate user inputs, preventing the injection of malicious scripts.
- **Output Encoding:** Apply proper output encoding to all user-generated content before rendering it on web pages to prevent script execution.
- **Content Security Policy (CSP):** Utilize a Content Security Policy to restrict the types of content that can be loaded on your web pages, mitigating the impact of XSS attacks.
- **Security Audits:** Conduct regular security audits, including automated tools and manual code reviews, to identify and address potential vulnerabilities proactively.

Thank You..!
Sincerely,
Deepak Mohanty
G Preetam Kumar
SALMAN DUDEKULA
Gorla Bhargav Reddy	
Lashkar Varunesh	
Devarasetti Kalyan	
C.sudheer Kumar Reddy     

## Verification: (https://www.openbugbounty.org/reports/3849918/)

![Screenshot 2024-02-07 210655](https://github.com/ItsDeepakgit/Bug-Bounty-Hunting-On-OpenBugBounty/assets/91217911/bbcdd67a-1313-42df-bae1-3e544de8e1d3)


![Screenshot 2024-02-07 210851](https://github.com/ItsDeepakgit/Bug-Bounty-Hunting-On-OpenBugBounty/assets/91217911/1c9037ac-60f0-4a0a-97ad-5e6a4d1f4d94)


## Conclusion:
The Bug hunting on any target of openbugbounty project can help to ensure that vulnerabilities are identified and reported accurately, and that website owners can take necessary measures to improve their website's security.

## References:
- https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html
- https://portswigger.net/web-security/cross-site-scripting













