---
title: Use an image classification model by Lobe in Power Apps (preview) - AI Builder | Microsoft Docs
description: Provides information about how to use an image classification model by Lobe in Power Apps
author: JakeCohenMicrosoft
ms.service: aibuilder
ms.topic: conceptual
ms.custom: intro-internal
ms.date: 11/01/2021
ms.author: jacohe
ms.reviewer: v-aangie
---

# Use an image classification model by Lobe in Power Apps (preview)

1. Sign in to [Power Apps](https://make.powerapps.com).

1. Use the preview [Power FX](/power-platform/power-fx/overview) formula:

    `’model-name’.Predict({image: ImageComponent.Image}).responsev2.predictionOutput.Prediction`

    To learn how to set up your app to use your model with Power FX, go to [Integrate the registered model](https://github.com/microsoft/PowerApps-Samples/tree/master/ai-builder/BringYourOwnModelTutorial#step-32-integrate-the-registered-model).
