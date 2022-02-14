---
title: Use image classification model by Lobe in Power Automate (preview) - AI Builder | Microsoft Docs
description: Learn how to use the image classification model from Lobe to predict labels and categorize images in Power Automate.
author: mbeissinger
ms.topic: conceptual
ms.custom: intro-internal
ms.date: 11/15/2021
ms.author: mabeis
contributors:
    - JakeCohenMicrosoft
    - v-aangie
---

# Use an image classification model by Lobe in Power Automate (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

To use your image classification model in a Power Automate flow, you'll need to create a new model or edit an existing one. Then you can add the Power Fx `Prediction` formula to generate results that can help you solve a variety of business problems.

> [!IMPORTANT]
> - This is a preview feature.
> - [!INCLUDE[cc_preview_features_definition](includes/cc-preview-features-definition.md)]
> - This feature is being gradually rolled out across regions and might not be available yet in your region.

## Create a flow in Power Automate

Create a flow in your image classification model. (If you're editing an existing flow type with images, skip this section and go to [Add the Power Fx Prediction formula](#add-the-power-fx-prediction-formula).

1. Sign in to [Power Automate](https://flow.microsoft.com/).

1. Select **My flows** > **New flow**.

1. Select the type of flow you want to create.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the creating a new flow.](media/image-classification-model-in-flow/new-flow.png "Create a new flow")

1. Name your flow, select how you want to trigger your flow under **Choose how to trigger this flow**, and then select **Create**.

## Add the Power Fx Prediction formula

1. From the flow, select **+New step**, and then type **Predict** on the **Choose an operation** search bar.

1. Select **Predict AI Builder**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Choose an operation screen.](media/image-classification-model-in-flow/operation.png "Choose an operation")

1. From the **Model** field dropdown, choose the model you exported.

1. Select the image content from your flow to predict the labels and confidences.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Predict action.](media/image-classification-model-in-flow/lobe-predict.png "Predict action")

## Use a flow with a classification model

A flow that uses a classification model can help you solve a variety of business problems.

The output of your flow contains *prediction* and *labels*. A *prediction* is the predicted label (text) of the input image from your model. *Labels* is the list of labels (text) and the model's confidence (number) for each label on the image. You'll need to loop this output to process the individual labels and confidences.

When you use the *prediction* output, you can:

- Arrange images into folders by label

- Create an Excel spreadsheet to send out as a report

- Apply filtering

When you use the *labels* output, you can:

- Determine actions of images with certain confidence scores

- Send alerts based on confidence scores (for example, different alerts for when scores are above or below 90 percent)

- Send an email with various images

