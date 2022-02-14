---
title: Key phrase extraction prebuilt AI model - AI Builder | Microsoft Docs
description: Describes the prebuilt key phrase extraction AI model in AI Builder.
author: alanabrito
ms.topic: conceptual
ms.custom: 
ms.date: 04/05/2021
ms.author: alanab
ms.reviewer: v-aangie
---

# Key phrase extraction prebuilt model

The key phrase extraction prebuilt model identifies the main points in a text document. For example, given input text "The food was delicious and there was great service!", the model returns the main talking points: "food" and "great service". This model can extract a list of key phrases from unstructured text documents.

## Use in Power Apps

### Explore key phrase extraction

You can try out the key phrase extraction model before you import it into your flow by using the "try it out" feature.

1. Sign in to [Power Apps](https://make.powerapps.com).
1. In the left pane, select **AI Builder** > **Build**.
1. Under **Get straight to productivity**, select **Key Phrase Extraction**.
1. In the **Key Phrase Extraction** window, select **Try it out**. 
1. Select predefined text samples to analyze, or add your own text in the **Or add your own here** box to see how the model analyzes your text.

### Use the formula bar

You can integrate your AI Builder key phrase extraction model in Power Apps Studio by using the formula bar. For more information, see [Use formulas for text AI models](formula-bar.md#key-phrase-extraction).

## Use in Power Automate

If you want to use this prebuilt model in Power Automate, you can find more information in [Use the key phrase extraction prebuilt model in Power Automate](flow-key-phrase-extraction.md).
 
## Supported language and data format

- **Language**: Danish, German, English, Spanish, Finnish, French, Italian, Japanese, Korean, Dutch, Norwegian, Polish, Portuguese (Brazil), Portuguese (Portugal), Russian, Swedish
- Documents can't exceed 5,120 characters.

## Model output

If text is detected, the key phrase extraction model outputs the following information:

- **Results**: A list of phrases from the document
- **Phrase**: Strings denoting the key talking points in the document text

## Limits

The following applies to calls made per environment across the following prebuilt models: language detection, sentiment analysis, and key phrase extraction.

|**Action**|**Limit**|**Renewal period**|
|:-----|:-----|-----:|
|Calls (per environment)|400|60 seconds|


[!INCLUDE[footer-include](includes/footer-banner.md)]
