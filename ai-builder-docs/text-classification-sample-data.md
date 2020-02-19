---
title: Use sample data to do text classification  -  AI Builder | Microsoft Docs
description: Provides steps to create a text classification model in AI Builder using sample data provided by Microsoft.
author: amina196
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 10/06/2019
ms.author: aminab
ms.reviewer: v-dehaas
---

# Use sample data to do text classification

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

Get started exploring AI Builder text classification by using sample data to build and train a text classification model. The sample data we provide uses customer feedback for a hospital. The goal would be to train a model that can predict the category of newly received feedback. This model could help the hospital administrator free up time from categorizing patient feedback, leaving more time to act on it and provide a better experience to patients.

> [!NOTE]
> This sample data is added to your environment automatically if you enable the [Deploy sample apps and data](build-model.md#deploy-sample-apps-and-data) setting when creating your database.

## Set up an environment with data

1. Download [AIBuilder_Lab.zip](https://go.microsoft.com/fwlink/?linkid=2103171) file, which contains text classification sample data.

    > [!NOTE]
    > The [AIBuilder_Lab.zip](https://go.microsoft.com/fwlink/?linkid=2103171) also contains sample files for working with other AI Builder model types, as well as some hands-on-labs that you can use to learn more about AI Builder. More information about the contents of the zip file is available in the [readme.txt](https://go.microsoft.com/fwlink/?linkid=2108226) file that is contained in the zip file.

2. Import the **AIBuildetTextSample_1_0_0** solution to your Common Data Service environment. More information: [Import, update, and export solutions](/powerapps/maker/common-data-service/import-update-export-solutions).
3. Upload data from **sampleData.zip** to the healthcare_feedback entity by following instructions in [Before you build a text classification model](before-you-build-text-classification-model.md).

## Create your model

1. Navigate to the AI Builder build screen, and select **Text classification**.
2. Choose a name, and then create your model.
3. Select **Text:** pick the **healthcare_feedback** entity and the **text** attribute.
4. Select **Tags:** choose the **tags** attribute.
5. Choose **English** as the language for classification.
6. Select **Train** to train your model.
