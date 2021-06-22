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

If you specify a single string as the argument, the return value is the sentiment of the string as a text, such as negative, positive or neutral:

### Syntax

AIBuilder.AnalyzeSentiment(*String*[, *Language*]).sentiment

- **String** - Required. This is the string to analyze sentiment for.
- **Language** - Optional. You can specify the language for your string to get the best result.

### Example

<<<<<<< Updated upstream
```powerapps-dot
AIBuilder.AnalyzeSentiment(TextInput1.Text).sentiment
=======
```
AIBuilder.AnalyzeSentiment("I love AI Builder").sentiment
>>>>>>> Stashed changes
```

### Input/output variation

To ensure the text is interpreted in context of a specific language, you can provide the language code in IETF [BCP-47 format](/openspecs/office_standards/ms-oe376/6c085406-a698-4e12-9d4d-c3b0ee3dbc4a). 
In the **Input** column, "en-us" is the language code of English (United States):

|Input  |Output  |
|---------|---------|
|**AIBuilder.AnalyzeSentiment(TextInput1.Text,{language:<br/>"en-us"}).sentiment** |positive   |

## Entity extraction

The basic input formula in the entity extraction model extracts the types of entities present in the text into a list:

```powerapps-dot
Concat(AIBuilder.ExtractTextEntities(TextInput1.Text).entities, type & ", ")
```
### Input/output variations

- This formula uses your custom AI Builder model to return all entities that belong to the text, in list form:

  |Input  |Output  |
  |---------|---------|
  |**Concat(AIBuilder.ExtractTextEntities CategorizeText(TextInput1.<br/>Text, { modelId: GUID("<yourModelId>").entities, type & ",")**  | <span style="color: red;">SCREENSHOT OF OUTPUT</span> |

- This formula uses specific language to interpret the text and return all types of entities into a list. In the **Input** column, "en-us" is the language code of English (United States). For a complete list of language code in IETF, see [BCP-47 format](/openspecs/office_standards/ms-oe376/6c085406-a698-4e12-9d4d-c3b0ee3dbc4a):

  |Input  |Output  |
  |---------|---------|
  | **Concat(AIBuilder.ExtractTextEntities(TextInput1.Text,{language:<br/>"en-us"}).entities, type & ", ")**  |<span style="color: red;">SCREENSHOT OF OUTPUT</span> |

## Key phrase extraction

The basic input formula in the key phrase extraction model extracts all key phrases from the text into a list:

```powerapps-dot
Concat(AIBuilder.ExtractKeyPhrases(TextInput1.Text).phrases, phrase & ",")
```

### Input/output variation

- This formula uses specific language and extracts all key phrases from the text into a list. In the **Input** column, "en-us" is the language code of English (United States). For a complete list of language code IETF, see [BCP-47 format](/openspecs/office_standards/ms-oe376/6c085406-a698-4e12-9d4d-c3b0ee3dbc4a):  

  |Input  |Output  |
  |---------|---------|
  |**Concat(AIBuilder.ExtractKeyPhrases(TextInput1.Text, ,{language:<br/>"en-us"}).phrases, phrase & ",")**   |<span style="color: red;">SCREENSHOT OF OUTPUT</span>         |

## Language detection

The basic input formula formula in the language detection model returns the two-letter language code (ISO 639) of the text:

```powerapps-dot
AIBuilder.DetectLanguage(TextInput1.Text).language
```

   |Text  |Language  |
   |---------|:---------:|
   |How are you    |en   |
   |Comment allez-vous  |fr  |

### Input/output variations

- To narrow down the prediction in context of a specific country, provide the country code in ISO-3166 format:

  |Input  |Output  |
  |---------|---------|
  |**AIBuilder.DetectLanguage(TextInput1.Text,{countryHint:"DK"}).language**<br/><br/>In this example, country **DK** refers to the ISO-3166 country code for Denmark.   | <span style="color: red;">SCREENSHOT OF OUTPUT</span>        |
  |If you provide **hvordan har du det** in **textinput1**, it returns **da** which is the<br/>language code for Danish. Without country code provided it would return **no**,<br/>which is the language code for Norwegian where this text is also valid.     | <span style="color: red;">SCREENSHOT OF OUTPUT</span>        |

- This formula returns the confidence score of the detected language. This returns a number in the range of 0 to 1. The greater the value, the higher the confidence is in the predictions made by the AI model:

  |Input  |Output  |
  |---------|---------|
  | **AIBuilder.DetectLanguage(TextInput1.Text).score** | <span style="color: red;">SCREENSHOT OF OUTPUT</span>  | 

## Category classification

The basic input formula in the category classification model returns all categories that belong to the text, in list form:

```powerapps-dot
Concat(AIBuilder.CategorizeText (TextInput1.Text).categories , type & ",")
```

### Input/output variations

- This formula uses your custom AI Builder model to return all categories that belong to the text, in list form:

  |Input  |Output  |
  |---------|---------|
    |**Concat(AIBuilder.CategorizeText(TextInput1.Text,{modelId:GUID("<your model id>"<br/>)}).categories,type,",")**    | <span style="color: red;">SCREENSHOT OF OUTPUT</span>         |

- This formula uses English (United States) as the language for interpretation to return all categories that belong to the text, in list form:

  |Input  |Output  |
  |---------|---------|
  | **Concat(AIBuilder.CategorizeText(TextInput1.Text ,{language:<br/>"en-us"}).categories,type,","));**  | <span style="color: red;">SCREENSHOT OF OUTPUT</span> |

[!INCLUDE[footer-include](includes/footer-banner.md)]
