---
services: cognitive-services
manager: nitinme
author: gm2552
ms.author: travisw
ms.service: azure-ai-openai
ms.topic: include
ms.date: 08/29/2023
---

## Retrieve required variables

To successfully make a call against Azure OpenAI, you need the following variables. This quickstart assumes you've uploaded your data to an Azure blob storage account and have an Azure Cognitive Search index created. See [Add your data using Azure AI studio](../use-your-data-quickstart.md?pivots=programming-language-studio)

|Variable name | Value |
|--------------------------|-------------|
| `AOAIEndpoint`               | This value can be found in the **Keys & Endpoint** section when examining your Azure OpenAI resource from the Azure portal. Alternatively, you can find the value in **Azure AI studio** > **Chat playground** > **Code view**. An example endpoint is: `https://my-resoruce.openai.azure.com`.|
| `AOAIKey` | This value can be found in **Resource management** > **Keys & Endpoint** section when examining your Azure OpenAI resource from the Azure portal. You can use either `KEY1` or `KEY2`. Always having two keys allows you to securely rotate and regenerate keys without causing a service disruption. |
| `AOAIDeploymentId` | This value corresponds to the custom name you chose for your deployment when you deployed a model. This value can be found under **Resource Management** > **Deployments** in the Azure portal or alternatively under **Management** > **Deployments** in Azure AI studio.|
| `SearchEndpoint` | This value can be found in the **Overview** section when examining your Azure Cognitive Search resource from the Azure portal. |
| `SearchKey` | This value can be found in the **Settings** > **Keys** section when examining your Azure Cognitive Search resource from the Azure portal. You can use either the primary admin key or secondary admin key. Always having two keys allows you to securely rotate and regenerate keys without causing a service disruption. |
| `SearchIndex` | This value corresponds to the name of the index you created to store your data. You can find it in the **Overview** section when examining your Azure Cognitive Search resource from the Azure portal. |

### Environment variables

**NOTE** Spring AI defaults the model name to `gpt-35-turbo`; it is only necessary to provide the SPRING_AI_AZURE_OPENAI_MODEL if you
have deployed a model with a different name.

# [Command Line](#tab/command-line)

```CMD
setx SPRING_AI_AZURE_OPENAI_API_KEY REPLACE_WITH_YOUR_AOAI_KEY_VALUE_HERE
```
```CMD
setx SPRING_AI_AZURE_OPENAI_ENDPOINT REPLACE_WITH_YOUR_AOAI_ENDPOINT_VALUE_HERE
```
```CMD
setx SPRING_AI_AZURE_COGNITIVE_SEARCH_ENDPOINT REPLACE_WITH_YOUR_AZURE_SEARCH_RESOURCE_VALUE_HERE
```
```CMD
setx SPRING_AI_AZURE_COGNITIVE_SEARCH_API_KEY REPLACE_WITH_YOUR_AZURE_SEARCH_RESOURCE_KEY_VALUE_HERE
```
```CMD
setx SPRING_AI_AZURE_COGNITIVE_SEARCH_INDEX REPLACE_WITH_YOUR_INDEX_NAME_HERE
```
```CMD
setx SPRING_AI_AZURE_OPENAI_MODEL "REPLACE_WITH_YOUR_MODEL_NAME_HERE" 
```

# [PowerShell](#tab/powershell)

```powershell
[System.Environment]::SetEnvironmentVariable('SPRING_AI_AZURE_OPENAI_ENDPOINT', 'REPLACE_WITH_YOUR_AOAI_ENDPOINT_VALUE_HERE', 'User')
```

```powershell
[System.Environment]::SetEnvironmentVariable('SPRING_AI_AZURE_OPENAI_API_KEY', 'REPLACE_WITH_YOUR_AOAI_KEY_VALUE_HERE', 'User')
```

```powershell
[System.Environment]::SetEnvironmentVariable('SPRING_AI_AZURE_COGNITIVE_SEARCH_ENDPOINT', 'REPLACE_WITH_YOUR_AZURE_SEARCH_RESOURCE_VALUE_HERE', 'User')
```

```powershell
[System.Environment]::SetEnvironmentVariable('SPRING_AI_AZURE_COGNITIVE_SEARCH_API_KEY', 'REPLACE_WITH_YOUR_AZURE_SEARCH_RESOURCE_KEY_VALUE_HERE', 'User')
```

```powershell
[System.Environment]::SetEnvironmentVariable('SPRING_AI_AZURE_COGNITIVE_SEARCH_INDEX', 'REPLACE_WITH_YOUR_INDEX_NAME_HERE', 'User')
```

```powershell
[System.Environment]::SetEnvironmentVariable('SPRING_AI_AZURE_OPENAI_MODEL', 'REPLACE_WITH_YOUR_MODEL_NAME_HERE', 'User')
```

# [Bash](#tab/bash)

```Bash
export SPRING_AI_AZURE_OPENAI_ENDPOINT=REPLACE_WITH_YOUR_AOAI_ENDPOINT_VALUE_HERE
```
```Bash
export SPRING_AI_AZURE_OPENAI_API_KEY=REPLACE_WITH_YOUR_AOAI_KEY_VALUE_HERE
```
```Bash
export SPRING_AI_AZURE_COGNITIVE_SEARCH_ENDPOINT=REPLACE_WITH_YOUR_AZURE_SEARCH_RESOURCE_VALUE_HERE
```
```Bash
export SPRING_AI_AZURE_COGNITIVE_SEARCH_API_KEY=REPLACE_WITH_YOUR_AZURE_SEARCH_RESOURCE_KEY_VALUE_HERE
```
```Bash
export SPRING_AI_AZURE_COGNITIVE_SEARCH_INDEX=REPLACE_WITH_YOUR_INDEX_NAME_HERE
```
```Bash
echo export SPRING_AI_AZURE_OPENAI_MODEL="REPLACE_WITH_YOUR_MODEL_NAME_HERE" >> /etc/environment && source /etc/environment
```

---

> [!div class="nextstepaction"]
> [I ran into an issue with the setup.](https://microsoft.qualtrics.com/jfe/form/SV_0Cl5zkG3CnDjq6O?PLanguage=SPRING&Pillar=AOAI&Product=ownData&Page=quickstart&Section=Set-up)
