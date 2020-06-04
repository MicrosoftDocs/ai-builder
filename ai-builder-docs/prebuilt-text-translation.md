---
title: Text translation prebuilt AI model -  AI Builder | Microsoft Docs
description: Describes the prebuilt text translation AI model in AI Builder.
author: alanabrito

ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 6/6/2020
ms.author: alanab
ms.reviewer: v-dehaas
---

# Text translation model

The text translation prebuilt model translates your text data in real time across more than 60 languages. You could use it to remove the language barrier within your company. The text translation model can also autodetect the language of your text data. 

## Use in Power Automate

If you want to use this prebuilt model in Power Automate, you can find more information in [Use text translation model in Power Automate](flow-text-translation.md).
  
## Supported language and data format

- Documents can't exceed 5,120 characters.
- For information on language support, see [Language and region support for the text translation API](/azure/cognitive-services/translator/language-support#translation).

## Model output

If text is detected and the target language defined, the text translation model will output the following information: 
- **Text**:  Strings containing the translated text
- **Detected language**: Script version of the language code (ex.: "en", "fr", "zh_chs", "ru") detected in the source text. The model will not detect the source language if it was specified by the user. 
- **Detected language confidence**: Numeric value from 0 to 1 where values close to 1 indicate 100% confidence that the identified source language is true. The model will not detect the source language if it was specified by the user.
