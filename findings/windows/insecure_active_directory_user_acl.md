# Finding Details 

### Finding Matrix
| Title  | VSR  |  CVSS  | Risk | ID |
|:-:|:-:|:-:|:-:|:-:|
| Insecure Active Directory User ACLs   |  5 |  8.0 – 10.0 | Critical  | OS-CFDB-1000

### Finding Service
| Service  |
|:-:|
| Internal Penetration Testing  |
| External Penetration Testing  |

### Finding NIST 800-53 Controls
| NIST  |
|:-:|
| AC-6  |


### Finding MITRE ATT&CK Correlation
| Name | Tactic | ID | Link |
|:-:|:-:|:-:|:-:|
|Credentials in Files| Credential Access | T1081 | https://attack.mitre.org/wiki/Technique/T1081 |

### Finding References
| URL |
|:-:|
|https://www.blackhat.com/docs/us-17/wednesday/us-17-Robbins-An-ACE-Up-The-Sleeve-Designing-Active-Directory-DACL-Backdoors-wp.pdf  |
|https://msdn.microsoft.com/en-us/library/windows/desktop/aa446597(v=vs.85).aspx|
|https://blogs.technet.microsoft.com/pfesweplat/2017/01/28/forensics-active-directory-acl-investigation/|

# Technical Information

## Description 
Service Principal Names (SPNs) are a Microsoft way of designating and identifying where services are running in a domain. These SPNs are attached to accounts within active directory. Any Domain User has the ability to lookup these attributes and view the DACL (Discretionary Access Control List). A DACL is an access control list that is controlled by the owner of an object, and that specifies the access particular users or groups can have to the object. An attacker can enumerate these DACLS to find users in the Domain that have over permissive DACLS. This data allows an attacker to target specific users where the current user context is granted "GenericAll/GenericWrite" rights over a given user object. An attacker can then modify the user’s "serviceprincipalname," conduct a Kerberos attack of the user SPN set by request the TGT (Ticket Granting Ticket). Immediately following attackers reset the "serviceprincipalname" and begin offline brute-forcing. 

## Impact
If an attacker gains access to any user within the domain, they can start to request all AD (Active Directory) DACLs. If an attacker can break the password due a weak password, they will have the ability to impersonate that users account. Which could lead to further Domain and system compromise.

## Recommendation(s)
The assessment team recommends removing the "GenericAll/GenericWrite" attribute for the affected systems. An audit of critical and high privileged accounts should be conducted to ensure they are following the least privileged model.

# Finding Metadata
### Finding Development
| Author Name | Twitter Handle | Email | Created | Updated |
|:-:|:-:|:-:|:-:|:-:|
| Alexander Rymdeko-Harvey | @Killswitch-GUI |  | 09/27/2017 | 09/27/2017 |

### Finding Sources
| URL | 
|:-:|
|  |
