---
title: Use generated tags | Microsoft Docs
description: Provides steps to use text classification model generated tags
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/10/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Use generated tags

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

## Microsoft Flow
If you want to use your trained model in Flow, you can find more information [here](text-classification-model-in-flow.md).


## What if the model is not writing new tag suggestions? 
 - Check that you didn’t  exceed the number of Flow runs for your subscription. 
 - Turn off the Common Data Service run setting, and then turn it back on. 