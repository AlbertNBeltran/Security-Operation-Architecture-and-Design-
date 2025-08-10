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
1. We will need to have deployed Nessus Scanners or Nessus Agents in order to inventory assets and prep them for credentialed vulnerability scanning.
- TVM Scanning guide: https://docs.tenable.com/vulnerability-management/Content/PDF/Tenable_Vulnerability_Management-User_Guide.pdf
<img width="800" height="600" alt="Pasted image 20250810003130" src="https://github.com/user-attachments/assets/2392bcb5-1296-4fc8-9b09-b707949f449b" />


2. Login into Tenable VM cloud.tenable.com and create bi-weekly vulnerability scans against your assets in addition to any discovery scans.
<img width="500" height="500" alt="Pasted image 20250810004219" src="https://github.com/user-attachments/assets/f2be5a10-153c-488d-a789-1e26b3c0b1ea" />
<img width="500" height="500" alt="Pasted image 20250809210002" src="https://github.com/user-attachments/assets/bc870362-9898-47f7-adf4-ded20358bfac" />

3. Create a service accont for the Splunk intergration and generate API keys in order to push data from TVM->Splunk.
<img width="500" height="500" alt="Pasted image 20250809210308" src="https://github.com/user-attachments/assets/3efe852d-ca24-49f8-ab00-8feb46e20dfb" />
<img width="500" height="500" alt="Pasted image 20250809210456" src="https://github.com/user-attachments/assets/44ec4547-e50f-41db-875f-f52498df5118" />

4. Document your API Access and Secret keys. 

## Splunk Setup 
1. We will be importing vulnerabilty data from TVM to Splunk in order to normalize and centralize the data.
- Splunk intergration guide: https://docs.tenable.com/integrations/Splunk/Content/PDF/Tenable_and_Splunk_Integration_Guide.pdf

<img width="800" height="600" alt="Pasted image 20250809113632" src="https://github.com/user-attachments/assets/e3a21609-76eb-430f-a283-c56d90fd160f" />

2. Signed up to Splunk Cloud
  > [!IMPORTANT]
  >Splunk Cloud can take a few hours to build and access.
<img width="500" height="500" alt="Pasted image 20250808004846" src="https://github.com/user-attachments/assets/90d899d3-6a82-492e-bcec-fa006cbba69a" />
<img width="500" height="500" alt="Pasted image 20250809112929" src="https://github.com/user-attachments/assets/4667295a-6499-48be-b377-77b2385015df" />

3. Install Tenable Add-on for Splunk and provide your TVM API keys to the addon configurtation.
<img width="5000" height="5000" alt="Pasted image 20250809115044" src="https://github.com/user-attachments/assets/b97c28bd-8657-4c86-95cc-40db35e731dd" />
<img width="5000" height="5000" alt="Pasted image 20250809130818" src="https://github.com/user-attachments/assets/87804962-8d04-4886-8c5c-4eb3a80fddb8" />
<img width="5000" height="5000" alt="Pasted image 20250809131022" src="https://github.com/user-attachments/assets/5a825309-b48c-4a56-aeea-1dc92295356a" />

4. Configure Tenable VM data inputs and establish import intervals.
<img width="5000" height="5000" alt="Pasted image 20250809132001" src="https://github.com/user-attachments/assets/a600b053-863e-44a6-b10f-32176003e1a8" />


5. Confirm vulnerability data is being imported
<img width="34520" height="18340" alt="Pasted image 20250809141454" src="https://github.com/user-attachments/assets/e933f9b2-204b-401a-a364-7da3d2d0b60a" />
<img width="34406" height="1844" alt="Pasted image 20250809140640" src="https://github.com/user-attachments/assets/f2e950e7-6d89-4eb5-b637-c7c92269de54" />

6. Download ```Tenable App for Splunk``` in order to view preconfigured templates for vulnerability trends, reporting and dashboards.
<img width="34540" height="18400" alt="Pasted image 20250809141753" src="https://github.com/user-attachments/assets/3fa85844-dc9e-4712-a1bd-52d7a7f7e200" />



## ServiceNow Setup
1. Splunk Cloud will be triggering alerts/incidents to ServiceNow which help maintain, assign and track vulnerability incidents for Security operation teams.
<img width="8000" height="6000" alt="Pasted image 20250809201701" src="https://github.com/user-attachments/assets/9dba46e2-3d29-4476-b97d-4c8dcbcbc80f" />
2. Created ServiceNow PDI Personal Developer Instance
  
3. <img width="400" height="400" alt="Pasted image 20250809152835" src="https://github.com/user-attachments/assets/65c52c05-de3b-4df8-b8c1-768adc932206" />
<img width="400" height="400" alt="Pasted image 20250809153333" src="https://github.com/user-attachments/assets/cf75e491-e0ac-4ce0-95cd-de5903a0f0d7" />

4. Download ``` Splunk add-on for ServiceNow ``` within Splunk Cloud.
<img width="500" height="500" alt="Pasted image 20250809152355" src="https://github.com/user-attachments/assets/82de39bd-a8f1-46c9-be2c-acf5be94f924" />
<img width="100000" height="100000" alt="Pasted image 20250809154213" src="https://github.com/user-attachments/assets/4a4ee95f-a2d3-4bb0-96ea-bc5ba7b9564b" />




 > [!IMPORTANT]
  >Ensure that you enable each individual input and add the Splunk account to the inputs as outlined here.

<img width="5000" height="5000" alt="Pasted image 20250809204137" src="https://github.com/user-attachments/assets/b9736b8a-d601-4876-81c8-0e5a888dd2c4" />


> [!IMPORTANT]
> Key information users need to know to achieve their goal.

| Left-aligned | Center-aligned | Right-aligned |
| :---         |     :---:      |          ---: |
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |
