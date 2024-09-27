---
title: Add inputs to a prompt
description: Learn how to add text, image or document input to a prompt.
author: antrod
contributors:
  - antrod
  - v-aangie
ms.topic: conceptual
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 0926/2024
ms.author: antrod
ms.reviewer: angieandrews
---

# Add text, image or document input to a prompt
Within your prompt, you have the ability to include inputs that will allow users to pass text but also image or document (preview) to the prompt at run time in an app, a flow or a copilot.


> [!IMPORTANT]
> - AI Builder prompts run on GPT 3.5 and GPT 4 models powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
> - This capability is [limited to some regions](availability-region.md#prompts).
> - This capability might be subject to usage limits or capacity throttling.

## Adding an input to a prompt
In the prompt builder experience, you have 2 options to include an input:

- Use the forward slash **/** within your prompt instruction, and select **Text**. Give your input a name and provide a sample data now or later.
:::image type="content" source="media/add-inputs-prompt/add-input-slash.png" alt-text="Add an input using /":::

- Click on the input icon on the top right of the prompt builder experience, then **+ Add input** > **Text**. Give your input a name and provide a sample data now or later.
:::image type="content" source="media/add-inputs-prompt/add-input-menu.png" alt-text="Add an input using menu":::
When using this second option, you need to include the input inside the prompt instruction using the "+ Insert" option at the top of the prompt builder experience.


## Text input
Using text inputs you allows you to perform actions on text content that is dynamically passed to the prompt at run time, such as text summarization, text classification, extracting text information, sentiment analysis of text, text generation and many more.

:::image type="content" source="media/add-inputs-prompt/input-text-summarize.png" alt-text="Summarize with a text input":::

If you are satisfied with your prompt, you can provide a sample value for your text input by clicking on the input icon on the top right of the prompt builder experience and adding text in the **Sample data** field of your input.


## Image or document input (preview)
[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

[!INCLUDE [cc_preview_features_definition](./includes/cc-preview-features-definition.md)]

Using image or document inputs allows you to perform actions on file content that is dynamically passed to the prompt at run time, such as file summarization, file categorization, extracting file information (both textual and visual), asking questions on file and many more. It is also possible to combine both text and document or image inputs.

:::image type="content" source="media/add-inputs-prompt/input-file-extraction.png" alt-text="Extract information from a document":::

If you are satisfied with your prompt, you can provide a sample value for your file input by clicking on the input icon on the top right of the prompt builder experience, and uploading a file in the **Sample data** field of your input.

File type supported with image or document input are PNG, JPG, JPEG, BMP, TIFF and PDF.


## Limitations

- For image or document input, size limitation for the files passed to be prompt is 25Mb in total for all files.
- For image or document input, you can't pass a file with a type other than PNG, JPG, JPEG, BMP, TIFF and PDF.
- Image or document input is not yet supported for prompts in Copilot Studio.


## Related information

- [Use your prompt actions in Copilot Studio](use-a-custom-prompt-in-mcs.md)
- [Use your prompt in Power Apps](use-a-custom-prompt-in-app.md)
- [Use your prompt in Power Automate](use-a-custom-prompt-in-flow.md)
- [Human review for automation with a prompt](azure-openai-human-review.md)
- [FAQ for prompts and text generation capabilities](faqs-text-generation.md)
