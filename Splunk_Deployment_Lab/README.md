# Splunk SIEM Deployment Overview
## Objective

The objective of this lab was to deploy a small-scale SIEM environment using Splunk Enterprise and validate successful log ingestion from a Windows 11 endpoint.

---

## What Was Implemented

- Splunk Enterprise installed on Ubuntu 22.04  
- TCP receiving port (9997) configured  
- Splunk Universal Forwarder deployed on Windows 11  
- Sysmon installed for enhanced endpoint telemetry  
- Dedicated index created for endpoint logs  

Log ingestion was validated before creating baseline monitoring queries.

---

## What This Lab Demonstrates

- Practical SIEM deployment  
- Forwarder configuration and log flow validation  
- Basic log analysis using SPL  
- Monitoring of authentication and privileged logon events  
- Visibility of endpoint process execution via Sysmon  

---

## Lab Structure

1. Architecture  
2. Setup and Configuration  
3. Log Ingestion Validation  
4. Baseline Detection Queries  

---

This lab establishes the technical foundation for more advanced detection development in the next phase.
