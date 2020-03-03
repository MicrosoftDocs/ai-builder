---
title: Transition to new object detection model version -  AI Builder | Microsoft Docs
description: Preview model versions won't be compatible with updated model versions, so you have to recreate existing models.
author: Jarennert
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 03/06/2020
ms.author: Jarennert
ms.reviewer: v-dehaas
---

# Transition to new object detection model version

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

AI Builder is improving its object detection  model using a new model version. Your object detection
preview models created before March 5, 2020 are deprecated. More information: [Form processing and object detection preview models in AI Builder are deprecated](/power-platform/important-changes-coming#form-processing-and-object-detection-preview-models-in-ai-builder-are-deprecated)

Starting March 5, you have to recreate your existing object detection models if you want to continue to use them. Models created after this date will automatically use the new model version. It's a good idea to transition to the new model version as soon as possible.

## What do I need to do?

**You must recreate object detection models created before March 5, 2020** 

1. Identify any object detection models created before March 5, 2020 that you want to continue using.
1. For each model, [create a new object detection model](get-started-with-object-detection.md) with the same training images you used in the original model.
1. After the new model is trained and published, make sure to update any apps or flows to use the new model.
1. After you're done with your deprecated object detection model, you can delete it.  

We understand you may have spent significant time building your object detection models.  [Contact us](mailto:aihelpen@microsoft.com) if you need help with migrating larger complex models.

## Why this change?

Object detection models are being upgraded for generally availability. Your existing preview models won't be compatible with the new model version.

Until March 5, 2020, object detection models stored images as attachments in the Note entity. With this update, these models now leverage the new [File and Image data types](https://powerapps.microsoft.com/blog/introducing-improvements-to-data-storage-in-common-data-services/) in Common Data Service, enabling a better and more optimized usage of capacity.
### Related topic

[Manage your AI model](manage-model.md)
