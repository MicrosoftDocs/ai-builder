---
title: Use prebuilt category classification model in Power Automate -  AI Builder | Microsoft Docs
description: Provides information about how to use a prebuilt category classification AI Builder model in Power Automate.
author: nijemcevic

ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 04/24/2020
ms.author: tatn
ms.reviewer: v-dehaas
---

# Use prebuilt category classification model in Power Automate


[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, select **+Add an input**, select **Text** as the input type, and set as input title **My Text**.
1. Select **+ New step**, search for the term **AI Builder**, and then select **Classify text into categories with the standard model** in text in the list of actions.
1. Select the language in the **Language** input and specify the **My Text** field from the trigger in the **Text** input:

1. In the successive actions, you can use any fields and tables extracted by the AI Builder model. The following example, saves each inferred **Classification** and **Confidence score** into a SharePoint list.


Congratulations! You've created a flow that uses a prebuilt category classification AI Builder model. Select **Save** on the top right and then select **Test** to try out your flow.


### Related topic

[Category classification model overview](prebuilt-category-classification.md)
