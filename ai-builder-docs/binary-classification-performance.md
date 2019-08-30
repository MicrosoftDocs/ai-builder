---
title: Understand prediction model performance -  AI Builder | Microsoft Docs
description: Provides information to help you better understand prediction model performance, and how performance scores are calculated
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/07/2019
ms.author: norliu
ms.reviewer: kvivek
---

# Understand prediction model performance

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

After each training, AI Builder uses the test data set to evaluate the quality and accuracy of the new model. A summary page for your model shows your model training result, including a **Performance** score.  

## Performance score calculations

AI Builder calculates the performance score for your model based on the precision and recall of the prediction results:

- **Performance score**: This is the harmonic mean of the precision and recall scores. It balances both scores for an imbalanced class distribution. Performance score values are between 0–100 percent. Generally, the higher the performance score, the better your model performs.
- **Precision**: The fraction of correct predictions among all the positive predictions.
- **Recall**: The fraction of correct predictions among all true positive cases.

For more information, go to [Evaluate your model](manage-model.md#evaluate-your-model).

## Understand data influence for prediction models

Each time you train a prediction model, AI Builder shows  a list of the most influential data fields in the training.

Each field used in the training has a score to represent its influence on the training. The higher the score is, the more influential the field is. These scores combined equal 100%. This helps show whether your model is trained as you expect. For example, if you want to predict online shopper intention, and you’re expecting **Age, Product** as the most influential field, it should appear in the most influential field list on the model details page. If not, it may indicate that the training result is not as expected. In this case, please check your [training report](binary-classification-training-report.md) for details.  

### Next step

[Use your published prediction model in a model-driven app](binary-classification-model-driven-app.md) 
