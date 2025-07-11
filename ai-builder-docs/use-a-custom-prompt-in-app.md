---
title: Use your prompt in Power Apps
description: Learn how to use your prompt in Power Apps.
author: ashbhati
contributors:
  - ashbhati
  - phil-cmd
  - v-aangie
ms.topic: how-to
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 06/23/2025
ms.update-cycle: 180-days
ms.author: ashbhati
ms.reviewer: angieandrews
---

# Use your prompt in Power Apps

A custom prompt in Power Apps empowers makers to incorporate custom generative AI capabilities into their apps, thus addressing their business needs with state of the art intelligence.

Once you create and test your prompts using the prompt builder, you can use them within your application by calling them through Power Fx Functions.
Custom prompts can be invoked as Power Fx function calls, this allows you to seamlessly integrate AI capabilities into your application.

> [!IMPORTANT]
> - AI Builder prompts are running on GPT 4o Mini and GPT 4o model versions powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
> - This capability is [limited to some regions](availability-region.md#prompts).
> - This capability might be subject to usage limits or capacity throttling.

## Prerequisite

You created a custom prompt.

## Create an app and configure it

To use a prompt as a Power Fx function, you simply need to call it by its name and pass any required arguments. The function then returns the response generated by the prompt, which can be used within your application as needed. This straightforward approach allows you to leverage the power of AI without needing to write complex code.

Using a prompt in an application is similar to using a custom AI model. Once the prompt is added from the **Add data** menu, it can be used as a Power Fx function by calling the `.Predict` on its name, and pass any required arguments. The function then returns the response generated by the GPT model, which can be used in your application. This straightforward approach enables leveraging the power of generative AI without needing to write complex code.

1. Sign in to [Power Apps](https://make.powerapps.com/).
1. Select **+Create** > **Blank app** > **Create**.
1. In the **App name** field, enter **Task ID**.
1. Under the **Format** heading, select **Phone**.
1. Select **Create**.
1. On the left pane, select **Data** > **+Add Data** > *your custom prompt*.

    The following example shows a custom prompt named **Task identifier**.

    :::image type="content" source="media/use-a-custom-prompt-in-app/add-data-source.png" alt-text="Screenshot of adding an app that uses a custom prompt.":::

1. On the menu at the top of the page, do the following:
    1. Select **+Insert** > **Text input**.
    1. Select **+Insert** > **Button**.
    1. Select **+Insert** > **Text label**.
1. Resize **Text input** and **Text label** accordingly.
1. On the left pane, select **Button1** > **OnSelect** (the property).
1. In the formula bar, enter `Set(result, 'Task identifier'.Predict(TextInput1.Text));`

    :::image type="content" source="media/use-a-custom-prompt-in-app/insert-menu.png" alt-text="Screenshot of adding data and a data source to your prompt.":::

1. On the left pane, Select **label1** > **Text** (the property).
1. In the formula bar, enter `result.text`
1. Select **Save**.

## Test your app

1. On the menu at the top of the page, select the play button.
1. Enter your text in the **Text input** screen.
1. Check the AI text generated in the text label.

## Related information

[Human review for automation with a prompt](azure-openai-human-review.md)
