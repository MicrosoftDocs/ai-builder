---
title: Use your prediction model in Power Automate - AI Builder | Microsoft Docs
description: Describes how to create a Power Automate flow that uses the real-time prediction feature.
author: billba
ms.topic: conceptual
ms.custom: 
ms.date: 04/05/2021
ms.author: billba
ms.reviewer: angieandrews
---

# Use a prediction model in Power Automate


1. Sign in to [Power Automate](https://flow.microsoft.com/).

1. Select **My flows** in the left pane.

1. Select **New flow** from the menu at the top, and then select a flow in the **Build your own from blank** section. (The example uses **Automated cloud flow**.)

1. Name your flow, and then select **Skip**. Instead of using this screen, you'll select you flow's trigger in the next step by filtering a list.

1. Find your trigger by typing it in the search bar and then selecting it in the **Triggers** list. (The example uses the **When a row is added, modified, or deleted** trigger.)

1. Configure the trigger.

1. If you want to add any steps to prepare your data, select **Next step**.

    > [!div class="mx-imgBorder"]
    > ![Configure the trigger.](media/predict-configure-trigger.png "Configure the trigger")

1. Select **Next step**, enter **predict** in the search bar, and select **Predict** in the **Actions** list.

1. Select your model in the input, and then complete the fields using your data or data from previous steps in the flow.

1. Update the row by using prediction output.

Congratulations! You've created a flow that uses the real-time prediction feature in AI Builder. Select **Save** on the top right, and then select **Test** to try out your flow.

### See also

[Use your prediction model](prediction-use.md)  
[Train your model in AI Builder](train-model.md)  
[Publish your model in AI Builder](publish-model.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]