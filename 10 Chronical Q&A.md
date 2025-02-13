# 📝 Google Chronicle Training – Q&A Session

Q&A session based on what I learned during my Google Chronicle training as a junior SOC analyst. This section will help reinforce the key concepts in an interactive way. Use this as a self-learning and testing tool.

---

## 🧐 Questions and Answers

### **Section 1: Short Answers**

**Q1. What is the purpose of the UI timeline in Google Chronicle?**  
**A:** The UI timeline ensures that the log timestamps match your local time zone (e.g., Sri Lanka time). Always adjust the timeline for accuracy.

---

**Q2. What are the five parts of a log in Google Chronicle?**  
**A:**  
1. **Metadata**: Timestamp, product details.  
2. **Event**: Inbound/outbound info, IP details.  
3. **Outcome**: Severity (High, Medium, Low).  
4. **Condition**: Trigger details.  
5. **Patch**: Records of similar incidents.

---

**Q3. Where should a Web Application Firewall (WAF) be placed in a bank’s network?**  
**A:** It should be placed **inside the DMZ** or on the line **coming out of the DMZ**.

---

**Q4. How often should you check the Rule Dashboard?**  
**A:** Every **30 minutes** to monitor rule triggers and identify anomalies.

---

**Q5. What are two additional tools used by the bank for security?**  
**A:**  
1. **IZO** for monitoring misuse of the bank’s name on social media.  
2. **FortiReason** for detecting and blocking leaked credit card or online banking information.

---

### **Section 2: Matching Questions**

**Q6. Match the following tools to their primary function:**

| **Tool**            | **Function**                                                  |
|----------------------|--------------------------------------------------------------|
| A. Rule Dashboard    | 1. Displays compromised cases from threat intelligence.      |
| B. IOC Dashboard     | 2. Monitors rule trigger frequency and graph patterns.       |
| C. IZO              | 3. Social media brand monitoring.                            |
| D. FortiReason      | 4. Detects and blocks leaked credit card details.            |

**Answer:**  
- A → 2  
- B → 1  
- C → 3  
- D → 4  

---

### **Section 3: Paragraph or Longer Answers**

**Q7. Explain the process of vulnerability investigation in Google Chronicle.**  
**A:**  
1. Start by searching the **vulnerability name** in the search field.  
2. Review the rules that address the vulnerability.  
3. Examine both **allowed and blocked traffic**, focusing on allowed ones, as blocked events are already mitigated.  
4. Use filters like “show only commands” to refine your search.  
5. Begin your investigation with allowed packets to identify potential threats.

---

**Q8. Why is the IOC (Indicator of Compromise) Dashboard referred to as the "diamond cave"?**  
**A:**  
The IOC Dashboard integrates threat intelligence and highlights compromised cases. It’s called the "diamond cave" because it provides the most valuable cases to investigate further. It helps SOC analysts identify traffic events or incidents that may have passed undetected, excluding already blocked ones.

---

**Q9. Describe the difference between queue-related rules and custom rules.**  
**A:**  
- **Queue-Related Rules**: Designed by Google engineers, these are complex and have a high chance (75% or more) of indicating a threat. Analysts must investigate them thoroughly.  
- **Custom Rules**: These are simpler, shorter, and created internally by the team. They handle specific organizational needs.  

---

### **Section 4: Multiple Choice Questions (MCQs)**

**Q10. What does the Rule Dashboard NOT show?**  
- A. Rule trigger count.  
- B. Alert graphs.  
- C. Raw logs directly.  
- D. Enabled rules with alerting off.  

**Answer:**  
**C. Raw logs directly.**  
*(Raw logs can only be viewed after clicking into detailed events from the Rule Dashboard.)*

---

**Q11. How can you search raw logs in Google Chronicle?**  
- A. Use UDM field searches only.  
- B. Use Legacy Search and locate raw log data.  
- C. Go to the IOC Dashboard.  
- D. Only queue-related rules can be searched.  

**Answer:**  
**B. Use Legacy Search and locate raw log data.**

---

**Q12. Which of the following is NOT a part of a log structure?**  
- A. Metadata.  
- B. Patch.  
- C. Authentication Details.  
- D. Outcome.  

**Answer:**  
**C. Authentication Details.**

---

**Q13. What is the first step in handling a case in Google Chronicle?**  
- A. Assign the case to the admin.  
- B. Investigate the case immediately.  
- C. Take screenshots and document findings.  
- D. Check the IOC Dashboard for similar cases.  

**Answer:**  
**C. Take screenshots and document findings.**

---

**Q14. What does IZO specifically monitor?**  
- A. Network traffic between firewalls.  
- B. Leaks of credit card data.  
- C. Social media misuse of the bank's brand.  
- D. Threat intelligence feeds.  

**Answer:**  
**C. Social media misuse of the bank's brand.**

---

**Q15. Which graph pattern on the Rule Dashboard indicates a repeating pattern?**  
- A. A constantly flat graph.  
- B. A sharply spiking graph.  
- C. A randomly fluctuating graph.  
- D. A completely blank graph.  

**Answer:**  
**A. A constantly flat graph.**

---

### **Section 5: True/False Questions**

**Q16. Google Chronicle can only analyze raw logs after converting them into UDM fields.**  
**A:** **False.** (You can use Legacy Search to analyze raw logs directly.)  

---

**Q17. IOC Dashboard focuses on analyzing newly discovered threats only.**  
**A:** **False.** (It also focuses on compromised items that were identified using threat intelligence.)  

---

**Q18. Queue-related rules are simpler than custom rules.**  
**A:** **False.** (Queue-related rules are more complex and designed by Google engineers.)  

---

### **Bonus: Fun GIF Reminder**  

> ![WAF Server GIF](https://media.giphy.com/media/7JjtaDlLiATz2UnfsU/giphy.gif?cid=ecf05e47v1z9lk94zfs4nyuvbp8bmj9p9ar78pph597krp4p&ep=v1_gifs_search&rid=giphy.gif&ct=g)  
> *Always remember to correctly place the WAF inside or coming out of the DMZ!*

---

## Author Mojii's note
This Q&A sheet covers all the important concepts we discussed during the training session, from the processes to the key points. Use this as a tool to revise your knowledge and sharpen your SOC analysis skills. Keep practicing, and let’s secure those networks like pros! 🔐
