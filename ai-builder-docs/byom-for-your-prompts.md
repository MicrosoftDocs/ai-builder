---
title: Bring your own model for your prompts
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

# Bring your own model for your prompts

The *Azure AI Foundry models for prompts* feature is available within Copilot Studio, Power Apps, and Power Automate. This native integration with Azure AI Foundry brings the latest frontier models into your prompts in Copilot Studio.

This includes the following models:

- [OpenAI GPT 4.5](https://azure.microsoft.com/blog/announcing-new-models-customization-tools-and-enterprise-agent-upgrades-in-azure-ai-foundry/?msockid=04801c13147c64e30fc30f7415cf65e4)
- [Llama](/azure/ai-foundry/concepts/models-featured#meta)
- [DeepSeek](https://azure.microsoft.com/blog/deepseek-r1-is-now-available-on-azure-ai-foundry-and-github/?msockid=04801c13147c64e30fc30f7415cf65e4)
- And 1,800 plus more in [Azure AI Foundry / Model
  catalog](https://ai.azure.com/explore/models?tid=72f988bf-86f1-41af-91ab-2d7cd011db47)

You can access a diverse portfolio of AI models, including cutting-edge open-source solutions, industry-specific models, and task-based AI capabilities&mdash;all within the trusted, scalable, and enterprise-ready platform of Copilot Studio. With the native Azure AI Foundry integration, we bring the best capabilities from across our platforms into Copilot Studio to make it your one-stop hub to build agents.

Learn more in [Use your prompt actions in Copilot Studio](use-a-custom-prompt-in-mcs.md).

## Create an agent

To use this feature, create an agent in Copilot Studio for your scenario.

1. Sign in to [Copilot Studio](https://copilotstudio.microsoft.com/).
1. In Copilot Studio, create an agent for your scenario by selecting **Agents** > **New agent** > **Skip to configure**.
1. Fill in the fields, and then select **Create**.

    Learn about alternative instructions in [Create an agent](/microsoft-copilot-studio/authoring-first-bot?tabs=web#create-an-agent).

## Add and configure a topic

After you create an agent, add a topic to it.

1. In Copilot Studio, select **Topics** > **Add a topic**.
1. Specify a trigger for your topic. (Learn more in [Add an event trigger](/microsoft-copilot-studio/authoring-trigger-event)).

1. To add a node, select the plus sign (**+**).
1. To add a prompt, select **Add an action** > **New prompt**.

    :::image type="content" source="media/byom-for-your-prompts/add-prompt.png" alt-text="Screenshot of a trigger and action in Copilot Studio.>":::

1. At the top of the screen, enter a name for your prompt.
1. Enter your prompt in one of the following ways:
    - Write or paste your own prompt under the **Instructions** heading.
    - Get help from Copilot by describing what you want your prompt to so under the **Get started with Copilot** heading. Copilot suggests a prompt for you.

1. On the panel to the left next to **Instructions**, select the dropdown menu in the **Model** field, and select **Connect model from AI Foundry**.

    :::image type="content" source="media/byom-for-your-prompts/connect-from.png" alt-text="Screenshot of the 'Connect model from AI foundry' option in the 'Model' field.>":::

1. In the **Connect a model from Azure AI Foundry** screen, enter information about the model from [Azure AI Foundry / Model
  catalog](https://ai.azure.com/explore/models?tid=72f988bf-86f1-41af-91ab-2d7cd011db47), and then select **Connect**.

    :::image type="content" source="media/byom-for-your-prompts/byom-connect.png" alt-text="Screenshot of the 'Connect a model from Azure AI Foundry' screen.>":::

    Your model is now added to the **Model** dropdown menu.

## Test your prompt

1. In the designer, select the **Prompt** card.
1. To save your topic, select **Save**. You can now use it in your agent.
1. In the Copilot panel, select **Test your Copilot** to test your prompt.

    :::image type="content" source="media/byom-for-your-prompts/save-prompt-topic.png" alt-text="Screenshot of the saved topic.":::

> [!NOTE]
> We recommend you apply Responsible AI (RAI) policies as applicable for the models you want to use and manage that in Azure AI Foundry.
>
> Learn more in [Responsible AI for Azure AI Foundry](/azure/ai-foundry/responsible-use-of-ai-overview).

