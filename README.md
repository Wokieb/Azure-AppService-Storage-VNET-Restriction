# Azure-AppService-Logging-Storage-VNET-Restriction
Information regarding enabling storage account firewall to access from Azure App Service 

### Enable diagnostics logging for apps in Azure App Service

## Overview
Azure provides built-in diagnostics to assist with debugging an App Service app. In this article, you learn how to enable diagnostic logging and add instrumentation to your application, as well as how to access the information logged by Azure.


### Restrict your storage account to a virtual network

When you written the application logging & webserver logging to storage account for azure app service. You can't currently use any virtual network restrictions on this account. If you configure a virtual network service endpoint on the storage account you're using for your app service logs, that configuration will break your application logging to storage account.

This is the known issue in Azure App Service and our product team is working on the issue is diligently fix it in the upcoming rollouts.

#Here is the brief RCA from the product team on this
```json
The Microsoft Azure Team has investigated the issue you reported on not being able to upload the Logs to Storage account.
This is a limitation of our existing functionality. We have opened a work item for this and we hope to support this functionality soon
 
We are continuously taking steps to improve the Azure Web App service and our processes to ensure such incidents do not occur in the future, and in this case it includes (but is not limited to):
 
     • Uploading logs to storage account locked with Service Endpoints.
      
We apologize for any inconvenience.
Regards,
The Microsoft Azure Team
```

