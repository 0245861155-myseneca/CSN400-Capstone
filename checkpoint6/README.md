- **COURSE INFORMATION: CSN 400 NBB**
- **STUDENT’S NAME: Tyler Kirkwood**
- **STUDENT'S NUMBER: 024861155**
- **GITHUB USER ID: 0245861155-myseneca**
- **TEACHER’S NAME: Atoosa Nasiri**

## Part A
#### 61 is my unique ID
```bash
ID="61"          #unique ID assigned to you
```
- 1. In network_config_test.sh what does if [[ ! $(az group list -o tsv --query "[?name=='$RG_NAME']") ]] do? Explain your answer.

- 1a. i will be breaking down the code.
```
az group list -o tsv --query "[?name=='$RG_NAME']": This command lists Azure resource groups (az group list) and uses the -o tsv option to format the output as tab-separated values. The --query parameter allows you to filter the results based on a specified query. In this case, the query [?name=='$RG_NAME'] filters the list to include only the resource groups whose name matches the value of the $RG_NAME variable.

$(...): This syntax allows the output of the command inside the parentheses to be captured and used within the script.

!: The exclamation mark negates the result. So, if the command inside the $(...) returns an empty value (no matching resource groups found), the negation will turn it into a true condition.

if [[ ... ]]: This is a conditional statement in Bash. The double brackets [[ ... ]] indicate the start and end of the condition. Wha
```

- 2. Why is it crucial to check if a resource exist before creating it? What bash syntax do you use to test this? How do you check if a vnet exits in vnet_create.sh?
```
2A .It is crucial to check if a resource exists before creating it to avoid unintended consequences and potential issues. Checking for the existence of a resource allows you to implement error handling, prevent duplicate creations, and ensure the script behaves as expected.
```
- 3.  What is the Azure CLI command to create vnet? Give the specific command as per your environment and unique ID configuration. What are the required and what are the optional parameters that you need to pass to it?
```
3a. The Azure CLI command to create a VNet is az network vnet create. The specific command may vary based on your environment and unique ID configuration, but I can provide you with an example command with the required and optional parameters that you need to pass.
```

``` bash

az network vnet create --name <vnet-name> --resource-group <resource-group-name> --location <location> --address-prefixes <address-prefix> --subnet-name <subnet-name> --subnet-prefix <subnet-prefix>

```

- 4. What is the Azure CLI command to create subnet? Give the specific command as per your environment and unique ID configuration. What are the required and what are the optional parameters that you need to pass to it?

- 4a. To create a subnet using Azure CLI, you can use the az network vnet subnet create command

``` bash
az network vnet subnet create \
  --name <subnet-name> \
  --resource-group <resource-group-name> \
  --vnet-name <vnet-name> \
  --address-prefix <subnet-address-prefix>

```

## Part B

- 6. error

```bash
(ResourceNotFound) The Resource 'Microsoft.Network/routeTables/router-61' under resource group 'Student-RG-964259' was not found. For more details please go to https://aka.ms/ARMResourceNotFoundFix
Code: ResourceNotFound
Message: The Resource 'Microsoft.Network/routeTables/router-61' under resource group 'Student-RG-964259' was not found. For more details please go to https://aka.ms/ARMResourceNotFoundFix
```
- 7. optional question 
```
az network  vnet subnet show --name SN1 --vnet-name router-61 --resource-group Student-RG-964259
``` 

## part C

- 1. What is Azure Virtual Network (VNET)? Elaborate in your own words, you may use diagrams if drawn by yourself.

- 1a. Azure Virtual Network (VNET) is a foundational networking service provided by Microsoft Azure that allows you to create and manage your own private virtual network in the cloud. It serves as a logical representation of your own network infrastructure within the Azure environment.
<br />

- 2. In the context of Hybrid Cloud architecture. How on-prem computers can access resources inside Azure virtual network?
- 2a. In a Hybrid Cloud architecture, on-premises computers can access resources inside an Azure virtual network (VNET) through different connectivity options. 
<br />

- 3. What are the most important benefits of Azure Virtual Networks? Elaborate in your own words. Do not copy/paste from Azure Documentation. Itemized list of just benefit without proper elaboration will not receive any marks
- 3a.Azure Virtual Networks (VNets) offer several important benefits that empower organizations to build scalable and secure network architectures in the cloud
<br />

- 4. What is the difference between Network Security Group (NSG) and Route-Tables?
- 4a.  both NSGs and Route Tables are involved in controlling network traffic within Azure VNets, they serve different purposes. NSGs focus on enforcing security policies and filtering traffic at the network interface or subnet level. Route Tables, on the other hand, determine the routing path for network traffic within the virtual network, allowing you to control the flow of traffic between subnets, virtual appliances, and other destinations.
<br />

- 5. What is the difference between NSG and Firewalls?
- 5a. NSGs and Firewalls play a role in network security, NSGs provide subnet-level or network interface-level traffic filtering within a virtual network. Firewalls, such as Azure Firewall, offer centralized and scalable network security services at the perimeter of the virtual network, providing advanced application-level filtering and threat protection capabilities.
<br />

- 6. What is a hob-and-spoc network topology and how be deployed in Azure Cloud?
- 6a. 
