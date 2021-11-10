---
title: Overview of image classification by Lobe (preview) - AI Builder | Microsoft Docs
description: Provides an overview of how you can use image classification models by Lobe in AI Builder to add intelligence to your apps.
author: JakeCohenMicrosoft
ms.service: aibuilder
ms.topic: conceptual
ms.custom: intro-internal
ms.date: 11/15/2021
ms.author: jacohe
ms.reviewer: v-aangie
---

# Overview of  image classification by Lobe (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
> - This is a preview feature.
>
> - [!INCLUDE[cc_preview_features_definition](includes/cc-preview-features-definition.md)]

Lobe is a free, easy-to-use Microsoft desktop application that allows you to build, manage, and use custom machine learning models. With Lobe, you can create an image classification model to categorize images into *labels* that represent their content. You can directly upload Lobe models to AI Builder for use with Microsoft Power Apps and Microsoft Power Automate.

Here are some examples of how Lobe can take your machine learning ideas to production:

- Import and label images.

- Train your model.

- Evaluate training results.

- Play with your model to experiment with different scenarios.

- Export and use your model in an app.

If you're familiar with the AI Builder [object detection](object-detection-overview.md) custom object detection model, you're already familiar with Lobe.

## Business scenarios

 Apps that use image classification can:

- Identify defects in a manufacturing line.

- Alert you when a shelf is empty.

- Identify signs in your environment.

- Filter or verify user-submitted images based on content.

- Notify you when a shipment arrives.

- Work with online retail images.

- Provide information about images in the field.

## What is image classification?

Image classification is categorizing an image into a single label to represent its content overall. Image classification models learn to find patterns such as textures, colors and shapes, from your images. These patterns can then be used to identify your labels.

For example, a project named *Vehicle Damage* might have labels named *Dent*, *Scratch* and *Broken glass* to indicate the type of damage to cars and trucks. An insurance claims adjuster might use these images determine the insurance company's liability.

> [!div class="mx-imgBorder"]
> ![Screenshot of a car dent image in the vehicle label.](media/lobe-overview/dent.png "Car dent image in the vehicle label")

With image classification by Lobe, you train all your models on your computer. When you train this way, you don't use AI Builder credits. Lobe is integrated with Power Platform, which adds the ability to export your model to AI Builder to use in [canvas apps](/powerapps/maker/canvas-apps/getting-started) and [Power Automate flows](/power-automate/flow-types).

## Use image classification by Lobe

To get started with Lobe, create a new project and import your images by selecting **New Project** > **Import**.

> [!div class="mx-imgBorder"]
> ![Screenshot of Lobe import screen.](media/lobe-overview/lobe-splash.png "Lobe import screen")

After you've imported images, you'll need to label your images and train the classification model. To learn more, go to the [Lobe Help site](https://www.lobe.ai/docs/welcome/welcome).

To watch a video of image classification by Lobe, go to the [Lobe home page](https://www.lobe.ai/) and select **Watch Tour**.

### Consider image quantity and object balance

You'll want to upload enough images to train your model accurately. You'll also want to make sure there are enough images to represent each object.
This will increase consistency when training your model.

For tips on choosing enough images so that you represent all your objects, go to [Data quantity and data balance](collect-images.md#data-quantity-and-data-balance).

### Adjust your model architecture

Lobe determines the best model architecture for your project, but you have the option to change it. Changing your project will reset any training completed and automatically train a new model.

Following are recommendations for Power Platform users:

- **Speed:** Use this setting as default for apps or flows that require quick response times.

- **Accuracy:** Use this setting for apps or flows that batch jobs or slower processing requirements.

## Next step

[Export your image classification model from Lobe to AI Builder (preview)](lobe-export.md)