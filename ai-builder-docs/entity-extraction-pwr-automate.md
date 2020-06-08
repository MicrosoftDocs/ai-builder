---
title: Use an AI Builder custom entity extraction AI model in Power Automate -  AI Builder | Microsoft Docs
description: Provides steps to use a custom entity extraction AI model in Power Automate.
author: mfotedar

ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 04/08/2020
ms.author: mfotedar
ms.reviewer: v-dehaas
---

# Use an AI Builder custom entity extraction AI model in Power Automate (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, select **+Add an input**, select **Text** as the input type, and set as input title **My Text**.
1. Select **+ New step**, search for **AI Builder** in the Search for filters and actions box, and then select **Extract entities from text with one of your custom models** in the list of actions.
1.	Select the entity extraction model you want to use, and in the **Text** field add **My Text** from the trigger.

    > [!div class="mx-imgBorder"]
    > ![Select model content](media/flow-eec-overview.png "Select model content")

1. In the successive actions, you can use any fields and tables extracted by the AI Builder model. The following example saves each inferred **Entity type**, **Entity value** and **Confidence score** into an Excel table.

    > [!div class="mx-imgBorder"]
    > ![Entity extraction flow example](media/flow-eec-example.png "Entity extraction flow example")

Congratulations! You've created a flow that uses an AI Builder entity extraction model. Select **Save** on the top right, and then select **Test** to try out your flow.
