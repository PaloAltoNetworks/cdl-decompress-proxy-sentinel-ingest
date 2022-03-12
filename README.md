# Proxy template to decompress data from CDL for ingestion into Azure Sentinel

### Deploy a Python (Flask) web app to Azure App Service - Sample Application

This is the sample Flask application for the Azure Quickstart [Deploy a Python (Django or Flask) web app to Azure App Service](https://docs.microsoft.com/en-us/azure/app-service/quickstart-python).  For instructions on how to create the Azure resources and deploy the application to Azure, refer to the Quickstart article.

A Django sample application is also available for the article at [https://github.com/Azure-Samples/msdocs-python-django-webapp-quickstart](https://github.com/Azure-Samples/msdocs-python-django-webapp-quickstart).

If you need an Azure account, you can [create one for free](https://azure.microsoft.com/en-us/free/).


## Pre-Requisties:

Configure the following variables (Store the secrets in Key vault or directly pass the values) for Azure Sentinel interaction after navigating to application settings (Web app -> Configuration -> Application Settings),

Name: WORKSPACE_ID  
Value: @Microsoft.KeyVault(SecretUri=<vault URI>)  

Name: SHARED_KEY  
Value: @Microsoft.KeyVault(SecretUri=<vault URI>)  

Key vault settings: 

https://docs.microsoft.com/en-us/azure/app-service/overview-managed-identity?tabs=portal%2Chttp


### Deploying through Visual Studio Code:

1. Install Visual Studio Code Version >= 1.64.1  
2. Install Extensions Azure Tools, Azure App Service in Visual Studio Code  
3. git clone https://github.com/PaloAltoNetworks/cdl-decompress-proxy-sentinel-ingest.git  
4. Open the folder cdl-decompress-proxy-sentinel-ingest in Visual Studio Code  
5. Click the Azure Icon, Sign Into Azure -> `Create new Web App`  
6. Right Click the Web App created and chose `Deploy to Web App`
