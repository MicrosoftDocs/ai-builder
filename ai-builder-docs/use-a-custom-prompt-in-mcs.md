---
title: Use your prompt in Copilot Studio
description: Learn how to create and use your prompt in Copilot Studio.
author: phil-cmd
contributors:
  - phil-cmd
  - ashbhati
  - v-aangie
ms.topic: conceptual
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 08/22/2024
ms.author: plarrue
ms.reviewer: angieandrews
---

# Use your prompt in Copilot Studio

Use *prompt in Copilot Studio* to natural language actions as copilot extensions. These actions use the generative AI models from AI Builder and natural language understanding to address specific scenarios for your copilots. This means you can extend the capabilities of your copilots by simply creating natural language based prompt actions.

This article explains the two ways to extend copilots with prompt actions:

- [Prompt action](#add-a-prompt-to-an-ai-plugin): Extend Microsoft copilots with natural language based prompt actions.
- [Topic node](#add-a-prompt-to-a-topic-node): You control how your custom copilot responds in a semi-scripted conversation.

> [!IMPORTANT]
> To use your prompt in a copilot, you need to create it from Copilot Studio.

## Prerequisites

- An environment that’s on the list of [available regions](availability-region.md).
- At least one of the following licenses: Power Apps, Power Automate, or Copilot Studio.
- A Microsoft Dataverse database that's installed on the environment.
- A created or accessible Dataverse table with data.
- (If you don't have a Copilot Studio license) An AI Builder add-on.

## Create a prompt action

Prompt actions are one of the ways to extend Microsoft Copilots. They do this by creating business specific natural language actions. The actions are interpreted by the GPT model to perform the necessary action as instructed. These actions are wrapped within a AI plugin definition, which copilots can invoke at runtime when a matching intent or utterance is encountered.

1. Sign in to [Copilot Studio](https://copilotstudio.microsoft.com/).
1. From the left navigation menu, select **Create**.
1. Select **New Microsoft Copilot action** > **Copilot for Microsoft 365** > **New action** > **Prompt**.

    The **Add a prompt action** wizard opens.

### Use the wizard to create a prompt action

 The **Add a prompt action** wizard is a step-by-step guide for how to create a prompt action.

 1. The first step is **Action details**. In the **Action name** and **Description** fields, add action details like a name and description of the action.

     These details are used by the copilot to perform a semantic matching of the action with the user query. Under **Solution**, a dropdown menu lists all solutions available within the current environment. If you defined a preferred solution, then it's preselected. Otherwise, select the solution you want to use. As an alternative, leave it for the wizard to auto create a new solution for this action.

    :::image type="content" source="media/use-a-custom-prompt-in-mcs/name-description.png" alt-text="Screenshot of prompt details.":::

1. The second step is **Create prompt**. This screen is where you enter the natural language action to describe the task you want GPT to perform.

    1. In the **Prompt** field, enter instructions and data that's used to generate the response pertinent details for the use case. To enable Copilot to pass important pieces of information at the runtime to the prompt action, add input variables. Write your own instructions or begin from one of the existing prompt templates. Examples of prompts are `Summarize text`, `Extract information from text`, and `Classify text`.

        :::image type="content" source="media/use-a-custom-prompt-in-mcs/add-prompt-action.png" alt-text="Screenshot of how to add instructions and data to a prompt.":::

    1. Try out your prompt by selecting **Test prompt**. Your prompt is generated and appears in the **Prompt response** field. You might need to revise and iterate on your prompt to meet your needs.
    1. When you're satisfied with the prompt response, select **Save custom prompt**.
1. The third step is **Select action parameters**. This step ensures descriptive input and output names are selected such that Copilot is able to prefill it with information from user utterance and consume the output from the prompt action.

    1. In the **Input parameters** section, add the input variables that the prompt action needs to generate the response. These are the variables that you want to pass to the prompt action at runtime. You can add multiple input variables.
    1. In the **Output parameters** section, add the output variables that the prompt action generates. These are the variables that you want to receive from the prompt action at runtime.

1. The fourth step is **Review and test**. This step presents the opportunity for a copilot developer to test the prompt plugin by side-loading it in the Copilot for Microsoft 365.
    1. To test the prompt plugin, select **Test action**.
    1. When it's ready to be tested on Copilot for Microsoft 365, select **Open to test**.
    1. After you test the prompt and verify that it performs as expected, select **Publish**.

        :::image type="content" source="media/use-a-custom-prompt-in-mcs/review-test-publish.png" alt-text="Screenshot of how to test and publish your prompt.":::

1. The fifth step is **Publish**. Select it to see the confirmation message, **Your prompt action is now published to Copilot for Microsoft 365**.

    It might take a few minutes for your action to show up in copilot experiences. Meanwhile, you can review information about using and administering actions in [Copilot for Microsoft 365](/copilot/microsoft-365/).

## Add a prompt to a topic node

To guide the copilot's responses in a semi-scripted conversation, add a prompt to a topic node. After you create your custom copilot, you can insert a node prompt in a topic.

1. On the left navigation menu, select **Copilots**, and then select your custom copilot.
1. On the menu at the top of the screen, select **Topics** > **Add a topic**.
1. Select **From blank** > **Add node**.

    :::image type="content" source="media/use-a-custom-prompt-in-mcs/add-node.png" alt-text="Screenshot of how to add a node.":::

1. From the **Add a node** dropdown menu, select **Call an action** > **Create a prompt** (in the **Basic actions** tab). You can also select an existing prompt from the pop-up menu as an action node for current topic.

    :::image type="content" source="media/use-a-custom-prompt-in-mcs/call-an-action.png" alt-text="Screenshot of selecting an action.":::

1. In the **Prompt** field, enter the prompt instructions, grounding data (if needed), and input variables relevant for the use case. The instructions define the action goal for the GPT model, data defines the knowledge that's leveraged to act on the goals, and input variables are placeholders for the information that the copilot sends to this action at the runtime while invoking the action.
1. Select **Test prompt** to test the output for you prompt, and ensure that the responses are compliant with the goals of this action. Provide sample input data that closely resembles the data that Copilot passes to this prompt action.

    :::image type="content" source="media/use-a-custom-prompt-in-mcs/test-prompt.png" alt-text="Screenshot of testing your prompt.":::

1. To finalize and save the action, select **Save custom prompt**. A new node gets added to the topic workflow.
1. Connect the input and output parameters of the prompt action node with input and output variables in the topic.
1. **Save** and **Test** the newly edited topic to ensure that it's compliant with the expectation.

## Add a prompt to an AI plugin

If you want Copilot to decide whether to invoke the prompt based on the user's question, you can add a prompt through an AI plugin.

1. Do steps 1 through 3 in [Add a prompt to a topic node](#add-a-prompt-to-a-topic-node).
1. From the **Add node** dropdown menu, select **Call an action** > **Add a plugin action (preview)** (in the **Plugin (preview)** tab).

    :::image type="content" source="media/use-a-custom-prompt-in-mcs/add-plugin.png" alt-text="Screenshot of the 'Add a plugin action (preview)' action.":::

1. In the **Step 1 of 3: Choose an action** screen, search for and select your prompt in the **Discover an action** field.
1. Select **Finish**.

## Related information

- [Try prompt builder](https://aka.ms/tryprompts) 
- [Prompt engineering guide](https://aka.ms/promptguide)
- [Use prompts to make your copilot perform specific tasks](/microsoft-copilot-studio/nlu-prompt-node)
- [How to use topics in a custom copilot in Copilot Studio](https://community.powerplatform.com/galleries/gallery-posts/?postid=a2fdb837-08bf-4011-a03b-66f27a10aa31)
- [Generate content or extract insights with AI Builder prompts](/microsoft-copilot-studio/copilot-ai-plugins?tabs=m365#generate-content-or-extract-insights-with-ai-builder-prompts)
- [Create AI plugin actions for Microsoft Copilot (preview)](/microsoft-copilot-studio/copilot-ai-plugins?tabs=m365#generate-content-or-extract-insights-with-ai-builder-dynamic-prompts)

