---
title: AI Builder Licensing- AI Builder | Microsoft Docs
description: Provides information about licensing in AI Builder.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 10/01/2019
ms.author: tatn
ms.reviewer: kvivek
---

# AI Builder Licensing


Power Platform administrators can use the [PowerApps admin center](https://admin.powerapps.com) and the [Power Platform Admin center](https://admin.powerplatform.microsoft.com) to manage environments and settings for PowerApps and AI Builder.

For more information, see the [Power Platform Administrator Guide](https://docs.microsoft.com/power-platform/admin/admin-documentation).

## Overview

AI Builder is licensed as an add-on to your PowerApps licenses. This means you can start your AI Builder trial after you have a PowerApps license that allows you to create a Common Data Service (CDS) instance.  

## Trial licenses

An AI Builder trial license enables you to use  AI Builder  for free for the duration of the trial period. 

What you get with an AI Builder trial license:
- Create and use AI models in any environment (trial or production) because AI Builder Trial is available at a user level, not environment level
- Store  your AI model results in Common Data Service
- Use  AI model results in your PowerApps, Flows, and elsewhere. 

After thet trial expires:
- You will need to sign up for a paid license to keep using your AI models and assign AI credits to an environment
- Trial environments are not available after 30 days
- No new model creation, and no new inference will be possible
- Existing models will not be able to be modified
- Models created in your Production environment will be deleted after 90 days if the trial license expires, however, model configurations will be saved in Common Data Service
Note:  These restrictions apply only to model types that have been released to  general availability. Model types inpreview release status will remain available without a license until they are released for general availability.  


For more information about trial environments, see https://docs.microsoft.com/en-us/power-platform/admin/trial-environments
- A trial license enables you to use all AI Builder model types and functionalities for 30 days free of charge. <Sign up link when available>
- After your trial period expires, you can’t create new models, or update existing ones until you purchase an AI Builder license. <Purchase link here when available>
- Ai Builder model types that are in preview release status  are free to use, and you do not need to start a trial license if you are only using preview release features. For example, the text classification model type will remain in preview release status during October 2019, but binary classification (prediction) will be released to general availability status (GA). To find out the release status for AI Builder features and model types,  select<Release page>
- AI Builder trial licenses is specific to a user not an environment. If you already have an environment with PowerApps license (free or paid), you can use that environment or create a new one for your AI Builder trial. Once you purchase the AI Builder license, the usage will be limited to a specific environement. 
- If you do not have a valid PowerApps license (free or paid), you will have the opportunity to sign up for a PowerApps license first and then AI Builder trial license. 

FAQ
How do I convert my Trial environment to a Production environment? https://docs.microsoft.com/en-us/power-platform/admin/trial-environments
What email address can I use? https://docs.microsoft.com/en-us/powerapps/maker/signup-for-powerapps#faq


## More information

More information about licenses and license management in PowerApps is available [here](//power-platform/admin/wp-license-management).
