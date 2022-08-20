---
title: Use AI Builder models in Power Apps - AI Builder | Microsoft Docs
description: Add more powerful and flexible integrations of AI models into your Power App.
author: v-aangie
ms.topic: conceptual
ms.custom: intro-internal
ms.date: 08/22/2022
ms.author: angieandrews
ms.reviewer: angieandrews
---

# Use AI Builder models in Power Apps

With the use of [Power Fx](/power-platform/power-fx/overview), the open-source low-code formulas, you can add more powerful and flexible integrations of AI models into your Power App. AI model prediction formulas can be integrated with any controls in canvas app. For example, you can detect the language of text in a text input control and output the results to a label control as can be seen in Use a model with controls section below.  

## Requirements

To use Power Fx in AI Builder models, you must have:

- Access to a [Microsoft Power Platform environment with a database](/power-platform/admin/create-environment#create-an-environment-with-a-database).

- AI Builder license (trial or paid). To learn more, go to [AI Builder licensing](administer-licensing.md).

## Select a model in canvas apps

To consume an AI model with Power Fx, you’ll need to create a canvas app, choose a control, and assign expressions to control properties.

> [!NOTE]
> For a list of AI Builder models you can consume, see [AI models and business scenarios](model-types.md). You can also consume models built in Microsoft Azure Machine Learning with the [bring your own model](byo-model.md) feature.

1. Create an app. More information: [Create a blank canvas app from scratch](/power-apps/maker/canvas-apps/create-blank-app).

1. Select **Data** > **Add data** > **AI models**.

    :::image type="content" source="media/powerfx-in-powerapps/data-sources.png" alt-text="Screenshot of how to select your model.":::

1. Select one or more models to add.

    If you don’t see your model in the list, you might not have permissions to use it in Power Apps. Contact your administrator to resolve this problem.

## Use a model with controls

Now that you've added the AI model to your canvas app, let’s see how to call an AI Builder model from a control.

In the following example, we’ll build an app that can detect the language entered by a user in the app.

1. Create an app. More information: [Create a blank canvas app from scratch](/power-apps/maker/canvas-apps/create-blank-app).

1. Select **Data** > **Add data** > **AI models**.

1. Search for, and select **Language detection** AI model.

    :::image type="content" source="media/powerfx-in-powerapps/language-detection.png" alt-text="Screenshot of language detection model.":::

    > [!NOTE]
    > You'll have to manually add the model to the app again in the new environment upon moving the app across environments.

1. Select **+** from the left-pane, and then select **Text input** control.

1. Repeat the previous step to add a **Text label** control.

1. Rename the text label to **Language**.

1. Add another text label next to the "Language" label.

    :::image type="content" source="media/powerfx-in-powerapps/app-controls.png" alt-text="App controls including text and both label controls.":::

1. Select the text label added in the previous step.

1. Enter the following formula in the formula bar for the text label's **Text** property.

    ```powerapps-dot
    'Language detection'.Predict(TextInput1.Text).Language
    ```

    Notice the label change to the language code based on your locale. For this example, **en** (English).

    :::image type="content" source="media/powerfx-in-powerapps/language-formula.png" alt-text="Language formula changes the label text.":::

1. Preview the app by selecting the **Play** button from the top-right corner of the screen.

    :::image type="content" source="media/powerfx-in-powerapps/play.png" alt-text="Preview the app.":::

1. In the textbox, enter `bonjour`. Notice that the language for French language (fr) appears below the textbox.

    :::image type="content" source="media/powerfx-in-powerapps/bonjour.png" alt-text="Example of French language detection.":::

1. Similarly, try other language text. For example, entering `guten tag` changes the detected language to **de** for German language.

## Best practices

- Try triggering model prediction from singular actions such as **OnClick** using a button rather than the **OnChange** action on a text input to ensure efficient use of AI Builder credits.

- To save time and resources, save the result of a model call so you can use it in multiple places. You can save an output into a global variable. After you save the model result, you can use the language elsewhere in your app to show the identified language and its confidence score in two different labels.

    ```powerapps-dot
    Set(lang, 'Language detection'.Predict("bonjour").Language)
    ```

## Input and output by model type

This section provides inputs and outputs for custom and prebuilt models by model type.

### Custom models

| Model type | Syntax | Output |
| - | - | - |
| Category classification | `'Custom text classification model name'.Predict(Text: String, Language?: Optional String)` | `{AllClasses: {Name: String, Confidence: Number}[],TopClass: {Name: String,Confidence: Number}}` |
| Entity extraction | `'Custom entity extraction model name’.Predict(Text: String,Language?:String(Optional))` | `{Entities:[{Type: "name",Value: "Bill", StartIndex: 22, Length: 4, Confidence: .996, }, { Type: "name", Value: "Gwen", StartIndex: 6, Length: 4, Confidence: .821, }]}` |
| Image classification | `‘Custom image classification model name’.Predict(Image: Image)` | `{ AllClasses: { Name: String, Confidence: Number }[],  TopClass: { Name: String, Confidence: Number }}` |
| Object detection | `'Custom object detection model name'.Predict(Image: Image)` | `{ Objects: { Name: String, Confidence: Number, BoundingBox: { Left: Number, Top: Number, Width: Number, Height: Number }}[]} ` |

### Prebuilt models

> [!NOTE]
> Prebuilt model names are shown in your environment’s locale. The following examples show the model names for English language (en).

| Model type | Syntax | Output |
| - | - | - |
| Business card reader | `‘Business card reader’.Predict( Document: Base64 encoded image )` | `{  Fields: { FieldName: { FieldType: "text", Value: { Text: String, BoundingBox: { Top: Number, Left: Number, Height: Number, Width: Number }}}}}` |
| Category classification | `'Category classification'.Predict( Text: String,Language?: Optional String, )` |  `{ AllClasses: { Name: String, Confidence: Number }[], TopClass: { Name: String, Confidence: Number }}` |
| Identity document reader | `‘Identity document reader’.Predict( Document: Base64 encoded image )` | `{ Context: { Type: String, TypeConfidence: Number }, Fields: { FieldName: { FieldType: "text", Confidence: Number, Value: { Text: String, BoundingBox: { Top: Number, Left: Number, Height: Number, Width: Number }}}}}` |
| Invoice processing | `‘Invoice processing’.Predict( Document: Base64 encoded image )` | `{ Fields: { FieldName: { FieldType: "text" | "date" | "number", Confidence: Number,Value: { Text: String, [Date: Date] | [Number: Number], BoundingBox: { Top: Number, Left: Number, Height: Number, Width: Number } } } }, Tables: { Items: { Rows: { FieldName: { FieldType: "text" | "date" | "number", Confidence: Number, Key: { Name: String, }, Value: { Text: String, [Date: Date] | [Number: Number], BoundingBox: { Top: Number, Left: Number, Height: Number, Width: Number } } } }[] } }}` |
| Key phrase extraction | `'Key phrase extraction'.Predict(Text: String, Language?: Optional String))` | `{ Phrases: String[]}` |
| Language detection | `'Language Detection'.Predict(Text: String)` | `{ Language: String, Confidence: Number}` |
| Receipt processing | `‘Receipt processing’.Predict( Document: Base64 encoded image)` | `{ Context: { Type: String, TypeConfidence: Number }, Fields: { FieldName: { FieldType: "text" | "date" | "number", Confidence: Number, Value: { Text: String, [Date: Date] | [Number: Number], BoundingBox: { Top: Number, Left: Number, Height: Number, Width: Number } } } }, Tables: {Items: {Rows: {FieldName: { FieldType: "text" | "date" | "number", Confidence: Number, Key: { Name: String, }, Value: { Text: String, [Date: Date] | [Number: Number], BoundingBox: { Top: Number, Left: Number, Height: Number,  Width: Number }  }  } }[] } } }` |
| Sentiment analysis | `'Sentiment analysis'.Predict( Text: String, Language?: Optional String )` | `{ Document: { AllSentiments: [ { Name: "Positive", Confidence: Number }, { Name: "Neutral", Confidence: Number }, { Name: "Negative", Confidence: Number } ],  TopSentiment: { Name: "Positive" | "Neutral" | "Negative", Confidence: Number  } } Sentences: { StartIndex: Number, Length: Number, AllSentiments: [ { Name: "Positive", Confidence: Number }, {  Name: "Neutral", Confidence: Number }, { Name: "Negative", Confidence: Number } ], TopSentiment: { Name: "Positive" | "Neutral" | "Negative", Confidence: Number } }[]}` |
| Text recognition | `'Text recognition'.Predict( Document: Base64 encoded image)` | `{Pages: {Page: Number,Lines: { Text: String, BoundingBox: { Left: Number, Top: Number, Width: Number, Height: Number }, Confidence: Number }[] }[]}` |
| Text translation | `'Text translation'.Predict(  Text: String,  TranslateTo?: String,  TranslateFrom?: String)` | `{ Text: String, // Translated text DetectedLanguage?: String, DetectedLanguageConfidence: Number} }` |

## Examples

Every model is invoked using the predict verb. For example, a language detection model takes text as an input and returns a table of possible languages, ordered by that language’s score. The score indicates how confident the model is with its prediction.

| Input | Output |
| - | - |
| `'Language detection'.Predict("bonjour")` | `{ Language: “fr”, Confidence: 1}` |
| `‘Text Recognition’.Predict(Image1.Image)` | `{ Pages: [ {Page: 1, Lines: [ { Text: "Contoso account", BoundingBox: { Left: .15, Top: .05, Width: .8, Height: .10 }, Confidence: .97 }, { Text: "Premium service", BoundingBox: { Left: .15, Top: .20,  Width: .8, Height: .10 }, Confidence: .96 }, { Text: "Paid in full", BoundingBox: { Left: .15, Top: .35, Width: .8, Height: .10 }, Confidence: .99 } } ] }` |

### See also

- [What are canvas apps?](/powerapps/maker/canvas-apps/getting-started)
- [Get started with formulas in canvas apps](/power-apps/maker/canvas-apps/working-with-formulas)
- [Microsoft Power Fx](/power-platform/power-fx/overview)
