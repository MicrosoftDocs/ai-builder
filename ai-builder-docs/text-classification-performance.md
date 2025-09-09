---
title: Understand category classification model performance - AI Builder | Microsoft Docs
description: Provides an understanding of how to evaluate and understand category classification model performance
author: ashishb
ms.topic: concept-article
ms.custom: 
ms.date: 09/08/2025
ms.author: plarrue 
ms.reviewer: angieandrews
---

# Understand category classification model performance

After each training, AI Builder uses the test dataset to evaluate the quality and accuracy of your AI model. A summary page for your model shows your model training results, including a **Performance** score.

AI Builder calculates your model's performance score based on the precision and recall of the prediction results, as well as the F1 score:

- **Performance score**: This score is calculated using precision, recall, and F1 scores. Performance score values are from 0 and 100. Generally, the higher the performance score, the better your model is.
- **Precision**: The fraction of correct predictions among all the positive predictions.
- **Recall**: The fraction of correct predictions among all true positive cases.

## Quick test

You can also select **Quick Test** to assess the quality of the model. Just enter text that you want to tag.  More information: [Evaluate your model](manage-model.md#evaluate-your-model)

### Next step

[Improve the performance of your category classification model](improve-text-classification-performance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
