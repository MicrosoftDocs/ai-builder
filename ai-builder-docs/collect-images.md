---
title: Collect images -  AI Builder | Microsoft Docs
description: Provides guidance on how to effectively collect images to build an object detection model in AI Builder.
author: amina196
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/06/2019
ms.author: aminab
ms.reviewer: v-dehaas
---



# Collect images

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

In order to train an object detection model to recognize your items, you will need to gather images containing these items. Adhere to guidelines on the image quantity and quality to get an AI model that performs well.

## Format and size

The images you’ll feed your object detection model need these characteristics:

- **Format**:
  - JPG
  -.png
  - BMP
  
- **Size**:

  6 MB maximum

## Data quantity and data balance

The most important thing is to upload enough images to train your AI model. We recommend at least 50 images per product for the training set as a starting point. With fewer images, there's a strong risk that your model will learn concepts that are in fact noise or irrelevant details. Training your model with more images will generally increase the accuracy of prediction results.

Another consideration is to make sure your data is balanced. For instance, having 500 images for one item and 50 images for another will produce an imbalanced training dataset, causing the model to be more accurate in predicting one item than another. You're likely to see better results if you maintain at least a 1:2 ratio between the item with the fewest images and the item with the most images. For example, if the item with the greatest number of images has 500 images, the item with the fewest images needs to have at least 250 images for training.

## Use more diverse images

Provide images that are representative of what will be submitted to the model during normal use. For example, if you're training a model that recognizes apples, your model might not be as accurate if you only train images of apples on plates but make predictions on images of apples in trees. Including a variety of images will make sure that your model isn't biased and can generalize well. Below are some ways you can make your training set more diverse.

### Background

Provide images of your object in front of different backgrounds (that is, fruit on plate versus fruit in grocery bag). Photos in context are better than photos in front of neutral backgrounds because they provide more information for the classifier.

> [!div class="mx-imgBorder"]
> ![Image backgrounds](media/image-background.png "Image backgrounds")

### Lighting

Provide images with varied lighting (that is, taken with flash, high exposure, and so on), especially if the images used for prediction have different lighting. It is also helpful to include images with varied saturation, hue, and brightness. These are all settings that your device camera allows you to set.

> [!div class="mx-imgBorder"]
> ![Image lighting](media/image-lighting.png "Image lighting")

### Object size

Provide images in which the objects are of varied sizes, capturing different parts of the object. For example, a photo of bunches of bananas and a closeup of a single banana. Different sizing helps the AI generalize better.

> [!div class="mx-imgBorder"]
> ![Object sizes](media/image-object-size.png "Object sizes")

### Camera angle

Provide images taken with different camera angles. If all your photos are taken with a set of fixed cameras (such as surveillance cameras), make sure you assign a different label to every camera even if they capture the same objects to avoid overfitting—modeling unrelated objects (such as lampposts) as the key feature.

> [!div class="mx-imgBorder"]
> ![Camera angles](media/image-camera-angle.png "Camera angles")

### Unexpected results

Sometimes the AI model incorrectly learns characteristics that your images have in common. For example, if you are creating an AI for apples versus citrus, and use images of apples in hands and of citrus on white plates, the AI model might train for hands versus white plates instead of apples versus citrus.

> [!div class="mx-imgBorder"]
> ![Unexpected results](media/image-unexpected-results.png "Unexpected results")

To correct this, use the above guidance on training with more varied images: provide images with different angles, backgrounds, object size, groups, and other variants.

### Next step

[Get started](get-started-with-object-detection.md) with object detection.
