# About
Azure automation runbook that can be used to scale Azure Sql Database based on a schedule. 
This is an up date date version that uses **managed identity** instead of RunAs connection. 

# Prerequisites
- make sure your Azure automation account uses a managed identity.
  - all new automation accounts are using managed identity
  - migrate if needed you account to use a managed identity. More info: https://learn.microsoft.com/en-us/azure/automation/migrate-run-as-accounts-managed-identity?tabs=sa-managed-identity
- Make sure Az powershell modules are on at least verion 8.
  - all new automation accounts are using latest version
  - for existing accounts update Az modules. More info: https://learn.microsoft.com/en-us/azure/automation/automation-update-azure-modules

# Reason why updated version exists
Azure Automation Run As accounts **will retire on 30 September 2023 and completely move to Managed Identities**. All runbook executions using RunAs accounts, including Classic Run As accounts wouldn't be supported after this date. Starting 01 April 2023, the creation of new Run As accounts in Azure Automation will not be possible.
More info: https://learn.microsoft.com/en-us/azure/automation/migrate-run-as-accounts-managed-identity?tabs=sa-managed-identity
## Differences between original version
- it uses Managed identity instead of a RunAs connection
- it uses Az modules for accessing Azure database instead of AzureRM. AzureRM modules will retire on 29 February 2024. More info: https://learn.microsoft.com/en-us/powershell/azure/migrate-from-azurerm-to-az?view=azps-10.3.0

# Original version and more info
For the initial version please check https://www.mssqltips.com/sqlservertip/6554/auto-scaling-azure-sql-db-using-automation-runbooks


