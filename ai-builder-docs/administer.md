---
title: Administer AI Builder - AI Builder
description: Administrators can learn about AI custom models and environment lifecycle, backup and restore, managing capacity, enabling or disabling the feature, and data loss prevention in AI Builder.
author: phil-cmd
contributors:
  - Antoine2F
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.custom: 
ms.date: 01/10/2024
ms.author: plarrue
ms.reviewer: angieandrews
---

# Administer AI Builder

Microsoft Power Platform administrators can use the [Power Apps admin center](https://admin.powerapps.com) and the [Power Platform admin center](https://admin.powerplatform.microsoft.com) to manage environments and settings for Power Apps and AI Builder.

More information: [Power Platform administrator guide](/power-platform/admin/admin-documentation)

The availability, which is also known as the release status, of AI Builder is dependent on your region. For a breakdown of AI Builder feature availability by region, go to [Feature availability by region](availability-region.md).

For more information, download the [AI Builder governance whitepaper](https://go.microsoft.com/fwlink/?linkid=2244137&clcid=0x409).

## AI custom model and environment lifecycle

This section applies to AI Builder custom models. It doesn't apply to prebuilt models.

### Lifecycle states of a model

A model can go through different states depending on the makers’ actions. The model states are stored through configurations within the AI Configuration table.

The states are draft, training (transient), trained, publishing (transient), published, unpublishing (transient), training error, importing (transient), and import error.

:::image type="content" source="media/model-lifecycle.png" alt-text="Screenshot of the lifecycle states of a model.":::

### Application lifecycle management

Makers should be able to continuously update and deploy their models across single or multiple environments.

Managing new versions of a model often requires going through different environments. A typical scenario would be to make model changes in a *development environment*, qualify the model in a *test environment*, and predict in a *production environment*.

:::image type="content" source="media/app-lifecycle.png" alt-text="Screenshot of application lifecycle management.":::

In AI Builder, all the environments need to be provided with a Microsoft Dataverse database.

Moving models between environments can be done through the solution concept. Solutions are vehicles to move components between Microsoft Power Platform environments. To learn more, go to [Introduction to solutions](/power-apps/developer/data-platform/introduction-solutions).

For more information on how to distribute an AI model as a solution component, go to [Distribute your AI model](distribute-model.md).

### Environment lifecycle

AI Builder models are fully moved, along with user data, during environment backup/restore and environment copy operations.

After restore and copy operations, document processing and object detection models may be in the importing state for a few minutes while copies are made in the back end.

## Backup and restore

Microsoft Dataverse has backup and restore capabilities to help protect your apps' data, providing continuous availability of service. System administrators and delegated admin users can use the standard capabilities described in [Back up and restore environments](/power-platform/admin/backup-restore-environments).

- Backup and restore are fully supported for prediction, object detection, document processing, and prebuilt models.

  > [!NOTE]
  > For object detection and document processing models, the restore process might take some time to be completed. The AI Builder models list shows an "importing" status message while the restore operation is in progress.

- **For models not supported by backup and restore**: If you restore an environment, you'll have to retrain and republish these models to make them available again.

## Prerequisite to set up an environment ready for AI Builder

AI Builder is licensed as an add-on to your Power Apps, Power Automate, or Dynamics 365 license. This means you need a Power Apps, Power Automate, or Dynamics 365 license that allows you to create a Microsoft Power Platform environment.

## Manage AI Builder credits

Access to AI Builder features within an environment requires access to AI Builder credits.

To learn more, go to [AI Builder licensing and credit management](credit-management.md).

## Where and how are data stored in Dataverse?

Your AI model is deployed in the region that hosts the environment. For example, if your environment is created in the Europe region, your model is deployed in datacenters in Europe. For more information, go to [Environments overview](/power-platform/admin/environments-overview).

Images and documents used for training purposes in object detection and document processing models are persisted in Dataverse. In contrast, images and documents used at prediction time aren't persisted. Examples of non-persisted images and documents are those in a Power Apps component framework (PCF) control and in Power Automate. Inputs of text scenarios are persisted in the AI Event Dataverse table to allow users to monitor [AI Builder activity](activity-monitoring.md).

## Enable or disable AI Builder preview features

Some AI Builder features are released for general availability. Others remain in preview release status.

Preview features appear on the Explore page with the **Preview** label. In the Power Platform admin center, administrators control whether users have access to preview features.

By default, the **AI Builder preview models** feature is enabled for any eligible environment. Eligible environments must have Microsoft Dataverse and be in a [supported region](availability-region.md). If the environment isn't eligible, the **AI Builder preview models** feature doesn't appear in the Power Platform admin center.

To control AI Builder preview feature availability:

1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com).

1. In the admin center, go to **Environments** > *[select an environment]* > **Settings** > **Features**.

1. On the **Features** settings page, under **AI Builder**, enable or disable **AI Builder preview models**.

### Important points related to enabling or disabling the feature

- If you disable **AI Builder preview models**:
  - We don't delete existing models that users of this environment have created.
  - AI Builder components are disabled.
  - Existing experiences that use existing AI Builder components will fail or return errors.
  - Admins and owners can delete preview models.

- If you enable **AI Builder preview models** again:
  - AI Builder components are available again.
  - Components function as they did before the feature was disabled (assuming nothing else has changed).

For more information about enabling or disabling features in the Power Platform admin center, go to [Manage feature settings](/power-platform/admin/settings-features).

## Data loss prevention (DLP)

You can control data loss prevention (DLP) policies within Power Platform admin center, **Data policies** menu item.

Connectors can be listed in three (3) categories: *Business*, *Non-business*, and *Blocked*.

- AI Builder is part of the Dataverse connector.

- Business and Non-business connectors can’t share data within the same consumption experience in Microsoft Power Platform.

  - For example, if you add the Dataverse connector in the *Business* category, and Microsoft Outlook in the *Non-business* category, you won’t be able to create a Power Automate flow that gets the output of an AI Builder model and sends it to a recipient in Outlook.

- Blocked connectors can’t be used in Power Platform consumption experiences.

To learn more, go to [Data loss prevention policies](/power-platform/admin/wp-data-loss-prevention).

## Move and copy environments

For prediction and prebuilt models, moving and copying environments is fully supported. For other models, after you move or copy an environment, you have to retrain and republish existing models to make them available again.

## Customer-managed keys (CMK) (preview)

[!INCLUDE [cc_preview_features_definition](./includes/cc-preview-features-definition.md)]

All your data stored in Power Platform is encrypted at rest using Microsoft-managed keys by default. With customer-managed keys (CMKs), you can bring your own encryption keys to encrypt Power Platform data, including AI Builder training data and trained models. This allows you to have an extra protective layer to manage your Power Platform assets. With this feature, you can rotate or swap encryption keys on demand. It also prevents Microsoft’s access to your customer data, if you choose to revoke key access to Microsoft services at any time.

> [!IMPORTANT]
> Only models created or copied to the environment after CMK is enabled are encrypted at rest with that key.
>
> Currently, customer-managed keys aren't leveraged to encrypt Object detection trained models. The training data of those modes stored in Dataverse is using customer managed keys.

Applying an encryption key is a gesture performed by Power Platform admins, and is invisible to users. Users can create, save, use, and include in solutions AI Builder models in exactly the same way they would if the data was encrypted by Microsoft-managed keys.

To learn more about the customer-managed key, and get step-by-step instructions to enable customer-managed keys, go to [Manage your customer-managed encryption key](/power-platform/admin/customer-managed-key). This enables you to leverage the single enterprise policy created on the environment to secure AI Builder models.

### See also

[Roles and security in AI Builder](security.md)<br/>
[Feature availability by region](availability-region.md)<br/>
[AI Builder consumption report](administer-consumption-report.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
