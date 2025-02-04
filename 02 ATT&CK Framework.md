# **🛡️ The ATT&CK Framework**

![MITRE ATT&CK](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExeXF5YzhhNndtNWx6MWU3dnE3NTZ2ZG8wc25xaTNtdDZ2ajVsbGx5bCZlcD12MV9zdGlja2Vyc19zZWFyY2gmY3Q9cw/4B1BTOMTi8b3OdPrzy/giphy.gif)

## **📖 Table of Contents**  
- [1️⃣ Introduction](#1️⃣-introduction)  
- [2️⃣ ATT&CK Matrices](#2️⃣-attck-matrices)  
- [3️⃣ What is TTP?](#3️⃣-what-is-ttp)  
- [4️⃣ Tactics](#4️⃣-tactics)  
- [5️⃣ Techniques & Sub-Techniques](#5️⃣-techniques--sub-techniques)  
- [6️⃣ Procedures](#6️⃣-procedures)  
- [7️⃣ Procedures vs. Sub-Techniques](#7️⃣-procedures-vs-sub-techniques)  
- [8️⃣ Data Sources & Mitigations](#8️⃣-data-sources--mitigations)  
- [9️⃣ Threat Intelligence](#9️⃣-threat-intelligence)  
- [📜 Glossary](#📜-glossary)  

---

## **1️⃣ Introduction**  
The **MITRE ATT&CK framework** is a globally recognized knowledge base of adversary tactics, techniques, and procedures (TTPs) used by cybercriminals and threat actors.  

### 🔥 **Why is ATT&CK Important?**  
✅ Helps security teams **understand cyber threats**.  
✅ Aids in **threat detection, response, and mitigation**.  
✅ Enhances **Cyber Threat Intelligence (CTI)**.  

---

## **2️⃣ ATT&CK Matrices**  
ATT&CK provides structured **matrices** to organize adversarial behaviors.  

### **📊 Types of Matrices**  
| Matrix       | Focus Area                              |
|-------------|--------------------------------------|
| **Enterprise** | Corporate networks & cloud environments |
| **Mobile**     | Mobile devices (iOS, Android) |
| **ICS**        | Industrial Control Systems (SCADA, PLCs) |

🔗 **[Learn More](https://attack.mitre.org/matrices/)**  

---

## **3️⃣ What is TTP?**  
**TTP = Tactics + Techniques + Procedures**  

```
🎯 Tactic (Why?) → 📌 Technique (How?) → 🔄 Procedure (Specific Steps)
```
🔹 **Tactics** are the **goals** of an attack (e.g., Initial Access).  
🔹 **Techniques** are **methods** used (e.g., Phishing).  
🔹 **Procedures** are **specific execution steps**.  

![TTP Flow](https://media.giphy.com/media/Nlt9hC0Rg91AFC19gR/giphy.gif?cid=ecf05e478n7vcxrmvvrjsl1nl0bslzg25tohpfbpicxewktq&ep=v1_gifs_search&rid=giphy.gif&ct=g)  

---

## **4️⃣ Tactics**  
Tactics represent **adversary goals**.  

### 🔥 **Common ATT&CK Tactics**  
| Tactic ID  | Name               | Description |
|------------|------------------|-------------------------|
| **TA0001** | Initial Access   | Gaining access to a system |
| **TA0004** | Privilege Escalation | Gaining higher privileges |
| **TA0007** | Discovery        | Gathering system info |

🔗 **[Full List of Tactics](https://attack.mitre.org/tactics/enterprise/)**  

---

## **5️⃣ Techniques & Sub-Techniques**  
Techniques describe **how** adversaries achieve their goals.  
🔹 Some techniques have **sub-techniques** (more specific variants).  

📌 **Example:**  
- **T1071 - Application Layer Protocol**  
  - **T1071.001 - Web Protocols**  
  - **T1071.002 - File Transfer Protocols**  

---

## **6️⃣ Procedures**  
Procedures are **real-world attack implementations** of techniques.  

📌 **Example:**  
- **APT29 (Russia-linked)** uses **T1071.001 - Web Protocols** to exfiltrate data.  
- **Lazarus Group (North Korea)** deploys **malware via T1566 - Phishing**.  

---

## **7️⃣ Procedures vs. Sub-Techniques**  

| **Procedures**  | **Sub-Techniques** |
|----------------|-------------------|
| Specific execution of techniques | Variations of techniques |
| Used by known threat groups | Predefined in ATT&CK framework |
| Change frequently | Defined by MITRE |

---

## **8️⃣ Data Sources & Mitigations**  

📌 **Data Sources:** Logs, sensors, and monitoring tools that help detect threats.  

| **Data Source** | **Example Technique** |
|----------------|----------------------|
| Active Directory | Credential Stealing (T1649) |
| Command Execution | Token Manipulation (T1134) |

📌 **Mitigations:** Defensive actions to prevent attacks.  

| **Mitigation** | **Example Use** |
|--------------|----------------|
| **M1041 - Encrypt Data** | Prevents Adversary-in-the-Middle attacks (T1557) |

🔗 **[Explore More](https://attack.mitre.org/data_sources/)**  

---

## **9️⃣ Threat Intelligence**  

### 🏴 **Threat Groups**  
ATT&CK tracks **threat actors** and their behaviors.  

📌 **Example:**  
| Group | Description |
|------|-------------|
| **APT28** | Russian cyber-espionage group |
| **Lazarus** | North Korean state-sponsored hackers |

### 🚀 **Campaigns**  
Campaigns are **specific attack operations**.  

📌 **Example: Operation Dust Storm**  
🔹 Targeted **Japan, South Korea, and the US**.  
🔹 Used **Android malware & phishing**.  

🔗 **[Campaign Database](https://attack.mitre.org/campaigns/)**  

---

## **📜 Glossary**  
| Term | Definition |
|------|-----------|
| **TTP** | Tactics, Techniques, and Procedures |
| **MITRE** | Nonprofit managing ATT&CK |
| **CTI** | Cyber Threat Intelligence |
| **APT** | Advanced Persistent Threat |
| **Adversary** | Threat actor or hacker |
| **Malware** | Malicious software |
| **Exploit** | Code used to take advantage of vulnerabilities |

---

## **🎯 Final Thoughts**  
The **MITRE ATT&CK Framework** is a powerful tool for **understanding cyber threats** and improving **defensive strategies**.  

✅ **Stay Updated**: ATT&CK is constantly evolving.  
✅ **Use ATT&CK for Defense**: Map threats and strengthen security.  
✅ **Learn from Attacks**: Study real-world adversary techniques.  

> 🔗 **Explore the ATT&CK Framework** 👉 [MITRE ATT&CK](https://attack.mitre.org/)    
