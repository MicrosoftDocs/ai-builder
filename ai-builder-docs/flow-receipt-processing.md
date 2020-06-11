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

1. [Sign in](https://flow.microsoft.com/signin) to Power Automate, select the **Create** tab, and then select **Instant flow**.

1. Select **Manually trigger a flow** in the list of triggers, and then select **Create**.

1. Select **File** and set *My receipt* as the input title.

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
|**Receipt file**|Yes|string|The unique identifier of the receipt file to process|

### Output
|Name|Type|Description|
|---------|---------|---------|
|**Merchant name**|string|Merchant name|
|**Confidence of merchant name**|float|How confident the model is in its detection|
|**Merchant address**|string|Merchant address|
|**Confidence of merchant address**|float|How confident the model is in its detection|
|**Merchant phone number**|string|Merchant phone number|
|**Confidence of merchant phone number**|float|How confident the model is in its detection|
|**Transaction date**|string|Transaction date|
|**Confidence of transaction date**|float|How confident the model is in its detection|
|**Transaction time**|string|Transaction time|
|**Confidence of transaction time**|float|How confident the model is in its detection|
|**Purchased item name**|string|Purchased item name|
|**Confidence of purchased item name**|float|How confident the model is in its detection|
|**Purchased item quantity**|string|Purchased item quantity|
|**Confidence of purchased item quantity**|float|How confident the model is in its detection|
|**Purchased item price**|string|Purchased item price|
|**Confidence of purchased item price**|float|How confident the model is in its detection|
|**Purchased item total price**|string|Purchased item total price|
|**Confidence of purchased item total price**|float|How confident the model is in its detection|
|**Detected text**|string|Line of recognized text|
|**Page number of detected text**|integer|Which page the line of recognized text is found on|
|**Height of detected text**|float|Height of line of text|
|**Left position of detected text**|float|Left position of line of text|
|**Top position of detected text**|float|Top position of line of text|
|**Width of detected text**|float|Width of line of text|


### Related topics

[Receipt processing overview](prebuilt-receipt-processing.md)
