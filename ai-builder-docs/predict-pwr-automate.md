---
title: Use Predict action in Power Automate -  AI Builder | Microsoft Docs
description: Provides information about how to use an object detection model in Power Automate
author: Antonio-Rodrigues
manager: cdbellar
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 5/4/2020
ms.author: antrod
ms.reviewer: v-dehaas
---

# Use Predict action in Power Automate


> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

While you can use dedicated actions for each AI Builder model, it is possible to use a **Predict** action that encompasses all the models.

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Select **+ New step**, search for **Predict** in the Search for filters and then select **Predict from AI Builder** or **Predict from Common Data Service". Both actions will offer same features.
1. In the **Model** field, select the model you created or a prebuilt model.
1. 


