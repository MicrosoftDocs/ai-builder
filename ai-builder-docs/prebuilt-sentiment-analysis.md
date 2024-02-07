---
title: Sentiment analysis prebuilt AI model - AI Builder | Microsoft Docs
description: Describes the prebuilt sentiment analysis AI model in AI Builder.
author: alanabrito
ms.topic: conceptual
ms.custom: 
ms.date: 1/10/2024
ms.author: alanab
ms.reviewer: angieandrews
---

# Sentiment analysis prebuilt model

The sentiment analysis prebuilt model detects positive or negative sentiment in text data. You can use it to analyze social media, customer reviews, or any text data you're interested in. Sentiment analysis evaluates text input, and gives scores and labels at a sentence and document level. The scores and labels can be positive, negative, or neutral. At the document level, there can also be a "mixed" sentiment label, which has no score. The sentiment of the document is determined by aggregating the sentence scores.

## Use in Power Apps

### Explore sentiment analysis

You can try out the sentiment analysis model before you import it into your flow.

1. Sign in to [Power Apps](https://make.powerapps.com) or [Power Automate](https://make.powerautomate.com).
1. On the left pane, select **... More**, select **AI hub**.
1. Under Discover an AI capability, select **AI models**.

    *(Optional)* To keep AI models permanently on the menu for easy access, select the pin icon.

1. Select **Sentiment analysis - Detect positive, negative, or neutral sentiment in text data**.
1. Select predefined text samples to analyze, or add your own text, select **Analyze text**  to see how the model analyzes your text.

### Use the formula bar

You can integrate your AI Builder sentiment analysis models in Power Apps Studio by using the formula bar. For more information, see [Use Power Fx in AI Builder models in Power Apps (preview)](powerfx-in-powerapps.md).

## Use in Power Automate

If you want to use this prebuilt model in Power Automate, you can find more information in [Use the sentiment analysis prebuilt model in Power Automate](flow-sentiment-analysis.md).
  
## Supported language and data format

- **Language**: German, Spanish, English, French, Hindi, Italian, Japanese, Korean, Dutch, Norwegian, Portuguese (Brazil), Portuguese (Portugal), Turkish, Chinese (Simplified), Chinese (Traditional)
- Documents can't exceed 5,120 characters.

## Model output

If text is detected, the sentiment analysis model outputs the following information: 

- **Sentiment**:
  - Positive
  - Negative
  - Neutral
  - Mixed

- **Confidence score**: Value in the range from 0 through 1. Values close to 1 indicate greater confidence that the identified sentiment is accurate.

- **Sentences**: List of sentences from the input text, with analysis of its sentiments.

  - **Sentiment**:
    - Positive
    - Negative
    - Neutral
    - Mixed

  - **Sentence confidence score**: Value in the range from 0 through 1<!--as above-->. Values close to 1 indicate greater confidence that the sentiment is accurate.

## Limits

The following applies to calls made per environment across the following prebuilt models: language detection, sentiment analysis, and key phrase extraction.

|**Action**|**Limit**|**Renewal period**|
|:-----|:-----:|:-----:|
|Calls (per environment)|400|60 seconds|

### See also

- [Training: Analyze the sentiment of text with AI Builder (module)](/training/modules/get-started-with-ai-builder-sentiment-analysis/)
- [Video: How to set up instant Microsoft Teams notifications for negative emails in 1 minute](https://www.youtube.com/watch?v=qfmQAObXTHQ)

[!INCLUDE[footer-include](includes/footer-banner.md)]
