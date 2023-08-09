# Backup the SQL DB into container by using AZ cli 

To create a backup of an Azure SQL Managed Database using the Azure CLI or Azure PowerShell, you can use the az sql db export command or the Start-AzSqlDatabaseExport cmdlet, respectively. Here are the steps for both methods:

# Using Azure CLI:

Open a command prompt or terminal.

Log in to your Azure account

```
az login
```

List the Servers in Resource Group

```
az sql server list --resource-group <rg-name>
```

List the Databases with specific SQL Server in Resource group

```
az sql db list --resource-group <rg-name> --server <server-name>
```

Create a backup using the az sql db export command. Replace the placeholders with your actual values:

```
az sql db export --resource-group <resource-group-name> --server <server-name> --name <database-name> --admin-user <admin-username> --admin-password <admin-password>  --storage-key-type StorageAccessKey --storage-key <storage-account-key> --storage-uri <storage-uri>
```
