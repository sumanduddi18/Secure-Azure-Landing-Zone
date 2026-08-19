# Secure Azure Landing Zone - Interview Preparation

Interview preparation based on the hands-on Secure Azure Landing Zone Lab.

## 🎯 Core Topics

- Azure Landing Zones
- Management Groups
- Subscription Organization
- Platform and Workload Separation
- Azure RBAC
- Least Privilege
- Resource Groups
- Resource Tagging
- Azure Virtual Network
- Network Security Groups
- Azure Monitor
- Log Analytics
- Diagnostic Settings
- Azure Activity Logs
- Cost Management
- Azure Governance

## 📚 Theory Questions

### 1. What is an Azure Landing Zone?

An Azure Landing Zone is a standardized Azure foundation that provides governance, identity, networking, security and management capabilities required to deploy and operate workloads at scale.

### 2. Why are Management Groups used?

Management Groups provide a governance layer above subscriptions and allow organizations to apply policies, RBAC and governance controls consistently across multiple subscriptions.

### 3. What is the Azure hierarchy?

Tenant → Management Group → Subscription → Resource Group → Resource

### 4. What is the purpose of a Platform structure?

The Platform structure separates shared cloud capabilities such as Connectivity, Identity and Management from application workloads.

### 5. Why separate Development, Production and Sandbox environments?

Environment separation allows different governance, access, security and operational controls to be applied based on the purpose and risk of each environment.

### 6. What is Azure RBAC?

Azure Role-Based Access Control controls who can access Azure resources, what actions they can perform and at which scope.

### 7. What is least privilege?

Least privilege means providing only the permissions required to perform a specific task or responsibility.

### 8. Why are Resource Groups used?

Resource Groups provide logical organization and lifecycle management for Azure resources.

### 9. Why use resource tags?

Tags provide metadata such as environment, project, ownership and cost-center information and help with governance and cost allocation.

### 10. What is an Azure Virtual Network?

An Azure Virtual Network provides private network connectivity and enables logical segmentation of Azure resources.

### 11. What is an NSG?

A Network Security Group controls inbound and outbound network traffic using security rules based on source, destination, port, protocol, direction and priority.

### 12. What is Azure Monitor?

Azure Monitor provides monitoring and observability for Azure resources using metrics, logs, Activity Logs and other telemetry.

### 13. What is Log Analytics?

Log Analytics provides centralized log collection and analysis and supports querying collected data using KQL.

### 14. What are Diagnostic Settings?

Diagnostic Settings configure which platform logs and metrics are collected and where they are sent, such as a Log Analytics workspace.

### 15. What is Azure Activity Log?

Azure Activity Log records subscription-level management-plane operations performed on Azure resources.

### 16. What is Azure Cost Management?

Azure Cost Management provides visibility into Azure spending through Cost Analysis, forecasting and other cost-governance capabilities.

## 🔐 Scenario-Based Questions

### Scenario 1 - Enterprise Azure Structure

An organization has separate Development, Production and Sandbox subscriptions. How would you organize them?

**Answer:**

I would use Management Groups to create a structured governance hierarchy and place each subscription under the appropriate Management Group based on its environment and purpose.

### Scenario 2 - Platform Services

An organization requires centralized Connectivity, Identity and Management capabilities.

**Answer:**

I would create a dedicated Platform Management Group and organize these shared capabilities under Connectivity, Identity and Management areas. This separates platform services from workload environments.

### Scenario 3 - Excessive Production Access

A developer has Owner access to a Production subscription.

**Answer:**

I would review the actual business requirement and replace the Owner role with the minimum required RBAC role at the smallest practical scope.

### Scenario 4 - Network Segmentation

A workload requires controlled network access.

**Answer:**

I would design appropriate VNet and subnet boundaries and associate NSGs with the relevant network resources to control allowed traffic.

### Scenario 5 - Sandbox Governance

Developers need an environment for experimentation.

**Answer:**

I would place the Sandbox subscription under a dedicated Sandbox Management Group and apply appropriate governance, access and cost controls.

### Scenario 6 - Resource Organization

An organization has many Azure resources and administrators cannot easily identify ownership.

**Answer:**

I would establish standardized Resource Groups, naming conventions and tags such as Environment, Project, Owner and CostCenter.

### Scenario 7 - Monitoring Azure Operations

Security wants visibility into administrative changes made to the Azure subscription.

**Answer:**

I would use Azure Activity Logs to review management-plane operations and configure Diagnostic Settings to send relevant logs to a centralized Log Analytics workspace for further analysis.

### Scenario 8 - Cost Increase

Azure spending suddenly increases.

**Answer:**

I would start with Cost Analysis, identify the services and resources contributing to the increase, review recent resource deployments and configuration changes, and then take appropriate optimization actions.

## 🛠️ Production Challenge Questions

### Challenge 1 - Incorrect Subscription Placement

A Production subscription has been placed under the Development Management Group.

**Approach:**

