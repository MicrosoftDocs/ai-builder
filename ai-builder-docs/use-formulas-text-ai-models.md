---
title: Use formulas for text AI models - AI Builder | Microsoft Docs
description: Provides steps by step instructions about how to use your model in AI Builder.
author: v-aangie
ms.service: aibuilder
ms.topic: conceptual 
ms.custom: 
ms.date: 06/30/2021
ms.author: norliu
ms.reviewer: v-aangie
---

# Use formulas for text AI models (preview)

You can integrate some AI Builder models in [Power Apps Studio](https://create.powerapps.com) by using the formula bar. Currently, this functionality is available only for the following AI Builder model types:

* Sentiment analysis
* Entity extraction
* Key phrase extraction
* Language detection
* Category classification

 > [!NOTE]
 > To improve the prediction score of the text AI models listed above and to narrow down the language in which they are interpreted, you can provide language code as an additional parameter. The language code needs to be provided in IETF [BCP-47 format](/openspecs/office_standards/ms-oe376/6c085406-a698-4e12-9d4d-c3b0ee3dbc4a).
> 
> For a complete list of languages supported for these models, see [Text Analytics v3 language support](/azure/cognitive-services/text-analytics/language-support?tabs=sentiment-analysis).

**Example**:

If you want, you can select the **Label** control, enter **AIBuilder**, and try out the various AI models, using **TextInput1** as the text. <!-- Angie: Verify this screenshot. -->

> [!div class="mx-imgBorder"]
> ![Insert label screen](media/use-formulas-example.png "Insert label screen")

## Sentiment analysis

Returns the sentiment of the text, such as negative or positive. 

AIBuilder.AnalyzeSentiment(TextInput1.Text).sentiment 

To ensure the text is interpreted in context of a specific language you can provide the language code in IETF BCP-47 format 

AIBuilder.AnalyzeSentiment(TextInput1.Text,{language:"en-us"}).sentiment 

en-us – is the language code of English (United States) 

## Entity extraction

Extracts the types of entities present in the text into a list. 

Concat(AIBuilder.ExtractTextEntities(TextInput1.Text).entities, type & ", ") 

Uses your custom AI Builder model to return all entities that belong to the text, in list form 

Concat(AIBuilder.ExtractTextEntities CategorizeText(TextInput1.Text, { modelId: GUID("<yourModelId>").entities, type & ",") 

Use specific language to interpret the text and return all types of entities into a list. For complete list of Language code in IETF BCP-47 format 

Concat(AIBuilder.ExtractTextEntities(TextInput1.Text,{language:"en-us"}).entities, type & ", ") 

en-us – is the language code of English (United States) 

## Key phrase extraction

Extracts all key phrases from the text into a list. 

Concat(AIBuilder.ExtractKeyPhrases(TextInput1.Text).phrases, phrase & ",") 

Use specific language and extract all key phrases from the text into a list. For complete list of Language code in BCP-47 format 

Concat(AIBuilder.ExtractKeyPhrases(TextInput1.Text, ,{language:"en-us"}).phrases, phrase & ",") 

en-us – is the language code of English (United States) 

## Language detection

Returns the two-letter language code (ISO 3166639) of the text.  

AIBuilder.DetectLanguage(TextInput1.Text).language 

<!-- Angie: Make this into a table -->
Text 
Language 
How are you 
en 
Comment allez-vous 
fr

To narrow down the prediction in context of a specific country provide the country code in ISO-3166 format.

AIBuilder.DetectLanguage(TextInput1.Text,{countryHint:"DK"}).language  

Country DK refers to ISO-3166 country code for Denmark 

The following text provided in textinput1 

hvordan har du det

returns da which is the language code for Danish. Without country code provided it would return “no” the language code for Norwegian where this text is also valid.

AIBuilder.DetectLanguage(TextInput1.Text).score  

Returns the confidence score of the detected language. This returns a number in the range of 0 to 1. Greater the value, higher the confidence in the predictions made by the AI model.

## Category classification

Returns all categories that belong to the text, in list form. 

Concat(AIBuilder.CategorizeText (TextInput1.Text).categories , type & ",") 

Uses your custom AI Builder model to return all categories that belong to the text, in list form.

Concat(AIBuilder.CategorizeText(TextInput1, { modelId: GUID("<yourModelId>").categories, type & ",")Concat( AIBuilder.CategorizeText(TextInput1.Text ,{modelId:GUID("<your model id>" )}).categories,type,",") 

Uses English (United States) as the language for interpretation to return all categories that belong to the text, in list form.  

Concat( AIBuilder.CategorizeText(TextInput1.Text ,{language:"en-us"}).categories,type,",")); 

### See also <!-- Angie: is this needed? -->