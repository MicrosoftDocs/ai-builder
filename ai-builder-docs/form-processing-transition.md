---
title: Transition to the new document processing model version - AI Builder | Microsoft Docs
description: Preview document processing model versions aren't compatible with updated model versions, so you have to re-create existing models. 
author: JoeFernandezMS
ms.topic: conceptual
ms.custom: 
ms.date: 01/10/2024
ms.author: Jofernan
ms.reviewer: angieandrews
---

# Transition to the newest document processing model version

AI Builder is improving its document processing model with a new model version. Your document processing preview models created before March 5, 2020 are deprecated. For more information, go to [Document processing and object detection preview models in AI Builder are deprecated](/power-platform/important-changes-coming#form-processing-and-object-detection-preview-models-in-ai-builder-are-deprecated)

Starting March 5, 2020, you have to re-create your existing document processing models if you want to continue to use them. Models created after this date will automatically use the new model version. It's a good idea to transition to the new model version as soon as possible.

## What do I need to do?

**You must re-create document processing models created before March 5, 2020** 

1. Identify any document processing models created before March 5, 2020, that you want to continue using.
1. For each model, [create a new document processing model](create-form-processing-model.md) with the same training documents you used in the original model.
1. After the new model is trained and published, make sure you update any apps or flows to use the new model.
1. After you're done with your deprecated document processing model, you can delete it.

We understand you might have spent significant time building your document processing models. [Contact us](mailto:aihelpen@microsoft.com) if you need help with migrating larger complex models.

## Why this change?

Document processing models are being upgraded for general availability. Your existing preview models won't be compatible with the new model version.

Until March 5, 2020, document processing models stored documents as attachments in the Note table. With this update, these models now use the new File and Image data types in Microsoft Dataverse, which enables a better and more optimized usage of capacity.

### See also

[Use a document processing model in Power Automate](form-processing-model-in-flow.md)  
[Use the document processor component in Power Apps](form-processor-component-in-powerapps.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
