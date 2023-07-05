---
title: Use your Azure OpenAI Service model in Power Automate (preview)
description: Learn how to use GPT and Azure OpenAI Service model in Power Automate with AI Builder.
author: ashbhati
contributors:
  - ashbhati
  - v-aangie
ms.topic: conceptual
ms.custom: 
ms.date: 03/06/2023
ms.author: ashbhati
ms.reviewer: angieandrews
---

# Use your Azure OpenAI Service model in Power Automate (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

GPT models (Generative Pre-trained Transformer) are a type of natural language processing (NLP) model that's pre-trained on a large corpus of text. These models have become increasingly popular due to their ability to generate human-like text from a given prompt. They're being used in a variety of applications, from text summarization to automated question answering. When combined with workflow automation, the AI models can be used to automate a variety of tasks. For example, GPT models can be used to automatically generate drafts of emails, customer service responses, and product descriptions. They can also be used to generate proposed customer service scripts, allowing customer service agents to quickly respond to customer inquiries.

> [!IMPORTANT]
> - This is a preview feature.
>
> - [!INCLUDE[cc_preview_features_definition](includes/cc-preview-features-definition.md)]
>
> - For more information, go to our [preview terms](https://go.microsoft.com/fwlink/?linkid=2189520).
>
> - This capability is in process of rolling out, and may not be available in your region yet.
>
> - This capability  may be subject to usage limits or capacity throttling.

## Create instructions

By combining the power of these models with Power Automate, you can automate mundane tasks such as writing emails and generating reports, which can free up time for employees to focus on more important tasks. This can lead to increased productivity and cost savings for the company.  

1. Sign in to [Power Automate](https://make.powerautomate.com). 

1. On the left pane, select **My flows**.

1. Select **New flow** > **Instant cloud flow**. 

    You can also select **Automated cloud flow** in case you want to build an automated flow.

1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**. 

1. Expand **Manually trigger a flow**, and then select **+ Add an input**, choose **Text** as the input type, and name it **Topic**. 

1. Select **+ New step** > **AI Builder**, and then select **Create text with GPT on Azure OpenAI Service** in the list of actions.

1. Create your instructions by selecting **Create instructions** and exploring the sample templates or start from a blank.

    Experiment with the prompt and sample context and click **Test it out** to see how it performs.

    :::image type="content" alt-text="Screenshot of the Create instructions screen." source="media/azure-openai-model-pauto/create-instruction.png":::

    The newly created instruction should have the sample context/text replaced by dynamic content, which in this case is the **Topic** variable from the previous step. This dynamic content can be anything that the model needs to have a context to generate new content every time (for example, an email to generate a response or text from a document to summarize).

1. Click **Use instructions in flow** to insert the prompt into the action's **Instructions**.

## Insert human oversight

Whenever you intend to post AI-generated content anywhere, you must decide if you're ok for such content to be posted on your behalf or on behalf of your organization. AI-generation context can be factually incorrect, inappropriate, or biased at times. It's recommended that you employ the safe practice of inserting [human oversight](azure-openai-textgen.md#human-oversight) before posting externally (and even internally to Teams or message boards, for example). 

To insert human oversight:

1. Select **+ New step** > **Approvals**.

1. In the list of actions, select **Start and wait for an approval**.

1. In the list of actions, select **+ New step** > **Condition**.

1. In the **Condition** box, set **Outcome** from the approval step as the condition to check.

1. In the **Condition** box, set **Approve** as the positive response to validate.  

1. If the condition is true (which is **Approve** in this case), select **+ New step** > **Teams**, and then select **Post message in a chat or channel** in the list of actions.

    Use the AI-generated **Text** as the content to post on a desired Teams chat or channel.

    :::image type="content" alt-text="Screenshot of inserting human oversight." source="media/azure-openai-model-pauto/post-message.png":::

Congratulations! You've created a flow that uses an AI Builder create text with GPT capability. Select **Save** on the top right, and then select **Test** to try out your flow.

## Parameters

### Input


|Name  |Required  |Type  | Description | Values |
|---------|---------|---------|-------------|--------|
|Prompt/instructions     | Yes        |  String       | The instruction or the prompt for the model to act on   |  Natural language instruction for the model along with the dynamic content that the model can act on  | 
|Parameters     |  Optional       | JSON        |  Model parameters to optimize the output  |  {<br/>"temperature": 0,<br/>"max_tokens": 750,<br/>"top_p": 1,<br/>"frequency_penalty": 0,<br/>"presence_penalty": 0<br/>} 

### Output

|Name  |Type  | Description | Values |
|---------|---------|---------|----------|
| Text    |String | Generated text | The response that the model has generated based on the input instructions |
| Finish reason | String  |  Finish reason returned by AI model  | TBD | 

### See also

- [Azure OpenAI Service model overview (preview)](prebuilt-azure-openai.md)
- [How text generation in Azure OpenAI Service works (preview)](azure-openai-textgen.md)
- [Use your Azure OpenAI Service model in Power Apps (preview)](azure-openai-model-papp.md)
