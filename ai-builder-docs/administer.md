---
title: Administer AI Builder - AI Builder | Microsoft Docs
description: Provides information about supported regions, enabling or disabling the feature, and backup/restore in AI Builder.
author: Dean-Haas
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/23/2019
ms.author: antode
ms.reviewer: v-dehaas
---

# Administer AI Builder

Microsoft Power Platform administrators can use the [Power Apps admin center](https://admin.powerapps.com) and the [Power Platform admin center](https://admin.powerplatform.microsoft.com) to manage environments and settings for Power Apps and AI Builder. More information: [Power Platform administrator guide](https://docs.microsoft.com/power-platform/admin/admin-documentation)

## Supported regions

Your AI model is deployed in the region that hosts the environment. For example, if your environment is created in the Europe region, your model is deployed in datacenters in Europe<!--Suggested to avoid the question of whether to use "European."-->. More information: [Environments overview](https://docs.microsoft.com/power-platform/admin/environments-overview)<!--note from editor: I used the stripped-down cross-reference wording because the introduction to this cross-reference didn't add anything new. ("For an overview... see Overview...") The title of the article you're linking to already said it all.-->

The availability (release status) of AI Builder is dependent on your region. For a breakdown of AI Builder feature availability by region, see [Feature availability by region](availability-region.md). 

## Enable or disable AI Builder preview features

Some AI Builder features are released for general availability. Others remain in preview release status.

Preview features appear on the build page with the **Preview** label. In the Power Platform admin center, administrators control whether users have access to preview features.

By default, the **AI Builder preview models** feature is enabled for any eligible environment. Eligible environments must have Common Data Service and be in a [supported region](availability-region.md). If the environment isn't eligible, the **AI Builder preview models** feature doesn't appear in the Power Platform admin center.

To control AI Builder preview feature availability:

1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com).
2. In the admin center, go to **Environments** > *[select an environment]* > **Settings** > **Features**.
3. On the **Features** settings page, under **AI Builder**, enable or disable **AI Builder preview models**.

### Important points related to enabling or disabling the feature

- If you disable **AI Builder preview models**:
  - We don't delete existing models that users of this environment have created.
  - AI Builder components are disabled.
  - Existing experiences that use existing AI Builder components will fail or return errors.
  - Admins and owners can delete preview models.<!--Is that what "of this type" meant?-->

- If you enable **AI Builder preview models** again:
  - AI Builder components are available again.
  - Components function as they did before the feature was disabled (assuming nothing else has changed).

For more information about enabling or disabling features in the Power Platform admin center, see [Manage feature settings](https://docs.microsoft.com/power-platform/admin/settings-features).

## Backup and restore

Common Data Service has backup and restore capabilities to help protect your apps' data, providing continuous availability of service. System administrators and delegated admin users can use the standard capabilities described here: [Back up and restore environments](https://docs.microsoft.com/power-platform/admin/backup-restore-environments).

- Backup and restore is fully supported for prediction, object detection, form processing and prebuilt models.

  >[!NOTE]
  >For object detection and form processing models, the restore process might take some time to be completed. The AI Builder models list shows an "importing" status message while the restore operation is in progress.<!--Suggested.-->

- For models not supported by backup and restore: if you restore an environment, you'll have to retrain and republish these models to make them available again.

## Move and copy environments

- For prediction and prebuilt models, moving and copying environments is fully supported.<!--Suggested, to make the wording of these two bullet points parallel. -->

- For other models, after you move or copy an environment, you have to retrain and republish existing models to make them available again.
