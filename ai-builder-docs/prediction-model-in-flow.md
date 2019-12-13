---
title: Use prediction model in Power Automate -  AI Builder | Microsoft Docs
description: Provides information about how to use a prediction model in Power Automate.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/12/2019
ms.author: v-dehaas
ms.reviewer: v-dehaas
---

# Use a prediction model in Power Automate

> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **Create from blank**.
1. Enter a name for your flow.
1. Search for *Dynamics365* and then select **When a record is updated**.
1. Select the organization name, and then select the entity that contains your prediction model output.
1. Add new steps to react to updated predictions.

Congratulations—you have created a flow that leverages a prediction AI Builder model. Select **Save** on the top right, and then select **Test** to try out your flow.

To learn more about the triggers and actions, see [Get started with Power Automate](/flow/getting-started).

### Related topic

[prediction model overview](prediction-overview.md)
