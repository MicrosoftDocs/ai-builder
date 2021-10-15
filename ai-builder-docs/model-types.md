---
title: AI models and business scenarios - AI Builder | Microsoft Docs
description: Provides an overview ofhow the AI model types that you can create in AI Builder relate to various business scenraios.
author: v-aangie
ms.service: aibuilder
ms.topic: conceptual
ms.custom:
ms.date: 10/29/2020
ms.author: joshrenn
ms.reviewer: v-aangie
---

# AI models and business scenarios

In AI Builder, you can choose from several model types that are suited to different business scenarios. For example, if you want to use AI to detect your products in images; you’d build, train, and publish  a custom AI Builder object detection model. If you want to use AI to automate your expense reports by scanning and processing business receipts, you could use AI Builder’s prebuilt receipt scanning model, which is ready to use out of the box. To design a marketing campaign based on patterns in your historical data; you’d build, train, and publish a custom prediction model in AI Builder tailored to your business and using your own historical data. These are just a few of the ways you can use AI Builder to add intelligence to your business processes.

To build a model by using AI Builder, sign in to [Power Apps](https://make.powerapps.com) and, in the left pane, select **AI Builder** > **Build**. Select the model type that matches what you want to do, and you're ready to get started.

> [!div class="mx-imgBorder"]
> ![AI Builder home page.](media/ai-builder-home.png "AI Builder home page")

> [!IMPORTANT]
> We're changing the look of the AI Builder home page to improve your experience for learning how AI Builder can help you and your company. We'll first roll it out to a random group, and then to all customers the week of October 24, 2021.
>
> For an overview of AI Builder, go to [What is AI Builder?](overview.md)


## Model types

Let’s look at the different model types that are available in AI Builder, and how they are classified. Later, we’ll look at common business scenarios and the model types that are suited to them.

| **Model type** | **Category** | **Build type** |
| ----- | ----- | ----- |
[Category classification](text-classification-overview.md)|Text|[Prebuilt](prebuilt-category-classification.md) and Custom
[Entity extraction](entity-extraction-overview.md)|Text|[Prebuilt](prebuilt-entity-extraction.md) and Custom
[Key phrase extraction](prebuilt-key-phrase.md)|Text|Prebuilt
[Language detection](prebuilt-language-detection.md)|Text|Prebuilt
[Sentiment analysis](prebuilt-sentiment-analysis.md)|Text|Prebuilt
[Text translation](prebuilt-text-translation.md)|Text|Prebuilt
[Prediction](prediction-overview.md)|Prediction|Custom
[Form processing](form-processing-model-overview.md)|Vision|Custom
[Object detection](object-detection-overview.md)|Vision|Custom
[Business card reader](prebuilt-business-card.md)|Vision|Prebuilt
[Text recognition](prebuilt-text-recognition.md)|Vision|Prebuilt
[Receipt processing](prebuilt-receipt-processing.md)|Vision|Prebuilt

AI Builder models are classified under the type of AI that they use (category), and the built type of the model. The build type indicates whether it’s a customizable model that you have to build, train, and publish for your intended use, or whether it is a prebuilt model  that’s ready to use out of the box. Generally speaking, custom AI Builder models are suited for applications where you are working with data that’s unique to your business. Prebuilt models are available for scenarios that are common across different types of businesses. 

## Common business scenarios

The different types of AI models that AI Builder provides put a broad range of AI capabilities in the hands of businesses without the need for coding or data expertise. But if you’re not a developer or data scientist, you may be wondering what the practical applications of these model types are. While the possibilities are endless, here are some common business scenarios, and the AI model types that are suited to addressing them:

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

### Next step

[Build a model](build-model.md)

### See also

[Feature availability by region](availability-region.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]