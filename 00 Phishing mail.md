# Email Header Analysis - SOC Analyst Flowchart

## **Step 1: Initial Email Inspection**
- [ ] Examine email body for URLs or attachments.
- [ ] If found, test them in a **sandbox environment**:
  - [ ] VirusTotal
  - [ ] Urlscan.io
  - [ ] Palo Alto URL filtering
  - [ ] Whois domaintools
  - [ ] Haveibeenpwned
  - [ ] Inspect element of webpage -> Check network activity
  - [ ] Google Dorks
  - [ ] Browserling
  - [ ] E-discovery check for user click actions
- **Decision Point:** Are URLs or attachments malicious?
  - **Yes →** Report & escalate incident
  - **No →** Proceed to Step 2

## **Step 2: Email Header Analysis**
- [ ] Download the email in `.eml` format.
- [ ] Open the original message page.
- [ ] Use an email header analyzer tool (e.g., [MXToolbox](https://mxtoolbox.com/EmailHeaders.aspx)).
- **Check the following header authentication mechanisms:**
  - [ ] **SPF (Sender Policy Framework)**
    - Is SPF **PASS**?
    - Compare "Return-Path" and "From" domain.
    - If different → Possible spoofing.
  - [ ] **DKIM (DomainKeys Identified Mail)**
    - Compare "d=domain.com" with "From" field.
    - If different → DKIM Alignment **FAIL**.
    - Check DKIM Signature field (`b=...`), if not verified → Possible tampering.
  - [ ] **DMARC (Domain-based Message Authentication Reporting and Conformance)**
    - DMARC policy (`v=DMARC1; p=none/quarantine/reject`)
    - Check if SPF & DKIM results align with policy.
- **Decision Point:** Are SPF, DKIM, and DMARC valid?
  - **Yes →** Proceed to Step 3
  - **No →** Possible spoofing, report and escalate

## **Step 3: Analyze Spam and Bulk Scores (SCL & BCL)**
- [ ] **Spam Confidence Level (SCL):**
  - Higher SCL = More likely to be spam
  - Use mail flow rules to adjust SCL
- [ ] **Bulk Complaint Level (BCL):**
  - Higher BCL = Bulk email is likely spam
- **Decision Point:** Is the email legitimate?
  - **Yes →** Close investigation
  - **No →** Report and escalate as phishing/spam
