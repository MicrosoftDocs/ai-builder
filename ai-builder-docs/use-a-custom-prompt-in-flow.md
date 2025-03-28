---
title: Use your prompt in Power Automate
description: Learn how to use your prompt in a Power Automate flow.
author: ashbhati
contributors:
  - ashbhati
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 03/28/2025
ms.author: ashbhati
ms.reviewer: angieandrews
ms.custom:
  - DevRelAdv
---

# Use your prompt in Power Automate

You can add a prompt as an action in a Power Automate flow so it's possible to generate text from it inside an automated process.

> [!IMPORTANT]
> - AI Builder prompts are running on GPT 4o Mini and GPT 4o model versions powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
> - This capability is [limited to some regions](availability-region.md#prompts).
> - This capability might be subject to usage limits or capacity throttling.

## Use an existing prompt in a flow

**Prerequisite**: You created a prompt named **Task Identifier** that has one input called **Text**, as described in [Create a custom prompt](create-a-custom-prompt.md).

1. Sign in to [Power Automate](https://make.powerautomate.com/).
1. Select **+Create** > **Instant cloud flow**.
1. Name the flow **Task ID**.
1. Select **Manually trigger a flow** > **Create**.
1. In the designer, select **manually trigger a flow**.
1. On the **Parameters** tab to the left, select **+Add an input**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/input-parameter.png" alt-text="Screenshot of adding 'Text' as an input.":::

1. Select **Text**, and then enter a name.  

    :::image type="content" source="media/use-a-custom-prompt-in-flow/input-text.png" alt-text="Screenshot of adding an input.":::

1. In the designer, select **+Insert a new step** after **Manually trigger a flow**.
1. On the left pane in the **Search** field, enter **GPT** and select the action **Create text with GPT using a prompt**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/gpt-parameters.png" alt-text="Screenshot of a prompt test.":::

1. On the left pane in the **Name** field, choose your custom prompt from the dropdown menu.

    The following example uses **Task Identifier** as the custom prompt. Task Identifier is a custom prompt that was previously built.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/custom-prompt.png" alt-text="Screenshot of the 'Task identifier' custom prompt.":::

1. On the left pane in the **Input Text** field, select **Input** Text from the Dynamic content list to the right.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/input-text-dynamic.png" alt-text="Screenshot of selecting the 'Input' text from the Dynamic content list for the 'Input Text' field.":::

Learn more about how to include your prompt in a flow in this quick video:</br>
</br>

> [!VIDEO 0b76ebb0-c95c-483b-b29b-7d5c0921f3a9]

## Create a new prompt in a flow

1. Sign in to [Power Automate](https://make.powerautomate.com/).
1. Select **+Create** > **Instant cloud flow**.
1. In the designer, select **+Insert a new step** after **Manually trigger a flow**.
1. On the left pane in the **Search** field, enter **GPT** and select the action **Create text with GPT using a prompt**.
1. On the left pane in the **Name** field, select **New custom prompt** from the dropdown menu.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/new-prompt.png" alt-text="Create a new prompt":::

1. To create your prompt instructions, follow the instruction from [Create a custom prompt](create-a-custom-prompt.md).
1. Save your prompt and follow the [instructions to use your prompt in a flow](use-a-custom-prompt-in-flow.md#use-an-existing-prompt-in-a-flow).

## Use the output of the GPT action

The **Create text with GPT using a prompt** action generates a flow variable called **Text**, which represents the output of your prompt generated by the GPT model. You can use this variable at your convenience in downstream actions.

For example, let's send a Teams message that encompasses the **Text** variable:

1. In the designer, select **+Insert a new step** after the **Create text with GPT using a prompt** action.
1. Search for the action **Post message in a chat or channel** and select it.
1. Fill in the parameters, making sure you select the **Text** variable in the body of the Teams message.

   :::image type="content" source="media/use-a-custom-prompt-in-flow/use-gpt-response.png" alt-text="Use the prompt output":::

1. Once you're satisfied with your flow, you can save it and select **Test** on the top right corner.
1. Make sure to enter values for the input variables that would be used in your flow, and then select **Run flow**.
1. Visualize the message received in Teams.

   :::image type="content" source="media/use-a-custom-prompt-in-flow/outputs-teams.png" alt-text="Screenshot of outputs.":::

## Incorporate human review

Having humans review the output generated by the GPT model allow an organization to ensure that this output is of high quality, aligns with ethical standards, and meets specific requirements. This combination of AI and human oversight optimizes processes and enhances overall outcomes. Learn [why human review is important](azure-openai-human-review.md).

This section explains how to add a human review step after the prompt action in a flow.

1. In the designer after the **Create text with GPT using a prompt** card, select **+Insert a new step**.
1. On the left pane in the **Search** field, enter **Approvals**.
1. To the right of the **Approvals** heading, select **See more**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/see-more.png" alt-text="Screenshot of the 'See more' button to get a list of all approval actions.":::

1. Select **Start and wait for an approval of text**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/start-and-wait.png" alt-text="Screenshot of the 'Start and wait for an approval of text' action.":::

1. Fill in the following **Approval** parameters:
    1. In the **Title** field, enter a title.
    1. In the **Suggested Text** field, select **Text** from the dynamic content list.
    1. In the **Assigned To** field, enter an email address.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/title-suggested-assigned-to.png" alt-text="Screenshot of adding an action, suggested text, and an email address.":::

1. In the designer after the **Start and wait for an approval of text** card, select **Add an action**.

1. On the left pane, search the control **Condition** and fill-in the following parameters:
    1. In **Condition Expression**, select **Outcome** from the dynamic content list.
    1. Next to **Outcome**, select **is equal to** from the dropdown list.
    1. Next to **is equal to**, enter **Approve**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/condition-expression.png" alt-text="Screenshot of selecting the condition expression parameters.":::

1. In the designer under **Condition** in the **True** branch, select **+Insert a new step**.
1. On the left pane, search **Teams** and select **Post message in a chat or channel**.
1. On the **Parameters** tab, do the following:
    1. In the **Post as** field, select **Flow bot**.
    1. In the **Post in** field, select **Chat with flow bot**.
    1. In the **Recipient** field, enter an email address.
    1. In the **Message** field, select **Accepted** text from the dynamic content list.
1. Select **Save**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/post-message.png" alt-text="Screenshot of adding parameters for 'Post message in a chat or channel'.":::

Once the flow runs and an approval is generated, the assigned reviewers can check the text generated by the GPT model from the **Approvals** menu in the Power Automate portal:

1. From the left pane, select **Approvals**, and then select the **Received** tab.  
1. Open the approval to review and edit the text if needed.
1. From the dropdown menu, choose your response.
1. Select **Confirm**.

    :::image type="content" source="media/use-a-custom-prompt-in-flow/approvals.png" alt-text="Screenshot of configuring human oversight approvals.":::

## Related information

[Human review for automation with a prompt](azure-openai-human-review.md)
