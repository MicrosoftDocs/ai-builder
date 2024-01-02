---
title: AI models and business scenarios - AI Builder | Microsoft Docs
description: This topic provides an overview of how the AI model types that you can create in AI Builder relate to various business scenarios.
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.custom:
ms.date: 01/23/2023
ms.author: plarrue
ms.reviewer: angieandrews
---

# AI models and business scenarios

In AI Builder, you can choose from several model types that are suited to different business scenarios. Here are some examples:

- If you want to use intelligence to detect your products in images, you can refine a *custom* AI Builder object detection model. With a customizable model, you'll build, train, and publish it for your intended use.

- If you want to use intelligence to automate your expense reports by scanning and processing business receipts, you can use a *prebuilt* AI Builder receipt scanning model. All prebuilt models allow you to go straight to productivity.

- If you want to design a marketing campaign based on patterns in your historical data, you can use a *custom* prediction model tailored to your business, using your own historical data.

These models are only a few of the ways you can use AI Builder to add intelligence to your business processes.

To build a model with AI Builder:

1. Sign in to [Power Apps](https://make.powerapps.com) or [Power Automate](https://flow.microsoft.com).

1. On the left pane, select **AI Builder** > **Explore**.

1. On the right pane, select the model type that matches what you want to do. Then, you're ready to get started.

    :::image type="content" source="media/ai-builder-home.png" alt-text="Screenshot of AI Builder home page.":::

## Model types

The following table lists the data type, models type, and build type. 

- The *data type* describes the type of AI that the models use (for example, documents, text, structured data, or images). 

- The *build type* indicates whether it’s a customizable model that you'll need to build, train, and publish for your intended use, or if it's a prebuilt model that’s ready to use. In general, use *custom* AI Builder models for applications where you're working with data that’s unique to your business. Use *prebuilt* models for scenarios that are common across different types of businesses.

[Common business scenarios](#common-business-scenarios) and the model types that are suited to them are described later in this topic.

| Data Type       | Model type              | AI Template table UniqueName mapping          | Build type          |
|-----------------|-------------------------|---------------------|---------------------|
| Documents       | [Business card reader](prebuilt-business-card.md)    | BusinessCard            | Prebuilt            |
| Documents       | [Document processing](form-processing-model-overview.md)         | DocumentScanning, (DocumentLayoutAnalysis is used during training)  | Custom  |
| Documents       | [Text recognition](prebuilt-text-recognition.md)        | TextRecognition            | Prebuilt            |
| Documents       | [Receipt processing](prebuilt-receipt-processing.md)      | ReceiptScanning            | Prebuilt            |
| Documents       | [Invoice processing](prebuilt-invoice-processing.md)      | InvoiceProcessing            | Prebuilt            |
| Documents       | [ID reader](prebuilt-id-reader.md)      | IdentityDocument            | Prebuilt            |
|Text             | [Text generation (preview)](prebuilt-azure-openai.md)         | GptPowerPrompt, (GptPromptEngineering was used during Preview)| Prebuilt  |
| Text            | Category classification  | TextClassificationV2            | [Prebuilt (preview)](prebuilt-category-classification.md) and [custom](text-classification-overview.md) |
| Text            | Entity extraction       | EntityExtraction       | [Prebuilt](prebuilt-entity-extraction.md) and [custom](entity-extraction-overview.md) |
| Text            | [Key phrase extraction](prebuilt-key-phrase.md)   | KeyPhraseExtraction            | Prebuilt            |
| Text            | [Language detection](prebuilt-language-detection.md)      | LanguageDetection            | Prebuilt            |
| Text            | [Sentiment analysis](prebuilt-sentiment-analysis.md)      | SentimentAnalysis            | Prebuilt            |
| Text            | [Text translation](prebuilt-text-translation.md)        | TextTranslation            | Prebuilt            |
| Structured data | [Prediction](prediction-overview.md)              | BinaryPrediction, GenericPrediction | Custom              |
| Images          | [Object detection](object-detection-overview.md)        | ObjectDetection, (ObjectDetectionProposal is used during training) | Custom              |
| Images          | [Image Description](prebuilt-image-description.md)        | ImageDescription | Prebuilt (preview)              |
| Images          | [Text Recognition](prebuilt-text-recognition.md)        | TextRecognition | Prebuilt              |
|           | Preview version of App Copilot      | CopilotSidePanePredict | Prebuilt (preview)              |


## Common business scenarios

The different types of AI models in AI Builder provide you with a broad range of AI capabilities without the need for coding or data expertise. Here are some common business scenarios, and the preferred AI model types for addressing them:

| Business scenario | Model type |
| ----- | ----- |
Automate customer application processing|Document processing
Automate expense reports|Receipt processing
Categorize user feedback based on their focus | Category classification
Extract insights from product reviews | Entity extraction
Identify language of text | Language detection
Identify and classify customer feedback|Sentiment analysis
Translate support requests into your language|Text translation
Identify fraudulent transactions|Prediction
Get alerted to social media posts referencing your brand | Key phrase extraction
Automate contact list |Business card reader
Automate inventory taking|Object detection
Take a photo of text and save it to a database |Text recognition

### Next step

[Build a model](build-model.md)

### See also

[Feature availability by region](availability-region.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
