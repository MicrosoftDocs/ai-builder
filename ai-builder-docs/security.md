---
title: Roles and security in AI Builder - AI Builder
description: Learn about security information related to roles, privileges, and access in AI Builder and the services it connects to.
author: jekom1
contributors:
  - jekom1
  - v-aangie
ms.topic: conceptual
ms.date: 12/06/2024
ms.author: jelenak
ms.reviewer: angieandrews
ms.collection: bap-ai-copilot
---

# Roles and security in AI Builder

AI Builder relies on environment security and Microsoft Dataverse security roles and privileges to grant access to AI features in Power Apps, Power Automate, and Microsoft Copilot Studio. For more information, go to [Security overview](/power-platform/admin/wp-security).

Some privileges are set by default in Dataverse. This allows built-in security roles to use AI Builder without further actions from system administrators. Specifically:

- Environment makers can use AI Builder to create AI models and prompts.
- Basic users can access data by using the models and prompts embedded in Power Apps.
- System administrators and system customizers can access all AI models and prompts created in the environment.

These security roles have privileges to the AI Builder tables in Dataverse. Custom security roles can create AI models and prompts if they have the same access to the AI Builder tables as the Environment Maker role.

:::image type="content" source="media/security-roles-screen-updated.png" alt-text="Screenshot of the security roles screen.":::

Scenarios such as object detection, category classification, and prediction need read access to Dataverse tables. Make sure Environment Makers have access to them. They need those tables for objects to detect, tagged text, and input data.

Some features need System Customizer privileges to publish your AI models and to allow them to be consumed. These actions can make changes to the Dataverse schema. Administrators should assign System Customizer privileges to users who want to create such AI models.

When you create a prediction AI model, a new data column is added to the input table to store the prediction results. For this reason, you need at least System Customizer rights to publish the model for the first time.

For category classification AI models, a data table is created for every new model as soon as the model runs for the first time. Therefore, only System Customizers or System Administrators can run the model. After the model runs, System Administrators must modify the access rights to the newly created category classification table in Dataverse to allow users to use the results.

## Roles

Microsoft Dataverse permissions are mapped to the Dataverse standard roles. Assigning these roles to a user provides the necessary privileges to use AI Builder features as described in this table.

| Privilege                            |System Administrator/Customizer|Environment Maker                                  |Basic User                                     |No privilege|
|-----------------------------|:-----------------------------:|:-------------------------------------------------:|:-------------------------------------------------:|:--:|
|View AI Builder Explore page   |&check;              |&check;                                  |&check;                                  |&cross;  |
|Create a model/prompt               |&check;             |&check;                                 |&cross;                                                |&cross; |
|View and use a created model/prompt |&check;             |owned or shared model/prompt                              |owned or shared model/prompt                              |&cross; |
|Create a flow to call a model/prompt|&check;             |&check;                                 |&cross;                                                |&cross; |
|Create an app to call a model/prompt|&check;             |&check;                                 |&cross;                                                |&cross; |
|Run a flow using a model/prompt     |&check;             |owned or shared flow using an owned or shared model/prompt|owned or shared flow using an owned or shared model/prompt|&cross; |
|Run an app using a model/prompt     |&check;             |owned or shared app using an owned or shared model/prompt |owned or shared app using an owned or shared model/prompt |&cross; |
|View AI Builder activity     |&check; (all rows)            |&check; (owned rows) |&check; (owned rows) |&cross; |

## Tables and privileges

By default, a model/prompt is only accessible by the owner of the model/prompt, so it must be shared to be used by other users. To share a model/prompt:

### Power Automate

1. On the left panel:

    - (For models) On the left panel, select **AI Models** > **My models** > *model name*
    - (For prompts) On the left panel, select **AI Models** > the **Prompts now have their own section** tile > **My prompts** > *prompt name*

1. To access its details page, find and select the model’s or prompt's name.
1. On the top-left corner, select **Share**.

### Power Apps

1. On the left panel, select **AI Hub** > **AI prompts** or **AI Models**.
1. To access its details page, find and select the model’s or prompt's name.
1. On the top-left corner, select **Share**.

### Microsoft Copilot Studio

1. On the left panel, select **Prompts (preview)** > **My prompts**.
1. To access its details page, find and select the model’s or prompt's name.
1. On the top-left corner, select **Share**.

The following table shows the AI Builder system tables, which are installed by default on every new environment. The tables are used to store the model configuration and training data. Each table shows the Dataverse privilege applied by AI Builder, including when a user shares a model. See the legend below the table.<br/><br/>

|Dataverse table  |Contains  |Create<br/> Dataverse privilege  |Use<br/> Dataverse privilege  |
|---------|---------|:---------:|:---------:|
|AI Builder Dataset (FP, OD, EE)   |Model’s training configuration         | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")       | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")<br/>(when shared)         |
|AI Builder Dataset File (FP, OD)     |Model’s training configuration         | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")        | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")<br/>(when shared)         |
|AI Builder Dataset Record (EE)     |Model’s training data         | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")        | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")<br/>(when shared)         |
|AI Builder Dataset Container (FP, OD, EE)    |Model’s training configuration         | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")        | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")<br/>(when shared)         |
|AI Builder File (FP, OD)    | Model’s training files        | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")        | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")<br/>(when shared)         |
|AI Builder File Attached Data (FP, OD)   |Model’s training configuration         | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")        | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")<br/>(when shared)         |
|AI Configuration    | Model's versions        | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")        | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")<br/>(when shared)        |
|AI Event   | Model activity       | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")        | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")|
|AI Model   | Model        | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")        | ![Users have access to the rows they've created](media/circle-no-fill.png "Users have access to the rows they've created")<br/>(when shared)         |
|AI Template     | Model type stereotype        | ![Users have access to all the rows of the table](media/circle-fill.png "[Users have access to all the rows of the table")        | ![Users have access to all the rows of the table](media/circle-fill.png "[Users have access to all the rows of the table")        |
|User-defined table to be predicted<br/>(batch P & CC only)     |         | ![Users must be granted access to the subset of rows required for the business](media/circle-dot.png "[Users must be granted access to the subset of rows required for the business")        | ![Users must be granted access to the subset of rows required for the business](media/circle-dot.png "[Users must be granted access to the subset of rows required for the business")        |

![Users have access to the rows they created](media/circle-no-fill.png "Users have access to the rows they created")Users have access to the rows they created.<br/>
![Users must be granted access to the subset of rows required for the business](media/circle-dot.png "[Users must be granted access to the subset of rows required for the business") Users must be granted access to the subset of rows required for the business.<br/>
![Users have access to all the rows of the table](media/circle-fill.png "[Users have access to all the rows of the table") Users have access to all the rows of the table.<br/>
**FP:** document processing **OD:** object detection  **EE:** entity extraction  **P:** prediction  **CC:** category classification<br/><br/>

The training files stored in the AI Builder File table are accessible only by the person who created the model. The exception is the administrator, who can view and delete any model, related data, and configuration.

AI Builder doesn’t support shared ownership of a model. It's possible to change the owner by following this procedure in [Share your AI model](share-model.md#the-owner-of-a-model-has-left-the-company-how-can-we-allow-non-admin-users-to-edit-this-model).

## Related information

[Security concepts in Dataverse](/power-platform/admin/wp-security-cds)


[!INCLUDE[footer-include](includes/footer-banner.md)]
