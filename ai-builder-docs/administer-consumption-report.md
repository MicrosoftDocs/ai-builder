---
title: AI Builder consumption report - AI Builder
description: Learn about the consumption report, which shows how your AI credits are being used in the Microsoft Power Platform admin center.
author: CedrickBellarosa
contributors:
  - CedrickBellarosa
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.custom: 
ms.date: 06/02/2022
ms.author: cdbellar
ms.reviewer: angieandrews
---

# AI Builder consumption report

AI Builder is licensed as a capacity add-on that must be allocated to a Microsoft Power Platform environment by an administrator. Each AI builder capability consumes credits at a different rate.

- The [AI Builder calculator](https://flow.microsoft.com/ai-builder-calculator/) allows you to perform an assessment of what you need for your business.
- The [AI Builder licensing page](administer-licensing.md) gives you more details on how AI Builder capacity works.

In addition, administrators can download an Excel report that shows the actual capacity consumption in your tenant. The consumption report shows the capacity used in the 30 days preceding the selected target date for each environment. This makes it easier to compare your allocated capacity with the actual capacity consumption of your organization so you can fine tune your capacity allocation.
This report shows the consumption data for the past (rolling) 30 days. Once generated, the report remains available for download for 30 days in the Power Platform Admin Center.

## View the consumption report

To download and view an Excel file showing your AI credit consumption report:

1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).

1. On the left pane, select **Resources** > **Capacity**.

1. On the **Summary** tab, select **Download reports** in the **Add-ons** section.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Power Platform admin center capacity screen.](media/ppac-capacity-screen.png "AI Builder credits is located in the 'Add-ons' section")

1. On the menu at the top, select **+New**.

1. In the **Choose a report** dropdown list, select **AI Builder**.

1. Select **Submit**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of Request a report.](media/administer-consumption-report/download-consumption.png "Request a report")

    The **Downloadable Reports** list shows that a new report is being generated.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of a report being generated.](media/administer-consumption-report/in-progress.png "A report being generated")

1. After the new report is generated, select the report in the list.

1. At the top of the screen, select **Download** to download the report as an Excel file.

## Understand the consumption report

The report shows AI credits consumed by date for each environment.

<img width="953" alt="image" src="https://github.com/MicrosoftDocs/ai-builder-pr/assets/131351086/554783b1-602f-481f-bac8-310b1d2c74c8">


- **Date** is the date of the AI credits consumption.
- **UserId** is the identifier visible in the Dataverse "User" table.
- **EnvironmentId** is the identifier visible in your Power Apps or Power Automate URL (for example, https://make.powerapps.com/environments/%GUID%).
- **EnvironmentName** is the name of the environment.
- **AIConsumption** contains the number of credits consumed by the user and in the environment for a given date.

You can compare the aggregated consumption for the current calendar month on each environment with what has been allocated. Using this information, you can take action to allocate more credits to environments that are in overage. Remember, the number of allocated credits by environment is visible and can be changed in the Power Platform admin center [Add-ons](https://admin.powerplatform.microsoft.com/resources/capacity#add-ons) page.

### See also

- [Microsoft Power Apps and Power Automate Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=2085130)<br/>
- [AI Builder licensing FAQ](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)

[!INCLUDE[footer-include](includes/footer-banner.md)]
