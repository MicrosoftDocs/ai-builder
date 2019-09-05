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

If you want other users in your organization to use your model in apps or flows, or even use a direct API to make a binary classification using your model, you have to share it. This applies to users creating apps or flows which would call your model, and also to users who would simply run these apps or flows. Both app makers and app users need a shared access to your model.

## Share action

The share action is available on the Models page in AI Builder for each model where you are the owner. It's also available if you are system admininistrator in the environment, or for any security role that was set up with the share permissions on AI Builder system entities by the administrator .

The share action is also available on the Model detail screen in AI Builder, with same rules.

## Share panel

When you select the share action, a share panel is displayed. This is where you select Common Data Service users and teams in your organization, and share your model with them.

  - "Sharing your model" with a user means give this user or team the ability to see and run your model.
  - "Sharing your model" doesn't mean this user/team will be able to edit it, retrain it, or publish it.
  - "Sharing your model" doesn't mean this user/team will be able to access the data you used to train your model.

## Model list pivots
The models you created and the models which were shared with you are now available in Model list under 2 different pivots:
  -My models
  -Shared with me
If you are an Administrator of the environment, you will also be able to see all models under 'Shared with me' pivot, whether explicitely shared or not.
When a model is shared with you, you have 'User' permission on it, so you can use it in Apps or Flow. You cannot view details, or edit it: you cannot perform any action from a model in this list.
It may happen that as Administrator, or as Owner of a model, you only have the Delete action available: that means that this model type is not supported any more, likely because it was in preview and Administrator has chosen to disable models in preview. (see   Administer AI Builder -> Enable or disable AI Builder preview features)

## FAQ

- *Can I allow other users to edit my model?*
 
 Yes, but it requires an administrator to go through advanced settings of the organization, select your AI Model and share it with other users.

- *The owner of a model has left the company. How can we allow non admin users to edit this model?*

 You need to reassign this model to another user. Reassign means changing ownership in the advanced settings of your organization in AI Builder.  You also need to give  access to data used to train the model.

- *Is this sharing step mandatory to use an app that includes calls to an AI Model? Why is app sharing not enough?*

Yes, it is mandatory. App sharing only allows users to launch the app. Other access like data access or AI Model access must be granted separately. AI Model access is given through this sharing mechanism. Without it, users will be able to launch the app, but won't be able to perform a call to the AI Model.

- *Is this sharing step mandatory to allow other environment makers to use my model in their apps?*

Yes, it is mandatory. Your model won't be listed in the AI Model control if it hasn't been shared with the maker of the app. This d allows you to control access to your work and decide when to release it.

- *The share action was not necessary when AI Builder was in preview. What happened?*

We added this additional step to help with privacy concerns, and to allow a model to be built within environment without fear of leakage.

