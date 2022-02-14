---
title: Use entity extraction model in Power Automate - AI Builder | Microsoft Docs
description: Provides step by step instructions to use AI Builder entity extraction in Power Automate.
author: mfotedar
ms.topic: conceptual
ms.custom: 
ms.date: 04/05/2021
ms.author: mfotedar
ms.reviewer: v-aangie
---

# Use the entity extraction prebuilt model in Power Automate

1. Sign in to [Power Automate](https://flow.microsoft.com/).

1. Select **My flows** in the left pane, and then select **New flow** > **Automated cloud flow**.

1. Name your flow, select **When a new email arrives V3 (Office 365 Outlook)** under **Choose your flow's trigger**, and then select **Create**.

1.	Select **+ New step**.

1. In the **Search connectors and actions** input, enter *html to text* to search for and select **Html to text (preview)** in the list of actions.

1. Select the text below the ribbon and select **Body** from the **Dynamic Content** list. This will covert the body your document to plain text.

1. Select **+ New step** > **AI Builder** > **Extract entities from text with the standard model** in the **Actions** list. (If you want to use your own model instead, select **Extract entities from text with one of your custom models**.)

1. In the **Language** input, select or enter your language.

1. In the **Text** input, select **The plain text content** from the **Dynamic content** list.

   > [!div class="mx-imgBorder"]
   > ![Choose an action'.](media/flow-EE-prebuilt1.png "Specify Text")

1. In the successive actions, you can use any columns extracted by the AI Builder model. For example, you can send an email using the **Entity type** and **Entity value** columns.
   > [!div class="mx-imgBorder"]
   > ![Choose an a action'.](media/flow-eep-example.png "Send an email")

Congratulations! You've created a flow that uses an entity extraction model. Select **Save** on the top right, and then select **Test** to try out your flow.

## Parameters

### Input
|Name |Required |Type |Description |Values |
|---------|---------|---------|---------|---------|
|**Text** |Yes |string |Text to analyze|Text sentences |
|**Language** |Yes |string |Language of the text to analyze|List of predefined languages or language code (ex.: "en", "fr", "zh_chs", "ru") |

### Output

|Name |Type |Description |Values |
|---------|---------|---------|---------|
|**Entity type** |string |Type of the entity|Example: DateTime or Organization |
|**Entity value** |string |Content of the entity|Example: June 1 or Contoso |
|**Confidence score** |float |How confident the model is in its prediction|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the extracted value is accurate |
|**Starting location** |integer |Where the entity's first character appear in the line| |
|**Character count** |integer |How long the entity is| |

### See also

[Entity extraction prebuilt model](prebuilt-entity-extraction.md)  
[AI Builder in Power Automate overview](use-in-flow-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]