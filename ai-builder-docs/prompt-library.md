---
title: Get started with prompt library
description: Learn how to access and use the prompt library to expedite AI prompt creation.
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.date: 05/07/2025
ms.author: plarrue
ms.reviewer: angieandrews
ms.collection: bap-ai-copilot
---

# Get started with prompt library

The prompt library feature provides a collection of predesigned prompts, serving as *templates to expedite the creation of AI prompts*. This resource accelerates development, and ensures best practices are followed in prompt engineering. You can modify templates to suit specific needs, adjusting language, tone, and detail to match organizational standards and requirements. The templates cover key areas like document extraction, data transformation, and content generation. This makes it easy for you to find the right starting point for your intelligent automation goals.

> [!IMPORTANT]
> - AI Builder prompts use GPT models powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
> - This capability is [limited to some regions](availability-region.md#prompts).
> - This capability might be subject to usage limits or capacity throttling.

You can access the prompt library either through the left navigation menu or the prompt builder. Both options provide access to the same set of templates, allowing you to choose the method that best suits your workflow.

## Use the left navigation menu

To access the prompt library and select a template through the left navigation menu, follow these steps:

1. Sign in to [Power Apps](https://make.powerapps.com/) or [Power Automate](https://make.powerautomate.com/).
1. Select **AI hub** > **Prompts**.
1. From the **Popular templates** list, select a template.

    To get an overview of all templates in the library, select **See all templates**.

    :::image type="content" source="media/prompt-library/see-all-templates.png" alt-text="Screenshot of the template selection screen in the prompt library.":::

    Alternatively, you can use the **Search** field to find the one you're looking for. You can also search by Job Type for example, **Common**, **Customer service**, **Legal**, **Marketing**, **Communications**, **Information technology**, **Learning**, **HR**, **Finance**, **Architecture**, and **Sales** or by Task for example, **Analyze**, **Classify**, **Create**, **Extract**, and **Summarize**.

    :::image type="content" source="media/prompt-library/prompt-library-select-jobtype-task.png" alt-text="Screenshot of the job type, task, and search functionality in the prompt library.":::

## Use the prompt builder

To access the prompt library and select a template through the prompt builder, follow these steps:

### From Copilot Studio

1. Sign in to [Copilot Studio](https://copilotstudio.com/).
2. On the left navigation pane, select **Tools**.
3. Select **+ Create a Tool**.
4. Select **New Prompt**.
5. Select **Browse prompt library** to search for a template, and select the job type and task of your choice

    :::image type="content" source="media/prompt-library/copilot-studio-browse-prompt-library.png" alt-text="Screenshot of the browse prompt library screen in Copilot Studio Prompt builder.":::
   

### From Power Apps or Power Automate

1. Sign in to [Power Apps](https://make.powerapps.com/) or [Power Automate](https://make.powerautomate.com/).
1. Select **AI hub** > **Prompts**.
1. Select **Build your own prompt**.

    :::image type="content" source="media/prompt-library/select-build-yourown-prompt.png" alt-text="Screenshot of the build your own prompt option in the prompt library.":::

1. Select **Browse prompt library**.

    :::image type="content" source="media/prompt-library/select-browse-prompt-library.png" alt-text="Screenshot of the 'Prompt library' selection in the builder.":::

1. From the **Browse Prompt library** screen, search for a template, and select the job type and task of your choice.

    :::image type="content" source="media/prompt-library/select-prompt-template.png" alt-text="Screenshot of the template selection in the 'Prompt library' screen.":::


## Frequently asked questions

### Can I edit a template?

Yes, you can edit a template to modify it at your convenience and save it with a different name.

### Can I modify the input data of a template?

Yes, you can edit a template and delete its input and add a new input text, image, or document at your convenience.

Learn more in [Add text, image, or document input to a prompt](add-inputs-prompt.md).

### Can I select the output of a template?

Yes, you can use **Text** or **JSON** output format.

Learn more in [Change the output of your prompt](change-prompt-output.md).

### Can I select the GPT model of a template?

Yes. From **Prompt model**, choose a Managed model.

Learn more in [Model version](prompt-modelsettings.md#model-version).

### Can I select the temperature of a template?

Yes. From **Prompt settings**, select the slider to select the temperature of the AI model.

Learn more in [Temperature](https://go.microsoft.com/fwlink/?linkid=2268182).

### Can I select a Dataverse table in a template?

Yes. From the panel on the right, select **Data used** to add a single Dataverse table

Learn more in [Use your own data in a prompt](use-your-own-prompt-data.md).

### Can I display the prompt library in a canvas app?

No. However, if you create a prompt from a template, you can use this prompt in your canvas app.

Learn more in [Use your prompt in Power Apps](use-a-custom-prompt-in-app.md).

### Can I display the prompt library in a flow?

We don't provide this functionality yet. However, if you modify and save a template, you can use your saved prompt and use it in a cloud flow or automated cloud flow.

Learn more in [Use your prompt in Power Automate](use-a-custom-prompt-in-flow.md).

### Are you planning to add more templates?

Yes. Our goal is to provide you with a set of templates that you can use in your business.

### What if I don't see what I need?

Share your thoughts and [suggest an idea](https://go.microsoft.com/fwlink/?linkid=2171994).

### I found a bug with a template. What can I do?

Nice catch! Share it with us on [AI Builder community](share-your-experience.md).


## Related information

- [Create a prompt](create-a-custom-prompt.md)
- [Add text, image, or document input to your prompt](add-inputs-prompt.md)
- [Change the output of your prompt](change-prompt-output.md)
- [Model selection and temperature settings](prompt-modelsettings.md)
- [Use your own data in a prompt](use-your-own-prompt-data.md)
- [Use your prompt in Power Automate](use-a-custom-prompt-in-flow.md)
- [Use your prompt in Power Apps](use-a-custom-prompt-in-app.md)

