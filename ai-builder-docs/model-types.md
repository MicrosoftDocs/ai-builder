---
title: AI model types - AI Builder | Microsoft Docs
description: Provides an overview of the AI model types that you can create in AI Builder.
author: Dean-Haas
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/06/2019
ms.author: joshrenn
ms.reviewer: v-dehaas
---

# AI model types

In AI Builder, AI is based on model types that you choose from, based on your business needs. For example, build an object detection model that recognizes your products in an image, or a prediction model that predicts business outcomes based on patterns that the AI learns from your historical data. Train and publish the model, and it's ready for use in your business.

To build a model by using AI Builder, sign in to [Power Apps](https://make.powerapps.com) and, in the left pane, select **AI Builder** > **Build**. Select the model type that matches what you want to do, and you're ready to get started.

> [!div class="mx-imgBorder"]
> ![AI Builder home page](media/ai-builder-home.png "AI Builder home page")

Different AI model types are designed for various business scenarios. With AI Builder, you can build and train your own AI custom model, designed by you for your specific business requirement. You can also choose from several prebuilt models for common business scenarios. Prebuilt models are ready to use 'out of the box' in Power Apps and Power Automate, without any need to build and train the model.

## Custom AI models

Custom AI models are models that you build by choosing a model type in AI Builder, and then training the model to do a specific AI task by using your data. You select the model type, provide the data, build and train your own unique AI model, and then use or share the model. Build your own custom AI model by using the following AI model types.
<!--"Category" and its values of Prediction, Language, and Vision only seem to occur on this page. I kept expecting to see it used elsewhere or at least for its significance to be explained. Can you expand on it?-->  
| AI model type  | Category| Start here |
|---|---|---|
| Category classification  |Language   | [Overview of the category classification custom model](text-classification-overview.md) |
| Entity extraction  |Language   | [Overview of the entity extraction custom model](entity-extraction-overview.md) |
| Form processing  | Vision   | [Overview of the form-processing model](form-processing-model-overview.md) |
| Object detection  | Vision   | [Overview of the object detection model](object-detection-overview.md) |
| Prediction   | Prediction  | [Overview of the prediction model](prediction-overview.md) |

## Prebuilt AI models

AI Builder features prebuilt AI models that you can use in Power Apps and Power Automate. With a prebuilt model, you get an AI model that Microsoft has built and trained to do a specific task. You don't need to build or train the model yourself to use it. The following prebuilt AI models are available.

| AI model type | Category |Start here |
|--------|--------|--------|
|Business card reader |Vision | [Overview of business card reader](prebuilt-business-card.md)
|Text recognition |Vision | [Overview of text recognition](prebuilt-text-recognition.md)
|Category classification |Language | [Overview of category classification](prebuilt-category-classification.md)
|Key phrase extraction |Language | [Overview of key phrase extraction](prebuilt-key-phrase.md)
|Language detection |Language | [Overview of language detection](prebuilt-language-detection.md)
|Sentiment analysis |Language | [Overview of sentiment analysis](prebuilt-sentiment-analysis.md)
|Receipt processing |Vision | [Overview of receipt processing](prebuilt-receipt-processing.md)
|Text translation |Language | [Overview of text translation](prebuilt-text-translation.md)

### Next step

[Build a model](build-model.md)

### See also

[Feature availability by region](availability-region.md)
