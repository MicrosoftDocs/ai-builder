---
title: Use AI Builder in Teams
description: Learn how to use AI Builder templates in Teams.
author: phil-cmd
contributors:
  - phil-cmd
  - Antonio-Rodrigues
  - v-aangie
ms.topic: conceptual
ms.custom: 
ms.date: 02/13/2023
ms.author: plarrue
ms.reviewer: angieandrews
---

# Use AI Builder in Teams

You can use Power Automate templates in Teams that solve a specific business purpose using AI Builder actions.

## Discover AI Builder templates in Teams

1. Go to your Teams app or [Teams web](https://teams.microsoft.com).

1. On the bottom left, select the **Apps** icon.

1. Search for **Power Automate** and install it. The app appears in the left panel in Teams.

   You can pin the app to keep it there when you reopen Teams.

1. Select the Power Automate app, and then select the **Create** tab.

   From there, you can search for the AI Builder templates listed in the next section in this article.

    :::image type="content" source="media/templates-list.png" alt-text="Screenshot of the templates list.":::

## Create a flow from a template

1. From the list of AI Builder templates, choose the one that fits your needs the most.

    - If you don't have a [Microsoft Power Platform environment with database](/power-platform/admin/create-environment#create-an-environment-with-a-database), you'll see the following dialog. Select **Continue** to add a database. It usually takes a couple of minutes (in some cases it can take more than one hour) and has to be done only once.

     :::image type="content" source="media/no-dataverse.png" alt-text="Screenshot of No Dataverse database found.":::

    - If you already have a Power Platform environment with database, you'll land on the simplified template experience for Teams. The first screen asks you to validate connections.

1. Once your connections are valid, select **Continue**.

    > [!NOTE]
    > An AI Builder trial will be started or extended if needed. This action will be performed silently upon selecting **Continue**.

    :::image type="content" source="media/start-trial.png" alt-text="Screenshot of the 30-day free trial message.":::

1. Enter the parameters required by the template to create the flow.

    > [!NOTE]
    > It's also possible to select **Edit in advanced mode**. This will open the full flow editor within Teams.

1. Once you entered all the parameters, select **Create flow**. After few seconds, your flow will be created and ready to use.

    :::image type="content" source="media/create-flow.png" alt-text="Screenshot of the Create a flow screen.":::

Created flows are visible and can be modified from the Power Automate home page. 

### See also

- [Use flows in Microsoft Teams](/power-automate/teams/overview)
- [Video: How to set up instant Microsoft Teams notifications for negative emails in 1 minute](https://www.youtube.com/watch?v=qfmQAObXTHQ)
