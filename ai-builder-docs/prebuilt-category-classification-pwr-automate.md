---
title: Use prebuilt category classification model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to use a prebuilt category classification AI Builder model in Power Automate.
author: nijemcevic
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 04/24/2020
ms.author: tatn
ms.reviewer: v-dehaas
---

# Use the category classification prebuilt model in Power Automate


1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, select **+Add an input**, select **Text** as the input type, and set as input title **My Text**.
1. Select **+ New step**, search for the term **AI Builder**, and then select **Classify text into categories with the standard model** in text in the list of actions.
1. Select the language in the **Language** input and specify the **My Text** column from the trigger in the **Text** input:

    > [!div class="mx-imgBorder"]
    > ![Select model content](media/flow-ccp-overview.png "Select model content")

1. In the successive actions, you can use any fields and tables extracted by the AI Builder model. The following example, saves each inferred **Classification** and **Confidence score** into a SharePoint list.


    > [!div class="mx-imgBorder"]
    > ![Category classification prebuilt flow example](media/flow-ccp-example.png "Category classification prebuilt flow example")


Congratulations! You've created a flow that uses an AI Builder prebuilt category classification model. Select **Save** on the top right and then select **Test** to try out your flow.



## Parameters
### Input
|Name |Required |Type |Description |Values |
|---------|---------|---------|---------|---------|
|**Text** |Yes |string |Text to analyze|Text sentences |
|**Language** |Yes |string |Language of the text to analyze|List of predefined languages or language code (ex.: "en", "fr", "zh_chs", "ru") |

Congratulations! You've created a flow that uses a prebuilt category classification AI Builder model. Select **Save** in the upper-right corner, and then select **Test** to try out your flow.


### Output
|Name |Type |Description |Values |
|---------|---------|---------|---------|
|**Classification** |string |Entity identified|Issues, compliment, customer service, documentation, price & billing, staff |
|**Confidence score** |float |How confident the model is in its prediction|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the extracted value is accurate |


### See also

[Category classification prebuilt model](prebuilt-category-classification.md)

