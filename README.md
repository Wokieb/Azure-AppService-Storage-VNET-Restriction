# Azure-AppService-Logging-Storage-VNET-Restriction
Information regarding enabling storage account firewall to access from Azure App Service 

### Restrict your storage account to a virtual network

When we are writing application and/or Web Server logs to a storage account for Azure App Service, as of today we cannot configure any virtual network restrictions on the respective storage account. If we configure a virtual network service endpoint on the storage account being used for storing App Service logs, that configuration will break the application logging to the storage account.

This is a known issue in Azure App Services and our product team is pro-actively working to fix this in a future updates.

# Here is the brief RCA from the product team on this
```json
The Microsoft Azure Team has investigated the issue you reported on not being able to upload the Logs to Storage account.
This is a limitation of our existing functionality. We have opened a work item for this and we hope to support this functionality soon
 
We are continuously taking steps to improve the Azure Web App service and our processes to ensure such incidents do not occur in the future, and in this case it includes (but is not limited to):
 
     • Uploading logs to storage account locked with Service Endpoints.
      
We apologize for any inconvenience.
Regards,
The Microsoft Azure Team
```

