# Azure Enumeration with Low-Privilege Access
## Overview
A standard Azure user account may be able to access information about:

- Azure subscriptions
- Resource groups
- Azure resources
- Entra ID objects
- User accounts
- Groups
- Role assignments

Visibility depends on the permissions granted to the account.

## Azure PowerShell
Azure PowerShell provides direct interaction with Azure services and Microsoft Graph.

Installation:

Install-Module Az

Connection:

Connect-AzAccount

## Common Enumeration Areas
### Tenant Information
- Current tenant
- Available subscriptions
- Resource groups
- Cloud resources

### Entra ID Information
- Users
- Groups
- Role assignments
- Directory objects

### Access Tokens
Azure PowerShell can interact with:

- Azure Resource Manager
- Microsoft Graph
- Other Azure APIs

## Learning Objectives
- Understand Azure tenant structure
- Understand subscription hierarchy
- Understand role-based access control (RBAC)
- Understand Entra ID visibility
