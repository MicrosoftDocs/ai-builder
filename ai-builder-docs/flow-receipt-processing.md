---
title: Use the receipt processing prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to receipt processing prebuilt model in Power Automate 
author: jarennert

ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 05/20/2020
ms.author: joshrenn
ms.reviewer: v-dehaas
---


# Use the receipt processing prebuilt model in Power Automate (preview)


> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. [Sign in](https://flow.microsoft.com/signin) to Power Automate and select the **My flows** tab.

1. Select **New**, then select **Instant—from blank**.

1. Name your flow, then select **Manually trigger a flow** under **Choose how to trigger this flow**.

1. Select **Create**.

1. Expand **Manually trigger a flow**, then select **+ Add an input**.

1. Select **File** as the input type, then set *My receipt* as the input title.

1. Select **+ New step**, search for *AI Builder*, and then select **Process and save information from receipts** in the list of actions.

1. Specify the *My receipt* field from the trigger in the **Receipt file** input.

1. In the successive actions, you can use any of the receipt values from the [model output](#output).

>[!NOTE]
> Receipt values are returned as strings. To manipulate them as numbers, you can use the [float](https://docs.microsoft.com/azure/logic-apps/workflow-definition-language-functions-reference#float) or [int](https://docs.microsoft.com/azure/logic-apps/workflow-definition-language-functions-reference#int) conversion functions.

Congratulations! You've created a flow that uses the AI Builder receipt processing model. Select **Save** on the top right, and then select **Test** to try out your flow.


## Parameters
### Input
|Name|Required|Type|Description|
|---------|---------|---------|---------|
|**Receipt file**|Yes|string|The receipt file to process|

### Output
|Name|Type|Description|
|---------|---------|---------|
|**Merchant name**|string|Merchant name|
|**Merchant address**|string|Merchant address|
|**Merchant phone number**|string|Merchant phone number|
|**Transaction date**|string|Transaction date|
|**Transaction time**|string|Transaction time|
|**Purchased item name**|string|Purchased item name. Returned as a part of a list of items.|
|**Purchased item quantity**|string|Purchased item quantity. Returned as a part of a list of items.|
|**Purchased item price**|string|Purchased item price. Returned as a part of a list of items.|
|**Purchased item total price**|string|Purchased item total price. Returned as a part of a list of items.|
|**Subtotal**|string|Subtotal|
|**Tax**|string|Tax|
|**Tip**|string|Tip|
|**Total**|string|Total|
|**Confidence of merchant name**|float|How confident the model is in its detection|
|**Confidence of merchant address**|float|How confident the model is in its detection|
|**Confidence of merchant phone number**|float|How confident the model is in its detection|
|**Confidence of transaction date**|float|How confident the model is in its detection|
|**Confidence of transaction time**|float|How confident the model is in its detection|
|**Confidence of purchased item name**|float|How confident the model is in its detection. Returned as a part of a list of items.|
|**Confidence of purchased item quantity**|float|How confident the model is in its detection. Returned as a part of a list of items.|
|**Confidence of purchased item price**|float|How confident the model is in its detection. Returned as a part of a list of items.|
|**Confidence of purchased item total price**|float|How confident the model is in its detection. Returned as a part of a list of items.|
|**Confidence of subtotal**|float|How confident the model is in its detection|
|**Confidence of tax**|float|How confident the model is in its detection|
|**Confidence of tip**|float|How confident the model is in its detection|
|**Confidence of total**|float|How confident the model is in its detection|
|**Detected text**|string|Line of recognized text. Returned as a part of a list of text.|
|**Page number of detected text**|integer|Which page the line of recognized text is found on. Returned as a part of a list of text.|
|**Height of detected text**|float|Height of the line of text. Returned as a part of a list of text.|
|**Left position of detected text**|float|Left position of the line of text. Returned as a part of a list of text.|
|**Top position of detected text**|float|Top position of the line of text. Returned as a part of a list of text.|
|**Width of detected text**|float|Width of the line of text. Returned as a part of a list of text.|


### Related topics

[Receipt processing overview](prebuilt-receipt-processing.md)
