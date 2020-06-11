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


# Use the receipt processing prebuilt model in Power Automate


> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. [Sign in](https://flow.microsoft.com/signin) to Power Automate, select the **Create** tab, and then select **Instant flow**.

1. Select **Manually trigger a flow** in the list of triggers, and then select **Create**.

1. Select **File** and set *My receipt* as the input title.

1. Select **+ New step**, search for *AI Builder*, and then select **Process and save information from receipts** in the list of actions.

1. Specify the *My receipt* field from the trigger in the **Receipt file** input.

1. In the successive actions, you can use any of the receipt values from the [model output](prebuilt-receipt-processing#model-output).

>[!NOTE]
> Receipt values are returned as strings. To manipulate them as numbers, you can use the [float](https://docs.microsoft.com/azure/logic-apps/workflow-definition-language-functions-reference#float) or [int](https://docs.microsoft.com/azure/logic-apps/workflow-definition-language-functions-reference#int) conversion functions.

Congratulations! You've created a flow that uses the AI Builder receipt processing model. Select **Save** on the top right, and then select **Test** to try out your flow.


## Parameters
### Input
|Name|Mandatory|Description|Values|
|---------|---------|---------|---------|
|Receipt file|Yes|Receipt to process|JPEG, PNG, or PDF file|

### Output
|Property|Definition|Values|
|---------|---------|---------|
|Merchant name|Merchant name||
|Confidence of merchant name|How confident the model is in its detection|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the detection is accurate.|
|Merchant address|Merchant address||
|Confidence of merchant address|How confident the model is in its detection|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the detection is accurate.|
|Merchant phone number|Merchant phone number||
|Confidence of merchant phone number|How confident the model is in its detection|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the detection is accurate.|
|Transaction date|Transaction date||
|Confidence of transaction date|How confident the model is in its detection|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the detection is accurate.|
|Transaction time|Transaction time||
|Confidence of transaction time|How confident the model is in its detection|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the detection is accurate.|
|Purchased item name|Purchased item name||
|Confidence of purchased item name|How confident the model is in its detection|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the detection is accurate.|
|Purchased item quantity|Purchased item quantity||
|Confidence of purchased item quantity|How confident the model is in its detection|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the detection is accurate.|
|Purchased item price|Purchased item price||
|Confidence of purchased item price|How confident the model is in its detection|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the detection is accurate.|
|Purchased item total price|Purchased item total price||
|Confidence of purchased item total price|How confident the model is in its detection|Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the detection is accurate.|
|Detected text|Line of recognized text||
|Page number of detected text|Which page the line of recognized text is found on||
|Height of detected text|Height of detected text||
|Left position of detected text|Left position of detected text||
|Top position of detected text|Top position of detected text||
|Width of detected text|Width of detected text||
