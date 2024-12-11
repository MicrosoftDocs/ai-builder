---
title: Get started with prompt library
description: Learn how to access and use the prompt library to expedite AI prompt creation.
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.date: 12/11/2024
ms.author: plarrue
ms.reviewer: angieandrews
ms.collection: bap-ai-copilot
---

# Get started with prompt library

The prompt library feature provides a collection of predesigned prompts, serving as *templates to expedite the creation of AI prompts*. This resource accelerates development, and ensures best practices are followed in prompt engineering. You can modify templates to suit specific needs, adjusting language, tone, and detail to match organizational standards and requirements. The templates cover key areas like document extraction, data transformation, and content generation. This makes it easy for you to find the right starting point for your intelligent automation goals.

> [!IMPORTANT]
> - AI Builder prompts are running on GPT 4o Mini and GPT 4o model versions powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
> - This capability is [limited to some regions](availability-region.md#prompts).
> - This capability might be subject to usage limits or capacity throttling.

You can access the prompt library either through the left navigation menu or the prompt builder. Both options provide access to the same set of templates, allowing you to choose the method that best suits your workflow.

## Use the left navigation menu

To access the prompt library and select a template through the left navigation menu, follow these steps:

1. Sign in to [Power Apps](https://make.powerapps.com/) or [Power Automate](https://make.powerautomate.com/).
1. Select **AI hub** > **Prompts**.
1. From the **Popular templates** list, select a template.

    To get an overview of all templates in the library, select **See all templates**.

    :::image type="content" source="media/prompt-library/all-templates.png" alt-text="Screenshot of the template selection screen in the prompt library.":::

    Alternatively, you can use the **Search** field to find the one you're looking for. You can also search by categories, for example, **Language and text analysis**, **Content creation and management**, and **Tasks and role specific tools**.

    :::image type="content" source="media/prompt-library/template-search.png" alt-text="Screenshot of the search functionality in the prompt library.":::

## Use the prompt builder

To access the prompt library and select a template through the prompt builder, follow these steps:

1. Sign in to [Power Apps](https://make.powerapps.com/) or [Power Automate](https://make.powerautomate.com/).
1. Select **AI hub** > **Prompts**.
1. Select **Build your own prompt**.

    :::image type="content" source="media/prompt-library/byo-prompt.png" alt-text="Screenshot of the build your own prompt option in the prompt library.":::

1. Select **Prompt library**.

    :::image type="content" source="media/prompt-library/prompt-library.png" alt-text="Screenshot of the 'Prompt library' selection in the builder.":::

1. From the **Prompt library** screen, select the template of your choice.

    :::image type="content" source="media/prompt-library/prompt-library-screen.png" alt-text="Screenshot of the template selection in the 'Prompt library' screen.":::

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

Yes. From **Prompt settings**, choose **Standard GPT-4o mini (default)** or **Advanced GPT-4o**.

Learn more in [Generative AI model versions](prompt-modelsettings.md#generative-ai-model-versions).

### Can I select the temperature of a template?

Yes. From **Prompt settings**, select the slider to select the temperature of the AI model.

Learn more in [Temperature](https://go.microsoft.com/fwlink/?linkid=2268182).

### Can I select a Dataverse table in a template?

Yes. From the panel on the right, select **Data used** to add a single Dataverse table

Learn more in [Use your own data in a prompt](use-your-own-prompt-data.md).

### Can I display the prompt library in Microsoft Copilot Studio?

No, it isn't currently available.

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

