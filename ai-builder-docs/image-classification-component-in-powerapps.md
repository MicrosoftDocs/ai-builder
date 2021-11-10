---
title: Use an image classification model by Lobe in Power Apps (preview) - AI Builder | Microsoft Docs
description: Provides information about how to use an image classification model by Lobe in Power Apps.
author: JakeCohenMicrosoft
ms.service: aibuilder
ms.topic: conceptual
ms.custom: intro-internal
ms.date: 11/15/2021
ms.author: jacohe
ms.reviewer: v-aangie
---

# Use an image classification model by Lobe in Power Apps (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

To use your image classification model with Power Fx, first you need to register it as a data source in your app. To learn how to do this, go to [Integrate the registered model](https://github.com/microsoft/PowerApps-Samples/tree/master/ai-builder/BringYourOwnModelTutorial#step-32-integrate-the-registered-model).

*(Markus: Is third bullet point needed?)*
> [!IMPORTANT]
> - This is a preview feature.
>
> - [!INCLUDE[cc_preview_features_definition](includes/cc-preview-features-definition.md)]
>
> - This feature is being gradually rolled out across regions and might not be available yet in your region.

## Create a canvas app

1. Sign in to [Power Apps](https://make.powerapps.com).

1. Select **Create** > **Canvas app from blank**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of create a canvas app from blank.](media/powerfx-in-powerapps/create-blank.png "Create a canvas app from blank")

1. In the **App name** field, enter a name and select **Create**.

1. If you see the **Welcome to Power Apps Studio** screen, select **Skip**.

## Add images and descriptions

1. Select **Data** > **Add data** > **AI Models**.

1. On the dropdown, select the image classification model you want to add.

    > [!div class="mx-imgBorder"]
    > ![Animation of adding an AI model as a data source.](media/image-classification-component-in-powerapps/add-ai-as-data-source.gif "Add an AI model as a data source")

1. Add an image by selecting an area on the canvas.

1. In the box below **Prediction**, type a description.

1. Select **Submit**.

    > [!div class="mx-imgBorder"]
    > ![Animation of adding an image and description.](media/image-classification-component-in-powerapps/ai-in-canvas-app.gif "Add an image and description")

## Add a Power Fx formula

1. Select the control area next to **Prediction**.

1. On the formula bar, type **'Model Name'.Predict(Image).Prediction**.

    In the following example, you'd type this:

    ````powerapps-dot
    'Car Damage Classifier'.Predict(AddMediaButton.Media).Prediction
    ````
    > [!div class="mx-imgBorder"]
    > ![Animation of adding a Power Fx formula.](media/image-classification-component-in-powerapps/ai-in-power-fx.gif "Add a Power Fx formula")
    
    The last property in the formula, `.Prediction`, will return the predicted label for the image from the model. If you want a list of all the possible labels and their corresponding confidence values from the model, use the `.Labels` property in the following example:

    ````powerapps-dot
    'Model Name'.Predict(Image).Labels
    ````
