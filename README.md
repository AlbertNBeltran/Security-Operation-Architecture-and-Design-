<picture>
    <img width="3000" height="500" alt="Image" align="left" src="https://github.com/AlbertNBeltran/AlbertNBeltran/blob/main/Gemini_Generated_Image_mfys5rmfys5rmfys.png" /> 
 
</picture>

<div align="center">

  # ⚙️🛠️ Automating Security Operations  

This project explains how to automate Vulnerability Management with security operations and change management workflows by implementing security tools and intergrations using design and architectural principles.

</div>

## Why automate?

- By automating Tenable with Splunk and ServiceNow, you establish a seamless, end-to-end vulnerability management workflow.
- This integration allows Splunk to prioritize vulnerabilities based on risk, while ServiceNow automatically handles the remediation process by creating, assigning, and tracking tickets.
  
## What's the goal?

- The goal is to create an automated, closed-loop vulnerability management system that dramatically reduces the time it takes to identify, prioritize, and fix security vulnerabilities.
- This process streamlines the entire workflow, connecting vulnerability data to security analytics and the security operations team's workflow to ensure that critical issues are addressed quickly and efficiently.

## 🧠 How does it work?
<div align="center">
<img  src="https://readme-typing-svg.herokuapp.com?color=45ffaa&center=true&vCenter=true&size=40&width=900&height=80&lines=Design+->+Create+->+Automate"/>
</div>

<img width="20376" height="7516" alt="Diagram Security Operations" src="https://github.com/user-attachments/assets/858ce5c9-c8d9-4061-977f-6dd09f2e959e" />

## ✅ Objectives
1. 🔎 🎯 Discover, Inventory and scan assets for vulnerabilities using Tenable Vulnerability Management (Nessus)
2. 📥 📊 Aggregate vulnerability and asset data using SPLUNK (SIEM) to manipulate, create reports and generate trending dashboards
3. ⚙️ 🎟️ Automate ticket creation for critical vulnerabilities to streamline security operation tasks using ServiceNow (ITSM)  

## 📋 Tech Stack

