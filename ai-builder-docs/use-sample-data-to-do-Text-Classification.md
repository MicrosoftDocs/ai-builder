---
title: Use sample data to do Text Classification  -  AI Builder | Microsoft Docs
description: Provides the information you need to know to try out a text classification model with sample data AI Builder.
author: raaourik
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 27/08/2019
ms.author: raaourik
ms.reviewer: kvivek
---

# Use sample data to do Text Classification 

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

You can use our sample data to try out AI Builder Text Classification and understand how to use a model. 

The sample data we provide uses canned customer feedbacks for a hospital. The goal would be to train a model that would be able to automatically predict categories for new incoming feedback. This would typically help the Hospital administrator free up time from categorizing patient feedbacks to act on it and offer a better experience to patients.

Please go through the following steps to prepare an environment with sample data:
1.	Download sample data and solution from this [link](https://github.com/microsoft/PowerApps-Samples/blob/master/ai-builder/labs/AIBuilder_Lab.zip). 
2.	Import the AIBuildetTextSample_1_0_0 solution to your CDS environment. 
3.	Upload data from sampleData.zip to the healthcare_feedback entity following these [instructions](before-you-build-text-classification-model.md). 

Once you’re done importing data, you can start the Text Classification wizard to create a model:
1.	Navigate to the AI Builder build page and pick a Text Classification model.
2.	Choose a name for the Text Classification model and create your model.
3.	Select Text: pick the healthcare_feedback entity and the “text” attribute.
4.	Select Tags: choose the “tags” attribute. 
5.	Choose “English” as the language for classification.
6.	Click on train.


### Next step
[View generated predictions](text-classification-performance.md)
