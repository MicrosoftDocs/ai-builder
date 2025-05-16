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
1. Add as Action in agent:
![image](https://github.com/user-attachments/assets/af9a3f8f-e7b9-4cfd-b7fd-8dfedcee0d6a)

2.Add prompt as Topic:
 ![image](https://github.com/user-attachments/assets/7ec807b3-37a9-4eeb-8113-590604fe594c)

3. Add from Tools:
![image](https://github.com/user-attachments/assets/93b73721-0fcf-499f-8b48-da3284854746)

## Add and configure a prompt

After you create an agent, add prompt as an action.You can create Prompt

1. In Copilot Studio, select **Tool** > **Prompt**.
![image](https://github.com/user-attachments/assets/2802a427-c59b-4bb3-89c0-f474ea91cf01)

2. At the top of the screen, enter a name for your prompt.
 Enter your prompt in one of the following ways:
    - Write or paste your own prompt under the **Instructions** heading.
    - Get help from Copilot by describing what you want your prompt to so under the **Get started with Copilot** heading. Copilot suggests a prompt for you.

3.On the panel to the left next to **Instructions**, select the dropdown menu in the **Model** field, and select **+** to connect model from Azure AI Foundry.
![image](https://github.com/user-attachments/assets/717d8d08-8311-4693-a418-d51276fb2ff3)


4. In the **Connect a model from Azure AI Foundry** screen, enter information about the model from [Azure AI Foundry / Model
  catalog](https://ai.azure.com/explore/models?tid=72f988bf-86f1-41af-91ab-2d7cd011db47), and then select **Connect**.

   ![image](https://github.com/user-attachments/assets/d81b6a1b-f3f3-46c1-bcae-39ddb681f976)

    5. Your model is now added to the **Model** dropdown menu.
       ![image](https://github.com/user-attachments/assets/434400be-d54d-4133-8944-21de2d47b5ce)

       6. When image input is added the dropdown will only show models from foundary that work with images.
          ![image](https://github.com/user-attachments/assets/98c740f5-0d37-4e1d-9cdc-cfd4d5fd065b)

## How can I manage my foundary model?

1.The Azure AI foundary models are connected by connected. You can set the governace policy for this connector in policy page in PPAC.Under name 'Azure AI Foundary'.
![image](https://github.com/user-attachments/assets/62a6b7a1-9be2-47ba-9ea3-b213c221071b)
2.Each model with which maker has set-up a connection is also available as a connection page.
![image](https://github.com/user-attachments/assets/71e258b2-df47-43b0-ac2c-c8bfa53bae99)

This currently supports models with chat completion type.

### Limitation

Some models, for example 'Mistral', 'O3', and 'O1', aren't supported.

> [!NOTE]
> We recommend you apply Responsible AI (RAI) policies as applicable for the models you want to use and manage that in Azure AI Foundry.
>
> Learn more in [Responsible AI for Azure AI Foundry](/azure/ai-foundry/responsible-use-of-ai-overview).

## Related information

- [Use your prompt actions in Copilot Studio](use-a-custom-prompt-in-mcs.md)
- [Use your prompt in Power Apps](use-a-custom-prompt-in-app.md)
- [Use your prompt in Power Automate](use-a-custom-prompt-in-flow.md)
