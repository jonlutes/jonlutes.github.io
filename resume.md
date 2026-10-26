---
layout: default
title: Resume
---

# Resume
**Jonathon Lutes** | Bountiful, UT  
[LinkedIn](https://www.linkedin.com/in/jonlutes/) | [Credly](https://www.credly.com/users/jonlutes)

## Summary
I am an early-career cybersecurity analyst with an M.S. in Cybersecurity and Information Assurance and the Security+, CySA+, PenTest+, and SSCP certifications. In two capstone projects, I designed a Splunk Cloud SIEM with MITRE ATT&CK-mapped detections for a PCI DSS-scoped fintech and built a multi-AZ AWS environment with network segmentation and CloudWatch monitoring. I bring 10+ years of customer-facing technical support experience, including triaging **485 SaaS tickets per month**, writing escalation documentation, and maintaining a **97.8% QA score**.

## Education
### Western Governors University — Millcreek, Utah
#### Master of Science, Cybersecurity and Information Assurance
**Feb 2026 - Oct 2026**  
* Focus on **cyber defense**, **cloud security**, and **GRC**.

#### Bachelor of Science, Cybersecurity and Information Assurance
**Dec 2022 - Dec 2025**  
* **NSA Validated Program of Study**: the program is designated a National Security Agency Center of Academic Excellence (NSA CAE).
* Coursework in **incident response**, **firewall configuration**, **event logging**, **AWS** and **VMware**, **network infrastructure**, and **Python/SQL/PowerShell automation**.

## Certifications
[**CompTIA PenTest+**](https://www.credly.com/badges/c57b0bc4-2687-4b15-8ed8-bdb2c6e17b72/public_url)  
[**CompTIA CySA+**](https://www.credly.com/badges/1b4ac475-e3af-4387-9ed1-48c2f516be13/public_url)  
[**CompTIA Project+**](https://www.credly.com/badges/dec73dc9-e66b-4794-ba7a-287feb717c58/public_url)  
[**CompTIA A+**](https://www.credly.com/badges/2607221e-08be-46f7-84db-63fc156140e4/public_url)  
[**CompTIA Network+**](https://www.credly.com/badges/f4d762dc-7169-4aaa-9038-2a72ed6492ee/public_url)  
[**CompTIA Security+**](https://www.credly.com/badges/90705896-79c8-4b2b-978b-b9defebaf1ad)  
[**ISC2 Systems Security Certified Practitioner (SSCP)**](https://www.credly.com/badges/e561d32f-4b57-488d-b29e-5a50b8d9bef2/public_url)  
[**LPI Linux Essentials**](https://www.credly.com/badges/3a5095a3-d76e-4762-b5cf-4d3cc6e6519b/public_url)  
[**Evolve Security Certified Professional**](https://www.credly.com/badges/507cc4bd-ae48-4a28-b6eb-b6c35911c99c/public_url)  
[**ITIL V4 Foundations**](https://drive.google.com/file/d/1IcWcVFRc2Wi-5zr8VTEt7g5k-PIkz0Zz/view?usp=share_link) (expired)

## Skills
**Security:** MITRE ATT&CK, incident response, vulnerability assessment, OSINT, firewall configuration, event logging  
**Frameworks and Compliance:** NIST CSF 2.0, NIST framework assessments, PCI DSS v4.0.1  
**Cloud:** AWS (VPC, EC2, RDS, S3, CloudFront, CloudWatch, Application Load Balancer, Auto Scaling, security groups), VMware  
**Systems:** Active Directory, Microsoft Configuration Manager, Windows 10/11, Linux, NGINX  
**Scripting:** Python, SQL, PowerShell  
**Tools:** Salesforce, ticketing and escalation workflows  

## Work History
### Technical Support Specialist (Tier 1, Remote) — iPipeline
**May 2026 - Present**  
* Resolve an average of **485 SaaS support tickets per month** for life insurance and financial services clients, triaging and tracking cases in **Salesforce**.
* Earned a **97.8% QA score** (58.7/60, rated Exceeds Expectations) while diagnosing browser, operating system, and authorization errors with backend administrative tools.
* Document complex issues for **engineering escalation** and coach clients on using new software platforms.

### LLM Training Specialist (Contract, project-based) — Handshake AI
**Oct 2025 - Present**  
* Evaluate and rank large language model outputs against project guidelines, with attention to accuracy and quality.
* Write prompts and structured written feedback used to improve model responses.

### Configuration Technician — Future Tech Enterprise
**Apr 2024 - Jun 2025**  
* **Diagnosed and resolved hardware and firmware issues** in non-operational enterprise **Windows 10/11** laptops and desktops, and **coordinated with vendors** to order and install the necessary parts.
* Managed users and machines using **Active Directory** and **Microsoft Configuration Manager (MCM)**.
* Installed operating systems, software packages, and hardware to ensure optimal system performance.

### Logistics Associate — United Parcel Service
**Nov 2023 - May 2026**  
* Maintained safety and procedural compliance while meeting daily deadlines in a **zero-error environment**.

### Technical Support Specialist — Podium
**Mar 2022 - Dec 2022**  
* Delivered **technical and general SaaS support** to small businesses using **Salesforce ticketing**, resolving issues across multiple products and driving product adoption.

### Earlier Experience, 2015 to 2022
Captioning Agent, CaptionCall (2020 - 2022); Customer Advocate and Account Specialist, Tesani Companies (2017 - 2019); additional technical support and customer service roles (2015 - 2017). Full history is on [LinkedIn](https://www.linkedin.com/in/jonlutes/).

## Projects
### [SIEM Design for a PCI DSS-Scoped Fintech](./projects/siem-implementation)
*M.S. Capstone, simulated environment*
* Designed a centralized **Splunk Cloud SIEM** for a simulated 475-employee fintech. The design consolidates logs from **8 disconnected security tools** (Palo Alto NGFW, CrowdStrike Falcon, Active Directory, Proofpoint, Qualys, Imperva, Veeam, Azure Monitor) across four network segments, including a cardholder data environment.
* Designed a correlation rule library of **10+ detections mapped to MITRE ATT&CK** and the **NIST CSF 2.0** Detect function. Added four end-to-end test scenarios (credential compromise with lateral movement, unauthorized CDE access, log tampering, multi-source correlation) with a false-positive ceiling of **under 5%**.
* Mapped four **PCI DSS v4.0.1 Requirement 10** audit findings to policies for scheduled log review, retention, log integrity, and automated CDE access alerting.
* Built a cost-benefit analysis projecting about **$230,000 per year** in reclaimed analyst time against a first-year cost of about **$59,800** (licensing, implementation, and certification exams). Modeled the outcomes in a post-implementation report: **MTTD from 9.5 to 1.5 hours** and **MTTR from 17 to 4 hours**.
* Defined role-based training plans (Splunk Core Certified User and Power User paths), an incident response runbook, and a PCI DSS reporting template as project deliverables.

### [Secure, Highly Available AWS Migration](./projects/aws-migration)
*B.S. Capstone, live AWS environment, synthetic dataset*
* Designed and built a **multi-AZ AWS environment** to migrate a WordPress/WooCommerce application and MySQL database off a single on-premises server. The environment uses a custom VPC with public and private subnets, an Application Load Balancer, an Auto Scaling Group, and EC2 instances running NGINX.
* Segmented the network so the Multi-AZ RDS MySQL database sat in private subnets and accepted traffic only from the web tier, with SSH limited to a single admin address. Confirmed enforcement: **10 of 10** connection attempts to the database from the public internet failed.
* Validated against pre-defined success metrics using CloudWatch:
  * **100% uptime** over a 7-day test (target 99.95%)
  * **95% of requests in under 320 ms** over 24 hours (target 500 ms)
  * A new instance in service **2 minutes 45 seconds** after a load-triggered CPU spike (target under 5 minutes)
* Offloaded static assets to S3 with CloudFront caching, and completed a cost-benefit analysis comparing the on-premises CapEx model to AWS OpEx.

## [Home](/)
