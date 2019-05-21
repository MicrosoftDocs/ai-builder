---
title: Binary classification model prerequisites | Microsoft Docs
description: Provides an overview of AI Builder.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/10/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Binary classification model prerequisites

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

For information about AI Builder requirements that are not specific to this AI model, go to the [Prerequisites section](prerequisites.md) of this topic.
## What skills do I need to have to use binary classification?
- The person creating the binary classification model should know enough about the business in question to understand the meaning of a data set. 

- Since no coding is needed to create an AI model in AI Builder, you do not need to be a developer or data scientist to use the AI Builder binary classification model. If you are not familiar with a certain concept, you can use Tips and Help.

## What data do I need?
- Your data must be in Common Data Service. For more information go to the [Common Data Service](https://docs.microsoft.com/en-us/powerapps/maker/common-data-service/data-platform-intro) section of PowerApps on Microsoft Docs. 
- You need at least 10 records of historical outcome for each class of the **Label** data field to train the model and predict the outcome. 
- 50 records is the minimum for training, but for best results you should have at least 1000 records. 
- You should delete data fields that have less relevance to train the model. For example, a field that has a single value for all training samples. 
- You should delete data fields that have a high rate of missing values. 


### Next steps
[Data preparation](binary-classification-data-prep.md)

### See also
[AI Builder Release Notes](/power-platform-release-notes/october19/ai-builder)<br/>
[PowerApps docs](https://docs.microsoft.com/powerapps/)<br/>
[Microsoft Flow docs](https://docs.microsoft.com/flow/getting-started)
