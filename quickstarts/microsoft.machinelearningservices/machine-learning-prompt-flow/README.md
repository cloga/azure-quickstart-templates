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
- Built-in roles may have too much permission. If you want to grant minimum permission you can:
    - Custom role with minimum permission, you can check [this temple](./create-custom-role/).
    - Assign custom role to user(CI) of endpoint(MIR), you can check [this temple](./assign-custom-role/).