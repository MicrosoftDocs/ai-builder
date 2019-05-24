---
title: Improve text classification model performance | Microsoft Docs
description: Provides tips to help you improve text classification model performance in AI Builder.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/10/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Improve text classification model performance

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

If your model performance score is not where you want, here are some tips on how to tweak your model to improve its predictive power.

## Add more correctly labeled training data
Even though the minimum requirement for training data is 50, this doesn't mean 50 data records can train a highly predictive AI model. For example, if your two-option label is **Yes** or **No**, and most of your data record only has a Yes in this field. It’s hard for your AI model to learn all the signals from your data. And if your data is not correctly labeled, it will give the model the wrong signal. It is ideal to provide 1000 data records or more to help your model be more predictive.

## Clean up your data
You may have a lot of correctly labeled training data. You may have added a lot of data fields. So why is the AI model not as predictive as you expect? It could be that you're selecting too many fields, adding an unwanted bias. Make sure all the fields you select influence what you want to predict. Deselect irrelevant or misleading fields.

Validate the data fields that you selected to train the AI model don't have high rate of missing values. Populate the missing values with a default value or remove the data field from the model training. If a data field has high correlation with prediction outcome, remove the data field from the model training.

Cleaning your data can avoid some types of training errors and improve model performance. Here are some quick pointers:
- Remove duplicate or irrelevant fields.
- Check for errors and inconsistencies:
    - Typos
    - Inconsistent capitalizations
    - Inconsistent or incorrect labels
- Remove abnormal records.
- Handle missing data.
    - For categorical, simply label them as missing.
    - For numeric, flag and fill.
## More tips
- There should be at least 100 text records per tag. Meaning that each tag would have been used to label at least 100 text entries.
- Make sure you have balanced use of tags in your training data. For example, if you have 4 tags for 100 text items and the two first tags (*tag1* and *tag2*) are used for 90 text items, but the other two (*tag3* and *tag4*) are only used on the remaining 10 text items, the lack of balance may cause your model to struggle to correctly predict *tag3* or *tag4*.
- Make sure you train your model on data that is similar to the one you want to start tagging

### Next steps
[Publish your text classification model](publish-text-classification-model.md) 

### Related topics
[Publish a model in AI Builder](publish-model-ai-builder.md)

