---
layout: default
title: AWS Cloud Migration
---

# AWS Cloud Migration & Security Hardening
Simulated Case Study

## Executive Summary
This project involved migrating "FillerName," a medium-sized e-commerce company, from a legacy on-premises environment to a secure Amazon Web Services (AWS) infrastructure. The legacy system suffered from single points of failure, lack of scalability, and security vulnerabilities due to a flat network architecture.

**The Goal:** Transition from a Capital Expenditure (CapEx) model to an Operational Expenditure (OpEx) model while ensuring high availability and strictly enforced security controls.

---

## Architecture & Design
The new environment utilizes a **Virtual Private Cloud (VPC)** with a multi-tier subnet strategy to isolate sensitive data.

### Key Components
* **Compute:** EC2 instances running NGINX for the web application.
* **Database:** AWS RDS (MySQL) deployed in private subnets for isolation.
* **Scaling:** Auto Scaling Groups (ASG) and Application Load Balancers (ALB) to handle traffic spikes.
* **Content Delivery:** Amazon CloudFront and S3 for caching static assets.

![Network Diagram](../images/aws-network-diagram.png)
---

## Security Controls Implemented
To mitigate lateral movement and unauthorized access, I implemented a Defense-in-Depth strategy.

| Control | Implementation Details |
| :--- | :--- |
| **Network Segmentation** | Database resides in a private subnet with no direct internet access. |
| **Security Groups** | The database SG only accepts traffic from the Web Server SG on port 3306. |
| **Access Control** | SSH access is restricted strictly to the Admin VPN IP address. |

---

## Validation & Success Metrics
The new architecture was stress-tested against four key performance indicators (KPIs).

### 1. System Uptime (Availability)
* **Target:** 99.95% uptime.
* **Result:** **100% uptime** achieved during the 7-day test period with zero downtime recorded.

### 2. Auto-Scaling Efficiency
* **Scenario:** Simulated traffic spike causing CPU >60%.
* **Result:** New instances were provisioned and "InService" within **2 minutes and 45 seconds**, well under the 5-minute SLA.

### 3. Latency & Performance
* **Target:** Response time <500ms for 95% of requests.
* **Result:** 95% of requests were served within **320 milliseconds**.

### 4. Security Validation
* **Test:** Attempted 10 direct connections to the database from the public internet.
* **Result:** **100% of attempts failed** (Connection Timed Out), confirming the firewall rules were active.

---

## Cost-Benefit Analysis
Moving to the cloud eliminated the need for upfront hardware purchases ($5,000) in favor of a pay-as-you-go model.

| Category | Legacy (On-Prem) | AWS Cloud (OpEx) |
| :--- | :--- | :--- |
| **Availability** | Single Point of Failure (0
