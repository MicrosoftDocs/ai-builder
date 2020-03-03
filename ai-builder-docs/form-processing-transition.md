---
title: Transition to new form processing model version - AI Builder | Microsoft Docs
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

# Transition to the new form processing model version

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

AI Builder is improving its form processing model using a new model version. Your form processing preview models created before March 5, 2020 are deprecated. More information: [Form processing and object detection preview models in AI Builder are deprecated](/power-platform/important-changes-coming#form-processing-and-object-detection-preview-models-in-ai-builder-are-deprecated)

Starting March 5, you have to recreate your existing form processing models if you want to continue to use them. Models created after this date will automatically use the new model version. It's a good idea to transition to the new model version as soon as possible.

## What do I need to do?

**You must recreate form processing models created before March 5, 2020** 

1. Identify any form processing models created before March 5, 2020 that you want to continue using.
1. For each model, [create a new form processing model](https://docs.microsoft.com/ai-builder/create-form-processing-model) with the same training documents you used in the original model.
1. After the new model is trained and published, make sure to update any apps or flows to use the new model.
1. After you're done with your deprecated form processing model, you can delete it.  

We understand you may have spent significant time building your form processing models.  [Contact us](mailto:aihelpen@microsoft.com) if you need help with migrating larger complex models.

## Why this change?

Form processing models are being upgraded for generally availability. Your existing preview models won't be compatible with the new model version.

Until March 5, 2020, form processing models stored documents as attachments in the Note entity. With this update, these models now leverage the new [File and Image data types](https://powerapps.microsoft.com/blog/introducing-improvements-to-data-storage-in-common-data-services/) in Common Data Service, enabling a better and more optimized usage of capacity.

### Related topics

[Form processing model in Power Automate](form-processing-model-in-flow.md)

[Form processing model in Power Apps](form-processor-component-in-powerapps.md)
