---
title: Use an image classification model by Lobe in Power Automate (preview) - AI Builder | Microsoft Docs
description: Provides information about how to use an image classification model by Lobe in AI Builder.
author: JakeCohenMicrosoft
ms.service: aibuilder
ms.topic: conceptual
ms.custom: intro-internal
ms.date: 11/01/2021
ms.author: jacohe
ms.reviewer: v-aangie
---

# Use an image classification model by Lobe in Power Automate (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

To use your image classification model in a Power Automate flow, you'll need to either create a new model or edit an existing model.

To create a new image classification model:

1. Sign in to [Power Automate](https://flow.microsoft.com/).

1. On the left navigation pane, select **AI Builder** > **Build**.

1. On the right pane, select **Image Classification**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Power Automate home screen.](media/image-classificaion-model-in-flow/power-automate-home.png "Power Automate home")

1. On the Image Classification with Lobe screen, you can:
    1. Download the Lobe app to your desktop.
    1. Learn about Lobe.
    1. Watch a tour of Lobe.
    1. Close the screen.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Image Classification with Lobe screen.](media/image-classificaion-model-in-flow/image-classification-help.png "Image Classification with Lobe")

If you already exported your image classification model from the Lobe application, it exists in your list of AI Builder models and an image classification model type.

To edit an existing model:

1. Sign in to [Power Automate](https://flow.microsoft.com/).

1. On the left navigation pane, select **AI Builder** > **Models**.
  
    1.  Select your image classification model.

    1. Select **More commands** (the three vertical dots) > **Edit**.

1. Select **+New step**.

1. In the **Choose your operation** field, type **predict** and select **Predict AI Builder**.

1. Choose the model you exported from the dropdown.

1. Select the image content from your flow to predict the labels and confidences.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Predict action.](media/image-classificaion-model-in-flow/lobe-predict.png "Predict action")
