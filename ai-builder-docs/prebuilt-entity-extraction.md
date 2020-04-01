---
title: Entity extraction prebuilt AI model -  AI Builder | Microsoft Docs
description: Describes the prebuilt AI models that are available in AI Builder.
author: mfotedar
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 3/19/2019
ms.author: mfotedar
ms.reviewer: v-dehaas
---

# Preview: Entity extraction model

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

The entity extraction prebuilt model recognizes specific data from text that is of interest to your business.  The model identifies key elements from text, and then classifies them into pre-defined categories. This can help to transform unstructured data into structured data that is machine readable.  You can then apply processing to retrieve information, extract facts, and answer questions.

## Explore entity extraction

You can try out the entity extraction model before you decide to import it into your flow by using the 'try it out' feature.

1. Sign in to [Power Apps](https://make.powerapps.com).
1. In the left navigation pane, select **AI Builder** > **Build**.
1. Under **Get straight to productivity**, select **Entity Extraction**.
1. In the **Entity Extraction** window, select **Try it out**. 
1. Select predefined text samples to analyze, or add your own text in the **Add your own here** box to see how the model analyzes your text.

## Use in Power Automate

If you want to use this prebuilt model in Power Automate, you can find more information in [Use an entity extraction model in Power Automate](prebuilt-entity-extraction-pwr-automate.md).  
 
## Supported data format and languages

- Documents can't exceed 5,000 characters.  
- Supported languages:

  - English
  - Chinese- Simplified
  - French
  - German
  - Portuguese
  - Italian
  - Japanese
  - Spanish

## Supported entity types

|Entity  |Description |
|---------|---------|
|Age|Age of a person, place, or thing, extracted as a number|
|Boolean|Positive or negative responses, extracted as a Boolean|
|City|City names, extracted as a string|
|Color|Primary colors and hues on the color spectrum, extracted as a string|
|Continent|Continent names, extracted as a string|
|Country or region|Country and region names, extracted as a string|
|Date and time|Dates, times, days of the week, and months relative to a point in time, extracted as a string|
|Duration|Lengths of time, extracted as a string, in standard TimeSpan format|
|Email|Email addresses, extracted as a string|
|Event|Event names, extracted as a string|
|Language|Language names, extracted as a string|
|Money|Monetary amounts, extracted as a number|
|Number|Cardinal numbers in numeric or text form, extracted as a number|
|Ordinal|Ordinal numbers in numeric or text form, extracted as a number|
|Organization|Names of organizations, associations, and corporations, extracted as a string|
|Percentage|Percentages in numerical or text form, extracted as a number|
|Person name|A person's partial or full name, extracted as a string|
|Phone number|Phone numbers in the standard US format, extracted as strings|
|Point of interest|Points of interest, extracted as a string|
|Speed|Speed, extracted as a number|
|State|Names and abbreviations for the United States, extracted as a string|
|Street address|Numbered addresses, streets or roads, city, state, zip or postal code in the standard US format, extracted as a string|
|Temperature|Temperature, extracted as a number|
|URL|Website URLs and links, extracted as a string|
|Weight|Weight, extracted as a number|
|Zip code|Zip codes in the standard US format, extracted as a string|


## Model output

The model output shows the identified entities and their entity types. For example:

**Input text:** "Utility costs have increased by 7% at our Boston office"

**Model output entities:**

|Entity |Entity type |
|---------|---------|
|7%    | Percentage  |
|Boston  |City   |

### Next step:

[Use an entity extraction model in Power Automate](prebuilt-entity-extraction-pwr-automate.md).  
