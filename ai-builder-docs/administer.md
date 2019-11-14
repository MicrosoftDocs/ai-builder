---
title: Administer AI Builder - AI Builder | Microsoft Docs
description: Provides information about supported regions, enabling or disabling the feature, and backup/restore in AI Builder.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/06/2019
ms.author: antode
ms.reviewer: v-dehaas
---

# Administer AI Builder

Power Platform administrators can use the  [PowerApps admin center](https://admin.powerapps.com) and the [Power Platform Admin center](https://admin.powerplatform.microsoft.com) to manage environments and settings for PowerApps and AI Builder.

For more information, see the [Power Platform administrator guide](https://docs.microsoft.com/power-platform/admin/admin-documentation).

## Supported regions

Your AI model is deployed in the region that hosts the environment. For example, if your environment is created in the Europe region, then your model is deployed in Europe datacenters. For an overview of environments, see [Environments overview](https://docs.microsoft.com/power-platform/admin/environments-overview).

Currently, AI Builder is available in the United States and Europe only. AI Builder features won't be available in environments created outside the United States or Europe.

## Enable or disable AI Builder preview features

Some AI Builder features are released for general availability. Others are considered in preview release status.

Preview features are shown on the build page with the **Preview** label displayed. Power Platform administrators can use the Power Platform admin center to control whether users can create and use preview features.

By default, the **AI Builder preview models** feature is set to **On** (enabled) for any eligible environment (environment must have Common Data Service and its region must be supported). If the environment is not eligible, the **AI Builder preview models** feature won't appear in the Power Platform admin center. 

To control the feature availability:

1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com).
2. In the admin center, go to **Environments** > *[select an environment]* > **Settings** > **Features**.
3. On the **Features** settings page, under **AI Builder**, enable or disable **AI Builder preview models**.  
    
### Important points related to enabling or disabling the feature

- If you set **AI Builder preview models** to **Off** (disabled), it won't delete existing models that users of this environment have created. However, AI Builder components will be disabled, and existing experiences that leverage existing AI Builder components will fail and/or return errors. Admins and owners can delete AI models of this type.

- If you set **AI Builder preview models** back to **On** (enabled), the AI Builder components will become visible again and function as they did before the feature was disabled, assuming nothing else is changed.

For more information about enabling or disabling features in the Power Platform admin center, see [Manage feature settings](https://docs.microsoft.com/power-platform/admin/settings-features).

## Backup and restore

Dynamics 365 allows protecting your apps data and providing continuous availability of service thanks to its built-in backup and restore capabilities. For more information, go to [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances) in PowerApps docs. 

> [!IMPORTANT]
> Currently, AI Builder provides limited support for backup and restore.

A system administrator or delegated admin user can use the standard capabilities described in [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances). 

After a restore operation, they must manually retrain and republish existing models to make them available again. For more information, go to [Retrain and republish existing models](manage-model.md#retrain-and-republish-existing-models).
