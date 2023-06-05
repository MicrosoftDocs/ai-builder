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

## Select an AI model

1. Sign in to [Power Apps](https://make.powerapps.com).

## Add an AI model as a data source

The following example creates a simple app that answers a question entered in a text box.

1. Sign in to [Power Apps](https://make.powerapps.com) and [create a canvas app](/power-apps/maker/canvas-apps/create-blank-app).

1. Add a text input box and a text output box and between them, a button labeled **Generate Text**.<!-- EDITOR'S NOTE: I'm guessing at the controls based on what I see in the screenshot. Please add the instructions to create the app shown. -->

1. Select **Data** > **Add data** > **AI models** > **Create text with GPT**.

    :::image type="content" alt-text="Screenshot of selecting an AI model as the data source in a canvas app." source="media/azure-openai-model-papp/data-source.png":::

    If you don't see your AI model in the list, you might not have permission to use it in Power Apps. Ask your administrator for help.

## Bind the model to a control

After you add an AI model to the app, bind the model to an event of a control to trigger the model response. In this example, we bind the model to the **OnSelect** event of the **Generate Text** button, but you can select any control and event that makes sense for your purposes.
<!-- EDITOR'S NOTE: Please make sure the instructions below are complete enough that a reader can create the app shown. -->

1. Select **Tree view**.

1. Above the **Tree view** heading, select **OnSelect** in the list.

1. On the **Screens** tab, select **GenerateText**.

    Notice the Power Fx function:

    ```powerapps-dot
    Set(TextCompletionResult, 'Create text with GPT'.Predict(TextInput1.Text));
    ````

    The `.Predict()` command accepts a string as a parameter and returns the generated text as the response. The full command passes the instruction from the text box as a prompt to the **Create text with GPT** model. The response from the model appears in the **Response** label.

    :::image type="content" alt-text="Screenshot of binding the AI model to a control in a canvas app." source="media/azure-openai-model-papp/generate-text.png":::

1. Select **Save**, and then select **Play** to try out your app.

For a list of the parameters used in Azure OpenAI Service, go to [parameters](azure-openai-model-pauto.md#parameters) in Power Automate.

### See also

[Azure OpenAI Service model overview (preview)](prebuilt-azure-openai.md)  
[How text generation in Azure OpenAI Service works (preview)](azure-openai-textgen.md)  
[Use your Azure OpenAI Service model in Power Automate (preview)](azure-openai-model-pauto.md)
