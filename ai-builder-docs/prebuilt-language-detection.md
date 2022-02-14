---
title: Language detection prebuilt AI model - AI Builder | Microsoft Docs
description: Describes the prebuilt language detection AI Builder model.
author: alanabrito
ms.topic: conceptual
ms.custom: 
ms.date: 04/05/2021
ms.author: alanab
ms.reviewer: v-aangie
---

# Language detection prebuilt model

The language detection prebuilt model identifies the predominant language of a text document. The model analyzes the text and returns the detected language and a numeric score from 0 through 1. Scores close to 1 indicate higher confidence in the result. The detected language is returned as the "script" of the language. For instance, for the phrase "I have a dog", it will return "en" instead of "en-US". The response for languages that can't be detected is **unknown**.

## Use in Power Apps

### Use the formula bar

You can integrate your AI Builder language detection model by using the formula bar. For more information, see [Use formulas for text AI models](formula-bar.md#language-detection).

## Use in Power Automate

If you want to use this prebuilt model in Power Automate, you can find more information in [Use the language detection prebuilt model in Power Automate](flow-language-detection.md).

## Supported language and data format

- Documents can't exceed 5,120 characters.
- For information about language support, see [Text Analytics API v3 language support](/azure/cognitive-services/text-analytics/language-support?tabs=language-detection).

## Model output

If text is detected, the language detection model outputs the following information:

- **Results**: A list of languages detected in the input text.
- **Language**: Script version of the language code (for example, "en", "fr", "zh_chs", "ru").
- **Confidence score**: Numeric value from 0 through 1, where values close to 1 indicate higher confidence.

## Limits

The following applies to calls made per environment across the following prebuilt models: language detection, sentiment analysis, and key phrase extraction.

|**Action**|**Limit**|**Renewal period**|
|:-----|:-----|-----:|
|Calls (per environment)|400|60 seconds|


[!INCLUDE[footer-include](includes/footer-banner.md)]
