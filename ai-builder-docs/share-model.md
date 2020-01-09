---
title: Share your AI model -  AI Builder | Microsoft Docs
description: Walks you through the steps to share your model in AI Builder.
author: Antoine2F
manager: cdbellar
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 01/03/2020
ms.author: antode
ms.reviewer: cdbellar
---

# Share your AI models

When you create and publish AI  models in AI Builder, they're private - only you can run them. This allows you to test them and use them within apps or flows.

If you want other users to use your model in apps or flows, or even use a direct API to make a prediction using your model, you have to share it. This applies to users creating apps or flows that call your model, and also to users who just run these apps or flows. Both app makers and app users need a shared access to your model.

## Share action

The share action is available on the **Models** page in AI Builder for each model where you're the owner. It's also available for the system administrator in the environment, or for any security role that has  share permissions on AI Builder system entities.

The share action is also available on the Model detail screen in AI Builder, with same rules.

## Share panel

When you select the share action, a share panel is displayed. The share panel is where you select Common Data Service users and teams in your organization, and share your model with them.

- "Sharing your model" with a user gives the user or team the ability to see and run your model.
- "Sharing your model" doesn't give the user or team permission to edit, retrain, or publish the model.
- "Sharing your model" doesn't give the user or team access to the data you used to train your model.

## Model list views

The models you create and the models that are shared with you appear in the model list under two different views:

- **My models**
- **Shared with me**

 > [!NOTE]
 > If you are an administrator of the environment,  all models in your environment appear under **Shared with me** view, whether shared or not.

When a model is shared with you, you have user permissions to it. You can use it in apps or flows. You can't view details or edit the model. No actions are available for models in the **Shared with me** list.

In some cases as administrator or owner of a model, only the **Delete** action is available. This happens when the model type is no longer supported.  It may be that the model type was a preview feature,  and the administrator [disabled AI Builder preview features](administer.md#enable-or-disable-ai-builder-preview-features).

## FAQ

### Is the sharing step necessary to use an app that includes calls to an AI Model? Why is app sharing not enough?

Yes. App sharing only allows users to launch the app. Things like data access or AI model access are granted separately. AI model access is given through the sharing mechanism. Without it, users could launch the app, but couldn't execute a call to the AI model.

### Is the sharing step necessary to allow other environment makers to use my model in their apps?

Yes. Your model isn't listed in the AI model control if it isn't shared with the maker of the app. This helps control access to your work and decide when to release it.

### The share action wasn't necessary when AI Builder was in preview. What happened?

We added the share action to help with privacy concerns. Now, you can build a model in your environment without fear of leakage.

### Can I allow other users to edit my model?

Yes. In the advanced settings of your organization, an administrator has to select your AI model and share it with other users, giving write, and append privileges.

### The owner of a model has left the company. How can we allow non-admin users to edit this model?

Reassign this model to another user. Reassign means changing ownership in the advanced settings of your organization in AI Builder.  You also need to give  access to data used to train the model.

### Can I disable the sharing feature for AI model makers and only allow Administrators to do it?

Yes. In advanced settings of your organization,  an administrator must create a security role where the share privilege is disabled for the **AI Model** custom entity. Assign this role to AI model makers.

### Why can't I share generic prediction models?

Generic prediction models only work as part of a scheduled run. They can't be used in Power Apps or Power Automate, so the share action is not available.
