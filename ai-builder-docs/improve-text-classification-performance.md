---
title: Improve the performance of the category classification model - AI Builder | Microsoft Docs
description: Provides tips to help you improve the performance of the category classification model in AI Builder.
author: raaourik 
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/31/2019
ms.author: raaourik 
ms.reviewer: v-dehaas
---

# Improve the performance of your category classification model

If your model performance isn't where you want it to be, there are a few things you can try. These tips can help you tweak your model to improve its predictive power.

## Add more correctly labeled training data

The more correctly labeled training data you have, the better your model will perform. For example, let's say your two-option label is *Yes* or *No*. If most of your data only has a *Yes* in this field, your AI model probably won't learn much from this data. If your data isn't correctly labeled, the model is probably not going to learn very well. It's ideal to begin with a small set of correctly labeled examples - perhaps 100 or less. From there, you can continue to double the number of examples iteratively and retrain each time, noting the performance change. Generally speaking, more data is better, but there are diminishing returns for adding data the larger your dataset gets.
<!--
## Clean up your data

You might have a lot of correctly labeled training data. You might have added a lot of data fields. So why is the AI model not as predictive as you expect? It might be that you're selecting too many fields, thereby adding an unwanted bias. Make sure all the fields you select influence what you want to predict. Deselect irrelevant or misleading fields. In addition:

- Verify that the data fields you selected to train the AI model don't have a high rate of missing values.
- Populate missing values with a default value, or remove the data field from the model training.
- If a data field has a high correlation with a prediction outcome, remove the data field from the model training.

Cleaning your data can avoid some types of training errors and improve model performance. Here are some additional pointers:

- Remove duplicate or irrelevant fields.
- Check for very similar text items labeled differently.
- Remove abnormal records.
- Handle missing data:
  - Label categorical data as missing.
-->

## More tips

- Make sure your use of tags is balanced in your training data. For example: You have four tags for 100 text items. The two first tags (*tag1* and *tag2*) are used for 90 text items, but the other two (*tag3* and *tag4*) are only used on the remaining 10 text items. The lack of balance might cause your model to struggle to correctly predict *tag3* or *tag4*.
- Make sure you train your model using data that's similar to the what you expect to use the model for.  

### Next step

[Publish your category classification model](publish-text-classification-model.md) 

### See also

[Publish your model in AI Builder](publish-model.md)