1. Identify the subscription.
2. Review its current Management Group.
3. Check inherited governance and access controls.
4. Move the subscription to the correct Management Group.
5. Validate inherited controls after the move.

### Challenge 2 - Excessive RBAC Permissions

A user has unnecessary Owner access to a Production subscription.

**Approach:**

1. Review the user's current role.
2. Identify the required administrative actions.
3. Select the minimum required RBAC role.
4. Reduce the assignment scope where possible.
5. Remove unnecessary permissions.
6. Validate the user's effective access.

### Challenge 3 - Unnecessary Network Access

An NSG contains rules allowing unnecessary inbound traffic.

**Approach:**

1. Review the NSG rules.
2. Identify unnecessary ports and sources.
3. Validate application dependencies.
4. Restrict or remove unnecessary rules.
5. Test required connectivity.
6. Monitor for unexpected access.

### Challenge 4 - Unexpected Administrative Activity

An unexpected resource configuration change is detected.

**Approach:**

1. Check Azure Activity Log.
2. Identify the operation.
3. Identify the caller.
4. Review the timestamp and affected resource.
5. Check recent RBAC changes.
6. Validate whether the activity was authorized.
7. Take corrective action if required.

### Challenge 5 - Unexpected Cost Increase

The Azure subscription shows an unexpected increase in cost.

**Approach:**

1. Open Cost Analysis.
2. Identify the affected service.
3. Identify the resource responsible.
4. Review recent deployments and configuration changes.
5. Check whether resources are still required.
6. Optimize or remove unnecessary resources.
7. Continue monitoring the cost trend.

## 💼 Project-Specific Questions

### 1. Explain your Secure Azure Landing Zone project.

**Answer:**

I implemented a structured Azure Landing Zone environment focused on Management Groups, subscription organization, platform separation, RBAC, resource governance, networking, monitoring and cost management.

I created a Landing Zones hierarchy with Platform, Development, Production and Sandbox areas and organized the lab subscription under the Development structure.

I also implemented resource organization, tagging, networking with VNet and NSGs, Azure RBAC, Log Analytics, Diagnostic Settings, Activity Log monitoring and Cost Management.

### 2. What Management Group structure did you implement?

**Answer:**

I created a Landing Zones hierarchy containing Platform, Development, Production and Sandbox areas.

The Platform area was further organized into Connectivity, Identity and Management to represent shared platform capabilities.

### 3. Why did you separate Platform from workloads?

**Answer:**

Platform services are shared capabilities that support multiple workloads. Separating them from workload environments improves governance, security boundaries, operational ownership and scalability.

### 4. How did you implement access control?

**Answer:**

I used Azure RBAC to review and control access based on roles and scope while following least-privilege principles.

### 5. How did you implement network security?

**Answer:**

I implemented Azure Virtual Network and Network Security Groups to establish network boundaries and control traffic using NSG security rules.

### 6. Why did you configure Log Analytics?

**Answer:**

I configured Log Analytics as a centralized destination for monitoring and diagnostic data. This provides a foundation for centralized log analysis and troubleshooting.

### 7. Why did you configure Diagnostic Settings?

**Answer:**

Diagnostic Settings allow Azure platform logs to be routed to a centralized destination such as Log Analytics. In this project, they were used to collect subscription-level administrative activity.

### 8. How did you monitor Azure administrative activity?

**Answer:**

I used Azure Activity Logs to review management-plane operations such as resource changes, deployments and configuration operations. Diagnostic Settings were used to route administrative logs to Log Analytics for centralized monitoring.

### 9. How did you approach cost governance?

**Answer:**

I used Azure Cost Management and Cost Analysis to review service and resource consumption, identify major cost contributors and monitor spending within the Pay-As-You-Go subscription.

### 10. How would you scale this Landing Zone for an enterprise?

**Answer:**

I would extend the Management Group hierarchy, onboard additional subscriptions under the appropriate governance scopes, establish centralized identity and connectivity, implement Azure Policy and standardized RBAC, and integrate centralized monitoring, security and cost governance.

## 🎓 Quick Interview Cheat Sheet

| Topic | Key Point |
|---|---|
| Azure Landing Zone | Standardized Azure foundation |
| Management Group | Governance hierarchy above subscriptions |
| Platform | Shared connectivity, identity and management capabilities |
| Subscription | Isolation and management boundary |
| Resource Group | Logical resource organization |
| RBAC | Controls access |
| Least Privilege | Minimum required permissions |
| VNet | Azure network boundary |
| NSG | Network traffic filtering |
| Azure Monitor | Monitoring and observability |
| Log Analytics | Centralized log collection and KQL analysis |
| Diagnostic Settings | Routes platform logs and metrics |
| Activity Log | Subscription-level management events |
| Tags | Resource metadata and cost allocation |
| Cost Management | Cost visibility and optimization |

## 📌 Project Status

**Completed**

Hands-on Azure Landing Zone implementation, validation, documentation and interview preparation completed using Microsoft Azure.
