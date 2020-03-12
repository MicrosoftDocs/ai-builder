---
title: Key phrase extraction prebuilt AI model -  AI Builder | Microsoft Docs
description: Describes the prebuilt AI models that are available in AI Builder.
author: alanabrito
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 10/04/2019
ms.author: alanab
ms.reviewer: v-dehaas
---

# Preview: Key phrase extraction model

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

The key phrase extraction model identifies the main points in a text document. For example, given input text "The food was delicious and there were wonderful staff", the service returns the main talking points: "food" and "wonderful staff". This model can extract a list of key phrases from unstructured text documents. 

## Use in Power Automate

If you want to use this prebuilt model in Power Automate, you can find more information in [Use key phrase extraction model in Power Automate](flow-key-phrase-extraction.md).  
 
## Supported language and data format

- Documents can't exceed 5,120 characters.  
- For information on language support, see [Language and region support for the text analytics API](/azure/cognitive-services/text-analytics/language-support?#sentiment-analysis-key-phrase-extraction-and-named-entity-recognition).

## Model output

If text is detected, the key phrase extraction model will output the following information:

- **Results**: A list of phrases from the document
- **Phrase**: Strings denoting the key talking points in the document text
