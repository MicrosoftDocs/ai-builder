---
title: Use your custom prompt in a Power Automate flow (preview)
description: Learn how to use your custom prompt in a Power Automate flow.
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.collection: get-started
ms.date: 11/14/2023
ms.author: plarrue
ms.reviewer: angieandrews
---

# Use your custom prompt in a Power Automate flow (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

A custom prompt in a Power Automate flow grants the ability to incorporate an existing prompt as a flow action.

> [!IMPORTANT]
> - This is a preview feature.
> - Preview features aren’t meant for production use and may have restricted functionality. These features are available before an official release so that customers can get early access and provide feedback.
> - As we traverse this rapidly evolving field, we are dedicated to refining and improving our services based on user feedback and insights. We encourage developers to be cognizant of the risks and incorporate human review when utilizing this capability.

## Prerequisite

You've created a custom prompt.

## Create a flow and configure it

1. Sign in to [Power Automate](https://make.powerautomate.com/).
1. Select **+Create** > **Instant cloud flow**.
1. Name the flow **Task ID**.
1. Select **Manually trigger a flow** > **Create**.
1. In the designer, select **manually trigger a flow**.
1. On the **Parameters** tab to the left, select **+Add an input**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/input-parameter.png" alt-text="Screenshot of adding 'Text' as an input.":::

1. Select **Text**, and then enter a name.  

    :::image type="content" source="media/use-a-custom-prompt-in-flow/input-text.png" alt-text="Screenshot of adding an input.":::

1. In the designer, select **+Insert a new step** after **Manually trigger a flow** > **Add an action**.
1. On the left pane in the **Search** field, select **GPT** > **Create text with GPT (V2)**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/gpt-parameters.png" alt-text="Screenshot of a prompt test.":::

1. On the left pane in the **Name** field, choose your custom prompt from the dropdown menu.

    The following example uses **Task Identifier** as the custom prompt. Task Identifier is a custom prompt that has been previously built.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/custom-prompt.png" alt-text="Screenshot of the 'Task identifier' custom prompt.":::

1. On the left pane in the **Input Text** field, select **Input** Text from the Dynamic content list to the right.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/input-text-dynamic.png" alt-text="Screenshot of selecting the 'Input' text from the Dynamic content list for the 'Input Text' field.":::

1. In the designer after the **Create text with GPT (V2)** card, select **+Insert a new step** > **Add an action**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/new-step-action.png" alt-text="Screenshot of selecting 'Add an action to the 'Input Text' field.":::

1. On the left pane in the **Search** field, enter **Approvals**.
1. To the right of the **Approvals** heading, select **See more**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/see-more.png" alt-text="Screenshot of the 'See more' button to get a list of all approval actions.":::

1. Select **Start and wait for an approval of text**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/start-and-wait.png" alt-text="Screenshot of the 'Start and wait for an approval of text' action.":::

1. In the **Parameters** tab:
    1. In the **Title** field, enter a title.
    1. In the **Suggested Text** field, select **Text** from the dynamic content list.
    1. In the **Assigned To** field, enter an email address.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/title-suggested-assigned-to.png" alt-text="Screenshot of adding an action, suggested text, and an email address.":::

1. In the designer after the **Start and wait for an approval of text** card, select **Add an action**.
1. On the left pane, search the control **Condition**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/control-condition.png" alt-text="Screenshot of adding a condition control.":::

1. Select the **Parameters** tab.
    1. In **Condition Expression**, select **Outcome** from the dynamic content list.
    1. Next to **Outcome**, select **is equal to** from the dropdown list.
    1. Next to **is equal to**, enter **Approve**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/condition-expression.png" alt-text="Screenshot of selecting the condition expression parameters.":::

1. In the designer under **Condition** in the **True** branch, select **+Insert a new step** > **Add an action**.
1. On the left pane, search **Teams** and select **Post message in a chat or channel**.
1. On the **Parameters** tab, do the following:
    1. In the **Post as** field, select **Flow bot**.
    1. In the **Post in** field, select **Chat with flow bot**.
    1. In the **Recipient** field, enter an email address.
    1. In the **Message** field, select **Accepted** text from the dynamic content list.
1. Select **Save**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/post-message.png" alt-text="Screenshot of adding parameters for 'Post message in a chat or channel'.":::

## Test your flow

1. On the right top corner, select **Test**.
1. Select **Manually** > **Test**.
1. In **Input**, enter your text, and then select **Run flow**.

## Ensure quality output with human oversight

By having a human in the loop, organizations can harness the efficiency and capabilities of AI while ensuring the output is of high quality, aligns with ethical standards, and meets specific requirements. This combination of AI and human oversight optimizes processes and enhances overall outcomes.

1. From the left pane, select **Approvals**, and then select the **Received** tab.  
1. Open the request **Task Identifier** to review the text generated by AI.
1. Choose your response, and then select **Approve** from the dropdown list.
1. Select **Confirm**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/approvals.png" alt-text="Screenshot of configuring human oversight approvals.":::

## Explore outputs

There are numerous potential outcomes to consider, including those related to email, data operation with Compose, Dataverse, Teams, and more. In this scenario, we explore the result using the Teams connector.

:::image type="content" source="media/use-a-custom-prompt-in-flow/outputs-teams.png" alt-text="Screenshot of outputs.":::

### See also

[Human review for automation with the text generation model (preview)](azure-openai-human-review.md)
