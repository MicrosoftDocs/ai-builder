---
title: Use the text generation model in Power Automate (deprecated)
description: Learn how to use the text generation model with AI Builder in Power Automate.
author: ashbhati
contributors:
  - ashbhati
  - antrod
  - phil-cmd
  - v-aangie
ms.topic: how-to
ms.custom: bap-template
ms.date: 12/20/2023
ms.author: antrod
ms.reviewer: angieandrews
---

# Use the text generation model in Power Automate (deprecated)

> [!IMPORTANT]
> - This feature is deprecated and won't be visible anymore starting from December 15, 2023.
> - The [new prompt builder feature](use-a-custom-prompt-in-flow.md) should be used instead. To learn more, go to [Migrate to the new prompt builder experience](#migrate-to-the-new-prompt-builder-experience).

## Migrate to the new prompt builder experience

This Power Automate action is deprecated. The [prompt builder action](use-a-custom-prompt-in-flow.md) should be used instead.

If you have flows using the old **Create text with GPT** action, here is the process you need to follow to migrate each of your prompts to the the new **Create text with GPT using a prompt** action:

1. From your flow, copy the prompt text inside the old **Create text with GPT** action.
1. From the Power Automate portal, [create a custom prompt](create-a-custom-prompt.md) using the prompt text you just copied. Note that this new prompt experience requires to add a dynamic parameter: If your previous prompt didn't require one, just add a dummy parameter that you will leave empty when running the prompt.
1. Back to your flow, replace the old **Create text with GPT** action with the new one **Create text using a prompt** and select the prompt you just created. [See how to use a custom prompt inside a flow](use-a-custom-prompt-in-flow.md).
1. Make sure to update the places where the GPT action output is used in the downstream actions of your flow.


## Create text with GPT (deprecated)

Text generation is powered by Azure OpenAI Service, which is built on Generative Pre-trained Transformer (GPT) technology. GPT models are a type of natural language processing model. GPT models are trained on a large body of content to generate human-like text from a prompt. When you combine them with workflow automation, you can use AI models like GPT to automate a variety of tasks. For example, you can build workflows to automatically generate drafts of emails, customer service responses, and product descriptions. You can also use them to generate scripts that allow customer service agents to respond quickly to customer inquiries.

### Prerequisites

Copilot enabled at the tenant level is the prerequisite to use the text generation model in Power Automate (preview).

### Create a prompt

[GPT model prompts](azure-openai-textgen.md#parts-of-a-prompt) have two parts: the *instruction* and the *context*. The instruction tells the model what it should do. The context is the information the model needs to follow the instruction. In an automation task, the instruction is constant and the context is provided by dynamic content.

The following example uses an instant cloud flow, but you can include a GPT model in an automated cloud flow, too.

1. Sign in to [Power Automate](https://make.powerautomate.com).
1. On the left pane, select **My flows**.
1. Select **New flow** > **Instant cloud flow**, and then name your flow.
1. Under **Choose how to trigger this flow**, select **Manually trigger a flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, and then select **+Add an input** > **Text** as the input type.
1. Select **+ New step** > **AI Builder**, and then select **Create text with GPT** in the list of actions.
1. Select **Create instructions** and enter instructions and a sample context. Refine the prompt based on the responses until you're satisfied the model is working as intended.

    :::image type="content" alt-text="Screenshot of the Create prompt page in Power Automate." source="media/azure-openai-model-pauto/create-prompt.png":::

1. Replace the sample context with dynamic content.

In this example, the dynamic content is the topic variable from the previous step. The dynamic content can be anything the model needs to generate a new response every time; for example, an email to generate a response or text from a document to summarize.

### Insert human oversight

AI-generated content can be factually incorrect, inappropriate, or biased. Hence, an approval action is required to ensure [human oversight](azure-openai-textgen.md#human-oversight) in workflows that use AI-generated text before it's posted or used anywhere.

In the following example, you send the AI-generated summary of a text by email after a human reviews it.

1. Select **+ New step** > **Approvals**.
1. In the list of actions, select **Start and wait for an approval of text**.
1. In the list of actions, select **+ New step** > **Condition**.
1. In the **Condition** box, set **Outcome** from the approval step as the condition to check and **Approve** as the positive response to validate.
1. If the condition is true, you can proceed with the email sending. In the body, make sure to select **Accepted text** from the approval step, which is the AI-generated text reviewed by a human.

    :::image type="content" alt-text="Screenshot of inserting human oversight in Power Automate." source="media/azure-openai-model-pauto/post-message.png":::

1. Select **Save**, and then select **Test** to try out your flow.

The human receiving the AI-generated text to review has the possibility to accept, edit, or reject the text.

  :::image type="content" alt-text="Screenshot of approval text edit." source="media/azure-openai-model-pauto/text-approval.png":::

### Input parameters

|Name  |Required  |Type  | Description | Values |
|---------|---------|---------|-------------|--------|
|Prompt/instructions     | Yes        |  String       | The instruction or the prompt for the model to act on   |  Natural language instruction for the model along with the dynamic content that the model can act on  | 

### Output parameters

|Name  |Type  | Description | Values |
|---------|---------|---------|----------|
| Text    |String | Generated text | The response that the model has generated based on the input instructions |
| Finish reason | String  |  Finish reason returned by AI model  | - | 

### See also

[Use your custom prompt in a Power Automate flow (preview)](use-a-custom-prompt-in-flow.md)
