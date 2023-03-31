---
title: Extract dates and numbers from documents (preview)
description: Learn how to extract dates and numbers from documents in AI Builder.
author: CedrickBellarosa
contributors:
  - v-aangie
ms.topic: conceptual
ms.custom: 
ms.date: 03/28/2023
ms.author: cdbellar
ms.reviewer: angieandrews
---

# Extract dates and numbers from documents (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

While many fields to be extracted are simple texts, there are cases where the information to extract is a date or a number including amounts.

> [!IMPORTANT]
>
> - [!INCLUDE[cc_preview_features_definition](includes/cc-preview-features-definition.md)]
>
> - This feature is in process of rolling out, and might not be available in your region yet.

Importing this data to a target system can be cumbersome, requiring significant custom conversion logic. Most of the import connectors and APIs only accept normalized dates in ISO 8601 format like YYYY-MM-DD. To learn more about date format, go to https://www.iso.org/iso-8601-date-and-time-format.html. They also only accept numbers using dot as a decimal separator without a thousands separator like NNN.DD.

We’ve added the ability to declare this type during the field creation step of the wizard and to choose a date or number convention (equivalent to a locale).

:::image type="content" source="media/document-processing-define-field-type.gif" alt-text="Animation of defining the fields' type.":::

 > [!NOTE]
 > For each field, only one convention is allowed for a given field for all the collections of this model. For instance, if you extract a field amount by selecting **Use comma (,) as decimal separator**, the following text 1234,56 or 1 234,56 will be converted to 1234.56. Amounts with format 12,34,576.78 or 1,234.56 won’t be converted.

During the extraction, the text will be automatically converted according to the convention provided. This converted value can be retrieved using the “YOURFIELDNAME value” result. This value will be empty If the conversion isn't possible. The original text can be retrieved using the “YOURFIELDNAME text” result. 

### Supported date formats

When defining the field, choose among **Year, Month, Day**, **Month, Day, Year**, or **Day, Month, Year**.

The following characters can be used as date delimiters: comma, dash, and forward slash. Whitespace can't be used as a delimiter. For example:
- 01,01,2020 (comma)
- 01-01-2020 (dash)
- 01/01/2020 (forward slash)

The day and month can each be written as one or two digits, and the year can be two or four digits:

- 1-1-2020
- 1-01-20

If a date string has eight digits, the delimiter is optional:

- 01012020
- 01 01 2020

The month can also be written as its full or short name. If the name is used, delimiter characters are optional. However, this format may be recognized less accurately than others.

- 01/Jan/2020
- 01Jan2020
- 01 Jan 2020

### Supported number formats

When defining the field, choose either **Use dot (.) as decimal separator** or **Use comma (,) as decimal separator**.

When the decimal separator is a dot (.), thousand separators can be omitted, and comma (,) or whitespace can be used. For example:

- 1234.56
- 1,234.56
- 1 234.56

When the decimal separator is a comma (,), thousand separators or whitespace   can be omitted.  For example:

- 1234,56
- 1 234.56

## Next step

[Train and publish your document processing model](form-processing-train.md)

### See also

[Training: Process custom documents with AI Builder (module)](/training/modules/get-started-with-form-processing/)

[!INCLUDE[footer-include](includes/footer-banner.md)]
