---
title: Train and publish your object detection model -  AI Builder | Microsoft Docs
description: Provides steps to train and publish your object detection model in AI Builder.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/07/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Train and publish your object detection model

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

In this section, you’ll learn how to verify your data, and then how to train, test, and publish your model.
1.	On the **Train your model** screen, verify that you have the correct names, and the correct amount of images 
2.	If the data is all good, select **Train** to kick off the training of your object detection model.

## Quick test your model 

Once your model is trained, you can see it in action from its details page, which you can learn more about [here](manage-model.md).

1. From your model details page, select **Quick Test** button in the **Last trained version** section. 
2. Drag and drop or upload an image which contains your objects to test your model.
3. Your model will be applied to the image you uploaded. This step might take a little while.
4. After your model is done running, the rectangles found will be drawn directly on the picture. 

![Quick test screen](media/quick-test.png)

## How to interpret your model performance score

After your model is trained, in addition to being able to quick-test it, a performance score appears on it's details page. This performance score indicates how well the model performs on the images you uploaded. This is not an indication of how well it will perform on your future images, since it hasn’t seen them yet! 

If you upload fewer than 50 images for a label, you are more likely get a high score - as high as 100%. This doesn’t mean your model is bullet-proof. It means your model has made no mistake on a subset of the images you provided, called the test set. The smaller the training set, the smaller the test set, and the more likely your model is to be right when the performance score is calculated.

Model performance scores are more reliable when the number of images per label is greater than 50,  and when performance scores are stable even when the training set changes.

## Publish your object detection model

From there, you can run more tests with other pictures. If you are happy with the results you are getting, you can [publish](publish-model.md) your model to use it in a Powerapps or Microsoft Flow.

### Related topics
[Manage your AI model](manage-model.md)
