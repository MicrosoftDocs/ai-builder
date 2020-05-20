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

1. [Sign in](https://flow.microsoft.com/signin) to Power Automate, select the **Create** tab, and then select **Instant flow**.

1. Select **Manually trigger a flow** in the list of triggers, and then select **Create**.

1. Select **File** and set **My receipt** as the input title.

1. Select **+ New step**, search for the term *Predict*, and then select **Predict - Common Data Service (Current Environment)** in the list of actions.
    >[!NOTE]
    > **Predict Common Data Service (current Environment)** does not appear if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution)

1. Select **Receipt Scanning Model**,  and specify the *My receipt* field from the trigger in the **File** input.
