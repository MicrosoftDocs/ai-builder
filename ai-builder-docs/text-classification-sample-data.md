---
title: Use sample data to do text classification  -  AI Builder | Microsoft Docs
description: Provides steps to create a text classification model in AI Builder using sample data provided by Microsoft.
author: amina196
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/05/2019
ms.author: aminab
ms.reviewer: kvivek
---

# Use sample data to do text classification 

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

To explore the possibilities of text classification in AI Builder, you can get started by building and training an text classification model using sample data. 

## Get the sample data

Download [AIBuilder_Lab.zip](https://github.com/microsoft/PowerApps-Samples/blob/master/ai-builder/labs/AIBuilder_Lab.zip) file, which contains text classification sample images and labels. 

> [!NOTE]
> The **AIBuilder_Lab.zip** file also contains sample files for working with other AI Builder model types, as well as some hands-on-labs that you can use to learn more about AI Builder. More information about the contents of the zip file  is available [here](https://github.com/microsoft/PowerApps-Samples/tree/master/ai-builder/labs), or in the **readme.txt** file contained in the zip file. 

## Instructions

1. Import the AIBuildetTextSample_1_0_0 solution to your CDS environment learn more.
1. Upload data from sampleData.zip to the healthcare_feedback entity following these instructions.
1. Once you’re done importing data, you can start the Text Classification wizard to create a model:
1. Navigate to the AI Builder build page and pick a Text Classification model.
1. Choose a name for the Text Classification model and create your model.
1. Select Text: pick the healthcare_feedback entity and the “text” attribute.
1. Select Tags: choose the “tags” attribute.
1. Choose “English” as the language for classification.
1. Click on train.



