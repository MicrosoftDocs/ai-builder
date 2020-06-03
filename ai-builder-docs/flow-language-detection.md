---
title: Use the language detection prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to use the AI Builder language detection prebuilt model in your flows
author: alanabrito

ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/30/2019
ms.author: alanab
ms.reviewer: v-dehaas
---

# Use the language detection prebuilt model in Power Automate

> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).


1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, select **+Add an input**, select **Text** as the input type, and set as input title **My Text**.
1. Select **+ New step**, search for the term **AI Builder**, and then select **Detect the language being used in text** in the list of actions.
1. Specify the **My Text** field from the trigger in the **Text** input for your flow:

    > [!div class="mx-imgBorder"]
    > ![Trigger text flow](media/trigger-text-flow-2.png "Manually trigger a flow screens")

1. In the successive actions, you can use any fields extracted by the AI Builder model. For example, you can add lines to an Excel file using **Language** and **Confidence score**:

    > [!div class="mx-imgBorder"]
    > ![Example](media/text-flow-example-2.png "Example")

Congratulations! You've created a flow that uses a language detection model. Select **Save** on the top right and then select **Test** to try out your flow.

### Related topic

[Language detection overview](prebuilt-language-detection.md)
