---
title: Get started with prebuilt prompts
description: Learn about the various prebuilt prompts available to you.
author: DanaMartens
contributors:
  - DanaMartens
  - v-aangie
ms.topic: conceptual
ms.date: 02/16/2024
ms.author: dmartens
ms.reviewer: angieandrews
---

# Get started with prebuilt prompts

The Power Platform empowers makers with prebuilt prompts for common business scenarios such as summarizing, classifying, extracting entities, translating, assessing sentiment, or drafting a reply. These prompts allow you to generate AI-driven responses without the need to manually create a prompt. Instead of specifying both the prompt and the text to process, you can simply provide the text you want to analyze, and the AI will generate the desired output.

You can use prebuilt prompts in multiple experiences, including the following:

- Dataverse low-code plug-ins
- Power Apps formulas
- Power Automate

## Prerequisites  

- An environment in a region where prompts are available.

    To learn if prompts are available in your region, go to [Feature availability by region&mdash;Prompts](availability-region.md#prompts).

- A Power Apps or Dynamics 365 license.
- A Dataverse database installed on the environment.
- An AI Builder add-on.

## Prebuilt prompts you can use 'as-is'

The following tables describe the available prebuilt prompts. If you find a prebuilt prompt you want to use, go to [Use a prebuilt prompt](#use-a-prebuilt-prompt) in this article to learn how to use it in a Dataverse low-code plug-in, a Power Apps app, or a Power Automate flow. If you don't find a prebuilt prompt that meets your needs, you can [create a custom prompt](create-a-custom-prompt.md).

### AISummarize

Summarize the text that you provide. For example, this prompt summarizes an email message or text from a document.

#### Input for AISummarize

| Name | Required | Type | Description   | Values     |
|----------|--------------|----------|-------------------|----------------|
| Text     | Yes          | string   | Text to summarize | Text sentences |

#### Output for AISummarize

| Name       | Description                      | Values     |
|----------------|--------------------------------------|----------------|
| SummarizedText | Summarized version of the input text | Text sentences |

### AISentiment

Detect the sentiment of the text that you provide. For example, this prompt detects whether the sentiment of a customer review is positive, negative, or neutral.

#### Input for AISentiment

| Name | Required | Type | Description   | Values     |
|----------|--------------|----------|-------------------|----------------|
| Text     | Yes          | string   | Text to analyze | Text sentences |

#### Output for AISentiment

| Name       | Description                      | Values     |
|----------------|--------------------------------------|----------------|
| AnalyzedSentiment | Overall sentiment of the analyzed text | Positive, neutral, or negative |

### AIReply

Draft a reply to the message that you provide. For example, this prompt drafts a reply to a customer's review of a product.

#### Input for AIReply

| Name | Required | Type | Description   | Values     |
|----------|--------------|----------|-------------------|----------------|
| Text     | Yes          | string   | Text to respond | Text sentences |

#### Output for AIReply

| **Name**         | **Description**  | **Values**     |
|------------------|------------------|----------------|
| PreparedResponse | A draft message in response to the provided input text | Text sentences |

### AITranslate

Translate text from another language. For example, this prompt translates a customer email or product review. The source language doesn't need to be specified, and is automatically detected.

To learn more about languages supported for the source and target language, go to [Translator language support&mdash;Translation](/azure/ai-services/translator/language-support#translation) and review the list of languages in the **Auto Language Detection** column.

#### Input for AITranslate

| Name | Required | Type | Description   | Values     |
|----------|--------------|----------|-------------------|----------------|
| Text     | Yes          | string   | Text to translate | Text sentences |
| TargetLanguage | No     | string   | Language code to which you want to translate | A valid language code such as en for English |

#### Output for AITranslate

| **Name**         | **Description**  | **Values**     |
|------------------|------------------|----------------|
| TranslatedText | Translated text | Text sentences |

### AIClassify

Classify text into one or more provided categories. For example, the following list of categories may be used to classify issues submitted by your customers:

`["Problem", "Billing", "How To", "Licensing"]`

#### Input for AIClassify

| Name | Required | Type | Description   | Values     |
|----------|--------------|----------|-------------------|----------------|
| Text       | Yes          | string               | Text to classify | Text sentences      |
| Categories | Yes          | table (string array) | Categories       | Table of categories |

#### Output for AIClassify

| **Name**         | **Description**  | **Values**     |
|------------------|------------------|----------------|
| Classification | Category        | Name of selected category |

### AIExtract

Extract specified entities such as registration numbers, phone numbers, or names of people.

#### Input for AIExtract

| Name | Required | Type | Description   | Values     |
|----------|--------------|----------|-------------------|----------------|
| Text     | Yes   | string   | Text from which to extract data | Text sentences    |
| Entity   | Yes          | string   | Entity to extract               | Name of entity to extract |

#### Output for AIExtract

| Name       | Type   | Description  | Values    |
|------------|--------|--------------|-----------|
| ExtractedData | table    | Extracted data that matched the type of entity provided | Table of 0 or more rows of data matching the provided entity. |

## Use a prebuilt prompt

The following sections provide links for how to use a prebuilt prompt in a Dataverse low-code plug-in, a Power App, or a Power Automate flow.

### Use in a Dataverse low-code plug-in

To learn how to use prebuilt prompts in a low-code plug-in, go to Use a prebuilt prompt in a Dataverse low-code plug-in.

### Use in Power Apps

With the exception of AI Translate, each of the prebuilt prompts mentioned above can be used in Power Apps the same way you can use custom prompts. To learn how to use custom or prebuilt prompts in Power Apps, go to [Use your custom prompt in Power Apps](use-a-custom-prompt-in-app.md).

### Use in Power Automate

With the exception of AI Translate, each of the prebuilt prompts mentioned above can be used in Power Automate the same way you can use custom prompts. To learn how to use custom or prebuilt prompts in Power Automate, go to [Use your custom prompt in Power Automate flow](use-a-custom-prompt-in-flow.md).

## Provide feedback

If you have feedback of your experience with the current prebuilt prompts, or ideas for additional prebuilt prompts, you can share your thoughts on the [Power Apps Ideas](https://ideas.powerapps.com/d365community/forum/f1458c72-ae29-ed11-9db2-000d3a8c451e) portaL. To do so, select the **AI Builder** checkbox in the **Categories** list in the **Filters** sidebar.  

### See also

[FAQ for text generation and prompts](faqs-text-generation.md)
