---
title: Understand text classification model performance | Microsoft Docs
description: Gives an overview of text classification model performance
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/10/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Understand text classification model performance

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

After each training, AI Builder uses the test data set to evaluate the quality and accuracy of the new model. A summary page for your model shows your model training result, including a **Performance** score .  

AI Builder calculates the performance score for your model based on the precision and recall of the prediction results:
- **Performance score**: This is the harmonic mean of precision and recall. It balances both for an imbalanced class distribution. Performance score values are between 0 - 100. Generally, the higher the performance score, the better your model performs. 
- **Precision**: The fraction of correct predictions among all the positive predictions.
- **Recall**: The fraction of correct predictions among all true positive cases.
 
Here is an example of how you might interpret your performance score. The following table shows a mapping of performance score range and model performance:

|    Performance score    |    Model performance     |
|-------------------------|--------------------------|
|    <63                  |    Bad                   |
|    63-80                |    OK                    |
|    81-100               |    Good                  |

In this example, if your model gets a score of 59, it means the model performance is not good, and you should go back and tweak your model, and then retrain it. If your model falls into the **OK** or **Good** band, you can either re-train the model to make it better, or you can go ahead and use the model, depending on your situation.  

> [!NOTE]
> These evaluations are rough guidelines. It is possible that, depending on the data you work with, you could have a lower score that performs well, or a higher score that performs less well.

## Quick Test
You can also select the **Quick Test** button and enter a text you want to tag to assess the quality of the model. The quick test generates a list of tags, each with a confidence score.


For more information, go to the [Evaluate your model](manage-model-ai-builder.md#evaluate-your-model) section

### Next steps
[Improve model performance](improve-text-classification-performance.md) 
