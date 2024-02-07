---
title: Create a category classification custom model - AI Builder
description: Learn how to create a category classification model.
author: ashishb
contributors:
   - ashishb
   - phil-cmd
   - v-aangie
ms.topic: conceptual
ms.custom: 
ms.date: 01/10/2024
ms.author: ashbhati
ms.reviewer: angieandrews
---

# Create a category classification custom model

Now that you have your training data in Microsoft Dataverse, you can create a new model and configure it.

1. Sign in to [Power Apps](https://make.powerapps.com/) or [Power Automate](https://make.powerautomate.com)
2. In the left pane, select **... More**, select **AI hub**.
3. Under Discover an AI capability, select **AI models**.

      _(Optional) To keep AI models permanently on the menu for easy access, select the pin icon._

4. Select **Text**.
5. Select **Category classification - Classify texts into custom categories**. 

1. Read the **Classify texts into custom categories** page, and then select **Create custom model**.

1. Choose **Select text**, select the table, select the column where your training text is stored, and then choose **Select column**.

1. Select **Next**.

1. Choose **Select tags**, select the column where the tags are stored, and then choose **Select column**.

1. (If not pre-selected) Select the separator you used for your tags, and then select **Next**.

1. Review your text and tags to verify the data and the configuration you applied, and then select **Next**.

1. Select the language you want to use for training, and then select **Next**.


That's it! Now you can train your AI model.

### Next step

[Train your category classification model](train-text-classification-model.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
