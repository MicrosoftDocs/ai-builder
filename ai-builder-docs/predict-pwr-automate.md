---
title: Use Predict action in Power Automate -  AI Builder | Microsoft Docs
description: Provides information about how to use an object detection model in Power Automate
author: Antonio-Rodrigues
manager: cdbellar
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 5/4/2020
ms.author: antrod
ms.reviewer: v-dehaas
---

# Use Predict action in Power Automate


> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

While you can use dedicated actions for each AI Builder model, it is also possible to use a **Predict** action that allows using any AI Builder model.

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Select **+ New step**, search for **Predict** in the Search for filters and then select **Predict from AI Builder** or **Predict from Common Data Service**. Both actions offer the same features.

    > [!div class="mx-imgBorder"]
    > ![Predict action](media/predict-action.png "Predict action")

1. In the **Model** field, select a custom model you created or choose a prebuilt model. Here is the list of the prebuilt models available:
   - Business card reader: BusinessCard model
   - Category classification (prebuilt): CategoryClassification model
   - Entity extraction (prebuilt): EntityExtraction model 
   - Key phrase extraction: KeyPhraseExtraction model
   - Language detection: LanguageDetection model
   - Sentiment analysis: SentimentAnalysis model
   - Text recognition: TextRecognition model
1. To learn more about the input parameters of each model, refer to the documentation explaining how to use the selected model in the following documentation sections:
   - Use a custom AI Builder model in Power Automate
   - Use a prebuilt AI Builder model in Power Automate


