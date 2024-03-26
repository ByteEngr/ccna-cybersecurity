## CCNA Cybersecurity – Operations Focused Labs

This repository provides a 50 lab, hands on curriculum that follows the Cisco Cybersecurity Operations Fundamentals domains.  
Every lab is scenario driven and focuses on investigation, analysis, and response rather than theory summaries.

### Curriculum Domains and Folders

1. **Security Operations Center** – SOC workflows and triage  
   - [`01-security-operations-center`](./01-security-operations-center/)
2. **Endpoint Security** – host level controls and telemetry  
   - [`02-endpoint-security`](./02-endpoint-security/)
3. **Network Security** – perimeter, internal segmentation, and traffic visibility  
   - [`03-network-security`](./03-network-security/)
4. **Data Security** – data exposure, DLP signals, and sensitive asset monitoring  
   - [`04-data-security`](./04-data-security/)
5. **Cloud Security** – SaaS and IaaS misconfigurations and cloud logs  
   - [`05-cloud-security`](./05-cloud-security/)
6. **Threat Analysis** – hunting, enrichment, and pattern recognition  
   - [`06-threat-analysis`](./06-threat-analysis/)
7. **Threat Investigation and Response** – end to end cases and playbooks  
   - [`07-threat-investigation-response`](./07-threat-investigation-response/)
8. **Capstone** – multi domain incident simulations  
   - [`08-capstone`](./08-capstone/)

### Cisco Learning companion topics – extras

If you are taking **Understanding Cisco Cybersecurity Operations Fundamentals** (for example to prepare for **200-201** and the **CCNA Cybersecurity** certification), the official course is organised into modules with named lessons. Those lessons are **concept and foundation** material (videos, knowledge checks). This repository is **hands-on lab practice** and does not replace that course.

Use the table below as **extras**: pair each official course lesson with the matching lab folder for practice after you study the topic. A few examples you asked to highlight:

- **Understanding Windows Operating System Basics** → study alongside **[`02-endpoint-security`](./02-endpoint-security/)** (Windows process, filesystem, and endpoint telemetry ideas show up in the endpoint labs).
- **Understanding Basic Cryptography Concepts** → study alongside **[`04-data-security`](./04-data-security/)** (encryption, hashing, and data protection tie to data classification and exfiltration scenarios).

| Course module | Example official lesson titles (extras to pair with labs) | Practice in this repo |
|------------------|-------------------------------------------------------------|------------------------|
| Module 1 – Security Operations Center | Defining the Security Operations Center; Understanding SOC Metrics; Understanding SOC Workflow and Automation | [`01-security-operations-center`](./01-security-operations-center/) |
| Module 2 – Endpoint Security | **Understanding Windows Operating System Basics**; Understanding Linux Operating System Basics; Understanding Endpoint Security Technologies | [`02-endpoint-security`](./02-endpoint-security/) |
| Module 3 – Network Security | Understanding Network Infrastructure and Network Security Monitoring Tools; Understanding Common TCP/IP Attacks | [`03-network-security`](./03-network-security/) |
| Module 4 – Data Security | Exploring Data Type Categories; **Understanding Basic Cryptography Concepts** | [`04-data-security`](./04-data-security/) |
| Module 5 – Cloud Security | Cloud Security Fundamentals; Securing Cloud Deployments | [`05-cloud-security`](./05-cloud-security/) |
| Module 6 – Threat Analysis | Understanding Incident Analysis in a Threat-Centric SOC; Identifying Common Attack Vectors; Identifying Malicious Activity; Identifying Patterns of Suspicious Behavior | [`06-threat-analysis`](./06-threat-analysis/) |
| Module 7 – Threat Investigation and Response | Identifying Resources for Hunting Cyber Threats; Understanding Event Correlation and Normalization; Conducting Security Incident Investigations; Using a Playbook Model to Organize Security Monitoring; Describing Incident Response | [`07-threat-investigation-response`](./07-threat-investigation-response/) |

**Capstone labs** [`08-capstone`](./08-capstone/) combine skills from multiple modules; complete them after you are comfortable with Modules 1–7.

Lesson titles and module runtimes in official course materials may change; treat this table as a **study map**, not a legal copy of Cisco’s catalog.

