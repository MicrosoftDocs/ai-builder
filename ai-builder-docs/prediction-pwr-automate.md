---
title: Use your prediction model in Power Automate- AI Builder | Microsoft Docs
description: Describes how to create a Power Automate flow that uses the real-time prediction feature.
author: Dean-Haas
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 04/13/2020
ms.author: rajvirk
ms.reviewer: v-dehaas
---

# Use a prediction model in Power Automate

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Sign in to [Power Automate](https://flow.microsoft.com/).

1. On the **Flows** tab, select **New**, and then select the type. (sample is from "Automated - from blank")<!--What does this mean? Can you put it in context a little better?-->

1. Select the trigger you want, and then select **Create**.

1. Configure the trigger and add any additional steps to prepare data.

> [!div class="mx-imgBorder"]
> ![Configure the trigger](media/predict-configure-trigger.png "Configure the trigger")

1. Add the **Predict** action.

1. Complete all fields using your data, or data from previous steps in the flow.

1. Update the record by using prediction output.

Congratulations! You've created a flow that uses the real-time prediction feature in AI Builder.

### See also

[Use your prediction model](prediction-use.md)  
[Train your model in AI Builder](train-model.md)  
[Publish your model in AI Builder](publish-model.md)
