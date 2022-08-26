---
title: Use image classification model by Lobe in Power Apps - AI Builder | Microsoft Docs
description: Learn how to use the image classification model from Lobe to predict labels and categorize images in Power Apps.
author: v-aangie
ms.topic: conceptual
ms.custom: intro-internal
ms.date: 06/06/2022
ms.author: angieandrews
contributors:
    - JakeCohenMicrosoft
    - v-aangie
---

# Use an image classification model by Lobe in Power Apps

In this article, you'll learn about using an image classification model by Lobe in Power Apps.

## Create a canvas app

Create a new canvas app for your image classification model. (If your model is already in a canvas app, skip this section and go to [Add the Power Fx Prediction formula](#add-the-power-fx-prediction-formula) later in this topic.)

1. Sign in to [Power Apps](https://make.powerapps.com).

1. Select **Create** > **Canvas app from blank**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of create a canvas app from blank.](media/powerfx-in-powerapps/create-blank.png "Create a canvas app from blank")

1. In the **App name** field, enter a name and select **Create**.

1. If you see the **Welcome to Power Apps Studio** screen, select **Skip**.

1. Select **Data** > **Add data** > **AI models**.

1. On the dropdown, select the image classification model you want to add.

    > [!div class="mx-imgBorder"]
    > ![Animation of adding an AI model as a data source.](media/image-classification-component-in-powerapps/add-ai-as-data-source.gif "Add an AI model as a data source")

## Add the Power Fx Prediction formula

1. On the image classification model, select the control area next to **Prediction**.

1. On the formula bar, type **'Model Name'.Predict(Image).Prediction**.

    In the following example of car damage, you would type this:

    ````powerapps-dot
    'Car Damage Classifier'.Predict(AddMediaButton.Media).Prediction
    ````
    > [!div class="mx-imgBorder"]
    > ![Animation of adding a Power Fx formula.](media/image-classification-component-in-powerapps/ai-in-power-fx.gif "Add a Power Fx formula")
    
    The last property in the formula, `.Prediction`, will return the predicted label for the image from the model. If you want a list of all the possible labels and their corresponding confidence values from the model, use the `.Labels` property in the following example:

    ````powerapps-dot
    'Model Name'.Predict(Image).Labels
    ````

## Use a canvas app with a classification model

The following animation shows how users of your new app can add their own images in Power Apps and have the appropriate label automatically predicted. For example, if the user is an insurance claim adjuster, they can upload an image of a broken window in a car. The app will then predict and assign the **Broken Glass** label to it. The user might also want to enter more detail on a claim, such as *Window broken on the driver's side*.

> [!div class="mx-imgBorder"]
> ![Animation of adding an image and description.](media/image-classification-component-in-powerapps/ai-in-canvas-app.gif "Add an image and description")
