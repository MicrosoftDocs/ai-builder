---
title: Use your prompt in Copilot Studio
description: Learn how to create and use your prompt in Copilot Studio.
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 07/31/2024
ms.author: plarrue
ms.reviewer: angieandrews
---

# Use your prompt in Copilot Studio

Use prompt in Copilot Studio to natural language actions as copilot extensions. These actions use the generative AI models from AI Builder and natural language understanding to address specific scenarios for your copilots. This means you can extend the capabilities of your copilots by simply create natural language based prompt actions.

This article explains the two ways to extend copilots with prompt actions:

- [Prompt action](#add-a-prompt-to-an-ai-plugin): Extend Microsoft Copilots with natural language based prompt actions.
- [Topic node](#add-a-prompt-to-a-topic-node): You control how your custom copilot responds in a semi-scripted conversation.


> [!IMPORTANT]
> To use your prompt in a copilot, you need to create it from Copilot Studio.

## Prerequisites

- An environment that’s on the list of [available regions](availability-region.md).
- At least one of the following licenses: Power Apps, Power Automate, or Copilot Studio.
- A Microsoft Dataverse database that's installed on the environment.
- A created or accessible Dataverse table with data.
- (If you don't have a Copilot Studio license) An AI Builder add-on.

## Creating a prompt action

Prompt action are one of the ways to extend Microsoft Copilots, by creating business specific natural language actions. The actions are interpretted by the GPT model, to perform the necessary action as instructed. These actions are wrapped within a AI Plugin definition, which Copilots can invoke at runtime, when a matching intent/utterance is encountered.

1. Sign in to [Copilot Studio](https://copilotstudio.microsoft.com/).
1. From the left navigation menu, select **Create**.
1. Select **New Microsoft Copilot action** > **Copilot for Microsoft 365** > **New action** > **Prompt**.
1. "Add a prompt action" wizard will open, this is a step by step guide to creating a Prompt action.
1. Start with adding "Action details" like **name** and **description** of the action. These are used by the copilot to perform a semantic matching with of the action with the user query.
<img width="509" alt="image" src="https://github.com/user-attachments/assets/dccb54d7-7f17-46f0-8313-cca30776a002">

1. The next step in the wizard is "Create prompt", this is where you write the natural language action describing the task your want GPT to perform. In the **Prompt** field, enter instructions and data that will be used to generate the response pertinent details for the use case. Input variables should be added, that enables Copilot to pass important pieces of information at the runtime to the prompt action. Write your own instructions or begin from one of the existing prompt templates. Examples of some prompts are "Summarize text", "Extract information from text", and "Classify text" etc.
<img width="785" alt="image" src="https://github.com/user-attachments/assets/06cd5012-a344-4c9c-ad7a-df455398770f">

1. Try out your prompt by selecting **Test prompt**. Your prompt is generated and appears in the **Prompt response** field. You might need to revise and iterate on your prompt to meet your needs. 
1. When the prompt response looks good, select **Save custom prompt**.
1. The next step is to ensure descriptive input and output names are selected such that Copilot will be able to prefill it with information from user utterance and consume the output from the prompt action.
<img width="509" alt="image" src="https://github.com/user-attachments/assets/dca746fa-69b0-4372-aefa-b598dd51484d">

1. "Review and test" step presents the opportunity for copilot developer to test the prompt plugin by side-loading it in the "Copilot for Microsoft 365".
<img width="636" alt="image" src="https://github.com/user-attachments/assets/74999cf9-1d2c-4f8b-a44a-b8c3191bde62">

1. The final step is to **Publish** the prompt once it has been tested and verfied to perform as expected.
<img width="636" alt="image" src="https://github.com/user-attachments/assets/201cf707-f838-47e3-96aa-7581ec35cbdd">

1. Finally you should have a published prompt action to **Copilot for Microsoft 365**.
<img width="730" alt="image" src="https://github.com/user-attachments/assets/8611b39b-c207-4781-bdf8-ab4e5c3c3efb">


## Add a prompt to a topic node

To guide the copilot's responses in a semi-scripted conversation, add a prompt to a topic node. After you create your custom copilot, you can insert a node prompt in a topic.

1. On the left navigation menu, select **Copilots**, and then select your custom copilot.
1. On the menu at the top of the screen, select **Topics** > **Add a topic**.

    :::image type="content" source="media/use-a-custom-prompt-in-mcs/add-topic.png" alt-text="Screenshot of how to add a topic.":::

1. Select **From blank** > **Add node**.

    :::image type="content" source="media/use-a-custom-prompt-in-mcs/add-node.png" alt-text="Screenshot of how to add a node.":::

1. From the **Add a node** dropdown menu, select **Call an action** > **Create a prompt** (in the **Basic actions** tab).

    :::image type="content" source="media/use-a-custom-prompt-in-mcs/create-prompt.png" alt-text="Screenshot of the 'Create a prompt' action.":::

1. In the **Prompt** field, enter instructions and other pertinent details for your use case.

## Add a prompt to an AI plugin

If you want Copilot to decide whether to invoke the prompt based on the user's question, you can add a prompt through an AI plugin.

1. Do steps 1 through 3 in [Add a prompt to a topic node](#add-a-prompt-to-a-topic-node).
1. From the **Add node** dropdown menu, select **Call an action** > **Add a plugin action (preview)** (in the **Plugin (preview)** tab).

    :::image type="content" source="media/use-a-custom-prompt-in-mcs/add-plugin.png" alt-text="Screenshot of the 'Add a plugin action (preview)' action.":::

1. In the **step 1 of 3: Choose an action** screen, search for and select your prompt in the **Discover an action** field.
1. Select **Finish**.

## Related information

- [Try prompt builder](https://aka.ms/tryprompts) 
- [Prompt engineering guide](https://aka.ms/promptguide)
- [Use prompts to make your copilot perform specific tasks](/microsoft-copilot-studio/nlu-prompt-node)
- [How to use topics in a custom Copilot Studio](https://community.powerplatform.com/galleries/gallery-posts/?postid=a2fdb837-08bf-4011-a03b-66f27a10aa31)
- [Generate content or extract insights with AI Builder prompts](/microsoft-copilot-studio/copilot-ai-plugins?tabs=m365#generate-content-or-extract-insights-with-ai-builder-prompts)
- [Create AI plugin actions for Microsoft Copilot (preview)](/microsoft-copilot-studio/copilot-ai-plugins?tabs=m365#generate-content-or-extract-insights-with-ai-builder-dynamic-prompts)

