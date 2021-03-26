---
title: Improve the performance of the category classification model - AI Builder | Microsoft Docs
description: Provides tips to help you improve the performance of the category classification model in AI Builder.
author: norliu
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 03/19/2021
ms.author: norliu
ms.reviewer: kvivek
---

# Improve the performance of your category classification model

If your model performance isn't where you want it to be, there are a few things you can try. These tips can help you tweak your model to improve its predictive power.

## Add more correctly labeled training data

The more correctly labeled training data you have, the better your model will perform. For example, let's say you have a Yes/No label. If most of your data only has a *Yes* in this column, your AI model probably won't learn much from this data. If your data isn't correctly labeled, the model is probably not going to learn very well. It's ideal to begin with a small set of correctly labeled examples - perhaps 100 or less. From there, you can continue to double the number of examples iteratively and retrain each time, noting the performance change. Generally speaking, more data is better, but there are diminishing returns for adding data the larger your dataset gets.

## More tips

- Make sure your use of tags is balanced in your training data. For example: You have four tags for 100 text items. The two first tags (*tag1* and *tag2*) are used for 90 text items, but the other two (*tag3* and *tag4*) are only used on the remaining 10 text items. The lack of balance might cause your model to struggle to correctly predict *tag3* or *tag4*.
- Make sure you train your model using data that's similar to the what you expect to use the model for.  

### Next step

[Publish your category classification model](publish-text-classification-model.md) 

### See also

[Category classification prebuilt model](prebuilt-category-classification.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]