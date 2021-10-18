---
title: AI models and business scenarios - AI Builder | Microsoft Docs
description: This topic provides an overview of how the AI model types that you can create in AI Builder relate to various business scenarios.
author: paulnog
ms.service: aibuilder
ms.topic: conceptual
ms.custom:
ms.date: 10/18/2021
ms.author: paulnog
ms.reviewer: v-aangie
---

# AI models and business scenarios

In AI Builder, you can choose from several model types that are suited to different business scenarios. Here are some examples:

- If you want to use intelligence to detect your products in images, you can refine a *custom* AI Builder object detection model. With a customizable model, you'll build, train, and publish it for your intended use.

- If you want to use intelligence to automate your expense reports by scanning and processing business receipts, you can use a *prebuilt* AI Builder receipt scanning model. All prebuilt models allow you to go straight to productivity.

- If you want to design a marketing campaign based on patterns in your historical data, you can use a *custom* prediction model tailored to your business, using your own historical data.

These models are only a few of the ways you can use AI Builder to add intelligence to your business processes.

To build a model with AI Builder:

1. Sign in to [Power Apps](https://make.powerapps.com).

1. On the left pane, select **AI Builder** > **Build**.

1. On the right pane, select the model type that matches what you want to do. Then, you're ready to get started.

> [!div class="mx-imgBorder"]
> ![Screenshot of AI Builder home page.](media/ai-builder-home.png "AI Builder home page")

## Model types

The following table lists the model types, their category, and build type. The AI *category* describes the type of AI that they use (for example, text, prediction, or vision). The *build type* indicates whether it’s customizable (custom) or ready to use (prebuilt).

The build type indicates whether it’s a customizable model that you'll need to build, train, and publish for your intended use, or if it's a prebuilt model that’s ready to use. In general, use custom AI Builder models for applications where you're working with data that’s unique to your business. Use prebuilt models for scenarios that are common across different types of businesses.

[Common business scenarios](#common-business-scenarios) and the model types that are suited to them are described later in this topic.

| **Model type** | **Category** | **Build type** |
| ----- | ----- | ----- |
| Category classification  |Text|[Prebuilt](prebuilt-category-classification.md) and [custom](text-classification-overview.md)  |
| Entity extraction  |Text|[Prebuilt](prebuilt-entity-extraction.md) and [custom](entity-extraction-overview.md)  |
| [Key phrase extraction](prebuilt-key-phrase.md)|Text|Prebuilt |
| [Language detection](prebuilt-language-detection.md)|Text|Prebuilt |
| [Sentiment analysis](prebuilt-sentiment-analysis.md)|Text|Prebuilt |
| [Text translation](prebuilt-text-translation.md)|Text|Prebuilt |
| [Prediction](prediction-overview.md)|Prediction|Custom |
| [Form processing](form-processing-model-overview.md)|Vision|Custom |
| [Object detection](object-detection-overview.md)|Vision|Custom |
| [Business card reader](prebuilt-business-card.md)|Vision|Prebuilt |
| [Text recognition](prebuilt-text-recognition.md)|Vision|Prebuilt |
| [Receipt processing](prebuilt-receipt-processing.md)|Vision|Prebuilt |

## Common business scenarios

The different types of AI models in AI Builder provide you with a broad range of AI capabilities without the need for coding or data expertise. Here are some common business scenarios, and the preferred AI model types for addressing them:

| **Business scenario** | **Model type** |
| ----- | ----- |
Automate customer application processing|Form processing
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

## New home page for AI Builder

We're changing the look of the home page to improve your experience for discovering how AI Builder can help you and your company. We are rolling out the new experience to a random set of users starting October, 2021, and it will eventually be available to all users by the end of calendar year, 2021.

<Add screen of new experience>
  
The new experience enables you to:
- Blah 1
- Blah 2





### Next step

[Build a model](build-model.md)

### See also

[Feature availability by region](availability-region.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
