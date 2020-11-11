---
title: Share your AI model - AI Builder | Microsoft Docs
description: Walks you through the steps to share your model in AI Builder.
author: Antoine2F
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 11/06/2020
ms.author: antode
ms.reviewer: v-dehaas
---

# Share your AI model

[!INCLUDE [cc-data-platform-banner](includes/cc-data-platform-banner.md)]

When you create and publish AI models in AI Builder, they're private&mdash;only you can run them. This allows you to test them and use them within apps or flows.

If you want other users to use your model in apps or flows, or even use a direct API to make a prediction using your model, you have to share it. This applies to users who create apps or flows that call your model, and also to users who just run those apps or flows. Both app makers and app users need a shared access to your model.

## Share action

The share action is available on the **Models** page in AI Builder for each model where you're the owner. It's also available for the system administrator in the environment, or for any security role that has Share permissions on AI Builder system entities.

The share action is also available on the model detail screen in AI Builder, with the same conditions.

## Share panel

When you select the share action, a share panel is displayed. The share panel is where you select Microsoft Dataverse users and teams in your organization, and share your model with them. Note the following:

- Sharing your model with a user or team gives the user or team the ability to see and run your model.
- Sharing your model doesn't give the user or team permission to edit, retrain, or publish the model.
- Sharing your model doesn't give the user or team access to the data you used to train your model.

## Model list views

The models you create and the models that are shared with you appear in the model list under two different views:

- **My models**
- **Shared with me**

 > [!NOTE]
 > If you're an administrator of the environment, all models in your environment appear in the **Shared with me** view, whether they've been shared or not.

When a model is shared with you, you have user permissions to it. You can use it in apps or flows, but you can't view details or edit the model. No actions are available for models in the **Shared with me** list.

As an admin or owner of a model, you might encounter a model where the only available action is **Delete**.<!--Suggested--> This happens when the model type is no longer supported. It might be that the model type was a preview feature, and the admin [disabled AI Builder preview features](administer.md#enable-or-disable-ai-builder-preview-features).

## FAQ

### Is the sharing step necessary to use an app that includes calls to an AI model? Why is app sharing not enough?

App sharing only allows users to open the app. Things like data access or AI model access are granted separately. AI model access is given through the sharing mechanism. Without it, users can open the app, but the app<!--Suggested--> can't execute a call to the AI model.

### Is the sharing step necessary to allow other environment makers to use my model in their apps?

Yes. Your model isn't listed in the AI model control if it isn't shared with the maker of the app. This helps you control access to your work and decide when to release it.

### The share action wasn't necessary when AI Builder was in preview. What happened?

We added the share action to help with privacy concerns. Now, you can build a model in your environment without fear of its being released prematurely.<!--Suggested-->

### Can I allow other users to edit my model?

Yes. In the advanced settings of your organization, an admin has to select your AI model and share it with other users by giving Write and Append privileges.

### The owner of a model has left the company. How can we allow non-admin users to edit this model?

Reassign this model to another user. _Reassign_ means changing ownership in the advanced settings of your organization in AI Builder. You also need to give access to the data used to train the model.

### Can I disable the sharing feature for AI model makers and only allow admins to do it?

Yes. In advanced settings of your organization, an admin must create a security role where the share privilege is disabled for the **AI Model** custom entity. Assign this role to AI model makers.

### Why can't I share generic prediction models?

Generic prediction models only work as part of a scheduled run. They can't be used in Power Apps or Power Automate, so the share action isn't available.

### Next step

[Distribute your AI model](distribute-model.md)

