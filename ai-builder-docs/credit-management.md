---
title: Licensing and AI Builder credits
description: Learn about licensing and AI Builder credit management.
author: Antoine2F
contributors:
  - Antoine2F
  - chplanty
  - jkom1
  - v-aangie
ms.topic: article
ms.collection: 
    - bap-ai-copilot
ms.date: 09/16/2025
ms.update-cycle: 180-days
ms.author: antode
ms.reviewer: angieandrews
---

# Licensing and AI Builder credits

This article focuses on AI Builder in the Power Apps and Power Automate context.

Access to AI Builder features within an environment requires AI Builder credits. AI Builder credits come with some specific user licenses, but mostly from AI Builder capacity add-on. Learn more in [Get entitlement to AI Builder credits](credit-management.md#get-entitlement-to-ai-builder-credits). Once acquired, credits can be allocated (also known as assigned) to a specific environment, or left at the organization (tenant) level. Learn more in [Make credits available for an environment](credit-management.md#make-ai-builder-credits-available-for-an-environment-allocated-and-unallocated-credits).

> [!NOTE]
> - Learn how to use AI models and prompts in Copilot Studio or agent flows in [Licensing and Copilot Credits](message-management.md).
> - Learn about licensing in [Copilot Studio licensing](/microsoft-copilot-studio/requirements-messages-management#message-scenarios).

Once an environment has access to AI Builder credits, AI Builder features are enabled in this environment.

Some AI Builder actions consume AI Builder credits. Learn more in [AI Builder credit consumption](#ai-builder-credit-consumption) in this article. AI Builder credit consumption can be monitored. Learn more in [Monitor usage](#monitor-usage) in this article.

In an environment, when consumption exceeds available credits, the environment is in overage and some features are progressively blocked. You need to purchase AI Builder credits and/or reassign AI Builder credits. Learn more in [Overage](#overage) in this article.

AI Builder credits can also come from AI Builder trial. In this case, they link to the user and don't need to be allocated. Learn more in [AI Builder trial](ai-builder-trials.md).

AI Builder is a premium feature within Power Apps. Adding an AI Builder action to an app transforms it into a premium app. This is also the case when incorporating a flow with an AI Builder action within an app. Premium apps have specific licensing requirements.

In Power Automate, adding an AI Builder action to a flow doesn't transform it into a premium flow.

## Get entitlement to AI Builder credits

First, you need to be entitled to some AI Builder capacity. Entitlement can happen through one of the following paid capacities.

- Some Microsoft products like Power Apps per app plan, Power Apps per user plan, and Power Automate Premium (previously Power Automate per user with attended RPA) plan include AI Builder capacity. Your environment admin can check entitlement in Power Platform admin center by following the instructions in [Capacity add-ons](/power-platform/admin/capacity-add-on). When this number isn't enough, you need to complete it with one or more AI Builder capacity add-ons.

- The main source of credits is the AI Builder credit add-on, which you can purchase in the Microsoft 365 admin center:

    1. In the admin center, select **Billing** > [Purchase services](https://go.microsoft.com/fwlink/p/?linkid=868433).
  
        You need to be the billing administrator of your organization (tenant) to access this page.
    1. On the **Purchase services** page, do the following steps:

        1. Search for **AI Builder**.
        1. On the **AI Builder Capacity add-on** tile, select **Details**.
        1. Follow the purchase process.

### Number of AI Builder credits by license

The following table explains the rules for number of credits per license.

|License|Number of AI Builder credits|Rules|
|-|-|-|
|AI Builder add-on (T1, T2, T3)|1,000,000|None.|
| Power Apps Premium |500| Maximum = 1,000,000 AI Builder credits per tenant.|
| Power Apps per app |250| Maximum = 1,000,000 AI Builder credits per tenant. Per app licenses purchased before November 2022 don't include any credits.|
| Power Automate Premium |5,000| Maximum = 1,000,000 AI Builder credits per tenant.|
| Power Automate Process |5,000| Maximum = 1,000,000 AI Builder credits per tenant.|
| Power Automate Hosted RPA add-on |5,000| Maximum = 1,000,000 AI Builder credits per tenant.|
| Power Automate Unattended RPA add-on |5,000| Maximum = 1,000,000 AI Builder credits per tenant.|
| Dynamics 365 F&O|20,000| Maximum = 20,000 AI Builder credits per tenant. |
| Power Apps for Cloud for Sustainability USL Plus | 25,000 AI Builder credits| None.|

### Entitlement through AI Builder trial

Entitlement can be through a trial. AI Builder credits are then linked to a user. Trials are available only when there's no paid capacity within the organization (tenant).

In a trial, there's no need for allocating AI Builder credits to an environment. Trials can be used in any environment. A trial brings 200,000 AI Builder credits and is valid 30 days.

Once AI Builder credits are consumed, AI Builder models are blocked for this user.
At the end of the 30 days, a trial can be renewed, and user receives another 200,000 AI Builder credits. Renewal is only allowed for a limited number of times.

Learn more in [AI Builder trial](ai-builder-trials.md).

## Make AI Builder credits available for an environment: allocated and unallocated credits

By default, the AI Builder credits are unallocated (also known as unassigned) and available as a pool on the organization (tenant), which can be used on any environment.

As an administrator, you assess which environments must consume AI Builder credits. To estimate your credit's usage in a monthly period on each environment and assess the credits to allocate, use the AI Builder rate card in [Microsoft Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130) (pdf).

Allocation happens in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/) when you select **Resources** > **Capacity** > **Summary** tab, and then select **Assign to an environment** in the upper-left menu.

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

As an administrator, you can view your overall AI Builder credit consumption in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/) in the **Licensing** > **Capacity add-ons** > **Summary** tab.  

The **Allocation bar** and the **Consumption bar** display the number of **allocated** AI Builder credits and **consumed** AI Builder credits out of the total number of **purchased** AI Builder credits.

:::image type="content" source="media/credit-management/ppac-consumption.png" alt-text="Screenshot of the overall AI Builder credit consumption in Power Platform admin center.":::

AI Builder credit extensions aren't counted in *purchased* AI Builder credits.

Administrators also have access to a [consumption report](administer-consumption-report.md) that has the following features:

- Provides the AI Builder credits consumption on a chosen period per environment.
- Allows you to fine-tune the AI Builder credits allocation, which can be updated at any time.
- Allows administrators to check the consumption level of an environment for the current month by adding all consumptions of this environment.

Administrators also can access the [AI Builder Activity](activity-monitoring.md) page in the Power Automate portal, showing all predicts made against the AI Builder models in that environment.

### AI Builder credit consumption

The following list presents AI Builder actions that consume AI Builder credits. It isn't all-inclusive.

|AI models  |Power Apps  |Power Automate  |
|---------|---------|---------|
| Train an object detection model.<br/><br/>Use custom documents, images or text to *try out* prebuilt models when using the tiles in the **AI models** section.<br/><br/>Batch runs of the prediction and trainable category classification models for each row to be predicted.  | *Run an AI prompt or an AI function* generating text.<br/><br/>*Scan a business card* with the business card reader.<br/><br/>*Analyze* with the document processor.<br/><br/>*Detect* with the object detector.<br/><br/>**+ New image** with the text recognizer.<br/><br/>*Use an action* bound to an AI Builder model in [Power Fx](powerfx-in-powerapps.md).  |Run a flow using any of the actions inside the **AI Builder** category, such as **Extract information from document**, or **Create text with GPT using a prompt**.<br/><br/>Run the generic action **Perform a bound action** of Dataverse on the entity AI models and action name **Predict**.   |

Each AI Builder model has a different AI Builder credit consumption mechanism. To perform an assessment, use the AI Builder rate card in [Microsoft Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130) (pdf).

#### Free actions

Preview scenarios in AI Models don't consume credits. However, using a prompt in Power Automate or Power Apps consumes AI Builder credits, even if the underlying model is preview: such models are tagged as 'paid preview' in prompt builder.

- Testing prompts in prompt builder doesn't consume credits.
- A **Quick test** on a trained object detection and document processing model doesn't consume credits.

### AI prompt licensing

AI prompts can be utilized in Power Apps, Power Automate flows, agent flows, and in Microsoft Copilot Studio.

In the context of Power Apps and Power Automate flows, AI prompts consume AI Builder credits.

The number of consumed AI Builder credits depends on the input tokens, output tokens, and the underlying generative AI model used. Learn more in [Prompt tokens](licensing-prompt-tokens.md).

## Overage

When browsing AI Builder pages in Power Apps or Power Automate portal, you might get this notification: **You've consumed all of your AI Builder credits. Creating, editing, and viewing is blocked. Contact your administrator to get more capacity**. This notification means the monthly consumption of your environment is higher than the available (at environment or organization -tenant- level) AI Builder credits.

Monthly consumption is computed from first day of the month and is refreshed on a daily basis.
  
Available AI Builder credits are the assigned AI Builder credits if AI Builder credits are assigned to the environment, or the unassigned AI Builder credits if no AI Builder credit is assigned to the environment.  

### Simple overage

As soon as monthly consumption is higher than the available AI Builder credits, creating and editing models is blocked.

- On a prebuilt models tile, you can open the tile but can't test or select **Use in Apps or Flow**.
- On a new custom models tile, you can't select **Customize your model** to start a new model.
- On an existing model, you can't view, quick test, or edit properties. You can only delete model.

As long as overage isn't important, AI Builder models continue to run and consume AI Builder credits. We allow some level of overage consumption&mdash;similar to a grace period&mdash;to avoid blocking business processes.

### Important overage

When monthly consumption becomes higher than the available AI Builder credits by a large margin, running models in flows and apps is blocked. In this state, AI Builder actions fail with `EntitlementNotAvailable` `QuotaExceeded` error codes. In flow editor, remediation panel displays **All AI Builder credits in this environment have been consumed**.

To get details on your environment allocation, check the [Make credits available for an environment](credit-management.md#make-ai-builder-credits-available-for-an-environment-allocated-and-unallocated-credits) section in this article.

To get details on your environment consumption, check [Monitor usage](credit-management.md#monitor-usage) section in this article.

If your environment has no more capacity, you need to provide capacity to your environment:  reallocate existing capacity from the organization (tenant) or environment level. Alternatively, you can purchase more capacity and make it available to your environment.

To help estimate the required add-on capacity based on your estimated consumption, use the AI Builder rate card in [Microsoft Power Platform licensing guide](https://go.microsoft.com/fwlink/?linkid=2085130) (pdf).

### Request AI Builder credit extension

In the case of simple or important overage, and when another purchase and/or reallocation of AI Builder credit can't be done in a timely manner, makers in AI Builder and admins in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/home) can request a free AI Builder credit extension.

To perform the following actions, select **Request extension** in the overage banner in AI Builder or [Power Platform admin center](https://admin.powerplatform.microsoft.com/home):

- Send an email to Power Platform admins.
- Add 200,000 free extension AI Builder credits for the current month.

These free temporary AI Builder credits can't be allocated or assigned. Any environment in overage can use them after 10 minutes.

The number of purchased AI Builder credits in the Allocation bar or in the Consumption bar isn't modified with these free temporary AI Builder credits. Learn more in [Monitor usage](credit-management.md#monitor-usage). These added temporary AI Builder credits don't appear in [Power Platform admin center](https://admin.powerplatform.microsoft.com/home).

In some cases, you might still see the overage banners, although extension AI Builder credits already unblock your models.

Depending on the level of overage, these 200,000 AI Builder credits might not be enough. They can be requested multiple times, but the number of extension requests per month and per year is limited. Each request grants 200,000 AI Builder credits and triggers an email.

The purpose of these free AI Builder credit extensions is to allow makers and admin to unblock themselves temporarily in case another purchase and/or reallocation can't be done in a timely manner. Customer shouldn't rely on credit extensions to cover repetitive overage. Repetitive overage must be managed with another purchase and/or reallocation.

## Preview features

AI Builder features in preview release status are free to use. You don't need a license to use AI Builder preview features. However, the o1 reasoning model in prompts is currently in a paid preview.

## AI Builder licensing FAQ

### How many AI Builder credits are consumed for each operation?

Each AI Builder capability consumes AI Builder credits at a different rate. You can check the consumption rates in the [Microsoft Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=2085130) in the **AI Builder capacity add-on** section.

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

Example 1:

One (1) add-on + 5 Power Automate premium licenses gives 1,000,000+5*5,000 = 1,025,000 AI Builder credits that you can assign and consume in any scenario.

Example 2:

You have a scenario with 32,000 receipts to process each month with receipt processing.

32,000 receipts require 32 AI Builder credits per receipt (exact rates are in the [Microsoft Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130)), so you have 1,024,000 AI Builder credits.

Suppose you own five (5) Power Automate premium licenses, you're covered with a single add-on:

One (1) add-on + 5 Power Automate premium licenses = 1,025,000 AI Builder credits, which is greater than your estimated consumption of 1,024,000 AI Builder credits.

### Where can I see AI Builder credit usage for this month?

Overall organization (tenant) level AI Builder credit consumption is available in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/) in the **Resources** > **Capacity** > **Summary** tab. The Consumption bar displays the number of *consumed* AI Builder credits out of the total of *purchased* AI Builder credits.

The data is aggregated daily. Some data might be delayed; if so, the consumption bar shows all known consumption at the **Last updated** date in the tooltip box.

Get details on your environment consumption by checking the [AI Builder consumption report](administer-consumption-report.md). It gives the amount of consumption per day per user per environment.
Adding all the consumptions of the current month of a specific environment gives you the monthly consumption of this environment.

### How do I find out which model is using the most AI Builder credits?

Once you identify which environment consumes the most AI Builder credits with the [AI Builder consumption report](administer-consumption-report.md), you can leverage the model consumption data in the Dataverse **AI Event** table of that environment either in the Power Apps portal or the [AI Builder Activity](activity-monitoring.md) page in Power Automate.

### How do I know the number of purchased AI Builder credits of my organization (tenant)?

The [consumption bar and allocation bar](https://go.microsoft.com/fwlink/?linkid=2255314) display the number of *purchased* AI Builder credits.

AI Builder credits come from AI Builder add-ons and are also seeded in premium licenses like Power Automate Premium.

You can find the remaining AI Builder credits in [Power Platform admin center](https://admin.powerplatform.microsoft.com/) and select **Resources** > **Add-ons** > **Assign to an environment**. It represents the purchased capacity, which isn't allocated yet.

### When is AI Builder credit usage count reset? Is it based on license acquisition date?

AI Builder credit usage is counted on a monthly basis, starting the first day of each month. It isn't based on the license acquisition date. AI Builder credit usage of an environment shouldn't exceed the AI Builder credit allocation.

### What happens to the remaining capacity at the end of the month? Is it used the following month?

No, unused capacity doesn't carry over to the next month. AI Builder credit usage is counted on a monthly basis and reset on first day of the month. Available capacity is based on allocated capacity.

### What can I do with the 5,000 AI Builder credits included in the per user plan with attended RPA?

Each user license grants you 5,000 AI Builder credits, allowing you to assess the capabilities in AI Builder. For instance, you could use these AI Builder credits to extract data from a few documents with [document processing](form-processing-model-overview.md) or perform hundreds of basic OCR extractions with [text recognition](prebuilt-text-recognition.md).

### What happens if a user turns on/off AI Builder per user capacity add-on license?

Some user licenses include seeded AI Builder credits. For example, the Power Apps per user license includes 500 seeded AI Builder credits. If **AI Builder capacity per user add-on** isn't selected, the 500 AI Builder credits are still added to the total number of AI Builder credits owned at your organization (tenant) level and can be used.

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

No, AI Builder credits either come from environment allocation or comes from organization (tenant) level unallocated AI Builder credits but there's no automatic switch from environment credits to organization (tenant) AI Builder credits.

As soon as environment allocates AI Builder credits, AI Builder credits only come from environment AI Builder credits.
If environment consumption is higher than allocated AI Builder credits, then environment is in overage.

### How do you consider the 'large margin' to block model runs in important overage?

For an environment with allocated AI Builder credits, we apply the ‘large margin’ when comparing allocated AI Builder credits and consumed AI Builder credits. We don't consider organization (tenant) level AI Builder credits.
For an environment without allocated AI Builder credits, we apply the 'large margin' when comparing unallocated AI Builder credits and consumed AI Builder credits.

- **Simple overage**: Limitation starts as soon as consumed credits are higher than available AI Builder credits (no margin here) and only impacts maker experience. (creating/editing models)
- **Important overage**: Blocking AI Builder models in flows and apps only happens if overage is important. (large margin applies here)

### If an environment is in overage, do the limitations apply to all environments?

No. Limitations only apply to the environments in overage. Other environments, whether consuming environment assignment or organization (tenant) level credits aren't affected.

For example, if an environment has no allocated credit, and organization (tenant) level AI Builder credits aren't all consumed, then editing and running of AI Builder functions are allowed for this environment. This remains true when other environments with assigned AI Builder credits are in overage.

Consumption of unassigned AI Builder credits never affectS the consumption of an environment with assigned AI Builder credits, even if it's in overage. Consumption of credits in an environment with assigned AI Builder credits never affectS the consumption of AI Builder credits in other environments, even if it's in overage.
  
Global consumption graph is for information purpose, and indicates at least one environment is in overage, but doesn't mean that all environments are in overage. All environments with a consumption lower than their assignment, continue to work as expected.

### Are overages charged? Do overages affect next month consumption?

No, overage is considered as a grace period to help you adapt to new consumption pattern and is never charged. Overage doesn't affect the next month's consumption.

You should be concerned with an environment that consumes more than its capacity during a month, because it might be blocked at some point in the month. It works again at the beginning of next month as consumption is reset.

You shouldn't be concerned about an environment whose monthly consumption is below its capacity.

### I created prompts before the model selection was possible. Which model and temperature were used?

By default, prompts are created with GPT 3.5 and temperature = 0. Prompts created before the release of the model/temperature selection feature were set with these default values.

### What happens to my prompt using o1 reasoning model (preview), if the AI Builder preview toggle is switched to off in Power Platform admin center?

Your prompt fails in any context (testing prompt in prompt builder, Power Apps, Power Automate, or Copilot Studio). You can edit your prompt and switch the model to GPT-4o mini or GPT-4o.

### What licensing applies to AI Builder's AI functions?

These AI Builder AI functions&mdash;AISummarize, AIExtract, AIReply, AIClassify, and AISentiment&mdash;are prebuilt prompts available in AI prompts.
The licensing options applicable to these capabilities are in the AI Builder rate card, "AI prompts, Create text with GPT 3.5" in the [Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130).

### Are all tests free?

No. Testing prompts and testing trained models are free. Testing prebuilt models consumes credits at the same rate as running them in production.

### I built an app that includes a flow. I want to add an AI Builder action in this flow. Does it turn my app into a premium app?

Yes. By adding an AI Builder action to a flow inside your app, you turn your app into a premium app. so it requires a premium license to be used.  
However, your flow is not considered as a premium flow.  

### Do you have FAQ about AI Builder trials?

Yes. Learn more in [AI Builder trial FAQ](ai-builder-trials.md#ai-builder-trial-faq).

## Related information

- [AI Builder trial](ai-builder-trials.md)
- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Licensing FAQ for AI Builder](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
