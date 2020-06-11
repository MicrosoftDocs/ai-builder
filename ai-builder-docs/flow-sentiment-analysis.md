---
title: Use the sentiment analysis prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to use the sentiment analysis prebuilt model in your Flows
author: alanabrito

ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/30/2019
ms.author: alanab
ms.reviewer: v-dehaas
---


# Use the sentiment analysis prebuilt model in Power Automate


> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, select **+Add an input**, select **Text** as the input type, and set as input title **My Text**.
1. Select **+ New step**, search for the term **AI Builder**, and then select **Analyze positive or negative sentiment** in text in the list of actions.
1. Select the language in the **Language** input and specify the **My Text** field from the trigger in the **Text** input:

    > [!div class="mx-imgBorder"]
    > ![Manually trigger flow screen](media/flow-sentiment-analysis-12.png "Manually trigger flow screen")

1. In the successive actions, you can use any fields extracted by the AI Builder model. For example, you can add lines to an Excel file for each sentence using **Sentence sentiment**, **Probability sentence is positive** and **Probability sentence is negative**:

    > [!div class="mx-imgBorder"]
    > ![Add row in Excel](media/flow-sentiment-analysis-22.png "Add row in Excel")

Congratulations! You've created a flow that uses a sentiment analysis model. Select **Save** on the top right and then select **Test** to try out your flow.


## Parameters
### Input
|Name |Required |Type |Description |Values |
|---------|---------|---------|---------|---------|
|**Text** |Yes |string |Text to analyze |Text sentences |
|**Language** |Yes |string | Language of the text to analyze | Item in a list of predefined languages or a language code (ex.: "en", "fr", "zh_chs", "ru")

### Output
|Name |Type |Description |Values |
|---------|---------|---------|---------|
|**Overall text sentiment** |string |Overall sentiment of the analyzed text|Positive, neutral or negative |
|**Probability overall text is positive** |float |Probability of the positive sentiment in the analyzed text|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the identified sentiment is accurate |
|**Probability overall text is negative** |float |Probability of the negative sentiment in the analyzed text|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the identified sentiment is accurate |
|**Probability overall text is neutral** |float |Probability of the neutral sentiment in the analyzed text|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the identified sentiment is accurate |
|**documentScores** |object |Object containing overall scores|Positive, neutral and negative scores |
|**sentences** |List |List of sentence data structures containing sentences overall sentiment and scores |Sentence sentiment, positive, neutral and negative scores |
|**Sentence sentiment** |string |Sentiment of the analyzed sentence|Positive, neutral or negative |
|**Probability sentence is positive** |float |Probability of the positive sentiment in the analyzed sentence|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the identified sentiment is accurate |
|**Probability sentence is negative** |float |Probability of the negative sentiment in the analyzed sentence|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the identified sentiment is accurate |
|**Probability sentence is neutral** |float |Probability of the neutral sentiment in the analyzed sentence|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the identified sentiment is accurate |
|**sentenceScores** |object |Data structure containing sentence scores|Positive, neutral and negative scores |



## Related topic

[Sentiment analysis overview](prebuilt-sentiment-analysis.md)
