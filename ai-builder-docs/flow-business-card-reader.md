---
title: Use the business card reader prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to  use the AI Builder business card reader prebuilt model in Power Automate
author: alanabrito
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/12/2019
ms.author: alanab
ms.reviewer: v-dehaas
---

# Use the business card reader prebuilt model in Power Automate

> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, select **+Add an input**, select **File** as the input type, and set as input title **My Image**.
1.	Select **+ New step**, search for **AI Builder** in the Search for filters and actions box, and then select **Read business card information** in the list of actions.
1. Leave **auto** in the **Image type** field as the type can be detected automatically.
1. Specify the **My Image** field from the trigger in the **Image** input for your flow:

    > [!div class="mx-imgBorder"]
    > ![Specify my image](media/flow-bcr.png "Specify my image")


Congratulations! You've created a flow that uses the business card reader AI model. Select  **Save**  on the top right, and then select  **Test**  to try out your flow.

## Example business card reader flow
The following example shows a new contact being created in Common Data Service using the business card data.

   > [!div class="mx-imgBorder"]
   > !['Create new record' screen](media/flow-business-card-overview-2.png "'Create new record' screen")


### Related topic

[Business card reader overview](prebuilt-business-card.md)
