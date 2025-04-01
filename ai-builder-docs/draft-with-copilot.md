---
title: Get started with Copilot
description: Learn how to use Copilot to expedite AI prompt creation.
author: ashbhati
contributors:
  - ashbhati
  - v-aangie
ms.topic: conceptual
ms.date: 04/01/2025
ms.author: ashbhati
ms.reviewer: angieandrews
ms.collection: bap-ai-copilot
---
  
# Get started with Copilot

Prompt builder is the authoring tool for creating AI prompts within Microsoft Power Platform. A better written prompt generalizes well and leads to better outcomes. To help you move faster and reduce the time spent writing prompts from scratch, you can now use Copilot to draft your prompts directly within the tool. Copilot provides intelligent suggestions based on your intent, helping you frame effective prompts while applying prompt engineering best practices. Whether you're designing prompts for summarizing data or generating natural language responses, Copilot gives you a high-quality starting point aligned with your solution goals.

> [!IMPORTANT]
> - This feature is Public Preview.
> - AI Builder prompts run on large language models (LLMs) powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
> - This capability is [limited to some regions](availability-region.md#prompts).
> - This capability might be subject to usage limits or capacity throttling.

This feature empowers makers of all skill levels to create reliable and well-structured prompts quickly, accelerating your agent, app, or workflow development and helping you focus on business outcomes instead of prompt syntax. You can benefit from a Copilot prompt draft on all the prompt builder surfaces.

## Use prompt builder

To access Copilot in prompt builder, follow these steps:

1. Sign in to [Power Apps](https://make.powerapps.com/), [Power Automate](https://make.powerautomate.com/), or [Copilot Studio](https://copilotstudio.microsoft.com/).
1. Depending on the app you're signed in to, do one of the following:
    - (Power Apps or Power Automate) Select **AI hub** > **Prompts** > **Build your own prompt**.
    - (Copilot Studio) Select **Tools** > **Prompts**.
 
    :::image type="content" source="media/draft-with-copilot/sign-in.png" alt-text="Screenshot of a sample screen when you sign in.":::

1. In the **Write your prompt with Copilot** section, type your intent and select **Submit**.

    :::image type="content" source="media/draft-with-copilot/write-prompt.png" alt-text="Screenshot of a prompt written with Copilot.":::

    Copilot suggests a draft prompt based on your intent.
  
1. Review the suggested prompt and select **Keep it**.

    :::image type="content" source="media/draft-with-copilot/keep-it.png" alt-text="Screenshot of a Copilot suggested prompt and the 'Keep it' button.":::

1. Edit the suggested draft from Copilot as per your need, and test the prompt outcomes.

    :::image type="content" source="media/draft-with-copilot/edit-test.png" alt-text="Screenshot of the instructions panel and the model response panel.":::

## FAQ

This section contains frequently asked questions and their answers.

### Can Copilot generate grounded prompts?

Copilot can't generate grounded prompts yet.

### Can Copilot improve my own draft?

Copilot can't improve an existing prompt. It can only be used in generating new drafts.

## Related information

- [Create a prompt](create-a-custom-prompt.md)
- [Get started with prompt library](prompt-library.md)
- [Add text, image, or document input to your prompt](add-inputs-prompt.md)
- [Change the output of your prompt](change-prompt-output.md)
- [Model selection and temperature settings](prompt-modelsettings.md)
- [Use your own data in a prompt](use-your-own-prompt-data.md)
- [Use your prompt in Power Automate](use-a-custom-prompt-in-flow.md)
- [Use your prompt in Power Apps](use-a-custom-prompt-in-app.md)


