---
description: This template creates an Azure Machine Learning compute instance on behalf of another user with a custom application which can be used as prompt flow runtime
page_type: sample
products:
- azure
- azure-resource-manager
urlFragment: machine-learning-compute-create-computeinstance
languages:
- json
---
# Create an Azure Machine Learning compute instance 
- Follow this doc to [Create and manage compute instance](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-create-manage-compute-instance)
- Use [this template](../create-compute-instance-with-custom-application/) to compute instance with custom application which can be used as prompt flow runtime.
    - You can use [![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fquickstarts%2Fmicrosoft.machinelearningservices%2Fmachine-learning-compute-create-computeinstance%2Fazuredeploy.json)
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
        ```
This template creates an Azure Machine Learning service compute instance on behalf of another user with a custom application which can be used as prompt flow runtime.

If you are new to Azure Machine Learning prompt flow, see:
- [What is prompt flow](https://promptflow.azurewebsites.net/overview-what-is-prompt-flow.html)
- [Start your prompt flow journey](https://promptflow.azurewebsites.net/quick-start.html)
