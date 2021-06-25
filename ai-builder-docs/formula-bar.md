---
title: Use formulas for text AI models - AI Builder | Microsoft Docs
description: Provides examples of formulas you can use in AI Builder text models.
author: norliu
ms.service: aibuilder
ms.topic: conceptual 
ms.custom: 
ms.date: 06/30/2021
ms.author: norliu
ms.reviewer: v-aangie
---

# Use formulas for text AI models in Power Apps (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

You can integrate some AI Builder models in [Power Apps Studio](https://create.powerapps.com) by using the formula bar. This functionality is available only for the following AI Builder model types:

|Model type | Build type  |
|---------|---------|
|[Sentiment analysis](#sentiment-analysis)  | Prebuilt     |
|[Entity extraction](#entity-extraction)    | Prebuilt and Custom    |
|[Key phrase extraction](#key-phrase-extraction)   | Prebuilt        |
|[Language detection](#language-detection)   | Prebuilt     |
|[Category classification](#category-classification)  | Prebuilt and Custom   |

> [!IMPORTANT]
 >* This is a preview feature. [!INCLUDE [cc-preview-features-definition](includes/cc-preview-features-definition.md)]
>
 >* [Data loss prevention policies](/power-platform/admin/wp-data-loss-prevention) that apply to Dataverse also apply to AI Builder.
 >* To use formulas in an app that was created before May 7, 2020, go to **Settings** > **Advance Settings** > **Preview Features**, and set **AI Builder formulas** to **ON**. This step isn't necessary for newly created apps.

When you enter **AIBuilder** in an app, it might take a few seconds to load its functions. After it loads, enter a period (**.**) to view the available functions. For detailed information about how to use formulas in canvas apps, see [Get started with canvas-app formulas in Power Apps](/powerapps/maker/canvas-apps/working-with-formulas).

To enable or disable this feature (for example, for data loss prevention), see **AI Builder formulas** under **Advanced Settings**. More information, see [Controlling which features are enabled](/powerapps/maker/canvas-apps/working-with-experimental-preview#controlling-which-features-are-enabled).

 > [!NOTE]
 > To improve the prediction score of the text AI models listed above and to narrow down the language in which they are interpreted, you can provide language code as an additional parameter. The language code needs to be provided in IETF [BCP-47 format](/openspecs/office_standards/ms-oe376/6c085406-a698-4e12-9d4d-c3b0ee3dbc4a).
>
> For a complete list of languages supported for these models, see [Text Analytics v3 language support](/azure/cognitive-services/text-analytics/language-support?tabs=sentiment-analysis).

**Example**:

If you want, you can select the **Label** control, enter **AIBuilder**, and try out the various AI models, using **TextInput1** as the text.

> [!div class="mx-imgBorder"]
> ![Available formulas](media/formula-menu.png "Available formulas")

## Sentiment analysis

If you specify a single string as the argument, the return value is the sentiment of the string as a text, such as negative, positive or neutral.

### Syntax

AIBuilder.AnalyzeSentiment(*String*[, *Language*]).sentiment

- **String** - (*Required*) This is the string to analyze sentiment for.
- **Language** - (*Optional*) You can specify the language for your string to get the best result.

### Example

```powerapps-dot
AIBuilder.AnalyzeSentiment(TextInput1.Text).sentiment
```

### Input/output variation

To ensure the text is interpreted in context of a specific language, you can provide the language code in IETF [BCP-47 format](/openspecs/office_standards/ms-oe376/6c085406-a698-4e12-9d4d-c3b0ee3dbc4a).
In the **Input** column, "en-us" is the language code of English (United States):

|Input  |Output  |
|---------|---------|
|AIBuilder.AnalyzeSentiment(TextInput1.Text,{language:<br/>"en-us"}).sentiment  |Positive   |

## Entity extraction

If you specify a single string as the argument, the return values are the types of entities present in the text in a list.

### Syntax

AIBuilder.ExtractTextEntities(*String*).entities, type & ", ") ***VERIFY THIS***

- **String** - (*Required*) This is the string to extract the tables.
- **Model ID** - (*Optional*) ***COMPLETE THIS***
- **Language** - (*Optional*) You can specify the language for your string to get the best result.

### Example

```powerapps-dot
Concat(AIBuilder.ExtractTextEntities(TextInput1.Text).entities, type & ",")
```

### Input/output variations

- This formula uses your custom AI Builder model to return all entities that belong to the text, in list form:

  |Input  |Output  |
  |---------|---------|
  *Concat(AIBuilder.ExtractTextEntities CategorizeText(TextInput1.<br/>Text, { modelId: GUID("<yourModelId>").entities, type & ",")  | ***EXAMPLE***  |

- This formula uses specific language to interpret the text and return all types of entities into a list. In the **Input** column, "en-us" is the language code of English (United States). For a complete list of language code in IETF, see [BCP-47 format](/openspecs/office_standards/ms-oe376/6c085406-a698-4e12-9d4d-c3b0ee3dbc4a):

  |Input  |Output  |
  |---------|---------|
  | Concat(AIBuilder.ExtractTextEntities(TextInput1.Text,{language:<br/>"en-us"}).entities, type & ", ")  | ***EXAMPLE***   |

## Key phrase extraction

If you specify a single string as the argument, the return values are all key phrases from the text in a list.

### Syntax

AIBuilder.ExtractKeyPhrases(*String*[, *Language*]).phrases, phrase & ",") ***VERIFY THIS***

- **String** - (*Required*) This is the string to extract the key phrases.
- **Phrases** - (*Required*) ***COMPLETE THIS***
- **Language** - (*Optional*) You can specify the language for your string to get the best result.

### Example

```powerapps-dot
Concat(AIBuilder.ExtractKeyPhrases(TextInput1.Text).phrases, phrase & ",")
```

### Input/output variation

This formula uses specific language and extracts all key phrases from the text into a list. In the **Input** column, "en-us" is the language code of English (United States). For a complete list of language code IETF, see [BCP-47 format](/openspecs/office_standards/ms-oe376/6c085406-a698-4e12-9d4d-c3b0ee3dbc4a):  

|Input  |Output  |
|---------|---------|
|Concat(AIBuilder.ExtractKeyPhrases(TextInput1.Text, ,{language:<br/>"en-us"}).phrases, phrase & ",")   |***EXAMPLE***      |

## Language detection

If you specify a single string as the argument, the return value is the two-letter language code (ISO 639) of the text:

   |Text  |Language  |
   |---------|:---------:|
   |How are you    |en   |
   |Comment allez-vous  |fr  |

### Syntax

AIBuilder.DetectLanguage(*String*).language ***VERIFY THIS***

- **String** - (*Required*) This is the string that finds the two-letter language code.
- **Language** - (*Required*) This is the language for your string.

### Example

```powerapps-dot
AIBuilder.DetectLanguage(TextInput1.Text).language
```

### Input/output variations

- To narrow down the prediction in context of a specific country, provide the country code in ISO-3166 format:

  |Input  |Output  |
  |---------|---------|
  |AIBuilder.DetectLanguage(TextInput1.Text,{countryHint:"DK"}).language<br/><br/>In this example, country **DK** refers to the ISO-3166 country code for Denmark.   | ***EXAMPLE***       |
  |If you provide **hvordan har du det** in **textinput1**, it returns **da** which is the<br/>language code for Danish. Without country code provided it would return **no**,<br/>which is the language code for Norwegian where this text is also valid.     | ***EXAMPLE***       |

- This formula returns the confidence score of the detected language. This returns a number in the range of 0 to 1. The greater the value, the higher the confidence is in the predictions made by the AI model:

  |Input  |Output  |
  |---------|---------|
  | AIBuilder.DetectLanguage(TextInput1.Text).score | ***EXAMPLE***  | 

## Category classification

If you specify a single string as the argument, the return values are the categories that belong to the text, in list form.

### Syntax

AIBuilder.CategorizeText(*String*).categorize

- **String** - (*Required*) This is the string to extract the tables.
- **Model ID** - (*Optional*) **COMPLETE THIS**
- **Language** - (*Optional*) You can specify the language for your string to get the best result.

### Example

```powerapps-dot
Concat(AIBuilder.CategorizeText (TextInput1.Text).categories , type & ",")
```

### Input/output variations

- This formula uses your custom AI Builder model to return all categories that belong to the text, in list form:

  |Input  |Output  |
  |---------|---------|
    |Concat(AIBuilder.CategorizeText(TextInput1.Text,{modelId:GUID("<your model id>"<br/>)}).categories,type,",")    | ***EXAMPLE***      |

- This formula uses English (United States) as the language for interpretation to return all categories that belong to the text, in list form:

  |Input  |Output  |
  |---------|---------|
  | Concat(AIBuilder.CategorizeText(TextInput1.Text ,{language:<br/>"en-us"}).categories,type,","));  | ***EXAMPLE*** |

[!INCLUDE[footer-include](includes/footer-banner.md)]
