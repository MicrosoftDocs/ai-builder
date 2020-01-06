---
title: Prediction model performance -  AI Builder | Microsoft Docs
description: Provides information to help you better understand prediction model performance, and how performance scores are calculated
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/27/2019
ms.author: norliu
ms.reviewer: v-dehaas
---

# Prediction model performance

After each training, AI Builder uses the test data set to evaluate the quality and accuracy of the AI model. A summary page for your model shows your model training result, including a **Performance** score.  

## Performance score calculations

AI Builder calculates the performance score for your model based on the precision and recall of the prediction results:

- **Performance score**: The harmonic mean of the precision and recall scores. It balances both scores for an imbalanced class distribution. Performance score values are between 0–100 percent. Generally, the higher the performance score, the better your model performs.
- **Precision**: The fraction of correct predictions among all the positive predictions.
- **Recall**: The fraction of correct predictions among all true positive cases.

For more information, see [Evaluate your model](manage-model.md#evaluate-your-model).

### Next step

[Use your published prediction model in a model-driven app](prediction-model-driven-app.md)
