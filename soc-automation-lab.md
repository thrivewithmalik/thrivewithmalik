# SOC Automation Project 🤖

## 1. Objective
The goal of this project was to build an automated Incident Response workflow to eliminate repetitive manual tasks. By integrating a SOAR platform with a Case Management System, I successfully automated the ingestion, enrichment, and alerting of security events, allowing analysts to focus on real threats rather than false positives.

## 2. Tools & Technologies
* **SOAR Platform:** Shuffle
* **Case Management:** TheHive
* **SIEM/Detection:** (e.g., Wazuh or Splunk)
* **Threat Intelligence:** VirusTotal / AbuseIPDB (for enrichment)
* **Communication:** (e.g., Email, Discord, or Slack for alerts)

## 3. Architecture & Workflow
*(Ideally, place a screenshot of your Shuffle workflow diagram here)*

This lab follows a classic SOC Automation lifecycle:
1.  **Ingestion:** The SOAR platform (Shuffle) receives an alert from the SIEM.
2.  **Enrichment:** Shuffle automatically extracts IP addresses/hashes and queries VirusTotal/AbuseIPDB.
3.  **Filtering:** If the reputation score is "Clean," the alert is closed automatically. If "Malicious," it proceeds.
4.  **Response:** The system creates a case in **TheHive**, updates the details, and sends a notification to the analyst.

## 4. Key Achievements
* **Automated Triage:** Reduced time-to-triage by automatically enriching indicators of compromise (IoCs) before an analyst opens the ticket.
* **Case Management:** Configured TheHive to accept API calls from Shuffle, ensuring a seamless flow of data.
* **Error Handling:** Built logic to handle failed API calls or missing data fields.

## 5. Visuals
### The Playbook Logic
*(Add a screenshot of your Shuffle "nodes" and connections here)*

### The Case in TheHive
*(Add a screenshot showing the automatically created ticket with the enriched data)*
