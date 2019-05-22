---
title: Administer AI Builder | Microsoft Docs
description: Provides information about supported regions, onboarding/opt out, and backup/restore in AI Builder.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/10/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Administer AI Builder

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

Power platform administrators can use the [PowerApps Admin center](https://admin.powerapps.com) and the [Power Platform Admin center](https://admin.powerplatform.microsoft.com) to manage environments and settings for PowerApps and AI Builder.

Features from the PowerApps Admin center are being moved to the Power Platform Admin center. Until the move to the Power Platform Admin center is complete, you’ll still be able to manage environments and settings in PowerApps Admin center as usual.

## Supported regions
Your AI model is deployed in the region that hosts the environment. For example, if your environment is created in the Europe region, then your model is deployed in Europe data centers. For an overview of environments, see [Environments overview](https://docs.microsoft.com/power-platform/admin/environments-overview).

Currently, AI Builder is available in the United States and Europe Power Platform regions only. AI Builder features will not be available in environments created in regions other than United States or Europe.
## Onboarding/opt in and opt out
Power platform administrators can use the [Power Platform Admin center](https://admin.powerplatform.microsoft.com) to control the availability of AI builder in a given environment. This is controlled with a toggle that administrators can modify like any other toggle in the Power Platform Admin center.

- By default, AI builder is set to **ON** for any eligible environment (environment must have CDS and its region must be supported – either the United States or Europe). If the environment cannot be supported, the toggle will not appear in the Power Platform Admin center.

- If you switch the toggle to **OFF**, this doesn’t delete existing models that users of this environment might have created but AI builder components are not visible, and existing experiences that leverage existing AI builder components fail and/or return errors.

- If you switch the toggle back to **ON**, the components become visible again and function as they did.

- In order to delete all AI builder models from an environment, one must delete each model, then then select toggle **OFF** AI builder in order to make sure that users can’t create new models using AI builder. You must do this on each environment where AI builder was turned on.

## Backup and restore
Dynamics 365 allows protecting your apps data and providing continuous availability of service thanks to its built-in backup and restore capabilities. For more information, go to [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances) in PowerApps docs. 

> [!IMPORTANT]
>
>Initially, AI Builder features limited support for backup and restore.
A System Administrator or Delegated Admin user can use the standard capabilities described in the [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances) topic. After a restore operation, they must manually retrain and republish existing models to make them available again.

To retrain and republish existing models:
1. Sign in to [PowerApps](https://web.powerapps.com/), and then in the navigation pane, select **AI Builder** > **Models**. 
2. In the **Performance** section, select the **…**menu to the right of **Training report**, and then select **Retrain**.

This replaces your last trained version. Now publish this version.

Perform these steps on each of your AI Builder models to get your AI models up and running again.



### See also
[AI Builder Release Notes](/power-platform-release-notes/october19/ai-builder)<br/>
[PowerApps docs](https://docs.microsoft.com/powerapps/)<br/>
[Microsoft Flow docs](https://docs.microsoft.com/flow/getting-started)
