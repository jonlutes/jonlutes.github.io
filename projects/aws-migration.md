---
layout: default
title: AWS Cloud Migration
---

# AWS Cloud Migration & Security Hardening

[**View Project Repository**](https://github.com/your-username/AWS-Cloud-Migration) *(Link this to your actual repo)*

## Executive Summary
[cite_start]This project involved migrating "FillerName," a medium-sized e-commerce company, from a legacy on-premises environment to a secure Amazon Web Services (AWS) infrastructure[cite: 17, 31]. [cite_start]The legacy system suffered from single points of failure, lack of scalability, and security vulnerabilities due to a flat network architecture[cite: 20, 22, 25].

[cite_start]**The Goal:** Transition from a Capital Expenditure (CapEx) model to an Operational Expenditure (OpEx) model while ensuring high availability and strictly enforced security controls[cite: 29, 40].

---

## Architecture & Design
[cite_start]The new environment utilizes a **Virtual Private Cloud (VPC)** with a multi-tier subnet strategy to isolate sensitive data[cite: 54].

### Key Components
* [cite_start]**Compute:** EC2 instances running NGINX for the web application[cite: 60].
* [cite_start]**Database:** AWS RDS (MySQL) deployed in private subnets for isolation[cite: 59].
* [cite_start]**Scaling:** Auto Scaling Groups (ASG) and Application Load Balancers (ALB) to handle traffic spikes[cite: 61].
* [cite_start]**Content Delivery:** Amazon CloudFront and S3 for caching static assets[cite: 62].

*(Place your Network Diagram image here: `![Network Diagram](../images/network-diagram.png)`)*

---

## Security Controls Implemented
[cite_start]To mitigate lateral movement and unauthorized access, I implemented a Defense-in-Depth strategy[cite: 26, 216].

| Control | Implementation Details |
| :--- | :--- |
| **Network Segmentation** | [cite_start]Database resides in a private subnet with no direct internet access[cite: 55]. |
| **Security Groups** | [cite_start]The database SG only accepts traffic from the Web Server SG on port 3306[cite: 229]. |
| **Access Control** | [cite_start]SSH access is restricted strictly to the Admin VPN IP address[cite: 228]. |

---

## Validation & Success Metrics
[cite_start]The new architecture was stress-tested against four key performance indicators (KPIs)[cite: 188].

### 1. System Uptime (Availability)
* **Target:** 99.95% uptime.
* [cite_start]**Result:** **100% uptime** achieved during the 7-day test period with zero downtime recorded[cite: 191, 192].

### 2. Auto-Scaling Efficiency
* **Scenario:** Simulated traffic spike causing CPU >60%.
* [cite_start]**Result:** New instances were provisioned and "InService" within **2 minutes and 45 seconds**, well under the 5-minute SLA[cite: 197, 199].

### 3. Latency & Performance
* **Target:** Response time <500ms for 95% of requests.
* [cite_start]**Result:** 95% of requests were served within **320 milliseconds**[cite: 201, 202].

### 4. Security Validation
* **Test:** Attempted 10 direct connections to the database from the public internet.
* [cite_start]**Result:** **100% of attempts failed** (Connection Timed Out), confirming the firewall rules were active[cite: 208].

---

## Cost-Benefit Analysis
[cite_start]Moving to the cloud eliminated the need for upfront hardware purchases ($5,000) in favor of a pay-as-you-go model[cite: 238].

| Category | Legacy (On-Prem) | AWS Cloud (OpEx) |
| :--- | :--- | :--- |
| **Availability** | Single Point of Failure (0% Redundancy) | [cite_start]High Availability (Multi-AZ) [cite: 238] |
| **Maintenance** | ~10 hours/month (Manual Patching) | [cite_start]~1 hour/month (Managed RDS) [cite: 238] |
| **Scalability** | Expensive (Requires new hardware) | [cite_start]Efficient (Pennies/hour for extra instances) [cite: 238] |

---

## Conclusion
The project successfully transformed a fragile, single-server environment into a resilient, auto-scaling cloud infrastructure. [cite_start]The migration not only resolved the immediate risks of downtime but also reduced the IT maintenance burden by leveraging managed services like RDS[cite: 211, 221].