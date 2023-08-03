# Azure SOC and Honeynet project

## Introduction

In this project, I build a mini honeynet in Azure and ingest log sources from various resources into a Log Analytics workspace, which is then used by Microsoft Sentinel to build attack maps, trigger alerts, and create incidents. I measured some security metrics in the insecure environment from 08/01/2023 to 08/03/2023. The metrics I will show are:

(TBD)
- SecurityEvent (Windows Event Logs)
- Syslog (Linux Event Logs)
- SecurityAlert (Log Analytics Alerts Triggered)
- SecurityIncident (Incidents created by Sentinel)
- AzureNetworkAnalytics_CL (Malicious Flows allowed into our honeynet)

The architecture of the mini honeynet in Azure consists of the following components:

- Virtual Network (VNet)
- Network Security Group (NSG)
- Virtual Machines (2 windows, 1 linux)
- Log Analytics Workspace
- Azure Key Vault
- Azure Storage Account
- Microsoft Sentinel

For the "BEFORE" metrics, all resources were originally deployed, exposed to the internet. The Virtual Machines had both their Network Security Groups and built-in firewalls wide open, and all other resources are deployed with public endpoints visible to the Internet; aka, no use for Private Endpoints.

## Attack Maps Before Hardening / Security Controls
![NSG Allowed Inbound Malicious Flows](https://github.com/4am-walking/Azure-SOC-Honeynet/blob/main/imgs/NSG%20Allowed%20In.PNG)<br>
![Linux Syslog Auth Failures](https://github.com/4am-walking/Azure-SOC-Honeynet/blob/main/imgs/Linux%20SSH%20Fail.PNG)<br>
![Windows RDP Auth Failures](https://github.com/4am-walking/Azure-SOC-Honeynet/blob/main/imgs/Windows%20RDP%20Fail.PNG)<br>
![MSSQL Auth Failures](https://github.com/4am-walking/Azure-SOC-Honeynet/blob/main/imgs/MSSQL%20Login%20Fail.PNG)<br>

## Conclusion

TBD
