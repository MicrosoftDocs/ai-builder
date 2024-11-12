---
title: AI Builder in Power Automate overview - AI Builder
description: Get an overview of how to create automated flows by using AI Builder in Power Automate.
author: Phil-cmd
ms.topic: overview
ms.date:   11/12/2024 
ms.author: plarrue
ms.reviewer: angieandrews
---

# AI Builder in Power Automate overview

Power Automate is a service that helps you create automated workflows between your favorite apps and services to synchronize files, get notifications, collect data, and more. More information: [Power Automate docs](/power-automate)

 > [!NOTE]
 > For any AI Builder action in a cloud flow, ensure that you leave the default **Asynchronous Pattern** setting to **On**. This ensures that results from the AI models are returned properly.

## Prebuilt AI models you can use in Power Automate right away

* [Business card reader model](flow-business-card-reader.md)
* [Category classification model](prebuilt-category-classification-pwr-automate.md)
* [Entity extraction model](prebuilt-entity-extraction-pwr-automate.md)
* [ID reader model (preview)](prebuilt-id-reader.md)
* [Key phrase extraction model](flow-key-phrase-extraction.md)
* [Language detection model](flow-language-detection.md)
* [Receipt processing model (preview)](flow-receipt-processing.md)
* [Sentiment analysis model](flow-sentiment-analysis.md)
* [Text recognition model](flow-text-recognition.md)
* [Text translation model](flow-text-translation.md)

## Custom AI models that you build and train

* [Category classification model](text-classification-model-in-flow.md)
* [Entity extraction model](entity-extraction-pwr-automate.md)
* [Document processing model](form-processing-model-in-flow.md)
* [Object detection model](object-detection-model-in-flow.md)
* [Prediction model](prediction-pwr-automate.md)

## Predict action

You can use the predict action in Power Automate with many different model types. For more information, see [Use the predict action in Power Automate](predict-action-pwr-automate.md).

## Power Automate AI Builder action

This table helps you identify which capabilities are associated with each AI Builder action.

Each AI Builder capability has a different rate. Get the latest rate card information in [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130).

| Power Automate AI Builder action | Capability |
|-|-|
|Analyze positive or negative sentiment in text|Sentiment analysis|
|Classify text into categories with one of your custom models	|Category classification|
|Classify text into categories with the standard model|	Category classification |
|Create text with GPT using a prompt|	AI prompts, Create text with GPT-3.5|
|Create text with GPT using a prompt| AI prompts, Create text with GPT-4o|
|Detect the language being used in the text|	Language detection|
|Extract entities from text with one of your custom models|	Entity extraction|
|Extract entities from text with the standard model	|Entity extraction|
|Extract information from business cards	|Receipt, Invoice, Identity document or Business card analysis|
|Extract information from documents|	Document processing|
|Extract information from identity documents|	Receipt, Invoice, Identity document or Business card analysis|
|Extract information from invoices|	Receipt, Invoice, Identity document or Business card analysis|
|Extract information from receipts|	Receipt, Invoice, Identity document or Business card analysis|
|Generate the key phrases from a text|	Key phrase extraction|
|Generate description of an image | Image description (Preview) |
|Predict whether something will happen by field|	Real-time Prediction, Scheduled Prediction|
|Predict whether something will happen by record ID|	Real-time Prediction, Scheduled Prediction|
|Recognize text in an image or a PDF document|	Text recognition|
|Translate text into another language|	Text translation|

## Next step

[Prerequisites](use-in-flow-prereq.md)

## Related information

- [Feature availability by region](availability-region.md)  
- [AI Builder in Power Apps overview](use-in-powerapps-overview.md)
- [Training: Use AI Builder in Power Automate (module)](/training/modules/ai-builder-power-automate/)<br/>
- [Training: Improve business performance with AI Builder (learning path)](/training/paths/improve-business-performance-ai-builder/) 


[!INCLUDE[footer-include](includes/footer-banner.md)]
