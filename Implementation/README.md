# Implementation

Hands-on implementation of a Secure Azure Landing Zone foundation using Microsoft Azure governance, management groups, resource organization, networking, identity, monitoring, tagging and cost-management capabilities.

## 🏗️ Implementation Areas

| Area | Hands-on Implementation |
|---|---|
| Management Groups | Created Landing Zones hierarchy and platform structure |
| Subscription Organization | Organized the Learning-labs subscription under Development |
| Platform Structure | Created Connectivity, Identity and Management management groups |
| Resource Organization | Created dedicated resource groups for platform and workload resources |
| Networking | Created Hub VNet and Network Security Groups |
| Identity & Access | Reviewed Azure RBAC and subscription-level role assignments |
| Governance | Applied standardized resource tagging |
| Monitoring | Created Log Analytics workspace |
| Diagnostic Settings | Sent subscription Administrative logs to Log Analytics |
| Activity Monitoring | Validated Azure Activity Logs and management operations |
| Cost Management | Reviewed Azure Cost Analysis and service consumption |
| Validation | Verified governance, networking, monitoring and organizational controls |

## 1. Management Group Hierarchy

Created a structured management group hierarchy to establish centralized governance and subscription organization.

### Implemented Hierarchy

Tenant Root Group  
└── landing-zones  
&nbsp;&nbsp;&nbsp;&nbsp;├── Development  
&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;└── Learning-labs  
&nbsp;&nbsp;&nbsp;&nbsp;├── Production  
&nbsp;&nbsp;&nbsp;&nbsp;├── Platform  
&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;├── Connectivity  
&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;├── Identity  
&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;└── Management  
&nbsp;&nbsp;&nbsp;&nbsp;└── Sandbox

### Configuration

- Created the `landing-zones` management group.
- Created Development, Production, Platform and Sandbox management groups.
- Created Connectivity, Identity and Management under Platform.
- Associated the `Learning-labs` subscription with Development.
- Validated the hierarchy through Azure Resource Manager.

## 2. Resource Group Organization

Created dedicated resource groups using an environment and platform-based naming convention.

### Resource Groups

- `rg-platform-network-dev`
- `rg-platform-identity-dev`
- `rg-platform-management-dev`
- `rg-shared-services-dev`
- `rg-workload-app1-dev`
- `rg-monitoring-dev`
- `NetworkWatcherRG`

The structure separates networking, identity, management, monitoring, shared services and workload resources.

## 3. Network Foundation

Implemented the foundational networking components required for the landing zone environment.

### Components

- Azure Virtual Network
- Network Security Groups
- Network segmentation
- Network Watcher
- Dedicated platform networking resource group

### Implemented Resources

- `vnet-hub-dev`
- `nsg-app-dev`
- `nsg-web-dev`
- `nsg-management-dev`
- `NetworkWatcher_centralindia`

The network components were organized under the dedicated platform networking resource group.

## 4. Identity & Access Management

Reviewed subscription-level Azure RBAC assignments and access permissions.

### Implemented / Validated

- Azure RBAC
- Owner role assignments
- Privileged role assignments
- Microsoft-managed service identities
- Subscription-level access control
- Least-privilege access principles

The IAM configuration was reviewed to understand human and service identity access at subscription scope.

## 5. Resource Tagging

Applied standardized tags to resource groups to support governance, ownership and cost tracking.

### Tags Applied

| Tag | Value |
|---|---|
| Environment | Development |
| Project | Secure-Landing-Zone |
| Owner | Suman Duddi |
| CostCenter | IT-001 |

These tags provide consistent environment classification, ownership, project identification and cost attribution.

## 6. Azure Monitor & Log Analytics

Created a dedicated Log Analytics workspace for centralized monitoring.

### Workspace Configuration

- Workspace Name: `law-monitoring-dev`
- Region: Central India
- Pricing Tier: Pay-as-you-go
- Resource Group: `rg-monitoring-dev`
- Subscription: Learning-labs

The workspace provides a centralized destination for Azure monitoring and diagnostic data.

## 7. Diagnostic Settings

Configured subscription-level diagnostic settings to send Azure platform logs to Log Analytics.

### Diagnostic Setting

`diag-subscription-monitoring`

### Configuration

- Administrative logs: Enabled
- Destination: Log Analytics workspace
- Workspace: `law-monitoring-dev`

This configuration enables centralized collection of subscription-level administrative activity for monitoring and audit purposes.

## 8. Azure Activity Logs

Validated Azure Activity Logs to monitor control-plane operations performed within the subscription.

### Operations Observed

- Resource group creation and updates
- Resource deployments
- Diagnostic setting creation and deletion
- Azure Policy-related operations
- Network Watcher operations
- Log Analytics workspace operations
- Deployment validation operations

Activity Logs provide visibility into management operations, including the operation performed, status, timestamp and initiating identity.

## 9. Cost Management

Reviewed Azure Cost Management and Cost Analysis to understand consumption within the Pay-As-You-Go subscription.

### Cost Analysis Activities

- Reviewed accumulated cost.
- Reviewed forecasted cost.
- Analyzed costs by service.
- Reviewed regional cost distribution.
- Identified major service-level cost contributors.
- Used cost visibility as part of the landing-zone governance approach.

Cost optimization was considered throughout the implementation to minimize unnecessary Azure consumption.

## 10. Validation

Validated the implemented landing-zone components through the Azure Portal.

### Validation Checklist

- Management group hierarchy created successfully.
- Development subscription placed under the correct management group.
- Platform management groups created successfully.
- Resource groups created using logical naming conventions.
- Hub VNet created successfully.
- Network Security Groups created successfully.
- Network Watcher available in Central India.
- Azure RBAC assignments reviewed.
- Standardized resource tags applied.
- Log Analytics workspace created and operational.
- Subscription diagnostic settings configured.
- Administrative activity logs generated successfully.
- Azure Activity Logs reviewed.
- Cost Analysis reviewed.
- Resources organized according to platform and workload responsibilities.

## 📸 Evidence

Implementation screenshots are available in the `Screenshots` folder and provide evidence of:

- Management Group hierarchy
- Subscription organization
- Resource groups
- Hub VNet
- Network Security Groups
- Azure RBAC
- Resource tags
- Log Analytics workspace
- Diagnostic Settings
- Azure Activity Logs
- Cost Analysis
- Network Watcher

## 🎯 Skills Demonstrated

**Azure Landing Zones • Management Groups • Azure Governance • Azure RBAC • Resource Organization • Azure Networking • Network Security Groups • Azure Monitor • Log Analytics • Diagnostic Settings • Activity Logs • Resource Tagging • Cost Management • Cloud Security**

## 📌 Project Status

**Completed**

The Secure Azure Landing Zone foundation was implemented, validated and documented using Microsoft Azure.
