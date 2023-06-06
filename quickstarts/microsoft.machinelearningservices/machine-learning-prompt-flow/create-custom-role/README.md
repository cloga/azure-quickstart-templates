# Create custom role with mininal permissions to use promptflow runtime
You can create custom role with mininal permissions needed to use promptflow runtime
## Assign role to user and identity
- Follow this doc to [Create or update Azure custom roles](https://learn.microsoft.com/en-us/azure/role-based-access-control/custom-roles-portal)
- Use [this template](../create-custom-role/) to create custom role whic minial permissions to use promptflow runtime.
    - You can use [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fcloga%2Fazure-quickstart-templates%2Flochen%2Fpromptflow%2Fquickstarts%2Fmicrosoft.machinelearningservices%2Fmachine-learning-prompt-flow%2Fcreate-custom-role%2Fazuredeploy.json)
    - Use Azure CLI to deploy this template
        ```bash
        echo "Enter the template file path and file name:"
        read templateFile
        echo "Enter the parameters file path and file name:"
        read parameterFile   
        echo "Enter the location of to store the deployment metadata:"
        read location        
        az deployment sub create \
          --name DeployLocalTemplate \
          --template-file $templateFile \
          --parameters $@parameterFile \
          --location $location \
          --verbose
        ```
## Learn more
- [Deploy resources with ARM templates and Azure CLI](https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-cli)
- [Tutorial - Create and deploy template - Azure Resource Manager](https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/template-tutorial-create-first-template)
- [Azure custom roles - Azure RBAC](https://learn.microsoft.com/en-us/azure/role-based-access-control/custom-roles)