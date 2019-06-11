---
title: Create a binary classification model -  AI Builder | Microsoft Docs
description: This topic lays out the steps you need to follow to create a binary classification model in AI Builder. 
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/07/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Create a binary classification model

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

This example creates a PowerApps binary classification AI model that uses the *online shopper intention* Common Data Service entity. 

1. Sign in to [PowerApps](https://web.powerapps.com) and then select **AI Builder (preview)** > **Build**. 
2. Select **Binary Classification**. Enter a model name and then select **Create**.
3. Select **Online shopper intention** as the entity, and **Label** as the field.

## Select the data fields to train your model

After you select the **Entity** and **Label** fields, you have to select different data fields as features to train the model. By default, all data fields are selected. You could deselect data fields that might not be important for your business or which might carry unwanted bias. 
 
 ### Data field selection considerations
- Make sure you select the data fields that you want to use in training the model. 
- Deselect the data fields that do not address the problem you want to solve. 
- Deselect the data fields that might carry unwanted bias.
- Make sure the data fields you select don't have a high rate of missing values. If it is a valuable data field, you can assign a default value.
 
> [!NOTE]
> These Common Data Service data types are excluded from the binary classification model. These will not appear in the **Field** drop-down menu: 
> - Customer
> - Image
> - Lookup
> - Multiple selection Option set
> - Multiline Text
> - Owner
> - Unique Identifier
> - String type data types with length greater than 100 characters 

### Next step
[Train and publish your binary classification model](binary-classification-train-model.md)<br/>
