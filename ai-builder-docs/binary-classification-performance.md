---
title: Prediction model performance -  AI Builder | Microsoft Docs
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

# Prediction model performance

After each training, AI Builder uses the test data set to evaluate the quality and accuracy of the new model. A summary page for your model shows your model training result, including a **Performance** score.  

## Performance scores

AI Builder calculates the performance score for your model based on the accuracy of the prediction results. This score shows how accurate your prediction is compared to a random guess. A  guess is correct 50% of the time, which means your model needs to score more than 50% to be better than a  guess.

Ai Builder performance scores do not correleate directly with the percentage of accurate predictions. That’s because you may be trying to identify a small percentage of occurrences – for example fraudulent transactions. If the actual fraud rate is 5%, and your model classifies 100% of transactions as valid, it would have a 95% rate accuracy, while failing 100% of the time to predict fraud.

Instead, AI Builder compares your model’s accuracy to a random guess model, which takes into account the data distribution in the training set. Using 50% as the baseline for a guess, your model needs to score consistently higher than 50% to be useful.

## Performance score ranges

After you understand the performance score, you can use it to evaluate your model Here is some general guidance:

### Extremely low scores

If your score is less than 10%, it probably means that your training data is irrelevant or not accurate for the target you want to predict. Revisit the data and make necessary changes, and then come back to retrain.

### Moderately low scores
If your score is between 10% and 50%, your model didn’t outperform the random guess. Again, this probably indicates an issue with training data. View the training details page to see if all the training rows and fields are as expected, and if so, double check the training data to make sure it’s accurate, relevant and connected.

### Good scores

If your score is between 50% and 98%, you need to evaluate the model and decide if it meets your requirements. For example, if you’re just trying to identify potential customers for a marketing campaign, you may be satisfied with any improvement over a guess. However, if you are trying to predict health issues, your analysis may require higher accuracy. 

### Very high scores

If your score higher than 98%, it probably means that you already have the answer in your training data. Just check the most influential data in your model result page. And if you see there’s one field that has extremely high impact (say 99%), and the rest field all have very low impact (less than 1%). It means the most influential field could be revealing the “answers” you’re trying to predict. It’s suggested to start a new version of model, deselect the most influential field and do the training again. 


For more information, go to [Evaluate your model](manage-model.md#evaluate-your-model).

## Data influence for prediction models

Each time you train a prediction model, AI Builder shows  a list of the most influential data fields in the training.

Each field used in the training has a score to represent its influence on the training. The higher the score is, the more influential the field is. These scores combined equal 100%. This helps show whether your model is trained as you expect. For example, if you want to predict online shopper intention, and you’re expecting **Age, Product** as the most influential field, it should appear in the most influential field list on the model details page. If not, it may indicate that the training result is not as expected. In this case, please check your [training report](binary-classification-training-report.md) for details.  

### Next steps

[Evaluate your model](manage-model.md#evaluate-your-model)
[Use your published prediction model in a model-driven app](binary-classification-model-driven-app.md) 
