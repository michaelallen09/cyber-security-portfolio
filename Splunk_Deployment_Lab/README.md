# Splunk Deployment Lab

This project documents the deployment of a small-scale SIEM environment within a controlled virtual lab. The objective was to build a working log collection setup using Splunk Enterprise and validate basic monitoring capability.

---

## What This Project Demonstrates

- Practical SIEM deployment
- Log forwarding and ingestion validation
- Windows Security log visibility
- Sysmon endpoint telemetry integration
- Basic authentication and privilege monitoring
- Threshold-based detection testing

---

## Section Breakdown

### 1. Architecture

A virtualised monitoring environment was created using:

- Ubuntu server 22.04 (Splunk Enterprise)
- Windows 11 Endpoint
- Splunk Universal Forwarder
- Sysmon (enhanced telemetry)
- VirtualBox isolated network

This configuration enabled centralised log collection and monitoring of endpoint activity.

---

### 2. Setup and Configuration

Deployment included:

- Installing Splunk Enterprise
- Enabling receiving port (TCP 9997)
- Creating a dedicated index (`win11_endpoint_logs`)
- Installing and configuring the Universal Forwarder
- Deploying Sysmon for process-level telemetry

---

### 3. Log Ingestion Validation

Log ingestion was validated by:

- Confirming sourcetypes were indexed
- Verifying Windows Security logs were searchable
- Confirming Sysmon process events were ingested

This ensured the ingestion pipeline was operational before detection testing.

---

### 4. Basic Detection Queries

Basic monitoring queries were created to validate detection capability:

- Failed logon threshold monitoring (Event ID 4625)
- Privileged logon visibility (Event ID 4672)
- Process execution monitoring via Sysmon

These detections confirm visibility across authentication, elevated access, and endpoint activity.

---

This lab establishes the technical foundation required for more advanced detection engineering and elevated access monitoring developed in upcoming subsequent labs.
