---
title: Use the key phrase extraction prebuilt model in Microsoft Flow - AI Builder | Microsoft Docs
description: Provides information about how to set up and use the AI Builder business card reader in model-driven apps 

author: alanabrito
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/12/2019
ms.author: alanab
ms.reviewer: v-dehaas
---


# Use the key phrase extraction prebuilt model in Power Automate

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. [Sign in](https://flow.microsoft.com/signin) to Power Automate, select the **My flows** tab, and then select **Create from blank**.
1. Search for the term *manually*, select **Manually trigger a flow** in the list of triggers, and then select **+ Add an input**.
1. Select **Text** and set as input title: **My Text**.
1. Select **+Add an input** again.
1. Select **Text** and set as input title: *My Language*.
1. Select **+ New step**, search for *Predict*, and then select **Predict Common Data Service (current Environment)** in the list of actions.
1. Specify  the **My Language** field from the trigger in the Language input, and the **My Text** field in Text input.

   > ![Manually trigger flow screen](media/flow-trigger-flow.png "Manually trigger flow screen")

Now you can iterate through the outputs returned by the key phrase extraction model. In the following example, we add each key phrase to a Common Data Service record.

![Add key phrases screen](media/flow-add-phrase.png "Add key phrases in Common Data Service")

Congratulations! You have created a flow that uses your key phrase extraction AI model. Select **Save** on the top right and then select **Test** to try out your flow.
