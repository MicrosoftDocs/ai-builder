---
title: Text translation prebuilt AI model -  AI Builder | Microsoft Docs
description: Describes the prebuilt text translation AI model in AI Builder.
author: alanabrito
ms.topic: conceptual
ms.custom: 
ms.date: 01/27/2025
ms.author: alanab
ms.reviewer: angieandrews
---

# Text translation prebuilt model

The text translation prebuilt model translates your text data in real time across more than 60 languages. This prebuilt model could help remove language barriers within your company. The text translation model can also detect the language of the text data you want to translate.

## Use in Power Automate

If you want to use this prebuilt model in Power Automate, you can find more information here: [Use text translation model in Power Automate](flow-text-translation.md).
  
## Supported language and data format

- Test can't exceed 10,000 characters.
- For information on language support, see [Language and region support for the text translation API](/azure/cognitive-services/translator/language-support#translation).

## Model output

If text is detected and the target language defined, the text translation model will output the following information:

- **Text**:  Strings containing the translated text.
- **Detected language**: Script version of the language code (ex.: "en", "fr", "zh_chs", "ru") detected in the source text. The model will not detect the source language if it was specified by the user.


[!INCLUDE[footer-include](includes/footer-banner.md)]
