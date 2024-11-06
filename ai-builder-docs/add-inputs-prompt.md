---
title: Add inputs to a prompt
description: Learn how to add text, image, or document input to a prompt.
author: antrod
contributors:
  - ashbhati
  - antoinecellerier
  - antrod
  - v-aangie
ms.topic: conceptual
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 11/06/2024
ms.custom: ignite-2024
ms.author: antrod
ms.reviewer: angieandrews
---

# Add text, image, or document input to a prompt

You can enhance your prompts by allowing users or systems to input text, images, or documents at runtime, whether in an app, a flow, or a copilot. This new capability to incorporate multimodal image and document data is currently in preview. By providing these input modalities, you enable the prompt to act on a diverse range of data types, thereby expanding the usability of the prompt and eliminating the need for developers to explicitly use OCR for processing images and documents.

> [!IMPORTANT]
> - AI Builder prompts run on GPT 4o Mini and GPT 4o models powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
> - This capability is [limited to some regions](availability-region.md#prompts).
> - This capability might be subject to usage limits or capacity throttling.

## Add an input to a prompt

In the prompt builder experience, you have two options to include an input:

- Use the forward slash (**/**) in your prompt instruction, and select **Text**. Give your input a name and provide a sample data now or later.

    :::image type="content" source="media/add-inputs-prompt/add-input-slash.png" alt-text="Add an input using /":::

- Select **Input** at the top right of the prompt builder experience, then **+Add input** > **Text**. Give your input a name and provide a sample data now or later.

    :::image type="content" source="media/add-inputs-prompt/add-input-menu.png" alt-text="Screenshot of adding an input using the menu.":::

    When using this second option, include the input inside the prompt instruction using the **+Insert** option at the top of the prompt builder experience.

## Text input

When you use text inputs, you can perform actions on text content that's dynamically passed to the prompt at run time, such as text summarization, text classification, extracting text information, sentiment analysis of text, text generation, and many more.

:::image type="content" source="media/add-inputs-prompt/input-text-summarize.png" alt-text="Screenshot of summarize with a text input.":::

If you're satisfied with your prompt, you can provide a sample value for your text input by selecting the input icon on the top right of the prompt builder experience and adding text in the **Sample data** field of your input.

## Image or document input (preview)

When you use image or document inputs, you can perform actions on file content that's dynamically passed to the prompt at run time, such as file summarization, file categorization, extracting file information (both textual and visual), asking questions on file, and many more. It's also possible to combine both text and document or image inputs.

[!INCLUDE [cc_preview_features_definition](./includes/cc-preview-features-definition.md)]

When you use image or document inputs, you can perform actions on file content that's dynamically passed to the prompt at run time, such as file summarization, file categorization, extracting file information (both textual and visual), asking questions on file, and many more. It's also possible to combine both text and document or image inputs in the same prompt.

If you're satisfied with your prompt, you can provide a sample value for your file input by selecting the input icon on the top right of the prompt builder experience, and uploading a file in the **Sample data** field of your input.

File types supported with image or document input are PNG, JPG, JPEG, BMP, TIFF, and PDF.

## Limitations

- For image or document input, size limitation for the files passed to be prompt is 25 MB in total for all files.
- For image or document input, you can't pass a file with a type other than PNG, JPG, JPEG, BMP, TIFF, and PDF.
- For image or document input, extracting information from large documents might not be accurate and skip information, especially for table lines.
- There is a limilation of processing documents with less than 50 pages.
- Image or document input isn't yet supported for prompts in Copilot Studio.

## Related information

- [Use your prompt actions in Copilot Studio](use-a-custom-prompt-in-mcs.md)
- [Use your prompt in Power Apps](use-a-custom-prompt-in-app.md)
- [Use your prompt in Power Automate](use-a-custom-prompt-in-flow.md)
- [Human review for automation with a prompt](azure-openai-human-review.md)
- [FAQ for prompts and text generation capabilities](faqs-text-generation.md)
