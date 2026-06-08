# Azure Tenant Enumeration

# Overview
Azure tenant enumeration is the process of identifying Microsoft Entra ID (formerly Azure Active Directory) tenants, discovering tenant information, and validating user accounts during cloud reconnaissance activities.

# OpenID Configuration Discovery
An Azure tenant's OpenID configuration can be queried using the tenant domain name.

# URL Format
https://login.microsoftonline.com/<tenant>.onmicrosoft.com/.well-known/openid-configuration

# Example
https://login.microsoftonline.com/company.onmicrosoft.com/.well-known/openid-configuration

# Purpose
* Confirm the existence of an Azure tenant
* Gather tenant configuration information
* Identify authentication endpoints
* Obtain tenant identifiers

# Information That May Be Identified
- Tenant existence
- Authentication endpoints
- Token endpoints
- Federation configuration
- OpenID metadata

# Tenant ID Discovery
A tenant ID can often be identified using:
https://www.whatismytenantid.com

# Purpose
* Retrieve Azure Tenant ID
* Support further Azure reconnaissance
* Assist in tenant mapping

# AADInternals
AADInternals is a PowerShell framework used for Azure and Microsoft Entra ID assessment and enumeration.

Repository:
https://github.com/Gerenios/AADInternals

# Common Uses
* Tenant enumeration
* Domain discovery
* User enumeration
* Azure security assessments

# Retrieve Tenant Information
# powershell
Get-AADIntTenantDomains -Domain targetdomain.com

# Example
# powershell
Get-AADIntTenantDomains -Domain rabobank.nl

# Purpose
* Enumerate internal tenant domains
* Identify associated Microsoft domains
* Discover additional attack surface

# Username Enumeration
AADInternals can validate whether usernames exist within a tenant.

# Single User Check
# powershell
Invoke-AADIntUserEnumerationAsOutsider -UserName user@tenant.onmicrosoft.com

# Bulk User Check
# powershell
Get-Content .\users.txt | Invoke-AADIntUserEnumerationAsOutsider -Method Normal

# Purpose
* Validate user accounts
* Support identity reconnaissance
* Assist with authorized security assessments

# Notes
* Microsoft Entra ID was formerly known as Azure Active Directory (Azure AD).
* Ensure all enumeration activities are authorized and within scope.
* Avoid excessive requests that could impact service availability.

## References
* AADInternals
* Microsoft OpenID Configuration
* Microsoft Entra ID Documentation
