# Secure Azure Landing Zone Architecture

This architecture represents the Azure Landing Zone environment implemented as part of this hands-on project.

## Architecture Overview

The architecture demonstrates:

- Management Group hierarchy
- Landing Zone organizational structure
- Platform, Development, Production and Sandbox separation
- Connectivity, Identity and Management platform areas
- Subscription organization
- Azure Resource Groups
- Virtual Network and Network Security Groups
- Microsoft Entra ID and Azure RBAC
- Azure Monitor and Log Analytics
- Diagnostic Settings and Activity Logs
- Resource tagging and governance
- Cost Management and optimization

## Architecture Diagram

![Secure Azure Landing Zone Architecture](Lab%20Architecture.png)

## Design Principles

- Centralized governance through Management Groups
- Environment and workload separation
- Least-privilege access using Azure RBAC
- Network segmentation and security controls
- Centralized monitoring and logging
- Standardized resource organization
- Resource tagging for governance and cost visibility
- Cost-aware Azure resource management

## Architecture Components

| Component | Purpose |
|---|---|
| Management Groups | Organize subscriptions and apply governance |
| Landing Zones | Establish standardized Azure environment structure |
| Platform | Provide shared connectivity, identity and management capabilities |
| Subscriptions | Provide logical isolation and management boundaries |
| Resource Groups | Organize Azure resources by workload/function |
| Virtual Network | Provide network connectivity and segmentation |
| NSG | Control inbound and outbound network traffic |
| Microsoft Entra ID | Identity and access management |
| Azure RBAC | Implement role-based and least-privilege access |
| Log Analytics | Centralized monitoring and log analysis |
| Diagnostic Settings | Route platform logs to monitoring destinations |
| Activity Logs | Track Azure control-plane operations |
| Resource Tags | Standardize ownership, environment and project metadata |
| Cost Management | Monitor and optimize Azure spending |

## Project Alignment

The architecture is based on the Azure resources, governance configuration, monitoring setup and organizational structure implemented during the hands-on lab.

**Project Status: Completed**
