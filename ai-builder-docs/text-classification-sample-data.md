---
title: Use sample data to do category classification  - AI Builder | Microsoft Docs
description: Provides steps to create a category classification model in AI Builder using sample data provided by Microsoft.
author: amina196
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 10/06/2019
ms.author: aminab
ms.reviewer: v-dehaas
---

# Use sample data to do category classification

Get started exploring AI Builder category classification by using sample data to build and train a category classification model. The sample data uses customer feedback for a hospital. The goal is to train a model that can predict the category of newly received feedback. This model can help the hospital administrator free up time from categorizing patient feedback, leaving more time to act on it and provide a better experience to patients.

> [!NOTE]
> This sample data is added to your environment automatically if you enable the [Deploy sample apps and data](build-model.md#deploy-sample-apps-and-data) setting when creating your database.

## Set up an environment with data

1. Download [AIBuilder_Lab.zip](https://go.microsoft.com/fwlink/?linkid=2103171), which contains category classification sample data.

    > [!NOTE]
    > The AIBuilder_Lab.zip file also contains sample files for working with other AI Builder model types, in addition to some hands-on labs that you can use to learn more about AI Builder. For more information about the contents of the zip file, see the [readme.txt](https://go.microsoft.com/fwlink/?linkid=2108226) file that's included in the zip file.<!--By the way, this readme file needs some work. Please see learn-ai-builder.md for my markup.-->

2. Import the **AIBuildetTextSample_1_0_0** solution to your Common Data Service environment. More information: [Import, update, and export solutions](/powerapps/maker/common-data-service/import-update-export-solutions)

3. Upload data from **sampleData.zip** to the healthcare_feedback entity by following instructions in [Before you build a category classification model](before-you-build-text-classification-model.md).

## Create your model

1. Go to the AI Builder build screen, and select **Category classification**.
2. Enter a name, and then create your model.
3. Select **Text:** pick the **healthcare_feedback** entity and the **text** attribute.<!--What does "Select **Text:**" signify? Is it orienting the reader to the UI, or is it a summary of the step that's then followed by the actual step? Can you provide a screenshot, or at least make this a regular procedure step?-->
4. Select **Tags:** choose the **tags** attribute.<!--Same question as step 3.-->
5. Select **English** as the language for classification.
6. Select **Train** to train your model.
