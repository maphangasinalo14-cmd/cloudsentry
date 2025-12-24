# CloudSentry: Automated Cloud Infrastructure Monitor

![Cloud](https://img.shields.io/badge/Cloud-AWS%2FAzure-orange) ![Status](https://img.shields.io/badge/Status-Active-green) ![Python](https://img.shields.io/badge/Built%20With-Python-blue) ![License](https://img.shields.io/badge/license-MIT-lightgrey)

> **A lightweight, real-time security bot that continuously scans cloud infrastructure for misconfigurations, open ports, and unauthorized access attempts.**

## ⚠️ The Problem
Cloud environments drift. A developer might open a port for testing and forget to close it, or an S3 bucket might be accidentally set to "Public." These simple misconfigurations are the #1 cause of cloud data breaches.

## 🛡️ The Solution: CloudSentry
CloudSentry is an automated watchdog. It runs on a schedule (or as a Lambda function) to audit your infrastructure against a set of security baselines. If a violation is detected, it instantly alerts the security team via Slack/Discord.

### Key Features
* [cite_start]**Port Scanning:** Automatically identifies high-risk open ports (SSH 22, RDP 3389, Database 5432) exposed to the public internet[cite: 84].
* [cite_start]**Storage Auditing:** Scans AWS S3 Buckets and Azure Blobs to ensure they are not publicly readable or writable[cite: 84].
* **IAM Surveillance:** Flags user accounts with excessive permissions (e.g., AdministratorAccess) or lack of MFA usage.
* [cite_start]**Instant Alerting:** Delivers real-time notifications with remediation steps directly to your chat ops channels[cite: 85].

## 🛠️ Tech Stack
* **Engine:** Python 3.10+
* **Cloud SDKs:** Boto3 (AWS), Azure Identity
* **Notifications:** Slack Webhook API / SMTP
* **Deployment:** Docker / AWS Lambda / Cron

## 🚀 Quick Start

### Prerequisites
* Python 3.8+
* Valid Cloud Credentials (AWS Access Keys or Azure Service Principal)

### 1. Installation
Clone the repo and install dependencies:
```bash
git clone [https://github.com/YourUsername/CloudSentry.git](https://github.com/YourUsername/CloudSentry.git)
cd CloudSentry
pip install -r requirements.txt
