---
title: Use category classification model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to use a category classification model in Power Automate.
author: v-aangie
ms.topic: conceptual
ms.custom: 
ms.date: 01/10/2024
ms.author: angieandrews
ms.reviewer: angieandrews
---

# Use a category classification custom model in Power Automate

1. Sign in to [Power Automate](https://flow.microsoft.com/).

1. Select **My flows** in the left pane, and then select **New flow** > **Instant cloud flow**.

1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.

1. Expand **Manually trigger a flow**, and then select **+Add an input** > **Text** as the input type.

1. Replace the word **Input** with **My Text** (also known as the title).

1. Select **+ New step** > **AI Builder**, and then select **Classify text into categories with one of your custom models** in the list of actions.

1. Select the category classification model you want to use, and in the **Text** column add **My Text** from the trigger.

    > [!div class="mx-imgBorder"]
    > ![Screenshot that shows selected model content.](media/flow-ccc-overview.png "Select model content")

1. In the successive actions, use any columns and tables extracted by the AI Builder model.

The following example saves each inferred **Classification** and **Confidence score** into a list created with Microsoft Lists in SharePoint.

> [!div class="mx-imgBorder"]
> ![Screenshot example of Category classification flow example.](media/flow-ccc-example.png "Category classification flow example")

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
|**Classification** |string |Table identified|Issues, compliment, customer service, documentation, price & billing, staff |
|**Confidence score** |float |How confident the model is in its prediction|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the extracted value is accurate |

### See also

- [Overview of the category classification custom model](text-classification-overview.md)
- [Training: Get started with AI Builder category classification (module)](/training/modules/ai-builder-category-classification/)

[!INCLUDE[footer-include](includes/footer-banner.md)]
