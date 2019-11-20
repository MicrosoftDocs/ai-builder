---
title: Share your AI model -  AI Builder | Microsoft Docs
description: Walks you through the steps to share your model in AI Builder.
author: Antoine2F
manager: cdbellar
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 08/26/2019
ms.author: antode
ms.reviewer: cdbellar
---

# Share your AI models

When you create and publish AI  models in AI Builder, they are private - only you can run them. This allows you to test them and use them within apps or flows.

If you want other users in your organization to use your model in apps or flows, or even use a direct API to make a prediction using your model, you have to share it. This applies to users creating apps or flows which would call your model, and also to users who would simply run these apps or flows. Both app makers and app users need a shared access to your model.

## Share action

The share action is available on the Models page in AI Builder for each model where you are the owner. It's also available if you are system administrator in the environment, or for any security role that was set up with the share permissions on AI Builder system entities by the administrator.

The share action is also available on the Model detail screen in AI Builder, with same rules.

## Share panel

When you select the share action, a share panel is displayed. This is where you select Common Data Service users and teams in your organization, and share your model with them.

- "Sharing your model" with a user means give this user or team the ability to see and run your model.
- "Sharing your model" doesn't mean this user/team will be able to edit it, retrain it, or publish it.
- "Sharing your model" doesn't mean this user/team will be able to access the data you used to train your model.

## Model list views

The models you create and the models that are shared with you are now shown in model list under two different views:

- **My models**
- **Shared with me**

 > [!NOTE]
 > If you are an administrator of the environment,  all models in your environment appear under **Shared with me** view, whether shared or not.

When a model is shared with you, you have user permissions on it, so you can use it in apps or flows. You cannot view details or edit the model. No actions are available for you to perform on models in the **Shared with me** list.

It may happen that as administrator or owner of a model, only the **Delete** action is available.  This happens when the model type is no longer supported.  It may be that the model type was a preview feature,  and the administrator [disabled AI Builder preview features](administer.md#enable-or-disable-ai-builder-preview-features).

## FAQ

### Is this sharing step mandatory to use an app that includes calls to an AI Model? Why is app sharing not enough?

Yes, it is mandatory. App sharing only allows users to launch the app. Other access like data access or AI Model access must be granted separately. AI Model access is given through this sharing mechanism. Without it, users will be able to launch the app, but won't be able to perform a call to the AI Model.

### Is this sharing step mandatory to allow other environment makers to use my model in their apps?

Yes, it is mandatory. Your model won't be listed in the AI Model control if it hasn't been shared with the maker of the app. This d allows you to control access to your work and decide when to release it.

### The share action was not necessary when AI Builder was in preview. What happened?

We added this additional step to help with privacy concerns, and to allow a model to be built within environment without fear of leakage.

### Can I allow other users to edit my model?
 
 Yes, it requires an administrator to go through advanced settings of your organization, select your AI Model and share it with other users with write, append privileges.

### The owner of a model has left the company. How can we allow non admin users to edit this model?

 You need to reassign this model to another user. Reassign means changing ownership in the advanced settings of your organization in AI Builder.  You also need to give  access to data used to train the model.

### Can I disable the sharing feature for AI model makers and only allow Administrators to perform it?

Yes, as administrator you can create in advanced settings of your organization a security role where Share privilege is disabled on "AI Model" custom entity and gives AI Model makers this role.

### Why can't I share generic prediction models?

Generic prediction models only work as part of a scheduled run. They cannot be used in Power Apps or Power Automate, so the share action is not available.
