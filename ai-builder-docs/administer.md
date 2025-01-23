---
title: Administer AI Builder - AI Builder
description: Administrators can learn about AI custom models and environment lifecycle, backup and restore, managing capacity, enabling or disabling the feature, and data loss prevention in AI Builder.
author: mregateiro
contributors:
  - mregateiro
  - jekom1
  - Antoine2F
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.date: 10/22/2024
ms.author: miregate
ms.reviewer: angieandrews
---

# Administer AI Builder

Microsoft Power Platform administrators can use the [Power Apps admin center](https://admin.powerapps.com) and the [Power Platform admin center](https://admin.powerplatform.microsoft.com) to manage environments and settings for Power Apps and AI Builder.

Learn more in [Power Platform administrator guide](/power-platform/admin/admin-documentation).

The availability, which is also known as the release status, of AI Builder is dependent on your region. For a breakdown of AI Builder feature availability by region, go to [Feature availability by region](availability-region.md).

Learn more by downloading the [AI Builder governance whitepaper](https://go.microsoft.com/fwlink/?linkid=2244137&clcid=0x409).

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

Learn more about on how to distribute an AI model as a solution component in [Distribute your AI model](distribute-model.md).

### Environment lifecycle

AI Builder models are fully moved, along with user data, during environment backup/restore and environment copy operations.

After restore and copy operations, document processing and object detection models might be in the importing state for a few minutes while copies are made in the back end.

## Backup and restore

Microsoft Dataverse has backup and restore capabilities to help protect your apps' data, providing continuous availability of service. System administrators and delegated admin users can use the standard capabilities described in [Back up and restore environments](/power-platform/admin/backup-restore-environments).

- Backup and restore are fully supported for prediction, object detection, document processing, and prebuilt models.

  > [!NOTE]
  > For object detection and document processing models, the restore process might take some time to be completed. The AI Builder models list shows an "importing" status message while the restore operation is in progress.

- **For models not supported by backup and restore**: If you restore an environment, you have to retrain and republish these models to make them available again.

## Prerequisite to set up an environment ready for AI Builder

AI Builder is licensed as an add-on to your Power Apps, Power Automate, or Dynamics 365 license. This means you need a Power Apps, Power Automate, or Dynamics 365 license that allows you to create a Microsoft Power Platform environment.

## Manage AI Builder credits

Access to AI Builder features within an environment requires access to AI Builder credits.

To learn more, go to [AI Builder licensing and credit management](credit-management.md).

## Where and how are data stored in Dataverse?

Your AI model is deployed in the region that hosts the environment. For example, if your environment is created in the Europe region, your model is deployed in datacenters in Europe. Learn more in [Environments overview](/power-platform/admin/environments-overview).

Images and documents used for training purposes in object detection and document processing models are persisted in Dataverse.

  - They're used solely to train the AI Builder model and never used for any other purpose.
  - Training data is never shared externally.

In contrast, images and documents used at prediction time aren't persisted. Examples of non-persisted images and documents are those in a Power Apps component framework (PCF) control and in Power Automate.

Inputs of text scenarios are persisted in the AI Event Dataverse table to allow users to monitor [AI Builder activity](activity-monitoring.md).

Dataverse has strong security mechanisms that prevent unauthorized access to user data. Data stored to train your AI Builder model is only accessible by the following users:

- The owner of the model.
- Individuals with Power Platform **System Administrator** and **System Customizer** roles in your organization.

Learn more in [Roles and security in AI Builder](/ai-builder/security).

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
  - We don't delete existing models that users of this environment created.
  - AI Builder components are disabled.
  - Existing experiences that use existing AI Builder components fail or return errors.
  - Admins and owners can delete preview models.

- If you enable **AI Builder preview models** again:
  - AI Builder components are available again.
  - Components function as they did before the feature was disabled (assuming nothing else changed).

For more information about enabling or disabling features in the Power Platform admin center, go to [Manage feature settings](/power-platform/admin/settings-features).

## Enable or disable AI prompts in Power Platform and Copilot Studio

By default, the AI prompts feature is enabled for makers to create and experiment with various AI-generated content. Admins can enable or disable this feature as needed.

If you turn off [AI prompts](prompts-overview.md), you aren't be able to use custom or prebuilt prompts. These prompts are essential for tasks like summarizing, categorizing, translating, text completion and generation, and more. They help automate and streamline your work in Power Automate, Power Apps, and Copilot Studio.

An AI prompt is a natural language instruction using a large language model such as GPT, which allows you to perform tasks and serve as a companion to help you meet specific business needs.

Without this feature, these advanced capabilities aren't available.

To control AI prompts feature availability for an environment:

1. Sign in to [Power Platform admin center](https://admin.powerplatform.microsoft.com).
2. In the admin center, select **Environments** > *[select an environment]* > **Settings** > **Product** > **Features**.
3. On the **Features** settings page under **AI Builder**, enable or disable the **AI prompts** the toggle.

If your environment is part of an [environment group](/power-platform/admin/environment-groups), you can also govern AI prompts feature availability through the AI prompts environment group rule. 

1. Sign in to [Power Platform admin center](https://admin.powerplatform.microsoft.com).
2. In the admin center, select **Environment groups** > *[select an environment group]* > **Rules**.
3. On the **Rules** tab under **AI prompts**, enable or disable the **AI prompts** toggle > **Save**
4. Select **Publish rules** to apply the rules to the environments in the group.

If an environment group rule governing AI prompts is published, it locks the AI prompts setting at the environment-level, preventing any system administrator of those individual environments from editing the setting. To change the setting, admins must modify the corresponding rule in the environment group that includes the environment. 

## Data loss prevention (DLP)

You can control data loss prevention (DLP) policies within Power Platform admin center, **Data policies** menu item.

Connectors can be listed in three (3) categories: *Business*, *Non-business*, and *Blocked*.

- AI Builder is part of the Dataverse connector.

- Business and Non-business connectors can’t share data within the same consumption experience in Microsoft Power Platform.

  - For example, if you add the Dataverse connector in the *Business* category, and Microsoft Outlook in the *Non-business* category, you aren't able to create a Power Automate flow that gets the output of an AI Builder model and sends it to a recipient in Outlook.

- Blocked connectors can’t be used in Power Platform consumption experiences.

Learn more in [Data loss prevention policies](/power-platform/admin/wp-data-loss-prevention).

## Move and copy environments

For prediction and prebuilt models, moving and copying environments is fully supported. For other models, after you move or copy an environment, you have to retrain and republish existing models to make them available again.

## Customer-managed keys (CMK)

All your data stored in Power Platform is encrypted at rest using Microsoft-managed keys by default. With customer-managed keys (CMKs), you can bring your own encryption keys to encrypt Power Platform data, including AI Builder training data and trained custom models or prompts. This allows you to have an extra protective layer to manage your Power Platform assets. With this feature, you can rotate or swap encryption keys on demand. It also prevents Microsoft’s access to your customer data, if you choose to revoke key access to Microsoft services at any time.

> [!IMPORTANT]
> Only models or prompts created or copied to the environment after CMK is enabled are encrypted at rest with that key.
>
> Currently, Object detection trained models continue to be encrypted using Microsoft-managed keys. The training data of those models is stored in Dataverse, using customer managed keys if CMK is enabled.

Applying an encryption key is a gesture performed by Power Platform admins, and is invisible to users. Users can create, save, use, and include in solutions AI Builder models in exactly the same way as if the data was encrypted by Microsoft-managed keys.

Learn more about the customer-managed key and get step-by-step instructions to enable customer-managed keys in [Manage your customer-managed encryption key](/power-platform/admin/customer-managed-key). This enables you to leverage the single enterprise policy created on the environment to secure AI Builder models.

## Related information

- [Roles and security in AI Builder](security.md)
- [Feature availability by region](availability-region.md)
- [AI Builder consumption report](administer-consumption-report.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
