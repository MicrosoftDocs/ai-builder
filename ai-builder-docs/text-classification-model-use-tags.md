---
title: Use generated tags -  AI Builder | Microsoft Docs
description: Provides information about how to use text classification model–generated tags, and some troubleshooting information
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/07/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Use generated tags

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

## Microsoft Flow

If you want to use your trained model in Microsoft Flow, you can find more information in [Use text classification model in Microsoft Flow](text-classification-model-in-flow.md).


## What if the model is not writing new tag suggestions? 


<!--from editor: Does "Flow," below, refer to a flow (lowercase) or to Microsoft Flow? (It should never just be Flow for Microsoft Flow. -->

 - Check that you didn’t  exceed the number of Flow runs for your subscription. 
 - Turn off the Common Data Service run setting, and then turn it back on. 
