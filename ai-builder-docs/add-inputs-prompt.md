---
title: Add text, image, or document input to a prompt
description: Learn how to add text, image, or document input to a prompt.
author: antrodfr
contributors:
  - antrodfr
  - chplanty
  - ashbhati
  - antoinecellerier
  - v-aangie
ms.topic: article
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 04/30/2025
ms.custom: ignite-2024
ms.author: antrod
ms.reviewer: angieandrews
---

# Add inputs to a prompt

You can enhance your prompts by allowing users or systems to input text, images, or documents at prompt runtime, whether in an app, a flow, or a copilot agent. By providing these input modalities, you enable the prompt to act on a diverse range of data types, which expands the usability of the prompt.

> [!IMPORTANT]
> - AI Builder prompts run on GPT models powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
> - This capability is [limited to some regions](availability-region.md#prompts).
> - This capability might be subject to usage limits or capacity throttling.

## Add an input to a prompt

To include an input object, type **/** or select **Add content**. Then, select **Text**,  **Image or document** or **Power Fx** in the **Input** section.

:::image type="content" source="media/add-inputs-prompt/custom-prompt-add-input.png" alt-text="Screenshot of adding input.":::

## Text input

When you use text inputs, you can perform actions on text content that dynamically pass to the prompt at runtime, such as text summarization, text classification, extracting text information, sentiment analysis of text, text generation, and more.

:::image type="content" source="media/add-inputs-prompt/input-text-summarize.png" alt-text="Screenshot of summarizing with a text input.":::

If you're satisfied with your prompt, you can provide a sample value for your text input by selecting the input icon on the top right of the prompt builder experience and adding text in the **Sample data** field of your input.

## Image or document input

When you use image or document inputs, you can perform actions on file content that dynamically pass to the prompt at run time, such as file summarization, file categorization, extracting file information (both textual and visual), asking questions on file, and many more. It's also possible to combine both text and document or image inputs in the same prompt.

:::image type="content" source="media/add-inputs-prompt/input-file-extraction.png" alt-text="Screenshot of extracting information from a document.":::

If you're satisfied with your prompt, you can provide a sample value for your file input by selecting the input icon on the top right of the prompt builder experience, and uploading a file in the **Sample data** field of your input.

File types supported with image or document input are PNG, JPG, JPEG, and PDF.

## Power Fx input

When you use Power Fx inputs, you augment your prompt with formulas. You perform operations like retrieving the current date, formatting or searching text, performing calculations, or working with memory tables. You can use any Power Fx functions that aren't related to connectors. You can use your prompt inputs as arguments for the function with this syntax: `Input.'Your input name'`. 

For example, you can get the current date and apply formatting provided as a prompt input with: `Text(Now(), Input.'Date Format')`.

:::image type="content" source="media/add-inputs-prompt/input-power-fx-formula.png" alt-text="Screenshot of using Power Fx formulas in a prompt.":::

Learn more in [Power Fx formula reference overview](/power-platform/power-fx/formula-reference-overview) about the functions available.

## Limitations

- For image or document input, size limitation for the files passed to be prompt is 25 MB in total for all files.
- For image or document input, you can't pass a file with a type other than PNG, JPG, JPEG, and PDF.
- For image or document input, extracting information from large documents might not be accurate and skip information, especially for table lines.
- There's a limitation of processing documents with fewer than 50 pages.
- Image or document input isn't yet supported for prompts in Copilot Studio.

## Related information

- [Use your prompt actions in Copilot Studio](use-a-custom-prompt-in-mcs.md)
- [Use your prompt in Power Apps](use-a-custom-prompt-in-app.md)
- [Use your prompt in Power Automate](use-a-custom-prompt-in-flow.md)
- [Human review for automation with a prompt](azure-openai-human-review.md)
- [FAQ for prompts and text generation capabilities](faqs-text-generation.md)
