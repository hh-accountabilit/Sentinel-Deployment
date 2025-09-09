# Microsoft Sentinel One Button Deploy

Microsoft Sentinel One Button Deploy automates the following tasks:

- Creates resource group
- Creates Log Analytics workspace
- Installs Microsoft Sentinel on top of the workspace
- Sets workspace retention, daily cap and commitment tiers
- Enables UEBA with the relevant identity providers (AAD and/or AD)
- Enables health diagnostics for Analytics Rules, Data Connectors and Automation Rules
- Installs Content Hub solutions from a predefined list in three categories: 1st party, Essentials and Training
- Enables Data Connectors from this list:
    + Azure Active Directory (with the ability to select which data types will be ingested)
    + Azure Active Directory Identity Protection
    + Azure Activity (from current subscription)
    + Dynamics 365
    + Microsoft 365 Defender
    + Microsoft Defender for Cloud
    + Microsoft Insider Risk Management
    + Microsoft Power BI
    + Microsoft Project
    + Office 365
    + Threat Intelligence Platforms


## Prerequisites

- Azure Subscription
- Azure user account with enough permissions to enable the desired connectors. See table at the end of this page for additional permissions. Write permissions to the workspace are needed.
- Some data connectors require the relevant licence in order to be enabled. See table at the end of this page for details.

## Deploy

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fhh-accountabilit%2FSentinel-Deployment%2Frefs%2Fheads%2Fmain%2FDeployment%2FazureDeploy.json/createUIDefinitionUri/https%3A%2F%2Fraw.githubusercontent.com%2Fhh-accountabilit%2FSentinel-Deployment%2Frefs%2Fheads%2Fmain%2FDeployment%2FcreateUiDefinition.json) 

## Supported connectors

The following table summarizes permissions, licenses and permissions needed to enable each Data Connector:

| Data Connector                                 | License         |  Permissions                    |
| ---------------------------------------------- | --------------- |---------------------------------|
| Azure Active Directory (Tenant scope version only) | Any AAD license | Global Admin or Security Admin  |
| Azure Active Directory Identity Protection  | AAD Premium 2   | Global Admin or Security Admin  |
| Azure Activity                                 | None            | Subscription Reader             |
| Dynamics 365                                   | D365 license    | Global Admin or Security Admin  |
| Microsoft 365 Defender                         | M365D license   | Global Admin or Security Admin  |
| Microsoft Defender for Cloud                   | MDC license     | Security Reader                 |
| Microsoft Insider Risk Management              | IRM license     | Global Admin or Security Admin  |
| Microsoft PowerBi                              | PowerBi license | Global Admin or Security Admin  |
| Microsoft Project                              | MS Project license | Global Admin or Security Admin |
| Office 365                                     | None            | Global Admin or Security Admin  |
| Threat Intelligence Platforms                  | None            | Global Admin or Security Admin  |
