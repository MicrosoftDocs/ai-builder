---
title: Use your Azure OpenAI Service model in Power Apps (preview)
description: Learn how to use GPT and the Azure OpenAI Service model with AI Builder in Power Apps.
author: ashbhati
contributors:
  - ashbhati
  - v-aangie
ms.topic: how-to
ms.custom: bap-template
ms.date: 03/06/2023
ms.author: ashbhati
ms.reviewer: angieandrews
---

# Use your Azure OpenAI Service model in Power Apps (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

GPT (Generative Pre-trained Transformer) models are a type of natural language processing model. GPT models are trained on a large body of content to generate human-like text from a prompt. Use them in your apps to interactively fill in forms or questionnaires, generate reports and summaries from a dataset, create automated chatbot conversations, and more. GPT models are especially helpful in generating responses for customer service teams that need to quickly reply to customer inquiries.

> [!IMPORTANT]
>
> - This is a preview feature.
>
> - [!INCLUDE [cc_preview_features_definition](includes/cc-preview-features-definition.md)]
>
> - [View our preview terms](https://go.microsoft.com/fwlink/?linkid=2189520).
>
> - This capability may not be available in your region yet.
>
> - This capability may be subject to usage limits or capacity throttling.

## Add an AI model as a data source

The following example creates a simple app that answers a question entered in a text box.

1. Sign in to [Power Apps](https://make.powerapps.com).

1. On the left navigation pane, select **Apps**.
1. On the menu at the top, select **+ New app** > **Canvas**. 

1. Enter a name for the app and choose between **Tablet** and **Phone** for the format of the app.

1. Select **Create**.

1. On the list of icons to the left of the **Tree view**, select **Data** > **Add data** > **AI models**.

    :::image type="content" alt-text="Screenshot of selecting a data source." source="media/azure-openai-model-papp/data-source.png":::

1. Select one or more models to add.

    If you don’t see your model in the list, you might not have permission to use it in Power Apps. Contact your administrator to resolve this problem. 

## Bind the model prediction to a control

Next, bind the model prediction with a control or an event to trigger the model response. The screenshot in this section shows a simple application to answer any question specified in the instruction text box.

To bind the **Create text with GPT** model to a control, identify an event of the control that you want to invoke the model prediction. In this case, we're binding the model to the **Generate Text** button and the **OnSelect** event on the button. The result is that whenever the button is selected, the **OnSelect** event is triggered, which triggers the Power Fx function mentioned here.

1. On the list of icons to the left, select **Tree view**.

1. Above the **Tree view** heading, select **OnSelect** in the dropdown menu.

1. On the **Screens** tab, select **GenerateText**.

1. Notice the Power Fx function:

```powerapps-dot
Set(TextCompletionResult, 'Create text with GPT'.Predict(TextInput1.Text));
````

The `.Predict()` on this model accepts a string as a parameter and returns the generated text as a response text. In the following example, we're passing the instruction from the text box as a prompt to the **Create text with GPT** model, and the response from the model appears in the **Response** label.  

:::image type="content" alt-text="Screenshot of binding the model prediction to a control." source="media/azure-openai-model-papp/generate-text.png":::

Congratulations! You've created an app that uses an AI Builder Create text with GPT capability. On the top of the screen, select **Save** to save all the changes in the app, and then select **Play** to test the application.  

## Parameters

For a list of the parameters used in Azure OpenAI Service, go to [input parameters](azure-openai-model-pauto.md#input-parameters) and [output parameters](azure-openai-model-pauto.md#output-parameters) in Power Automate.

### See also

[Azure OpenAI Service model overview (preview)](prebuilt-azure-openai.md)
[How text generation in Azure OpenAI Service works (preview)](azure-openai-textgen.md)
[Use your Azure OpenAI Service model in Power Automate (preview)](azure-openai-model-pauto.md)
