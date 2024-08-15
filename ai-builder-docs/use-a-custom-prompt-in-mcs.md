---
title: Use your prompt in Copilot Studio
description: Learn how to create and use your prompt in Copilot Studio.
author: phil-cmd
contributors:
  - phil-cmd
  - 
  - v-aangie
ms.topic: conceptual
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 08/16/2024
ms.author: plarrue
ms.reviewer: angieandrews
---

# Use your prompt in Copilot Studio

Use AI Builder in Copilot Studio to create prompt actions. These actions use AI Builder and natural language understanding to target specific scenarios and workflows within your business. This means you can extend the AI capabilities of Copilot to suit the unique needs of your business.

This article explains the two paths to add prompts to configure your copilot extensions:

- [Topic node](#add-a-prompt-to-a-topic-node): You control how the copilot responds in a semi-scripted conversation.
- [AI plugin](#add-a-prompt-to-an-ai-plugin): Copilot chooses if it invokes the prompt depending on the user's question.

> [!IMPORTANT]
> To use your prompt in a copilot, you need to create it from Copilot Studio.

## Prerequisites

- An environment that’s on the list of [available regions](availability-region.md).
- At least one of the following licenses: Power Apps, Power Automate, or Copilot Studio.
- A Microsoft Dataverse database that's installed on the environment.
- A created or accessible Dataverse table with data.
- (If you don't have a Copilot Studio license) An AI Builder add-on.

## Create a prompt

Create your prompt in Copilot Studio.

1. Sign in to [Copilot Studio](https://copilotstudio.microsoft.com/).
1. From the left navigation menu, select **Create**.
1. Select **New Microsoft Copilot extension** > **Copilot for Microsoft 365** > **New action** > **Prompt**.
1. In the **Please enter a valid prompt name** field, enter a prompt name.

    You can now start to create a prompt action.

1. In the **Prompt** field, enter instructions and other pertinent details for your use case.

    You can get help from Copilot to help build your prompt by selecting options in the **Try these prompts** section. Examples of some prompts are **Summarize text**, **Extract information from text**, and **Classify text**. Other can provide sentiment analysis or respond to a complaint.

    :::image type="content" source="media/use-a-custom-prompt-in-mcs/valid-prompt.png" alt-text="Screenshot of the screen where you enter a prompt name, instructions, and other pertinent details.":::

1. Try out your prompt by selecting **Test prompt**.

    Your prompt is generated and appears in the **Prompt response** field. You might need to revise your prompt to meet your needs. To revise it, repeat steps 5 and 6 until it meets your satisfaction.

1. When you finish, select **Finalize prompt**.

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

