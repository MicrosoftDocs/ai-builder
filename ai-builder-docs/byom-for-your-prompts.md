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
1. Add as Tools in agent: In your agent click on Tools tab>'Add a tool. You can select any of you existing prompts or click on 'New tool' and select prompt action.
![image](https://github.com/user-attachments/assets/3596acab-96d9-4fe3-9c1e-0ce706e5bc28)

You can also create a prompt directly in tools tab in Copilot Studio and it to the agent.

2.Add prompt as Topic:
 ![image](https://github.com/user-attachments/assets/7ec807b3-37a9-4eeb-8113-590604fe594c)



## Add and configure a prompt

After you create an agent, add prompt as an action.You can create Prompt

1. In Copilot Studio, select **Tool** > **Prompt**. The Tools tab has all the different tools you can use in Copilot studio. To use models from foundary you can use prompt tool.
![image](https://github.com/user-attachments/assets/2802a427-c59b-4bb3-89c0-f474ea91cf01)

2. At the top of the screen, enter a name for your prompt.
 Enter your prompt in one of the following ways:
    - Write or paste your own prompt under the **Instructions** heading.
    - Get help from Copilot by describing what you want your prompt to so under the **Get started with Copilot** heading. Copilot suggests a prompt for you.

3.While working with prompts you have an option to choose a model you want to work with. By default you have some managed models available and now you can also bring in Azure AI foundary models and use them for prompt. On the panel to the left next to **Instructions**, select the dropdown menu in the **Model** field, and select **+** to connect model from Azure AI Foundry.
![image](https://github.com/user-attachments/assets/717d8d08-8311-4693-a418-d51276fb2ff3)


4. In the **Connect a model from Azure AI Foundry** screen, enter information about the model from [Azure AI Foundry / Model
  catalog](https://ai.azure.com/explore/models?tid=72f988bf-86f1-41af-91ab-2d7cd011db47), make sure to add base model and deployment name exactly as you see in Azure AI foundary and then select **Connect**.

   ![image](https://github.com/user-attachments/assets/d81b6a1b-f3f3-46c1-bcae-39ddb681f976)

    5. Your model is now added to the **Model** dropdown menu and now you can select this model for your prompt and add it to the agent. Anytime this prompt will be run it will always use the selected model.
       ![image](https://github.com/user-attachments/assets/434400be-d54d-4133-8944-21de2d47b5ce)

       6. These models also work well with image and documents input. However some models have a limitation, so when image input is added the dropdown will only show models from foundary that work with images. This will allow you to make selection of model where you will be successful when you use image or documents.
          ![image](https://github.com/user-attachments/assets/98c740f5-0d37-4e1d-9cdc-cfd4d5fd065b)
Models that work with images: "Phi-3.5-vision-instruct","Phi-4-multimodal-instruct","Phi-3-vision-128k-instruct","o1","gpt-4o","gpt-4o-mini","gpt-4","gpt-4.5-preview".(more will be added soon)
## How can I manage my foundary model?

1.The Azure AI foundary models are connected by connectors. You can set the governace policy for this connector in policy page in PPAC.Under name 'Azure AI Foundary'. This will allow you to add specific DLP policy for these models in addition to the tenant DLP policy.
![image](https://github.com/user-attachments/assets/62a6b7a1-9be2-47ba-9ea3-b213c221071b)
2.Each model with which maker has set-up a connection is also available as a connection page.
![image](https://github.com/user-attachments/assets/71e258b2-df47-43b0-ac2c-c8bfa53bae99)

This currently supports models with chat completion type.

### Limitation

Some models, for example 'Mistral', 'O3', 'LLana' and 'O4 mini', aren't supported yet.They will be available soon.

> [!NOTE]
> We recommend you apply Responsible AI (RAI) policies as applicable for the models you want to use and manage that in Azure AI Foundry.
>
> Learn more in [Responsible AI for Azure AI Foundry](/azure/ai-foundry/responsible-use-of-ai-overview).

## Related information

- [Use your prompt actions in Copilot Studio](use-a-custom-prompt-in-mcs.md)
- [Use your prompt in Power Apps](use-a-custom-prompt-in-app.md)
- [Use your prompt in Power Automate](use-a-custom-prompt-in-flow.md)
