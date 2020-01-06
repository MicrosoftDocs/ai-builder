---
title: Administer AI Builder - AI Builder | Microsoft Docs
description: Provides information about supported regions, enabling or disabling the feature, and backup/restore in AI Builder.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/23/2019
ms.author: antode
ms.reviewer: v-dehaas
---

# Administer AI Builder

Power Platform administrators can use the  [Power Apps admin center](https://admin.powerapps.com) and the [Power Platform Admin center](https://admin.powerplatform.microsoft.com) to manage environments and settings for Power Apps and AI Builder.

For more information, see the [Power Platform administrator guide](https://docs.microsoft.com/power-platform/admin/admin-documentation).

## Supported regions

Your AI model is deployed in the region that hosts the environment. For example, if your environment is created in the Europe region, then your model is deployed in Europe datacenters. For an overview of environments, see [Environments overview](https://docs.microsoft.com/power-platform/admin/environments-overview).

The availability (release status) of AI Builder is dependent on your region. For a breakdown of AI Builder feature availability by region, see [Feature availability by region](availability-region.md). 

## Enable or disable AI Builder preview features

Some AI Builder features are released for general availability. Others are considered in preview release status.

Preview features appear on the build page with the **Preview** label. In the Power Platform admin center, administrators control whether users have access to preview features.

By default, the **AI Builder preview models** feature is enabled for any eligible environment. Eligible environments must have Common Data Service, and be in a [supported region](availability-region.md). If the environment isn't eligible, the **AI Builder preview models** feature doesn't appear in the Power Platform admin center.

To control the feature availability:

1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com).
2. In the admin center, go to **Environments** > *[select an environment]* > **Settings** > **Features**.
3. On the **Features** settings page, under **AI Builder**, enable or disable **AI Builder preview models**.  
    
### Important points related to enabling or disabling the feature

- If you disable **AI Builder preview models**:
  - We don't delete existing models that users of this environment have created.
  - AI Builder components are disabled.
  - Existing experiences that use existing AI Builder components will fail or return errors.
  - Admins and owners can delete AI models of this type.

- If you enable **AI Builder preview models** again:
  - AI Builder components are available again.
  - Components function as they did before the feature was disabled (Assuming nothing else is changed).

For more information about enabling or disabling features in the Power Platform admin center, see [Manage feature settings](https://docs.microsoft.com/power-platform/admin/settings-features).

## Backup and restore

Common Data Service has backup and restore capabilities to protecting your apps data, providing continuous availability of service. For more information, see [Backup and restore environements](https://docs.microsoft.com/power-platform/admin/backup-restore-environments).

> [!IMPORTANT]
> Currently, AI Builder provides limited support for backup and restore.

A system administrator or delegated admin user can use the standard capabilities described in [Backup and restore environments](https://docs.microsoft.com/power-platform/admin/backup-restore-environments).

After a restore operation, you have to [retrain and republish existing models](manage-model.md#retrain-and-republish-existing-models). to make them available again. 
