<p align="left">
    <img src="https://img.shields.io/badge/terraform-%235835CC.svg?style=plastic&logo=terraform&logoColor=white" alt="Terraform">
    <img src="https://img.shields.io/badge/microsoft%20azure-0089D6?style=plastic&logo=microsoft-azure&logoColor=white" alt="Microsoft Azure">
    <img src="https://img.shields.io/badge/Azure_DevOps-0078D7?style=plastic&logo=azure-devops&logoColor=white" alt="AzureDevops">
    <img src="https://img.shields.io/badge/.NET-512BD4?style=plastic&logo=dotnet&logoColor=white" alt="Dotnet">
    <img src="https://img.shields.io/badge/Docker-2CA5E0?style=plastic&logo=docker&logoColor=white" alt="Docker">
    <img src="https://img.shields.io/badge/Visual_Studio_Code-0078D4?style=plastic&logo=visual%20studio%20code&logoColor=white" alt="Visual Studio Code">
    <img src="https://img.shields.io/badge/powershell-5391FE?style=plastic&logo=powershell&logoColor=white" alt="PowerShell">
</p>

<h1 align="left">Microsoft Applied Skill</h1>
<h3 align="left">Deploy cloud-native apps using Azure Container Apps</h3>

<img src="https://github.com/ZCHAnalytics/cloud-native-azure-paas/assets/146954022/46adcb5e-d7b1-4c89-84e3-5a51f677fe5d" alt="certificate-image" width="300" align="right">
For this Microsoft Applied Skill Credential, I configure a secure Platform as a Service (PaaS) solution for cloud-native apps with Azure. 



## 1. PaaS components in Azure Portal <img src="https://img.shields.io/badge/microsoft%20azure-0089D6?style=plastic&logo=microsoft-azure&logoColor=white" alt="Microsoft Azure">
- A Resource Group to help manage and deploy related resources together 
- Networking infrastructure: Azure Virtual Network (VNet), subnets, private endpoints
- Service Bus (applications messaging service)
- Azure Container Registry (ACR), a managed Docker Registry Service 

## 2. Development of the web application in Visual Studio Code <img src="https://img.shields.io/badge/Visual_Studio_Code-0078D4?style=plastic&logo=visual%20studio%20code&logoColor=white" alt="Visual Studio Code">
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

## 5. Automate deployment in Azure DevOps <img src="https://img.shields.io/badge/Azure_DevOps-0078D7?style=plastic&logo=azure-devops&logoColor=white" alt="AzureDevops">
- Configure a PaaS environment for managing software development lifecycle 
- Define CI/CD workflow with a starter pipeline and task `Azure App Service Deploy`
- Add a self-hosted Windows agent to access resources with Azure cloud shell
- Run the pipeline and check the outcome in Azure Portal

## 6. Manage Revisions in Azure Container Apps
- Switch to multiple revision management to facilitate versioning
- Create a new revision for changes to the application
- Add labels to revisions to enable easy identification
- Split traffic between different revisions
