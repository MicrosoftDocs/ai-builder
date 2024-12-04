---
title: Use the text recognition prebuilt model in Power Automate - AI Builder
description: Learn how to use the text recognition prebuilt model in Power Automate. 
author: antrodfr
ms.topic: conceptual
ms.custom: 
ms.date: 12/04/2024
ms.author: antrod
ms.reviewer: angieandrews
---

# Use the text recognition prebuilt model in Power Automate

The text recognition prebuilt model in AI Builder extracts printed and handwritten text from images and documents. By using this model in Power Automate, you can create workflows that automatically process text from scanned documents, photos, and PDFs, enabling efficient data handling and integration with other applications.

This document provides a guide on using the text recognition prebuilt model in Power Automate.

## Initialize the Power Automate flow

Initializing the Power Automate flow is the first step in setting up your automated process. This step allows you to define the trigger and the initial input parameters for your flow. When you initialize, you can ensure that your flow starts correctly and has the necessary information to process the text recognition tasks efficiently.

To initialize your flow, follow these steps:

1. Sign in to [Power Automate](https://make.powerautomate.com/).
1. On the navigation menu to the left, select **My flows**, and then select **New flow** > **Instant cloud flow**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, and then select **+Add an input** > **File** as the input type.
1. Select **+New step** > **AI Builder**, and then select **Recognize text in an image or a PDF document** in the list of actions.
1. Select the **Image** input, and then select **File Content** from the **Dynamic content** list:

    :::image type="content" source="media/trigger-text-recognition-2.png" alt-text="Screenshot of initializing a Power Automate flow in the 'Parameters' tab.":::

1. To process results, your can either use the full document text, a page text, or the document text line by line.

## Get the full document text or a full page text

If you need to perform an action on the full document text, or on specific page text, this option is useful. An example of using page text is when you want to search for a substring, or pass it to a downstream action.

You can post all the extracted text in a Teams channel using **Full text of the document** from the Dynamic content list.

:::image type="content" source="media/text-flow-fulldoctext.png" alt-text="Screenshot of a trigger text recognition flow.":::

## Get the document text line by line

Getting the document text line by line can be useful if you need to isolate a specific line of text, or reformat the text at your convenience.

1. To create a string variable, select **+New step** > **Control**, and then select **Initialize variable**.
1. Name it **Extracted text** for example.
1. Select **+New step** > **Control**, and then select **Append to string variable**.
1. In the **value** field, select **Text** from the Dynamic content list.

    It autogenerates two **Apply to each** actions as it is reading a list of lines text in a list of pages. You can then post all the extracted text in a Teams channel.

    :::image type="content" source="media/text-flow-example2-2.png" alt-text="Screenshot of getting text line by line.":::

Congratulations! You created a flow that uses a text recognition model. You can continue to build on this flow until it suits your needs. Select **Save** on the top right, and then select **Test** to try out your flow.

## Parameters

The text recognition prebuilt model in AI Builder contains the following input and output parameters.

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
|**Full text of the document** |string |Full text detected |
|**Full text of the page** |string |Full page text detected |

## Related information

[Text recognition overview](prebuilt-text-recognition.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]
