---
title:  Common issues and resolutions for AI Builder -  AI Builder | Microsoft Docs
description: Provides a list of common issues that have been seen AI Builder, and potential workarounds where applicable.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/27/2019
ms.author: joshrenn
ms.reviewer: v-dehaas
---

# Common issues and resolutions for AI Builder

Here are some issues that have been seen in AI Builder. Where applicable, workarounds are provided.

## AI Builder is not set up correctly in your environment

AI Builder might not work in some environments created before the release of AI Builder. To work around this issue, [create a new environment](https://docs.microsoft.com/power-platform/admin/create-environment). If you need to use a particular environment, [contact support](https://docs.microsoft.com/power-platform/admin/get-help-support) for more options.

## AI Builder gets errors trying to read data from your Common Data Service entity

See the data preparation section for your AI model type. Make sure your Common Data Service environment is configured correctly so that your model can access it.

## AI Builder business card reader doesn't work for some users

Make sure business card reader component users have access to Common Data Service, or to the AI Builder model entity configured in the business card reader component.

## Training document is not displayed on Form Processing model details page

When you create a Form Processing model, you will see the preview of one of the documents used for training on the model’s details page once training is complete.

If the training document is not displayed this can be because:

* You are not the owner of the model. The model was shared with you to use in Power Apps and Power Automate, but you don’t have the rights to see the documents that were used for training.
* You imported the model from another environment. When you import a Form Processing model from one environment to another, the original training data is not moved across environments and thus the document preview can’t be displayed.  
