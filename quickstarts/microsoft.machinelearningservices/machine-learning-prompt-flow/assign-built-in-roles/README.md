# Grant access to promptflow with built-in roles
This simple way to grant permission is using built-in roles. You can check [this template](./assign-built-in-roles/).
We need follow built-in roles assign to user (compute instance) and identity (endpoint):
|Resource| Built-in role |
|--------|---------------|
|Azure Machine learning Workspace|AzureML Data Scientist|
|ACR linked with Azure Machine learning Workspace|AcrPull|
|Storage linked with Azure Machine learning Workspace|Storage Blob Data Contributor|
|Storage linked with Azure Machine learning Workspace|Storage Table Data Contributor|

## Assign role to user and identity
- Follow this doc to [Assign role in portal](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal)
- Use [this template](../assign-custom-role/) to use this custom role to grand enough permission to use promptflow runtime.
    - You can use [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fcloga%2Fazure-quickstart-templates%2Flochen%2Fpromptflow%2Fquickstarts%2Fmicrosoft.machinelearningservices%2Fmachine-learning-prompt-flow%2Fassign-built-in-roles%2Fazuredeploy.json)
    - Use Azure CLI to deploy this template
        ```bash
        echo "Enter the template file path and file name:"
        read templateFile
        echo "Enter the parameters file path and file name:"
        read parameterFile      
        az deployment group  create \
          --name DeployLocalTemplate \
          --resource-group $resourceGroupName \
          --template-file $templateFile \
          --parameters @$parameterFile \
          --verbose
## Find workspace linked storage and container registry.
- Got to workspace detail page in Azure portal
Find the workspace in the Azure portal 

Or find it's Azure portal link in workspace page.
![workspace-link-in-azure-portal](../media/workspace-link-in-azure-portal.png)

- Find linked storage and container registry
![workspace_linked-storage-acr](../media/workspace-linked-storage-acr.png)

## Find Principle of user
Use `az ad user show --id jondoe@contoso.com --query id` to get principle of user

## Find Principle of identity of managed online endpoint
- Find related endpoint in runtime page
![](../media/endpoint-in-runtime.png)
- Click metrics to jump to endpoint detail page in Azure portal
![](../media/jump-to-managed-online-endpoint-detail-page-in-azure-portal.png)
- Find identity id under identity page
![](../media/principle-id-in-identity-page.png)