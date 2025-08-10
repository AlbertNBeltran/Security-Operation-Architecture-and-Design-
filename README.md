# ⚙️🛠️ Security Operations Automation (Architecture and Design)
This project explains how to automate security operations and change management workflows by implementing security tools and intergrations via design and architectural principles.
### Why automate?
- By automating Tenable with Splunk and ServiceNow, you establish a seamless, end-to-end vulnerability management workflow. This integration allows Splunk to prioritize vulnerabilities based on risk, while ServiceNow automatically handles the remediation process by creating, assigning, and tracking tickets.
### What's the goal?
- The goal is to create an automated, closed-loop vulnerability management system that dramatically reduces the time it takes to identify, prioritize, and fix security vulnerabilities. This process streamlines the entire workflow, connecting vulnerability data to security analytics and the security operations team's workflow to ensure that critical issues are addressed quickly and efficiently.


## 🧠 How it works
<img width="20376" height="7516" alt="Diagram Security Operations" src="https://github.com/user-attachments/assets/858ce5c9-c8d9-4061-977f-6dd09f2e959e" />

## Objectives
1. 🔎 🎯 Discover, Inventory and scan assets for vulnerabilities using Tenable Vulnerability Management (Nessus)
2. 📥 📊 Aggregate vulnerability and asset data using SPLUNK (SIEM) to manipulate, create reports and generate trending dashboards
3. ⚙️ 🎟️ Automate ticket creation for critical vulnerabilities to streamline security operation tasks using ServiceNow (ITSM)  

## Tech Stack
- Tenable Vulnerability Management
- Splunk
- ServiceNow

## Tenable Vulnerability Management Setup
1. Login into Tenable VM cloud.tenable.com and create bi-weekly vulnerability scans against your assets in addition to any discovery scans.

<img width="500" height="500" alt="Pasted image 20250809205654" src="https://github.com/user-attachments/assets/87497ee4-29c6-4e92-91ff-dc998fa33b53" />
<img width="500" height="500" alt="Pasted image 20250809210002" src="https://github.com/user-attachments/assets/bc870362-9898-47f7-adf4-ded20358bfac" />

2. Create a service accont for the Splunk intergration and generate API keys in order to push data from TVM->Splunk.
<img width="500" height="500" alt="Pasted image 20250809210308" src="https://github.com/user-attachments/assets/3efe852d-ca24-49f8-ab00-8feb46e20dfb" />
<img width="500" height="500" alt="Pasted image 20250809210456" src="https://github.com/user-attachments/assets/44ec4547-e50f-41db-875f-f52498df5118" />

3. Document your API Access and Secret keys. 

## Splunk Setup 
<img width="800" height="600" alt="Pasted image 20250809113632" src="https://github.com/user-attachments/assets/e3a21609-76eb-430f-a283-c56d90fd160f" />



## ServiceNow Setup


> [!IMPORTANT]
> Key information users need to know to achieve their goal.

| Left-aligned | Center-aligned | Right-aligned |
| :---         |     :---:      |          ---: |
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |
