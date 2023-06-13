---
description: These templates grant enough permission to let you use promptflow runtime.
page_type: sample
products:
- azure
- azure-resource-manager
urlFragment: machine-learning-prompt-flow
languages:
- json
- bicep
---
# To use promptflow runtime, you need to grant enough permission to user(CI) of endpoint(MIR).
- Using built-in roles is the simple way to grant permission. you can check [this temple](./assign-built-in-roles/).
- Built-in roles may have too much permission. If you want to grant minimum permissions you can:
    - Create custom role with minimum permission, you can check [this temple](./create-custom-role/).
    - Assign custom role to user(CI) of endpoint(MIR), you can check [this temple](./assign-custom-role/).
 - Create compute instance with custom application which can be used as prompt flow runtime. you can check [this temple](./create-compute-instance-with-custom-application/).

If you are new to Azure Machine Learning prompt flow, see:
- [What is prompt flow](https://promptflow.azurewebsites.net/overview-what-is-prompt-flow.html)
- [Start your prompt flow journey](https://promptflow.azurewebsites.net/quick-start.html)