---
title: Bring your own model for your prompts (preview)
description: Learn how to bring your own models into your prompts so that you can use them in Microsoft Copilot Studio, Power Apps, and Power Automate.
author: MKBajwa-PM
contributors:
  - MKBajwa-PM
  - v-aangie
ms.topic: article
ms.collection: 
- overview
- bap-ai-copilot
ms.date: 05/19/2025
ms.author: mbajwa
ms.reviewer: angieandrews
---

# Bring your own model for your prompts (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

The *Azure AI Foundry models for prompts* feature is available within Copilot Studio, Power Apps, and Power Automate. This native integration with Azure AI Foundry brings the latest frontier models into your prompts in Copilot Studio.

This includes the following models:

- [OpenAI GPT 4.5](https://azure.microsoft.com/blog/announcing-new-models-customization-tools-and-enterprise-agent-upgrades-in-azure-ai-foundry/?msockid=04801c13147c64e30fc30f7415cf65e4)
- [Llama](/azure/ai-foundry/concepts/models-featured#meta)
- [DeepSeek](https://azure.microsoft.com/blog/deepseek-r1-is-now-available-on-azure-ai-foundry-and-github/?msockid=04801c13147c64e30fc30f7415cf65e4)
- And 1,800 plus more in [Azure AI Foundry / Model
  catalog](https://ai.azure.com/explore/models?tid=72f988bf-86f1-41af-91ab-2d7cd011db47)

> [!IMPORTANT]
> - This is a production-ready preview feature.
>- Production-ready previews are subject to [supplemental terms of use](https://www.microsoft.com/business-applications/legal/supp-powerplatform-preview/).

You can access a diverse portfolio of AI models, including cutting-edge open-source solutions, industry-specific models, and task-based AI capabilities&mdash;all within the trusted, scalable, and enterprise-ready platform of Copilot Studio. With the native Azure AI Foundry integration, we bring the best capabilities from across our platforms into Copilot Studio to make it your one-stop hub to build agents.

Learn how to use your prompt in Copilot Studio, Power Apps, and Power Automate by selecting from the following links:

- [Use your prompt actions in Copilot Studio](use-a-custom-prompt-in-mcs.md)
- [Use your prompt in Power Apps](use-a-custom-prompt-in-app.md)
- [Use your prompt in Power Automate](use-a-custom-prompt-in-flow.md)

## Create an agent

To use this feature, create an agent in Copilot Studio for your scenario.

1. Sign in to [Copilot Studio](https://copilotstudio.microsoft.com/).
1. In Copilot Studio, create an agent for your scenario by selecting **Agents** > **New agent** > **Skip to configure**.
1. Fill in the fields, and then select **Create**.

    Learn about alternative instructions in [Create an agent](/microsoft-copilot-studio/authoring-first-bot?tabs=web#create-an-agent).

## Add a prompt in an agent

You can add a prompt directly as an action to an agent, or add a prompt to a topic.

### Add a tool in an agent

1. In your agent, select the **Tools** tab > **Add a tool**.
1. Select any of your existing prompts, or select **New tool** and select a prompt action.

    :::image type="content" source="media/byom-for-your-prompts/add-tool.png" alt-text="Screenshot of the 'Add tool' screen.":::

### Add a prompt as a topic

Alternatively, you can create a prompt directly in the **Topics** tab in Copilot Studio and add it to the agent.

1. In your agent, select the **Topics** tab.
1. Select the plus sign (**+**) to add a node where you want to add a topic.
1. Select **Add a topic** > **New prompt**.

    :::image type="content" source="media/byom-for-your-prompts/add-tool-in-tab.png" alt-text="Screenshot of adding a tool in the 'Topics' tab.":::

## Add and configure a prompt

After you create an agent, add prompt as an action to create a prompt.

1. In Copilot Studio, select **New tool** > **Prompt**.

    The **Tools** tab contains the tools you can use in Copilot Studio. To use models from Azure AI Foundry, you can use the **Prompt** tool.

    :::image type="content" source="media/byom-for-your-prompts/new-tool-prompt.png" alt-text="Screenshot of the Copilot Studio tools.":::

1. At the top of the screen, enter a name for your prompt.
1. Enter your prompt in one of the following ways:
    - Use your own prompt: Under the **Instructions** heading, write or paste your own prompt.
    - Get help from Copilot: Under the **Get started with Copilot** heading, describe what you want your prompt to do, and then select the right arrow. Copilot suggests a prompt for you.
1. While working with prompts, you can choose a model you want to work with. By default, you have some managed models available. You can also bring in Azure AI Foundry models and use them for your prompt.

    On the panel to the right of **Instructions**, select the dropdown menu in the **Model** field, and select the plus sign (**+**) to connect to a model from Azure AI Foundry.

    :::image type="content" source="media/byom-for-your-prompts/prompt-description.png" alt-text="Screenshot of the 'New Prompt' screen, where you add a prompt and select a model.":::

1. In the **Connect a model from Azure AI Foundry** screen, enter information about the model from [Azure AI Foundry / Model
  catalog](https://ai.azure.com/explore/models?tid=72f988bf-86f1-41af-91ab-2d7cd011db47). Make sure to add the **Model deployment name** and **Base model name** exactly as they appear in Azure AI Foundry.
1. Select **Connect**.

    :::image type="content" source="media/byom-for-your-prompts/connect-foundry-model.png" alt-text="Screenshot of the 'Connect a model from Azure AI Foundry' screen.":::

## Use your model

Your model is now added to the **Model** dropdown menu. You can now select this model for your prompt and add it to the agent. Anytime this prompt runs, it always uses the selected model.

:::image type="content" source="media/byom-for-your-prompts/prompt-model.png" alt-text="Screenshot of the 'Model' dropdown menu.":::

These models also work well with image and documents input. However, some models have a limitation. When image input is added, the dropdown menu shows only models from Azure AI Foundry that work with images. This allows you to select a model where you can be successful when you use images or documents.

:::image type="content" source="media/byom-for-your-prompts/image-doc-models.png" alt-text="Screenshot of the 'Models' dropdown menu with image and document models.":::

The following models work with images:
- Phi-3.5-vision-instruct
- Phi-4-multimodal-instruct
- Phi-3-vision-128k-instruct
- o1
- GPT-4o
- GPT-4o-mini
- GPT-4
- GPT-4.5-preview

## Manage your Azure AI Foundry model

The Azure AI Foundry models are connected by connectors. You can set the governance policy for this connector in the policy page in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/home) under the name 'Azure AI Foundry'. This allows you to add a specific DLP (data loss prevention) policy for these models and the tenant DLP policy.

:::image type="content" source="media/byom-for-your-prompts/ppac-dlp.png" alt-text="Screenshot of the Power Platform admin center 'Data policies' page.":::

Each model where a maker set up a connection is also available as a connection page.

:::image type="content" source="media/byom-for-your-prompts/contoso-connections.png" alt-text="Screenshot of the 'Connections' page in Power Apps.":::

This currently supports models with chat completion type.

### Limitation

Some models, for example **Mistral**, **O3**, **LLana**, and **O4 mini** aren't supported yet.

> [!NOTE]
> We recommend you apply Responsible AI (RAI) policies as applicable for the models you want to use and manage that in Azure AI Foundry.
>
> Learn more in [Responsible AI for Azure AI Foundry](/azure/ai-foundry/responsible-use-of-ai-overview).

## Related information

- [Use your prompt actions in Copilot Studio](use-a-custom-prompt-in-mcs.md)
- [Use your prompt in Power Apps](use-a-custom-prompt-in-app.md)
- [Use your prompt in Power Automate](use-a-custom-prompt-in-flow.md)
