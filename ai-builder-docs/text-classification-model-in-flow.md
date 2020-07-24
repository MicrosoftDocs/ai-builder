---
title: Use category classification model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to use a category classification model in Power Automate.
author: raaourik
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/03/2020
ms.author: raaourik
ms.reviewer: v-dehaas
---


# Use a category classification custom model in Power Automate

> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, select **+Add an input**, select **Text** as the input type, and set as input title **My Text**.
1. Select **+ New step**, search for **AI Builder** in the Search for filters and actions box, and then select **Classify text into categories with one of your custom models** in the list of actions.
1.	Select the category classification model you want to use, and in the **Text** field add **My Text** from the trigger.

    > [!div class="mx-imgBorder"]
    > ![Select model content](media/flow-ccc-overview.png "Select model content")

1. In the successive actions, you can use any fields and tables extracted by the AI Builder model. The following example, saves each inferred **Classification** and **Confidence score** into a SharePoint list.

    > [!div class="mx-imgBorder"]
    > ![Category classification flow example](media/flow-ccc-example.png "Category classification flow example")

Congratulations! You've created a flow that uses an AI Builder category classification model. Select **Save** on the top right, and then select **Test** to try out your flow.


## Parameters
### Input
|Name |Required |Type |Description |Values |
|---------|---------|---------|---------|---------|
|**AI model** |Yes |model |Category classification model to use for analysis|Trained and published category classification model |
|**Text** |Yes |string |Text to analyze|Text sentences |
|**Language** |Yes |string |Language of the text to analyze|"Detect automatically" or language code (ex.: "en", "fr", "zh_chs", "ru") |


### Output
|Name |Type |Description |Values |
|---------|---------|---------|---------|
|**Classification** |string |Entity identified|Issues, compliment, customer service, documentation, price & billing, staff |
|**Confidence score** |float |How confident the model is in its prediction|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the extracted value is accurate |



### See also

[Overview of the category classification custom model](text-classification-overview.md)
