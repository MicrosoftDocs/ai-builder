---
title: AI Builder consumption report - AI Builder
description: Learn about the consumption report, which shows how your AI credits are being used in the Microsoft Power Platform admin center.
author: CedrickBellarosa
contributors:
  - jkom1
  - CedrickBellarosa
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.custom: bap-template
ms.date: 06/02/2022
ms.author: jelenak
ms.reviewer: angieandrews
---

# AI Builder consumption report

AI Builder is licensed as a capacity add-on that must be allocated to a Microsoft Power Platform environment by an administrator. Each AI builder capability consumes credits at a different rate.

- The [AI Builder calculator](https://flow.microsoft.com/ai-builder-calculator/) allows you to perform an assessment of what you need for your business.
- The [AI Builder licensing page](administer-licensing.md) gives you more details on how AI Builder capacity works.

In addition, administrators can download an Excel report that shows the actual capacity consumption in your tenant. The consumption report shows the capacity used in the 30 days preceding the selected target date for each environment. This makes it easier to compare your allocated capacity with the actual capacity consumption of your organization so you can fine tune your capacity allocation.

This report shows the consumption data for the past rolling 30 days. Once generated, the report remains available for download for 30 days in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).

## View the consumption report

To download and view an Excel file showing your AI credit consumption report:

1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).

1. On the left pane, select **Resources** > **Capacity**.

1. On the **Summary** tab, select **Download reports** in the **Add-ons** section.

    :::image type="content" source="media/ppac-capacity-screen.png" alt-text="Screenshot of the Power Platform admin center capacity page.":::

1. On the menu at the top, select **+New**.

1. In the **Choose a report** dropdown list, select **AI Builder**.

1. Select **Submit**.

    :::image type="content" source="media/administer-consumption-report/download-consumption.png" alt-text="Screenshot of Request a report.":::

    The **Downloadable Reports** list shows that a new report is being generated.

    :::image type="content" source="media/administer-consumption-report/in-progress.png" alt-text="Screenshot of a report being generated.":::

1. After the new report is generated, select the report in the list.

1. At the top of the screen, select **Download** to download the report as an Excel file.

## Understand the consumption report

The report shows AI credits consumed by date for each environment.

:::image type="content" source="media/administer-consumption-report/credits-by-date.png" alt-text="Screenshot of AI credits consumed by date for each environment.":::

- **Date**: The date of the AI credits consumption.
- **UserId**: The identifier visible in the Dataverse **User** table.
- **EnvironmentId**: The identifier visible in your Power Apps or Power Automate URL (for example, https://make.powerapps.com/environments/%GUID%).
- **EnvironmentName**: The name of the environment.
- **AIConsumption**: Contains the number of credits consumed by the user and in the environment for a given date.
- **IsTrial**: If the value is **TRUE**, credits that have been consumed are AI Builder trial credits. **More information**: [Ai Builder trial](ai-builder-trials.md)

You can compare the aggregated consumption for the current calendar month on each environment with what has been allocated. Using this information, you can take action to allocate more credits to environments that are in overage. Remember, the number of allocated credits by environment is visible and can be changed in the Power Platform admin center [Add-ons](https://admin.powerplatform.microsoft.com/resources/capacity#add-ons) page.

### See also

- [Microsoft Power Apps and Power Automate Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=2085130)<br/>
- [AI Builder licensing FAQ](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Monitor model activity](https://learn.microsoft.com/en-us/ai-builder/activity-monitoring)

[!INCLUDE[footer-include](includes/footer-banner.md)]

