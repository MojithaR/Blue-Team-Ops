# SOC Analyst Notes: Wing Bank Monitoring with FortiSIEM  

### **Table of Contents**  
1. [Introduction to Wing Bank Monitoring](#introduction-to-wing-bank-monitoring)  
2. [Priority Levels and Incident Closure Status](#priority-levels-and-incident-closure-status)  
3. [Incident Follow-Up Procedure](#incident-follow-up-procedure)  
4. [FortiSIEM Overview and Use Case Management](#fortisiem-overview-and-use-case-management)  
5. [Performance Logs vs. True Logs](#performance-logs-vs-true-logs)  
6. [Scenario: Monitoring Pending and Decommissioned Devices](#scenario-monitoring-pending-and-decommissioned-devices)  
7. [System Event Categories](#system-event-categories)

---

## **Introduction to Wing Bank Monitoring**  
Wing Bank (VING BANK) is monitored using **EDR (CrowdStrike)** and **FortiSIEM** tools. Key responsibilities include:  
- Event detection and reporting.  
- Escalating incidents and following up until closure.  
- Prioritizing and categorizing incidents based on their impact on business operations.  

---

## **Priority Levels and Incident Closure Status**

### **Priority Levels**  
| **Priority** | **Response Time** | **Closure Requirement**       |  
|--------------|-------------------|-------------------------------|  
| **P1**       | 15 minutes        | Close as **True Positive**    |  
| **P2**       | 30 minutes        | Close as **True Positive**    |  
| **P3**       | 45 minutes        | Close as **Legit**            |  
| **P4**       | 60 minutes        | Close as **Legit**            |  

### **Incident Closure Status**  
1. **True Positive**:  
   - Actual impact on business detected.  
   - Example: A legitimate threat confirmed by SOC analysis.  

2. **Legit**:  
   - Activity performed by an authorized person or known entity.  
   - Example: Authorized logins or maintenance events.  

3. **False Positive**:  
   - Incorrectly flagged cases that are not threats.  

---

## **Incident Follow-Up Procedure**  
When an incident is escalated to the Wing Bank security team:  
1. **Escalate and Notify** via email.  
2. Wait for an **Acknowledgement Email** from the Wing Bank team.  
3. Follow up until receiving a **Case Closure Email**.  
4. If no closure email is received:  
   - Send **Reminder Emails** based on priority levels:  
     - **P1**: Every **1 hour**.  
     - **P2**: Every **2 hours**.  
     - **P3 & P4**: Every **8 hours**.  

---

## **FortiSIEM Overview and Use Case Management**

### **Use Case Management**  
1. **Use Case Onboarding**:  
   - Creation of new rules or use cases to meet specific security requirements.  

2. **Use Case Offboarding**:  
   - Removal or unlisting of outdated or unnecessary use cases to prevent excessive alerts.  

3. **Use Case Fine-Tuning**:  
   - Customizing default use cases or creating new ones by editing rules and logic.  
   - Continuous process to achieve optimal results.  

---

## **Performance Logs vs. True Logs**

| **Type of Log**       | **Description**                                                                 | **Example**                  |  
|-----------------------|-------------------------------------------------------------------------------|-----------------------------|  
| **Performance Logs**  | System-generated logs showing device health and performance metrics.         | CPU usage, memory status.   |  
| **True Logs**         | Active logs reflecting actual network activity and traffic.                  | Firewall alerts, WAF logs.  |  

### **Key Notes**  
- Only **Approved Devices** are primarily monitored.  
- Logs from **Pending** or **Decommissioned Devices** are checked only when necessary.  

---

## **Scenario: Monitoring Pending and Decommissioned Devices**  
If an ATM or CRM machine goes down:  
1. SOC Analyst is the **first responder**.  
2. Investigate the machine's status in FortiSIEM **CMDB**:  
   - **Approved**: Actively monitor and analyze.  
   - **Pending/Decommissioned**: Initially dismiss, unless relevant to the case.  

3. Identify the device IP and perform analysis.  

---

## **System Event Categories**  
System event categories (0–7) help classify logs received in FortiSIEM:  

| **Category Code** | **Event Type**            | **Description**                              |  
|-------------------|--------------------------|----------------------------------------------|  
| 0                 | `PH_INIT`                | Initialization events.                       |  
| 1                 | `PH_SESSION`             | Session-related events.                      |  
| 2                 | `PH_ALERT`               | Alert or threat logs.                        |  
| 3                 | `PH_DEV_MON`             | Device performance monitoring logs.          |  
| 4                 | `PH_RULE_MATCH`          | Logs matching active rules or use cases.     |  
| 5                 | `PH_USER_ACTIVITY`       | Logs of user actions or logins.              |  
| 6                 | `PH_SYS_LOG`             | System performance and operation logs.       |  
| 7                 | `PH_NETWORK_TRAFFIC`     | Logs of network activity and traffic.        |  

---

## **Dashboard and EPS Monitoring**

### **Dashboard Overview**  
1. **Event Per Second (EPS) Graph**:  
   - Displays real-time log traffic received from devices.  
   - Normal EPS Range for Wing Bank: **12K–16K**.  

2. **Analyzing EPS Peaks**:  
   - If EPS exceeds or falls below the normal range, investigate:  
     1. Check the **Reporting Device List**.  
     2. Identify the **IP Address** of the suspicious device.  

### **Key Actions**  
- For unexpected peaks, analyze devices not usually on the **Reporting Device List**.  
- Focus on device performance and active traffic logs for investigation.

---

## **CMDB Overview**  
The **CMDB (Configuration Management Database)** stores all devices, rules, and user information.  

### **Wing Bank CMDB**  
| **Device Type**     | **Count**         |  
|---------------------|------------------|  
| Linux Servers       | 4                |  
| UNIX Systems (ATMs) | 531              |  

### **Device States**  
1. **Approved**: Communication and log flow approved.  
2. **Pending**: Connection approved, but logs not yet received.  
3. **Decommissioned**: Communication ended, but logs may still appear (performance logs).  

---

## **Additional Notes**
- **Log into FortiSIEM** using credentials from **Bitwarden** (password management system).  
- Union Bank operates on the latest FortiSIEM version, differing from Wing Bank.  

