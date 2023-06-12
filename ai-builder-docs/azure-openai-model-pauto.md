---
title: Use your Azure OpenAI Service model in Power Automate (preview)
description: Learn how to use GPT and the Azure OpenAI Service model with AI Builder in Power Automate.
author: ashbhati
contributors:
  - ashbhati
  - v-aangie
ms.topic: how-to
ms.custom: bap-template
ms.date: 03/06/2023
ms.author: ashbhati
ms.reviewer: angieandrews
---

# Use your Azure OpenAI Service model in Power Automate (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

GPT (Generative Pre-trained Transformer) models are a type of natural language processing model. GPT models are trained on a large body of content to generate human-like text from a prompt. When you combine them with workflow automation, you can use AI models like GPT to automate a variety of tasks. For example, you can build workflows to automatically generate drafts of emails, customer service responses, and product descriptions. You can also use them to generate scripts that allow customer service agents to respond quickly to customer inquiries.

> [!IMPORTANT]
>
> - This is a preview feature.
>
> - [!INCLUDE [cc_preview_features_definition](includes/cc-preview-features-definition.md)]
>
> - [View our preview terms](https://go.microsoft.com/fwlink/?linkid=2189520).
>
> - This capability might not be available in your region yet.
>
> - This capability may be subject to usage limits or capacity throttling.

## Create instructions

[GPT model prompts](azure-openai-textgen.md#parts-of-a-prompt) have two parts, the *instruction* and the *context*. The instruction tells the model what it should do. The context is the information the model needs to follow the instruction. In an automation task, the instruction is constant and the context is provided by dynamic content.

The following example uses an instant cloud flow, but you can include a GPT model in an automated cloud flow, too.

1. Sign in to [Power Automate](https://make.powerautomate.com).

1. On the left pane, select **My flows**.

1. Select **New flow** > **Instant cloud flow**, and then name your flow.

1. Under **Choose how to trigger this flow**, select **Manually trigger a flow**, and then select **Create**.

1. Expand **Manually trigger a flow**, and then select **+Add an input** > **Text** as the input type.

1. Select **+ New step** > **AI Builder**, and then select **Create text with GPT on Azure OpenAI Service** in the list of actions.

1. Select **Create instructions** and enter instructions and a sample context. Refine the prompt based on the responses until you're satisfied the model is working as intended.

    :::image type="content" alt-text="Screenshot of the Create instructions page in Power Automate." source="media/azure-openai-model-pauto/create-instruction.png":::

1. Replace the sample context with dynamic content.

In this example, the dynamic content is the topic variable from the previous step. The dynamic content can be anything the model needs to generate a new response every time; for example, an email to generate a response or text from a document to summarize.

## Insert human oversight

AI-generated content can be factually incorrect, inappropriate, or biased. We strongly recommend that you institute a practice of inserting [human oversight](azure-openai-textgen.md#human-oversight) in workflows that use AI-generated text before it's posted or used anywhere.

In the following example, we send the AI-generated summary of a text by email after a human reviews it.

1. Select **+ New step** > **Approvals**.

1. In the list of actions, select **Start and wait for an approval of text**.

1. In the list of actions, select **+ New step** > **Condition**.

1. In the **Condition** box, set **Outcome** from the approval step as the condition to check and **Approve** as the positive response to validate.

1. If the condition is true, you can proceed with the email sending. In the body, make sure to select **Accepted text** from the approval step, which is the AI-generated text reviewed by a human.

    :::image type="content" alt-text="Screenshot of inserting human oversight in Power Automate." source="media/azure-openai-model-pauto/post-message.png":::

1. Select **Save**, and then select **Test** to try out your flow.

The human receiving the AI-generated text to review has the possibility to accept, edit or reject the text.

  :::image type="content" alt-text="Screenshot of approval text edit." source="media/azure-openai-model-pauto/text-approval.png":::


## Input parameters

|Name  |Required  |Type  | Description | Values |
|---------|---------|---------|-------------|--------|
|Prompt/instructions     | Yes        |  String       | The instruction or the prompt for the model to act on   |  Natural language instruction for the model along with the dynamic content that the model can act on  | 
|Parameters     |  Optional       | JSON        |  Model parameters to optimize the output  |  {<br/>"temperature": 0,<br/>"max_tokens": 750,<br/>"top_p": 1,<br/>"frequency_penalty": 0,<br/>"presence_penalty": 0<br/>} 

## Output parameters

|Name  |Type  | Description | Values |
|---------|---------|---------|----------|
| Text    |String | Generated text | The response that the model has generated based on the input instructions |
| Finish reason | String  |  Finish reason returned by AI model  | TBD | 

### See also

[Azure OpenAI Service model overview (preview)](prebuilt-azure-openai.md)  
[How text generation in Azure OpenAI Service works (preview)](azure-openai-textgen.md)  
[Use your Azure OpenAI Service model in Power Apps (preview)](azure-openai-model-papp.md)
