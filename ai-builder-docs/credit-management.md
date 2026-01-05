---
title: Licensing and AI Builder credits
description: Learn about licensing and AI Builder credit management.
author: Antoine2F
contributors:
  - PhillyUrbs
  - Antoine2F
  - chplanty
  - jkom1
  - v-aangie
ms.topic: article
ms.collection: 
    - bap-ai-copilot
ms.date: 01/05/2026
ms.update-cycle: 180-days
ms.author: antode
ms.reviewer: angieandrews
---

# Licensing and AI Builder credits

This article focuses on AI Builder credits management. 
 - Get a global view of AI Builder licensing in [Overview of Licensing](administer-licensing.md).
 - Learn about Copilot Credits management in the context of AI Builder features in [Licensing and Copilot Credits](message-management.md).

You can use AI Builder credits to run AI Builder features in Power Automate and Power Apps.

AI Builder credits come with some specific user licenses, but mostly from AI Builder capacity add-on. Learn more in this page in [Get entitlement to AI Builder credits](#get-entitlement-to-ai-builder-credits) section.  

Once acquired, AI Builder credits can be allocated (also known as assigned) to a specific environment, or left at the organization (tenant) level. Learn more in this page in [Make credits available for an environment](#make-ai-builder-credits-available-for-an-environment-allocated-and-unallocated-credits) section.  

Once an environment has access to AI Builder credits, AI Builder features are enabled in this environment.  

Some AI Builder actions consume AI Builder credits. Learn more in this page in [AI Builder credit consumption](#ai-builder-credit-consumption) section. AI Builder credit consumption can be monitored. Learn more in [Monitor usage](#monitor-usage) in this article.  

In an environment, when consumption exceeds available credits, the environment is in overage and some features might be blocked. You need to purchase AI Builder credits and/or reassign AI Builder credits or rely on Copilot Credits. Learn more in [Overage](#overage) in this article.

AI Builder is a premium feature within Power Apps. Adding an AI Builder action to an app transforms it into a premium app. This is also the case when incorporating a flow with an AI Builder action within an app. Premium apps have specific licensing requirements.

In Power Automate, adding an AI Builder action to a flow doesn't transform it into a premium flow.

## Get entitlement to AI Builder credits

First, you need to be entitled to some AI Builder capacity. Entitlement can happen through one of the following paid capacities.

- Some Microsoft products like Power Apps per app plan, Power Apps per user plan, and Power Automate Premium (previously Power Automate per user with attended RPA) plan include AI Builder capacity. Your environment admin can check entitlement in Power Platform admin center by following the instructions in [Capacity add-ons](/power-platform/admin/capacity-add-on). These seeded AI Builder credits will be removed on November 1, 2026. When this number isn't enough, you need to complete it with one or more AI Builder capacity add-ons.

- The main source of AI Builder credits is the AI Builder credit add-on. If you're an existing customer, you can renew or get more credits in the Microsoft 365 admin center up to November 1, 2026. New customers can't purchase AI Builder capacity add-on anymore, and must purchase Copilot Credits. See [Licensing and Copilot Credits](message-management.md)

### Number of AI Builder credits by license

The following table explains the rules for number of credits per license.

|License|Number of AI Builder credits|Rules|
|-|-|-|
|AI Builder add-on (T1, T2, T3)|1,000,000|None.|
| Power Apps Premium |500| Maximum = 1,000,000 AI Builder credits per tenant.|
| Power Apps per app |250| Maximum = 1,000,000 AI Builder credits per tenant. Per app licenses purchased before November 2022, don't include any credits.|
| Power Automate Premium |5,000| Maximum = 1,000,000 AI Builder credits per tenant.|
| Power Automate Process |5,000| Maximum = 1,000,000 AI Builder credits per tenant.|
| Power Automate Hosted RPA add-on |5,000| Maximum = 1,000,000 AI Builder credits per tenant.|
| Power Automate Unattended RPA add-on |5,000| Maximum = 1,000,000 AI Builder credits per tenant.|
| Dynamics 365 F&O|20,000| Maximum = 20,000 AI Builder credits per tenant. |
| Power Apps for Cloud for Sustainability USL Plus | 25,000 AI Builder credits| None.|

Post November 1, 2026, only AI Builder add-on credits remain active. All other ones are removed.

## Make AI Builder credits available for an environment: allocated and unallocated credits

By default, the AI Builder credits are unallocated (also known as unassigned) and available as a pool on the organization (tenant), which can be used on any environment.

As an administrator, you assess which environments must consume AI Builder credits. To estimate your credit's usage in a monthly period on each environment and assess the credits to allocate, use the AI Builder rate card in [Microsoft Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130) (pdf).

Allocation happens in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/) when you select **Licensing** > **Capacity add-ons** > **Add-ons** tab, and then select **Assign to an environment**.

### Block use of unallocated AI Builder credits

The administrator can block the use of unallocated AI Builder credits through an organization (tenant) setting in [Power Platform admin center](https://admin.powerplatform.microsoft.com/). To do this, remove the check from the **Allow users to consume unassigned AI Builder credits** checkbox.

:::image type="content" source="media/credit-management/credits.png" alt-text="Screenshot of the option to allow users to consume unassigned AI Builder credits in Power Platform admin center.":::

By default, this setting is enabled. When disabled, only environments with allocated AI Builder credits have access to AI Builder features.

Learn more in [Tenant settings](/power-platform/admin/tenant-settings).

> [!NOTE]
> This is how administrators stay in control of *where* AI is used in their organization and, with the role assignments described in [Roles and security in AI Builder](security.md#roles), *who* is using it.

Learn more about how to allocate AI Builder credits in the Power Platform admin center in [Allocate or change capacity in an environment](/power-platform/admin/capacity-add-on#allocate-or-change-capacity-in-an-environment).

## Monitor usage and understand AI Builder credit consumption

You can gain insights into your AI Builder credit consumption by monitoring usage.

### Monitor usage

Monthly consumption is computed from first day of the month and is refreshed periodically, ideally on a daily basis. However, it can happen that it isn't computed during a long period like seven (7) days.
As an administrator, you can view your overall computed AI Builder credit consumption in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/) in the **Licensing** > **Capacity add-ons** > **Summary** tab.  

The **Allocation bar** and the **Consumption bar** display the number of **allocated** AI Builder credits and **consumed** AI Builder credits out of the total number of **purchased** AI Builder credits.

:::image type="content" source="media/credit-management/ppac-consumption.png" alt-text="Screenshot of the overall AI Builder credit consumption in Power Platform admin center.":::

Administrators also have access to a [consumption report](administer-consumption-report.md) that has the following features:

- Provides the AI Builder credits consumption on a chosen period per environment.
- Allows you to fine-tune the AI Builder credits allocation, which can be updated at any time.
- Allows administrators to check the consumption level of an environment for the current month by adding all consumptions of this environment.

Administrators also can access the [AI Builder Activity](activity-monitoring.md) page in the Power Automate portal, showing in real time all predicts made against the AI Builder models in that environment.

### AI Builder credit consumption

Each AI Builder model has a different AI Builder credit consumption mechanism. To perform an assessment, use the [AI Builder capability rate table](administer-licensing.md#aibuildercapabilityrate-table)

#### Free actions

- Preview scenarios in AI Models don't consume credits, except Prompts, which always consume credits, even when in preview.

- Testing prompts in prompt builder doesn't consume credits.
- Training models in AI Models page doesn't consume credits.
- Testing prebuilt or custom models doesn't consume credits.

### AI prompt licensing

AI prompts can be utilized in Power Apps, Power Automate flows, and in Microsoft Copilot Studio in agent flows, or in agents.

They can run on AI Builder credits in the context of Power Apps and Power Automate flows.  
The number of consumed AI Builder credits depends on the input tokens (including system prompt tokens), output tokens (including reasoning tokens), and the underlying generative AI model used. Learn more in [Prompt tokens](licensing-prompt-tokens.md).

## Overage

Monthly consumption is computed from first day of the month and is refreshed periodically. You can check the computed consumption in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).
  
Available AI Builder credits are the allocated AI Builder credits if AI Builder credits are allocated to the environment, or the unallocated AI Builder credits if no AI Builder credit is allocated to the environment.  

There's overage when the computed monthly consumption is higher than the available AI Builder credits.
If there's overage, the system tries to use Copilot Credits. If there's no Copilot Credit available, running models in flows and apps is blocked. In this state, AI Builder actions fail with `EntitlementNotAvailable` `QuotaExceeded` error codes. In flow editor, remediation panel displays **All AI Builder credits in this environment have been consumed**.

To get details on your environment allocation, check the [Make credits available for an environment](credit-management.md#make-ai-builder-credits-available-for-an-environment-allocated-and-unallocated-credits) section in this article.

To get details on your environment consumption, check [Monitor usage](credit-management.md#monitor-usage) section in this article.

To provide capacity to your environment, you can:

 1. Reallocate existing capacity from the organization (tenant) or environment level. You need to allocate enough AI Builder credits to entirely fill the gap. This allocation can be important when computed monthly consumption takes a long time to be triggered.
 1. Purchase more AI Builder capacity and make it available to your environment (only for existing customers, up to November 1, 2026).
 1. Purchase Copilot Credits and make them available to your environment.
 1. Allow Copilot Credit pay-as-you-go capacity to your environment

## AI Builder licensing FAQ

### How many AI Builder credits are consumed for each operation?

Each AI Builder capability consumes AI Builder credits at a different rate. You can check the consumption rates in the [AI Builder capability rate table](administer-licensing.md#aibuildercapabilityrate-table).

### My Power Automate flow or my Power App fails in AI Builder with an error message that contains one of the following. How do I unblock it?

- **EntitlementNotAvailable**
- **NoCapacity**
- **QuotaExceeded**
- **No capacity was found**
- **Credit usage exceeds allocation**

You need to check entitlement allocation of your environment. If there's no allocation, and no allocation at the organization (tenant) level, [allocate capacity](credit-management.md#make-ai-builder-credits-available-for-an-environment-allocated-and-unallocated-credits) to the environment or organization (tenant) level from other environments or by [purchasing AI Builder add-on](credit-management.md#get-entitlement-to-ai-builder-credits).

If there are AI Builder credits allocated or available at organization (tenant) level, compare the number with the [AI Builder consumption report](administer-consumption-report.md).
Then [allocate more capacity](credit-management.md#make-ai-builder-credits-available-for-an-environment-allocated-and-unallocated-credits) eventually by [purchasing the AI Builder add-on](credit-management.md#get-entitlement-to-ai-builder-credits).

### I have seeded AI Builder credits. How many add-ons should I buy to cover my need?

AI Builder credits coming from the AI Builder add-on (1,000,000 credits per add-on) and AI Builder credits coming from licenses with seeded capacity (like Power Automate premium, which brings 5,000 credits) are gathered at the tenant level. They represent your entitlement.
Seeded credits will be removed on November 1, 2026.  
Example 1:

One (1) add-on + 5 Power Automate premium licenses gives 1,000,000+5*5,000 = 1,025,000 AI Builder credits that you can assign and consume in any scenario.

Example 2:

You have a scenario with 32,000 receipts to process each month with receipt processing.

32,000 receipts require 32 AI Builder credits per receipt (exact rates are in the [AI Builder capability rate table](administer-licensing.md#aibuildercapabilityrate-table)), so you have 1,024,000 AI Builder credits.

Suppose you own five (5) Power Automate premium licenses, you're covered with a single add-on:

One (1) add-on + 5 Power Automate premium licenses = 1,025,000 AI Builder credits, which is greater than your estimated consumption of 1,024,000 AI Builder credits.

### Where can I see AI Builder credit usage for this month?

Overall organization (tenant) level AI Builder credit computed consumption is available in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/) in the **Licensing** > **Capacity add-ons** > **Summary** tab. The Consumption bar displays the number of computed *consumed* AI Builder credits out of the total of *purchased* AI Builder credits.

The data is computed periodically, ideally on a daily basis. Some computation might be delayed; if so, the consumption bar shows all known consumption at the **Last updated** date in the tooltip box.

Get details on your environment consumption by checking the [AI Builder consumption report](administer-consumption-report.md). It gives the amount of computed consumption per day per user per environment.
Adding all the consumptions of the current month of a specific environment gives you the monthly computed consumption of this environment.

### How do I find out which model is using the most AI Builder credits?

Once you identify which environment consumes the most AI Builder credits with the [AI Builder consumption report](administer-consumption-report.md), you can leverage the model consumption data in the Dataverse **AI Event** table of that environment either in the Power Apps portal or the [AI Builder Activity](activity-monitoring.md) page in Power Automate.

### How do I know the number of purchased AI Builder credits of my organization (tenant)?

The [consumption bar and allocation bar](https://go.microsoft.com/fwlink/?linkid=2255314) display the number of *purchased* AI Builder credits.

AI Builder credits come from active AI Builder add-ons and are also seeded in premium licenses (up to November 1, 2026) like Power Automate Premium.

You can find the non allocated AI Builder credits in [Power Platform admin center](https://admin.powerplatform.microsoft.com/) and select **Licensing** > **Capacity add-ons** > **Assign to an environment**. It represents the purchased capacity, which isn't allocated yet.

### When is AI Builder credit usage count reset? Is it based on license acquisition date?

AI Builder credit usage is counted on a monthly basis, starting the first day of each month. It isn't based on the license acquisition date. AI Builder credit usage of an environment shouldn't exceed the AI Builder credit allocation, or else the environment is in overage.

### What happens to the remaining capacity at the end of the month? Is it used the following month?

No, unused capacity doesn't carry over to the next month. AI Builder credit usage is counted on a monthly basis and reset on first day of the month. Available capacity is based on allocated capacity.

### What can I do with the 5,000 AI Builder credits included in the per user plan with attended RPA?

Each user license grants you 5,000 AI Builder credits up to November 1, 2026, allowing you to assess the capabilities in AI Builder. For instance, you could use these AI Builder credits to extract data from a few documents with [document processing](form-processing-model-overview.md) or perform hundreds of basic OCR extractions with [text recognition](prebuilt-text-recognition.md).

### What happens if a user turns on/off AI Builder per user capacity add-on license?

Some user licenses include seeded AI Builder credits up to November 1, 2026. For example, the Power Apps per user license includes 500 seeded AI Builder credits. If **AI Builder capacity per user add-on** isn't selected, the 500 AI Builder credits are still added to the total number of AI Builder credits owned at your organization (tenant) level and can be used.

### Where can I learn more about license management in Power Apps and Power Automate?

Learn more about licenses and license management in Power Apps in [About licensing and license management](/power-platform/admin/wp-license-management).

### What are the differences between AI Builder credit assignment and credit AI Builder allocation?

AI Builder credit assignment and AI Builder credit allocation are same concept. In documentation, we mainly use allocation. In product, we mainly use assignment.

- assignment = allocation
- assigned credits = allocated credits = environment credits
- unassigned credits = unallocated credits = organization (tenant) level credits

### What are the differences between allocated AI Builder credits and unallocated AI Builder credits?

When an organization (tenant) purchases AI Builder capacity, corresponding AI Builder credits are by default unallocated and available as a pool for the organization (tenant). In this state, AI Builder credits can be used on any environment without assigned credits, unless admin blocks usage of unallocated AI Builder credits using the ['AI Builder credit'](#block-use-of-unallocated-ai-builder-credits) organization (tenant) setting.

The administrator can restrict usage by allocating all AI Builder credits to specific environments or by blocking the usage of unallocated AI Builder credits. They can reserve some capacity to an environment by allocating AI Builder credits to this environment.

Environments with allocated AI Builder credits only consume allocated AI Builder credits. There's no automatic switch to unallocated AI Builder credit consumption when in overage. Environments without allocated AI Builder credits only consume unallocated AI Builder credits.

Learn more in [Make credits available for an environment](credit-management.md#make-ai-builder-credits-available-for-an-environment-allocated-and-unallocated-credits) in this article.

Learn how to allocate capacity in [Power Platform admin center](https://admin.powerplatform.microsoft.com/) in [Allocate or change capacity in an environment](/power-platform/admin/capacity-add-on#allocate-or-change-capacity-in-an-environment).

### Is there a way to automatically consume organization (tenant) level AI Builder credits once environment allocated AI Builder credits are consumed?

No, AI Builder credits come from either environment allocation or organization (tenant) level unallocated AI  credits. There's no automatic switch from environment credits to organization (tenant) AI Builder credits.

As soon as the environment allocates AI Builder credits, AI Builder credits only come from environment AI Builder credits. If environment consumption is higher than allocated AI Builder credits, then the environment is in overage.

### If an environment is in overage, do the limitations apply to all environments?

No. Limitations only apply to the environments in overage. Other environments, whether consuming environment assignment or organization (tenant) level credits aren't affected.

For example, if an environment doesn't have allocated credit, and organization (tenant) level AI Builder credits aren't all consumed, then editing and running of AI Builder functions are allowed for this environment. This remains true when other environments with assigned AI Builder credits are in overage.

Consumption of unassigned AI Builder credits never affectS the consumption of an environment with assigned AI Builder credits, even if it's in overage. Consumption of credits in an environment with assigned AI Builder credits never affectS the consumption of AI Builder credits in other environments, even if it's in overage.
  
Global consumption graph is for information purpose, and indicates at least one environment is in overage, but doesn't mean that all environments are in overage. All environments with a computed consumption lower than their assignment, continue to work as expected.

### Are overages charged? Do overages affect next month consumption?

No, overage is considered as a grace period to help you adapt to new consumption pattern and is never charged. Overage doesn't affect the next month's consumption.

You should be concerned with an environment that consumes more than its capacity during a month, because it will be blocked at some point in the month (or switch to Copilot Credit consumption). It works again at the beginning of next month as consumption is reset and will restart consuming AI Builder credits.

### I created prompts before the model selection was possible. Which model and temperature were used?

By default, prompts were created with a basic model, so follow the basic rates.

### What happens to my prompt using a preview model if the AI Builder preview toggle is switched to off in Power Platform admin center?

Your prompt fails in any context (testing prompt in prompt builder, Power Apps, Power Automate, or Copilot Studio). You can edit your prompt and switch to another non preview model.

### What licensing applies to AI Builder's AI functions?

These AI Builder AI functions&mdash;AISummarize, AIExtract, AIReply, AIClassify, and AISentiment&mdash;are prebuilt prompts available in AI prompts.
They follow the same rates as AI Prompts in the basic category. See [AI Builder capability rate table](administer-licensing.md#aibuildercapabilityrate-table)

### Are all tests free?

Yes, all tests in AI Models page or in Prompt Builder are free.

### I built an app that includes a flow. I want to add an AI Builder action in this flow. Does it turn my app into a premium app?

Yes. By adding an AI Builder action to a flow inside your app, you turn your app into a premium app, so it requires a premium license to be used. However, your flow isn't considered as a premium flow.

## Related information

- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Licensing FAQ for AI Builder](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
