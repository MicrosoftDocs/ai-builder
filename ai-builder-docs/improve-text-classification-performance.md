---
title: Improve category classification model performance -  AI Builder | Microsoft Docs
description: Provides tips to help you improve category classification model performance in AI Builder.
author: raaourik 

ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/31/2019
ms.author: raaourik 
ms.reviewer: v-dehaas
---

# Improve category classification model performance

If your model performance score isn't where you want, there are a few things you can try. These tips can help you tweak your model to improve its predictive power.

## Add more correctly labeled training data

The more correctly labeled training data you have, the better your model will perform. For example, let's say your two-option label is *Yes* or *No*. If most of your data only has a *Yes* in this field,  your AI model probably won't learn much from this data. If your data isn't correctly labeled, the model is probably not going to learn very well. It is ideal to provide 1,000 or more correctly labeled data records to train your prediction model.

## Clean up your data

You might have a lot of correctly labeled training data. You might have added a lot of data fields. So why is the AI model not as predictive as you expect? It could be that you're selecting too many fields, adding an unwanted bias. Make sure all the fields you select influence what you want to predict. Deselect irrelevant or misleading fields.

- Validate the data fields that you selected to train the AI model don't have a high rate of missing values.
- Populate missing values with a default value or remove the data field from the model training.
- If a data field has a high correlation with a prediction outcome, remove the data field from the model training.

Cleaning your data can avoid some types of training errors and improve model performance. Here are some additional pointers:

- Remove duplicate or irrelevant fields.
- Check for errors and inconsistencies:
  - Typos.
  - Inconsistent capitalizations.
  - Inconsistent or incorrect labels.
- Remove abnormal records.
- Handle missing data.
  - For categorical, label them as missing.
  - For numeric, flag and fill.

## More tips

- There should be at least 100 text records per tag, meaning that each tag would have been used to label at least 100 text entries.
- Make sure you have balanced use of tags in your training data. For example, if you have four tags for 100 text items and the two first tags (*tag1* and *tag2*) are used for 90 text items, but the other two (*tag3* and *tag4*) are only used on the remaining 10 text items, the lack of balance might cause your model to struggle to correctly predict *tag3* or *tag4*.
- Make sure you train your model on data that is similar to the one you want to start tagging.

### Next step

[Publish your category classification model](publish-text-classification-model.md) 

### Related topic

[Publish a model in AI Builder](publish-model.md)

