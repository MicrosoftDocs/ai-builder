---
title: Create a text classification model | Microsoft Docs
description: Provides steps to create a text classification model
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/10/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Create a text classification model

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

Now that you have your training data in Common Data Service, you can create a new model and configure it:
1. Sign in to [PowerApps](https://web.powerapps.com/), and then select **AI Builder (preview)** > **Build**.
![Build text classification model screen](media/build-text-classification-model.png "Build text classification model screen")
2. Select the **Text classification** AI Builder AI model type, name your model, and then select **Create**.
3. Select **Select text**, select the entity, and then select the field where your training text is stored.
4. Select **Select tags**, select the field where the tags are stored, and then select the separator you used for your tags.
5. Preview your selection to verify the data and the configuration you applied.
6. Select the language you want to use for training, and then select **Next**. 

That's it! Now you can [train](train-text-classification-model.md) your AI model. 


### Next steps
[Train your text classification model](train-text-classification-model.md) 
