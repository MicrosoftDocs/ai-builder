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

Power Platform administrators can use the [PowerApps Admin center](https://admin.powerapps.com) and the [Power Platform Admin center](https://admin.powerplatform.microsoft.com) to manage environments and settings for PowerApps and AI Builder.

For more information, see [Power Platform Administrator Guide](https://docs.microsoft.com/power-platform/admin/admin-documentation)

## Supported regions

Your AI model is deployed in the region that hosts the environment. For example, if your environment is created in the Europe region then your model is deployed in Europe data centers. For an overview of environments, see [Environments overview](https://docs.microsoft.com/power-platform/admin/environments-overview).

Currently, AI Builder is available in the United States and Europe regions only. AI Builder features will not be available in environments created in regions other than United States or Europe.

## Enable or disable AI Builder feature

Power Platform administrators can use the Power Platform Admin center to control the availability of AI builder in an environment.

By default, the **AI Builder** features is set to **On** (enabled) for any eligible environment (environment must have Common Data Service and its region must be supported; either the United States or Europe). If the environment is not eligible, the **AI Builder** feature won't appear in the Power Platform Admin center. 

To control the feature availability:
1. Sign in to [Power Platform Admin center](https://admin.powerplatform.microsoft.com).
2. In the admin center, go to **Environments** > *[select an environment]* > **Settings** > **Features**.
3. On the **Feature** settings page, enable or disable the **AI Builder** option.

Some important points related to enabling or disabling the feature:

- If you set **AI Builder** to **Off** (disabled), it won't delete existing models that users of this environment might have created. However, AI Builder components won't be visible anymore, and existing experiences that leverage existing AI builder components will fail and/or return errors.

- If you set **AI Builder** back to **On** (enabled), the AI Builder components will become visible again and function as they did earlier.

- To delete all AI Builder models from an environment, you must delete each model and then disable the **AI Builder** feature by setting it to **Off**  ensure that users can’t create new models using AI builder. You must do this on each environment where AI Builder was turned on.

For more information about enabling/disabling features in the Power Platform Admin center, see [Manage feature settings](https://docs.microsoft.com/power-platform/admin/settings-features)

## Backup and restore

Dynamics 365 allows protecting your apps data and providing continuous availability of service thanks to its built-in backup and restore capabilities. For more information, go to [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances) in PowerApps docs. 

> [!IMPORTANT]
>
>Initially, AI Builder features limited support for backup and restore.
A System Administrator or Delegated Admin user can use the standard capabilities described in the [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances) topic. After a restore operation, they must manually retrain and republish existing models to make them available again.

To retrain and republish existing models:
1. Sign in to [PowerApps](https://web.powerapps.com/), and then in the navigation pane, select **AI Builder** > **Models**. 
2. In the **Performance** section, select the **…** menu to the right of **Training report**, and then select **Retrain**.

This replaces your last trained version. Now, publish this version.

Perform these steps on each of your AI Builder models to get your AI models up and running again.

### Related topic
[AI Builder Release Notes](/power-platform-release-notes/october19/ai-builder)<br/>