---

## Lab Distribution and Progression

Labs are numbered globally from **01 to 50** and spread across the domains to give you a clear path from beginner to advanced:

- **Labs 01 to 08** – Security Operations Center  
  Tier 1 alert triage, ticketing, queue management, and basic correlation.
- **Labs 09 to 16** – Endpoint Security  
  Malware and PUA activity, persistence mechanisms, and EDR or endpoint telemetry.
- **Labs 17 to 24** – Network Security  
  Perimeter alerts, internal lateral movement, and basic segmentation analysis.
- **Labs 25 to 30** – Data Security  
  Data exfiltration patterns, DLP style signals, and sensitive asset misuse.
- **Labs 31 to 36** – Cloud Security  
  Misconfigurations, credential abuse, and cloud audit log analysis.
- **Labs 37 to 42** – Threat Analysis  
  Campaign tracking, IOC clustering, enrichment, and pattern building.
- **Labs 43 to 48** – Threat Investigation and Response  
  Case based investigations and playbook style response design.
- **Labs 49 to 50** – Capstone  
  Multi stage, multi domain incidents that bring all earlier skills together.

Complexity progresses from:

- **Early labs** – tightly scoped investigations that use a single primary data source.  
- **Middle labs** – correlation across multiple tools and log types.  
- **Later labs and capstones** – end to end intrusions, multi stage campaigns, and coordinated response.

---

## Lab Structure

Each lab has its own folder, for example:

- `01-security-operations-center/lab-01/`
- `02-endpoint-security/lab-09/`
- `08-capstone/lab-50/`

Inside each `lab-XX` folder you will find a single documentation file named `README.md` with these sections:

- **Scenario** – short story that sets the context, environment, and triggering event.
- **Investigation Objectives** – specific goals you must achieve as the analyst.
- **Logs/Artifacts Description** – what data is available, such as SIEM alerts, EDR events, packet captures, proxy logs, email headers, or cloud audit logs.
- **Tasks** – concrete investigative steps to follow with those artifacts.
- **Questions** – key questions you should be able to answer from your investigation.
- **Indicators of Compromise** – IOCs you should identify and document, such as IPs, domains, file hashes, process names, or accounts.
- **Expected Analyst Outcome** – what a successful junior analyst would hand back as findings, decisions, and next actions.

Labs are intentionally light on theory. The focus is on hands on investigation and reasoning with realistic style artifacts.

---

## How to Use This Repository

### For learners

- Work through the labs roughly in order to get a smooth increase in difficulty.
- For each lab:
  - Read the **Scenario** and **Investigation Objectives** to understand what is happening and what you are expected to achieve.
  - Use the **Logs/Artifacts Description** to load or approximate similar data in your own tools, such as a SIEM, an EDR console, or a packet analyzer.
  - Follow the **Tasks** list and answer every **Question** as if you were working a real SOC ticket.
  - Write down the **Indicators of Compromise** you find and summarise the case using the **Expected Analyst Outcome** section as a template.

### For instructors and academies

- Treat each `lab-XX` folder as a reusable exercise blueprint.
- Attach your own sample data next to the `README.md` file, for example:
  - Packet captures (`.pcap`)
  - CSV or JSON exports of logs
  - Screenshots of SIEM or EDR consoles
- Use the **Questions** and **Expected Analyst Outcome** sections to build grading rubrics, discussion prompts, and debrief sessions.

### For SOC teams

- Map each scenario onto your own tools and workflows, for example Splunk, QRadar, Elastic, SecureX, Defender, or any other platform you use.
- Use the labs for:
  - Onboarding new analysts
  - Cross training between Tier 1 and Tier 2
  - Tabletop exercises and purple team style drills

---

## Project Status and Contributions

This repository is ready for use as a practice lab set for the CCNA Cybersecurity pathway.

If you plan to adapt or extend these labs:

- Add your own sample data inside each `lab-XX` folder so that learners can work with real artifacts.
- Keep the existing lab structure and section names to stay consistent and easy to follow.
- If you share your version publicly, consider adding a `LICENSE` file and a short `CONTRIBUTING.md` to explain how others can reuse or improve the material.