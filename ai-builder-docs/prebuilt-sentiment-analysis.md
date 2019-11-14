---
title: Sentiment analysis prebuilt AI model -  AI Builder | Microsoft Docs
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

# Preview: Sentiment analysis model

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

The sentiment analysis prebuilt model can be used to detect positive or negative sentiment in social media, customer reviews or any text data you want to analyze.  This model evaluates text input and return scores and labels at a sentence and document level. The scores and labels are positive, negative, and neutral. At the document level, the mixed sentiment label (not the score) also can be returned. The sentiment of the document is determined by aggregating the scores of the sentences.


## Use in Power Automate

If you want to use this prebuilt model in Power Automate, you can find more information in [Use sentiment analysis model in Power Automate](flow-sentiment-analysis.md).
  
## Supported language and data format

- Documents cannot exceed 5,120 characters.
- For information on language support, see [Language and region support for the text analytics API](/azure/cognitive-services/text-analytics/language-support?#sentiment-analysis-key-phrase-extraction-and-named-entity-recognition).

## Model output

If text is detected, the sentiment analysis model will output the following information: 
- **Sentiment**: 
    - Positive
    - Negative
    - Neutral
    - Mixed
- **DocumentScores**: Value in the range of 0 to 1 for the sentiments positive, negative and neutral where values close to 1 indicate greater certainty that the identified sentiment is accurate.
- **Sentences**: List of sentences from the input text with analysis of its sentiments.
    - **Sentiment**: 
        - Positive
        - Negative
        - Neutral
        - Mixed
    - **SentenceScores**: Value in the range of 0 to 1 for the sentiments positive, negative and neutral where values close to 1 indicate greater certainty that the identified sentiment is accurate.
