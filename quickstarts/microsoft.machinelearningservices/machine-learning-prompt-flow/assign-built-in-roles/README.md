# Grant access to promptflow with built-in roles
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fcloga%2Fazure-quickstart-templates%2Flochen%2Fpromptflow%2Fquickstarts%2Fmicrosoft.machinelearningservices%2Fmachine-learning-prompt-flow%2Fassign-built-in-roles%2Fazuredeploy.json)

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