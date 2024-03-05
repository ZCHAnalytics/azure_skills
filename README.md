# Downsizing from Azure Kubernetes Service to Azure Container Apps 

# Scenario:
Company wants to switch from Azure Kubernetes Service (AKS) to Azure Container Apps as they are not using the custom service mesh or autoscaling features of AKS.

# Re-requisites (for installation guides, check the end of the document):
- Docker Desktop
- Visual Studio Code with Docker and Azure App extentions
- Azure CLI with `containerapp` extention
- Windows PowerShell

## 1. Configure Azure resources
- resource group
- Virtual Network and subnets
- Service bus
- Azure Container Registry

## 2. Configure app and deployment resources
- WebAPI app and publish to a GitHub repository
- Docker image pushed to Azure Container Registry
- Azure DevOps starter pipeline
- Deployment of a self-hosted Windows agent

## 3. Configure Azure Container Registry for a secure connection with Azure Container Apps
-  Configure a user-assigned managed identity.
- Configure your container registry with AcrPull permissions for the managed identity.
- Configure your container registry with a private endpoint connection.

# 4. Create and configure a container app in Azure Container Apps
- Container app that uses an ACR image
- Authenticate using the user assigned identity
- Connection between the container app and Service Bus
- HTTP scale rules

# Configure continuous integration by using Azure Pipelines
- Use the self-hosted agent pool
- Pipeline1 with an Azure Container Apps deployment task

# Manage revisions in Azure Container Apps
- Set revision management to multiple
- Create a new revision with a v2 suffix
- Configure labels on the -
- Configure a traffic percentage on the revisions
