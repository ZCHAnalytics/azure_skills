#  Platform as a Service solution for containerised web apps with Azure

In this project I configure a secure Platform as a Service (PaaS) solution for cloud-native apps with Azure

## 1. PaaS components in Azure Portal
- A Resource Group to help manage and deploy related resources together 
- Networking infrastructure: Azure Virtual Network (VNet), subnets, private endpoints
- Service Bus (applications messaging service)
- Azure Container Registry (ACR), a managed Docker Registry Service 

## 2. Development of the web application in Visual Studio Code
- Create a WebAPI app and publish to a GitHub repository
- Containerise WebAPI app using a Docker image
- Push the Docker image to Azure Container Registry for storing and managing

## 3. Protecting data with secure connection between Container Registry and Container Apps
- Add a user-assigned managed identity to the resource group
- Container registry must be able to use the managed identity to pull artifacts
- Add AcrPull permission to the the managed identity, using the principle of least privilege
- Add a private endpoint connection to the container registry

## 4. Configure a runtime environment with a container app in Azure Container Apps
- Add a container app that pulls specified image from container registry
- Add authentication with user assigned identity
- Configure a connection between the container app and Service Bus
- Configure HTTP scale rules to allow autoscaling

## 5. Automate deployment in Azure DevOps 
- Configure a PaaS environment for managing software development lifecycle 
- Define CI/CD workflow with a starter pipeline and task `Azure App Service Deploy`
- Add a self-hosted Windows agent to access resources with Azure cloud shell
- Run the pipeline and check the outcome in Azure Portal

## 6. Manage Revisions in Azure Container Apps
- Switch to multiple revision management to facilitate versioning
- Create a new revision for changes to the application
- Add labels to revisions to enable easy identification
- Split traffic between different revisions

# Tools and Technologies Utilised

## Development Tools:
Visual Studio Code, .NET Core SDK, Docker Desktop, GitHub

## Azure Services:
Azure Container Registry (ACR), Azure Container Apps, Azure DevOps, Azure CLI