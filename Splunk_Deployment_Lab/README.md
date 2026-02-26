# 1. Architecture

## 1.1 Overview

This lab environment was built to simulate a basic SIEM deployment using virtual machines. The objective of this phase was to establish a working log ingestion pipeline from a Windows endpoint into Splunk Enterprise.

The focus here is infrastructure and log visibility.

---

## 1.2 Lab Components

The environment consists of:

- Windows 11 endpoint  
- Splunk Universal Forwarder  
- Splunk Enterprise (Ubuntu 22.04)  
- Host machine for management and web access  

---

## 1.3 Windows 11 Endpoint

The Windows machine generates:

- Security Event Logs  
- Sysmon logs  

These logs include authentication events and process activity.

---

## 1.4 Splunk Universal Forwarder

The Universal Forwarder is installed on the Windows endpoint.

It:

- Monitors the Security and Sysmon event channels  
- Forwards logs to Splunk Enterprise over TCP 9997  

The forwarder does not index data locally.

---

## 1.5 Splunk Enterprise

Splunk Enterprise is installed on Ubuntu 22.04.

It:

- Receives logs on TCP 9997  
- Indexes data into `win11_endpoint_logs`  
- Provides search access via the web interface on TCP 8000  

---

## 1.6 Log Flow

1. Windows generates Security and Sysmon events.  
2. The Universal Forwarder collects the events.  
3. Logs are sent to Splunk over TCP 9997.  
4. Events are indexed into `win11_endpoint_logs`.  
5. Searches are performed using the Splunk Web interface.

---

## 1.7 Architecture Diagram
<img width="1280" height="720" alt="Splunk SIEM Lab Architecture" src="https://github.com/user-attachments/assets/e56da2a8-e357-4e7f-b0a6-6d43d5972ca8" />

