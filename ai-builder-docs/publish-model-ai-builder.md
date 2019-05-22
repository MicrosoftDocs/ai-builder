---
title:  Publish a model in AI Builder | Microsoft Docs
description: Provides an overview of AI Builder.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/10/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Publish model 


[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

After you successfully train your model, you must publish it to make it available for use. All users in your current environment will be able to use your published model.

On the **Details** page, under **Last trained version**, select **Publish**.
After you publish your last trained version, it appears as the published version. For certain AI model types, you may need to take additional steps to use your model in PowerApps or Common Data Service.

> [!NOTE]
> - Any previous published version is overwritten when you publish a new version.
> - If you have a published version and a last trained version, you will lose the published version when you unpublish because the last trained version is more recent.

## When should I publish my model?
Publish your model when you want to make it usable for you and for other people. If you are not yet satisfied with your model, you can create a new version to try to yield better results. For information about how to create a new version, go to the [Manage a model in AI Builder](manage-model-ai-builder.md) section. 

If you are satisfied with your model, you can publish it to make it available. Similarly, as you can only have up to two trained versions available at a time, you can publish a version if you do not want it to be overwritten by a new version.

> [!TIP]
> For more information on using your published model, view the **Tips** section under the **Published version**.

