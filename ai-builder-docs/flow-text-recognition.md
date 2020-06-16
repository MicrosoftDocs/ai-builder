---
title: Use the text recognition prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to text recognition prebuilt model in Power Automate 
author: alanabrito
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/30/2019
ms.author: alanab
ms.reviewer: v-dehaas
---

# Use the text recognition prebuilt model in Power Automate

> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, select **+Add an input**, select **File** as the input type, and set as input title **My Image**.
1.	Select **+ New step**, search for **AI Builder** in the Search for filters and actions box, and then select **Recognize text in an image** in the list of actions.
1.	Specify the **My Image** field from the trigger in the **Image** input for your flow:

    > [!div class="mx-imgBorder"]
    > ![Trigger text recognition flow](media/trigger-text-recognition-2.png "Trigger text recognition flow")

1. To process results, select **+New step** and select **Apply to each**. In the field, select **lines** from the AI Builder model. This will automatically create another Apply to each action.
1. In the successive actions, you can use any fields extracted by the AI Builder model. For example, you can extract **Text** field to a SharePoint list:

    > [!div class="mx-imgBorder"]
    > ![Text recognition flow example](media/text-flow-example2-2.png "Text recognition flow example")

Congratulations! You've created a flow that uses a text recognition model. You can continue to build on this flow until it suits your needs. Select **Save** on the top right, and then select **Test** to try out your flow. 

## Parameters
### Input
|Name |Required |Type |Description |
|---------|---------|---------|---------|
|**Image** |Yes |file |Image to analyze|

### Output

**Note:** The detected text is embedded into **lines** sub list of the **results** list. You first need to select the **lines** field from an **Apply to each** action to view all the following fields.

|Name |Type |Description |
|---------|---------|---------|
|**Text** |string |Strings containing the line of text detected|
|**Page number** |string |Page number of the text detected|
|**Coodinates** |float |Coodrinates of the text detected|

### See also

[Text recognition overview](prebuilt-text-recognition.md)

