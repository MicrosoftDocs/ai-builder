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
<!--Edit suggested, to avoid a bit of a "noun stack." -->
If your model performance score isn't where you want it to be<!--Suggested.-->, there are a few things you can try. These tips can help you tweak your model to improve its predictive power.

## Add more correctly labeled training data

The more correctly labeled training data you have, the better your model will perform. For example, let's say your two-option label is *Yes* or *No*. If most of your data only has a *Yes* in this field, your AI model probably won't learn much from this data. If your data isn't correctly labeled, the model is probably not going to learn very well. It's ideal to provide 1,000 or more correctly labeled data records to train your prediction model.

## Clean up your data

You might have a lot of correctly labeled training data. You might have added a lot of data fields. So why is the AI model not as predictive as you expect? It might be that you're selecting too many fields, thereby<!--Suggested.--> adding an unwanted bias. Make sure all the fields you select influence what you want to predict. Deselect irrelevant or misleading fields. In addition:

- Verify<!--Suggested.--> that the data fields you selected to train the AI model don't have a high rate of missing values.
- Populate missing values with a default value, or remove the data field from the model training.
- If a data field has a high correlation with a prediction outcome, remove the data field from the model training.

Cleaning your data can avoid some types of training errors and improve model performance. Here are some additional pointers:

- Remove duplicate or irrelevant fields.
- Check for errors and inconsistencies:
  - Typos
  - Inconsistent capitalizations
  - Inconsistent or incorrect labels
- Remove abnormal records.
- Handle missing data:
  - Label categorical data as missing.
  - Flag and fill numeric data.<!--Will the reader know what "flag and fill" means?-->

## More tips

- There should be at least 100 text records per tag, meaning that each tag has been used to label at least 100 text entries.
- Make sure your use of tags is balanced in your training data. For example: You have four tags for 100 text items. The two first tags (*tag1* and *tag2*) are used for 90 text items, but the other two (*tag3* and *tag4*) are only used on the remaining 10 text items. The lack of balance might cause your model to struggle to correctly predict *tag3* or *tag4*.
- Make sure you train your model on data that's similar to the data<!--Edit okay? I wasn't sure what "the one" meant here.--> you want to start tagging.

### Next step

[Publish your category classification model](publish-text-classification-model.md) 

### See also

[Publish your model in AI Builder](publish-model.md)