---
title: Use the text recognition prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to text recognition prebuilt model in Power Automate 
author: alanabrito
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 04/05/2021
ms.author: alanab
ms.reviewer: v-aangie
---

# Use the text recognition prebuilt model in Power Automate

1. Sign in to [Power Automate](https://flow.microsoft.com/).

1. Select **My flows** in the left pane, and then select **New flow** > **Instant cloud flow**.

1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.

1. Expand **Manually trigger a flow**, and then select **+Add an input** > **File** as the input type.

1. Select **+New step** > **AI Builder**, and then select **Recognize text in an image or a PDF document** in the list of actions.

1. Select the **Image** input, and then select **File Content** from the **Dynamic content** list:

    > [!div class="mx-imgBorder"]
    > ![Trigger text recognition flow.](media/trigger-text-recognition-2.png "Trigger text recognition flow")

1. To process results, select **+New step** > **Control**, and then select **Apply to each**.

1. Select the input, and then select **lines** from the Dynamic content list. This will add **results** to the input and automatically create another **Apply to each** action.

1. In the successive actions, you can use any columns extracted by the AI Builder model. For example, you can extract **Text** into a variable, and then post all the extracted text in a Teams channel:

    > [!div class="mx-imgBorder"]
    > ![Text recognition flow example.](media/text-flow-example2-2.png "Text recognition flow example")

Congratulations! You've created a flow that uses a text recognition model. You can continue to build on this flow until it suits your needs. Select **Save** on the top right, and then select **Test** to try out your flow. 

## Parameters
### Input
|Name |Required |Type |Description |
|---------|---------|---------|---------|
|**Image** |Yes |file |Image to analyze|

### Output

The detected text is embedded into **lines** sub list of the **results** list. You first need to select the **lines** column from an **Apply to each** action to view all the following columns.

|Name |Type |Description |
|---------|---------|---------|
|**Text** |string |Strings containing the line of text detected |
|**Page number** |string |Page number of the text detected |
|**Coordinates** |float |Coordinates of the text detected |

### See also

[Text recognition overview](prebuilt-text-recognition.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]
