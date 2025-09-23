---
title: New AI Builder Licensing
description: Learn about new licensing system of AI Builder 
author: Antoine2F
contributors:
  - Antoine2F
  - jkom1
  - v-aangie
ms.topic: article
ms.collection: 
    - bap-ai-copilot
ms.date: 09/23/2025
ms.update-cycle: 180-days
ms.author: antode
ms.reviewer: angieandrews
---

AI Builder licensing will see a major change happening on November 1st 2025. Goal of this page is to explain what will happen.  

# Overview of AI Builder Licensing and new licensing rules
AI Builder features (AI Prompts, AI Models) are available in 2 different contexts:
- Power Automate/Apps context : it allows to enrich Cloud flows, or Apps with AI Prompts or AI Models like document processing tools.
- Copilot Studio context: it allows to enrich Agents with AI Prompts, or Agent flows with AI Prompts or AI Models like document processing tools. In this context, AI Builder features are sometimes called 'AI Tools'.

In Copilot Studio context, AI Builder features are licensed based on Copilot Credits. This doesn't change.  

In Power Automate/Apps context, AI Builder features are licensed exclusively based on AI Builder credits up to November 1st, 2025.  

Starting November 1st, 2025, AI Builder features in Power Automate/Apps context will also be licensed based on Copilot Credits.  
Existing customers with paid or seeded AI Builder credits will continue using their AI Builder credits. 
When AI Builder credits are in overage, or not present, the licensing system will check Copilot Credits availability, and allow the feature to run if any.

New customers won't be able to purchase paid AI Builder credits addon, and won't receive seeded AI Builder credits in Power Automate premium licenses any more.
They will need Copilot Credits to access and run AI Builder features in Power Automate/Apps context.

This change comes along with several simplifications:
 - Access to AI Prompts and AI Models page in Power Automate and Power Apps portal doesn't require any AI Builder credits or Copilot Credits
 - All custom model trainings are now free
 - Binary classification and Business Card models are now free
 - AI Builder trials are no longer available
 - There is no distinction between simple and important overage
 - There is no extension requests any more

# Dual mode for existing customers : check AI Builder credits first, then fall back to Copilot Credits
This dual mode allows business continuity.
All existing Cloud flows and Apps will continue running their AI Builder features based on existing AI Builder credit assignments to their environments.  

**In the case an environment is in overage**, maker access won't be blocked.  An email will still be sent to admins, but extension requests won't be possible, and the licensing system will try to access Copilot Credits.
If there is no Copilot Credits available in this environment, AI Builder feature will be blocked. (without waiting for 'important overage')  
If there are Copilot Credits available in this environment, AI Builder feature will run successfully and consume these Copilot Credits.

# New customers exclusively rely on Copilot Credits for AI Builder features
It was already the case for AI Builder features in Copilot Studio context.
For new customers, it will also be the case for AI Builder features in Power Apps/Automate context.

# Copilot Credits management
Copilot Credits can be purchased as prepaid packs, and are also available as paygo.
Prepaid pack Copilot Credits can be assigned to environments. Each environment has a toggle to indicate whether it can consume unassigned Copilot Credits or not. 

## Copilot Credit Rate card
Each AI Builder Model or Prompt is consuming one of these 4 Copilot Features:
| Feature                                | Cost per page/image/1K characters/1K tokens | Prompts or Models consuming this feature |
|----------------------------------------|---------------------------------------------|------------------------------------------|
|Text and generative AI tools (basic)    | 0.1 Copilot Credit                          |Prompts using basic LLM,  Text recognition, Sentiment analysis, Language detection, Key phrase extraction|
|Text and generative AI tools (standard) | 1.5  Copilot Credits                        |Prompts using standard LLM, Text translation, Entity extraction, Category classification|
|Text and generative AI tools (premium)  | 10   Copilot Credits                        |Prompts using premium LLM|
|Content processing tools                | 8  Copilot Credits                          |Custom document processing, Invoice processing, Receipt processing, Identity document reader, Object detection |
 
Prompts are using the 'per 1K tokens' unit: for each prompt, the licensing system computes the size of input + output (including system prompt, reasoning) in tokens and rounds it up.  
This provides the number of 'Feature' which will be consumed.
Eg : A prompt based on standard model with 3.1K tokens in input and 1.5K tokens in output will consume 5 * 1.5 Copilot Credits = 7.5 Copilot Credits.

Custom document processing, Invoice processing, Receipt processing, Identity document reader, Object detection and Text recognition are using the 'per page' or 'per image' unit.
Eg : Processing a document with 3 pages using a Custom document processing model will consume 3 * 8 Copilot Credits = 24 Copilot Credits.

Sentiment analysis, Language detection, Key phrase extraction,  Text translation, Entity extraction, Category classification are using the 'per 1K characters' unit (rounded up).
Eg : Translating 3.4 K characters will consume 4* 1.5 Copilot Credits = 6 Copilot Credits.
 
# Consumption monitoring

Copilot Credit consumption will now include consumption coming from Power Automate/Apps context. It can be monitored in the PPAC/Copilot Studio section.  
AI Builder credit consumption will continue to be monitored in the PPAC/AddOns section.  

For environment using first AI Builder credits, then Copilot Credits, admins will need to check both reports.  
However, the AI Builder activity in the Power Automate portal will help  understand whether a particular action has been billed in AI Builder credit or Copilot Credit. 

Banners in the PPAC/AddOns section and emails will continue to inform admins about AI Builder credit overages.  

# End of AI Builder trials
Users who have started AI Builder trials will be able to use them until the end of the trial period (30 days), within the consumption limit (200,000 AI Builder credits).
Starting November 1st, it won't be possible for new customers to start or renew AI Builder trials : they will need to use Copilot Credits to use AI Builder features.  

# End of Extension requests
Extension requests will be available up to end of October.  
Starting November 1st, environments in overage will block AI Builder features, unless Copilot Credits are available, or admin allocates more AI Builder credits to the environment.

# Ungated access to AI Models and Prompts in Power Automate/Apps portal
Makers will now be able to train custom models, and test prebuilt and custom models or prompts in Power Automate and Power Apps portal, without any AI Builder credits, or Copilot Credits.  
Admins can decide to block access to Prompts using a specific toggle in PPAC.