| Software     | Version |
| ---      | ---       |
| [Tenable Vulnerability Management](https://docs.tenable.com/release-notes/Content/vulnerability-management/2025.htm)  | io Cloud |
| [Splunk Cloud Platform](https://www.splunk.com/en_us/download.html?_gl=1*1ag37oo*_gcl_au*MTE0MTg3NzU1MS4xNzU0NDU2NDY5LjY5MTMzNzI1MS4xNzU0NzYzODYxLjE3NTQ3NjM4Njg.*FPAU*MTE0MTg3NzU1MS4xNzU0NDU2NDY5*_ga*MTkwMDI4NzUxMS4xNzU0NDU2NDY5*_ga_5EPM2P39FV*czE3NTQ3OTUwNDYkbzckZzEkdDE3NTQ3OTUwNjYkajQwJGwwJGgxMTU3MTI0Mjcx)    |  Cloud Platform |
| [ServiceNow PDI Instance](https://developer.servicenow.com/dev.do#!/learn/learning-plans/washingtondc/new_to_servicenow/app_store_learnv2_buildmyfirstapp_washingtondc_personal_developer_instances)  | Developer Cloud Platform (Yokohama) |

| Store    | Add-Ons     | Version |
| ---      | ---      | ---       |
|SplunkBase |[Tenable Add-On for Splunk](https://splunkbase.splunk.com/app/4060)|8.0.0|
|SplunkBase |[Tenable App for Splunk](https://splunkbase.splunk.com/app/4061)|6.1.0|
|ServiceNow Store|[Splunk Integration](https://store.servicenow.com/store/app/890cab2e1b246a50a85b16db234bcb17)|1.1.8|


<img src="https://raw.githubusercontent.com/alo7lika/PyVerse/refs/heads/main/Images/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="9000">

## 🔎 🎯 Tenable Vulnerability Management Setup
1. We will need to have deployed Nessus Scanners or Nessus Agents in order to inventory assets and prep them for credentialed vulnerability scanning.
- [TVM Scanning guide](https://docs.tenable.com/vulnerability-management/Content/PDF/Tenable_Vulnerability_Management-User_Guide.pdf)
<img width="800" height="600" alt="Pasted image 20250810003130" src="https://github.com/user-attachments/assets/2392bcb5-1296-4fc8-9b09-b707949f449b" />


2. Login into Tenable VM cloud.tenable.com and create bi-weekly vulnerability scans against your assets in addition to any discovery scans.
<img width="500" height="500" alt="Pasted image 20250810004219" src="https://github.com/user-attachments/assets/f2be5a10-153c-488d-a789-1e26b3c0b1ea" />
<img width="500" height="500" alt="Pasted image 20250809210002" src="https://github.com/user-attachments/assets/bc870362-9898-47f7-adf4-ded20358bfac" />

3. Create a service accont for the Splunk intergration and generate API keys in order to push data from TVM->Splunk.
<img width="500" height="500" alt="Pasted image 20250809210308" src="https://github.com/user-attachments/assets/3efe852d-ca24-49f8-ab00-8feb46e20dfb" />
<img width="500" height="500" alt="Pasted image 20250809210456" src="https://github.com/user-attachments/assets/44ec4547-e50f-41db-875f-f52498df5118" />

4. Document your API Access and Secret keys. 

## 📥 📊 Splunk Setup 
1. We will be importing vulnerabilty data from TVM to Splunk in order to normalize and centralize the data.
- [Splunk intergration guide](https://docs.tenable.com/integrations/Splunk/Content/PDF/Tenable_and_Splunk_Integration_Guide.pdf)

<img width="800" height="600" alt="Pasted image 20250809113632" src="https://github.com/user-attachments/assets/e3a21609-76eb-430f-a283-c56d90fd160f" />

2. Signed up to Splunk Cloud [here](https://www.splunk.com/en_us/download.html?_gl=1*1ag37oo*_gcl_au*MTE0MTg3NzU1MS4xNzU0NDU2NDY5LjY5MTMzNzI1MS4xNzU0NzYzODYxLjE3NTQ3NjM4Njg.*FPAU*MTE0MTg3NzU1MS4xNzU0NDU2NDY5*_ga*MTkwMDI4NzUxMS4xNzU0NDU2NDY5*_ga_5EPM2P39FV*czE3NTQ3OTUwNDYkbzckZzEkdDE3NTQ3OTUwNjYkajQwJGwwJGgxMTU3MTI0Mjcx)
  > [!IMPORTANT]
  >Splunk Cloud can take a few hours to build and access.
<img width="500" height="500" alt="Pasted image 20250808004846" src="https://github.com/user-attachments/assets/90d899d3-6a82-492e-bcec-fa006cbba69a" />
<img width="500" height="500" alt="Pasted image 20250809112929" src="https://github.com/user-attachments/assets/4667295a-6499-48be-b377-77b2385015df" />

3. [Install](https://splunkbase.splunk.com/app/4060) ```Tenable Add-on for Splunk``` and provide your TVM API keys to the addon configurtation.
<img width="5000" height="5000" alt="Pasted image 20250809115044" src="https://github.com/user-attachments/assets/b97c28bd-8657-4c86-95cc-40db35e731dd" />
<img width="5000" height="5000" alt="Pasted image 20250809130818" src="https://github.com/user-attachments/assets/87804962-8d04-4886-8c5c-4eb3a80fddb8" />
<img width="5000" height="5000" alt="Pasted image 20250809131022" src="https://github.com/user-attachments/assets/5a825309-b48c-4a56-aeea-1dc92295356a" />

4. Configure Tenable VM data inputs and establish import intervals.
<img width="5000" height="5000" alt="Pasted image 20250809132001" src="https://github.com/user-attachments/assets/a600b053-863e-44a6-b10f-32176003e1a8" />


5. Confirm vulnerability data is being imported
<img width="34520" height="18340" alt="Pasted image 20250809141454" src="https://github.com/user-attachments/assets/e933f9b2-204b-401a-a364-7da3d2d0b60a" />
<img width="34406" height="1844" alt="Pasted image 20250809140640" src="https://github.com/user-attachments/assets/f2e950e7-6d89-4eb5-b637-c7c92269de54" />

6. [Download](https://splunkbase.splunk.com/app/4061) ```Tenable App for Splunk``` in order to view preconfigured templates for vulnerability trends, reporting and dashboards.
<img width="34540" height="18400" alt="Pasted image 20250809141753" src="https://github.com/user-attachments/assets/3fa85844-dc9e-4712-a1bd-52d7a7f7e200" />

> [!IMPORTANT]
> ServiceNow account details will be needed to complete Splunk -> ServiceNow Intergration.

7. Download ``` Splunk add-on for ServiceNow ``` within Splunk Cloud.
- [Splunk Intergation Details](https://store.servicenow.com/store/app/890cab2e1b246a50a85b16db234bcb17)
<img width="5000" height="5000" alt="Pasted image 20250809152355" src="https://github.com/user-attachments/assets/82de39bd-a8f1-46c9-be2c-acf5be94f924" />
<img width="100000" height="100000" alt="Pasted image 20250809154213" src="https://github.com/user-attachments/assets/4a4ee95f-a2d3-4bb0-96ea-bc5ba7b9564b" />
<img width="34560" height="7060" alt="Pasted image 20250809152520" src="https://github.com/user-attachments/assets/07d39b29-f3a7-46b6-ab49-7435fda781da" />

8. Ensure that you enable each individual input and add the Splunk account to the inputs as outlined here.

<img width="5000" height="5000" alt="Pasted image 20250809204137" src="https://github.com/user-attachments/assets/b9736b8a-d601-4876-81c8-0e5a888dd2c4" />


9. Create an Alert in Splunk based on saved filters. For example, we can focus on non informational vulns to focus on Critical, High, medium and low vulnerabilities.

 Filter:
 ```
| inputlookup io_vuln_data_lookup where (severity!="informational") AND data_source=Host  state=open OR state=reopened | eval product="Tenable.io" | rename synopsis as signature, plugin_id as definition_id, last_found as time_field, first_found as first_time_field, dns_name as asset_name_detail | search asset_name_detail!=null
```
<img width="34560" height="18048" alt="Pasted image 20250810221549" src="https://github.com/user-attachments/assets/ac0fab04-fce1-47bd-ab9c-fa733c19aff1" />

    
<img width="34420" height="18400" alt="Pasted image 20250809190639" src="https://github.com/user-attachments/assets/a0282e7c-fd7d-4e86-ac3e-13e6f1c00788" />
<img width="34560" height="18340" alt="Pasted image 20250809190835" src="https://github.com/user-attachments/assets/74e963f0-9afe-4f61-adb4-95e520268704" />
<img width="34520" height="11800" alt="Pasted image 20250809191203" src="https://github.com/user-attachments/assets/9d7d1c16-bafb-4d13-bffb-4d6da59910ed" />


## ⚙️ 🎟️ ServiceNow Setup
1. Splunk Cloud will be triggering alerts/incidents to ServiceNow which then helps maintain, assign and track vulnerability incidents/tickets for Security operation workflow.
<img width="8000" height="6000" alt="Pasted image 20250809201701" src="https://github.com/user-attachments/assets/9dba46e2-3d29-4476-b97d-4c8dcbcbc80f" />
2. Create a ServiceNow PDI Personal Developer account and deploy the PDI instance using https://signon.servicenow.com/.
<img width="500" height="500" alt="Pasted image 20250809152835" src="https://github.com/user-attachments/assets/65c52c05-de3b-4df8-b8c1-768adc932206" />
<img width="500" height="500" alt="Pasted image 20250809153333" src="https://github.com/user-attachments/assets/cf75e491-e0ac-4ce0-95cd-de5903a0f0d7" />

3. [Install](https://store.servicenow.com/store/app/890cab2e1b246a50a85b16db234bcb17) ```The Splunk Intergration``` from the ServiceNow store to intstall the neccessary plugins to enable you to sync incidnets from Splunk to ServiceNow.

> [!IMPORTANT]
> [Note that The Splunk Integration requirements will need a non-PDI ServiceNow subscription/license](https://www.servicenow.com/community/developer-forum/splunk-integration-with-pdi-instance/m-p/3065261)

<img width="34404" height="18300" alt="Pasted image 20250810222556" src="https://github.com/user-attachments/assets/103e1913-cbfa-49aa-a44e-81cd1a6c4a97" />

4. This will now allow you to fully sync critical vulnerabilties as INC incidents which can then be assigned to Security Operation teams for remediation or to a patch managment team for a continous and automated workflow.
<img width="34500" height="18042" alt="Pasted image 20250809203631" src="https://github.com/user-attachments/assets/81d00321-e54e-4844-a34d-6815dff03261" />
<img width="34054" height="18030" alt="Pasted image 20250809205035" src="https://github.com/user-attachments/assets/54872c80-2939-4f2d-bcd6-e5b7f4e12ac6" />
<img width="35804" height="18024" alt="Pasted image 20250809201814" src="https://github.com/user-attachments/assets/4fba64fd-48b1-49a5-b72f-31aaab75a1dd" />

<img src="https://raw.githubusercontent.com/alo7lika/PyVerse/refs/heads/main/Images/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="9000">

