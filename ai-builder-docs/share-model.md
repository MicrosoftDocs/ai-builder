---
title: Share your processing model -  AI Builder | Microsoft Docs
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

# Sharing your AI Builder models with other users
When you create and publish AI Builder models, they remain private so only you can run them.
This allows you to test them and use them within apps or flows.

If you want other users in your organization to use your model within apps or flows, or even use direct API to make a prediction using your model, you need to share it with them.
This applies to users creating Apps or Flows which would call your model, and also to users who would simply run these Apps or Flows. Both App Makers and App users need a shared access to your model.

## Share action
Share action is available in Models page for each model where you are the owner.
It's also available if you are System admin in this environment, or other security role that was set up by your admin with the share privilege on AI Builder system entities.

Share action is also available in Model Detail Page, with same rules.

## Share panel
When clicking the share action, a share panel is displayed. 
It allows to select CDS users and CDS teams of your organization, and share your model with them.
"Sharing your model" with a user means give this user or Team the ability to see and run your model.
"Sharing your model" doesn't mean this user/team will be able to edit it, retrain it, or publish it.
"Sharing your model" doesn't mean this user/team will be able to access the data you used to train your model.

## FAQ
1. Can I allow other users to edit my model (Share for edit/co-owner)?
 Yes, but it requires an admin to go through Advanced Settings of the organization, select your AI Model and share it with proper rights with other users.
 We are considering to include the capability of making other users co-owner.
2. The owner of a model has left the company. How can we allow non admin users to edit this model?
 You need to reassign this model to another user. Reassign means changing ownership, and this operation can be done in the Advanced Settings of your organization.
 You also need to give proper access to data used to train the model.
3. Is this Sharing step mandatory to use an App which includes calls to an AI Model? Why is App sharing not enough?
Yes, it is mandatory. App sharing only allows users to launch the App.
Other access like data access or AI Model access must be granted separately.
AI Model access is given through this sharing mechanism. Without it, users will be able to launch the App, but won't be able to perform a call to the AI Model.
4.Is this Sharing step mandatory to allow other Environment makers to use my model in their apps?
Yes, it is mandatory. Your model won't be listed in the AI Model control if it hasn't been shared with the Maker of the App. This prevents all leak about your ongoing work while you feel it's not ready to be used, and allows you to decide who can access it.
5. Share action was not necessary when AI Builder was in preview. What happened?
We added this additional step to respect privacy and allow more targeted model to be built within environment without fear of leakage.


 
