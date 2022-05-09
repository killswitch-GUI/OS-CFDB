# Finding Details 

### Finding Matrix
| Title  | VSR  |  CVSS  | Risk | ID |
|:-:|:-:|:-:|:-:|:-:|
| Firewall Misconfiguration  |  4 |  6.0 – 7.9 | High | OS-CFDB-1002

### Finding Service
| Service  |
|:-:|
| Internal Penetration Testing  |
| External Penetration Testing  |

### Finding NIST 800-53 Controls
| NIST  |
|:-:|
| SC-32  |
| SC-7   |

### Finding MITRE ATT&CK Correlation
| Name | Tactic | ID | Link |
|:-:|:-:|:-:|:-:|
| Exfiltration Over Command and Control Channel | Exfiltration | T1041 | https://attack.mitre.org/wiki/Technique/T1041 |

### Finding References
| URL |
|:-:|
| https://www.infosecurity-magazine.com/opinions/to-err-is-human-to-automate-divine/ |
| https://pdfs.semanticscholar.org/c644/7ffe218ad2a68f1df858900328534fe849ed.pdf |


# Technical Information

## Description 
Firewall misconfigurations are most likely to occur during security change processes – that is, when new rules are added, or existing ones changed or removed on a firewall. When a firewall rule is added that is over permissive it may allow an attacker to target specific machines to gain access to a high-security environment. In some cases, rules will be added when the organization accepts the risk. 

## Impact
If a rule is exposed or discovered by an attacker, they may have the ability to subvert in place security controls. This could lead to cross-boundary lateral movement and compromise of high-security environments which were believed to be secure.


## Recommendation(s)
To effectively mitigate against the risk of device misconfiguration an organization needs to implement proper change management processes. This process should allow stakeholders to understand the risk of the configuration. If business requirements require acceptance of a risk, an audit should be conducted to ensure all rules are still applicable. 

# Finding Metadata
### Finding Development
| Author Name | Twitter Handle | Email | Created | Updated |
|:-:|:-:|:-:|:-:|:-:|
| Alexander Rymdeko-Harvey | @Killswitch-GUI |  | 09/27/2017 | 09/27/2017 |

### Finding Sources
| URL | 
|:-:|
|  |
