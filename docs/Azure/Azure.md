# Azure Labs

[TOC]

## Task 1: Azure Fundamentals

Understand and Implement Azure Fundamentals

**Goal:** Gain a foundational understanding of Azure services, management tools, and security features.

**Description:** Explore core Azure services, including Azure Compute, Storage, and Networking services.
Set up a basic Azure environment with a virtual network and a couple of VMs.

**Acceptance Criteria** Successfully create an Azure account and navigate the Azure portal.
Deploy a virtual network and two VMs within the Azure portal.
Document the process and key learnings in a shared repository.

## Task 2: Infrastructure as Code with Azure ARM Templates

Deploy Infrastructure Using Azure Resource Manager (ARM) Templates

**Goal:** Learn how to define and deploy infrastructure as code on Azure using ARM templates.

**Description:** Create an ARM template to deploy a scalable web application infrastructure.
Include resources such as Azure App Service, SQL Database, and Application Insights.

**Acceptance Criteria** ARM template is written in JSON and stored in a version-controlled repository.
Infrastructure deployment is automated and repeatable with the ARM template.
Validate the deployment through the Azure portal and ensure all components are correctly configured.

## Task 3: Azure Active Directory and RBAC

Configure Azure Active Directory (AD) and Role-Based Access Control (RBAC)

**Goal:** Understand and implement security and identity management through Azure AD and RBAC.

**Description:** Set up an Azure AD instance and create user groups.
Assign RBAC roles to different user groups to manage access to Azure resources.

**Acceptance Criteria** The Azure AD instance is correctly set up with at least two user groups.
RBAC roles are assigned to these groups, ensuring the principle of least privilege.
Successfully demonstrate access control by having different users access resources based on their RBAC roles.

## Task 4: Implement and Manage Azure Networking

Design and Implement a Secure Azure Networking Solution

**Goal:** Develop skills in designing, implementing, and managing secure and scalable Azure networking solutions.

**Description:** Create a Virtual Network with subnetting to separate different parts of the system.
Implement Network Security Groups (NSGs) and Application Security Groups (ASGs) for fine-grained access control.

**Acceptance Criteria** Virtual Network and subnets are correctly configured and documented.
NSGs and ASGs are implemented to secure network access, with rules documented.
Connectivity is tested and verified between different parts of the system without compromising security.

## Task 5: Azure DevOps and CI/CD Pipelines

Build CI/CD Pipelines Using Azure DevOps

**Goal** Gain hands-on experience with Azure DevOps Services to automate the build and deployment process.

**Description:** Set up an Azure DevOps project and connect it to a source control repository.
Create CI/CD pipelines to automate the build and deployment of a web application to Azure App Service.

**Acceptance Criteria** Azure DevOps project is correctly set up and integrated with a version control system.
CI pipeline successfully builds the code upon each commit.
CD pipeline deploys the build artifacts to Azure App Service automatically upon successful build.
Deployment is verified by accessing the deployed application.

## Task 6: Azure Monitoring and Diagnostics

Implement Monitoring, Logging, and Diagnostics in Azure

**Goal:** Learn to implement and configure monitoring and diagnostics features in Azure to maintain and optimize applications.

**Description:** Configure Azure Monitor and Application Insights for a web application.
Set up alerts and diagnostic logging to track performance issues and exceptions.

**Acceptance Criteria** Azure Monitor and Application Insights are correctly configured for the web application.
Custom alerts are set up for key metrics and log searches.
Successfully demonstrate the ability to diagnose and troubleshoot an issue using the logs and metrics collected.
