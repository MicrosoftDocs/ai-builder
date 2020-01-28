---
title: Use the sentiment analysis prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to use the sentiment analysis prebuilt model in your Flows
author: alanabrito
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/30/2019
ms.author: alanab
ms.reviewer: v-dehaas
---


# Use the sentiment analysis prebuilt model in Power Automate

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. [Sign in](https://flow.microsoft.com/signin) to Power Automate, select the **My flows** tab, and then select **Create from blank**.

1. Search for the term *manually*, select **Manually trigger a flow** in the list of triggers, and then select **+ Add an input**.

1. Select **Text**, and set as input title: **My Text**.

1. Select **+Add an input** again.

1. Select **Text** and set as input title: *My Language*.

1. Select **+ New step**, search for *Predict*, and then select **Predict Common Data Service (current Environment)** in the list of actions.

1. Select **SentimentAnalyses model**.

1. Specify  the **My Language** field from the trigger in the Language input, and the **My Text** field in Text input.
   > ![Manually trigger flow screen](media/flow-sentiment-analysis.png "Manually trigger flow screen")
   
Now you can use the sentiment properties detected by the sentiment analysis model. In the following example, we set the Sentiment property to a new Common Data Service record.

![Update record](media/flow-update-sentiment.png "Update record")

Congratulations! You've created a flow that uses a sentiment analysis model. Select **Save** on the top right and then select **Test** to try out your flow.
