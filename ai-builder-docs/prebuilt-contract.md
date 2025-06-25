---
title: Contract prebuilt model
description: Learn about the contract prebuilt model in AI Builder.
author: phil-cmd
ms.topic: conceptual
ms.custom: 
ms.date: 06/27/2025
ms.author: plarrue
ms.reviewer: angieandrews
---

# Contract prebuilt model

The contract prebuilt model uses Optical Character Recognition (OCR) capabilities to analyze and extract key fields and line items from contract entities. Contracts can be of various formats and quality including phone-captured images, scanned documents, and digital PDFs.

## Learn how to use the contract prebuilt model

To learn how to use the contract prebuilt model, select from the following articles:

- **Power Apps**: [Use the contract prebuilt model in Power Apps](use-prebuilt-contract-power-apps.md)
- **Power Automate**: [Use the contract prebuilt model in Power Automate](use-prebuilt-contract-power-automate.md)

## Supported language, format, and file size

### Supported language

|Language locale code|Default|
|--------------------|-------|
|English (United States)|English (United States) en-US|

### Supported format

For best results, provide one clear photo or high-quality scan per document.

|Supported file types|Format|
|-----|--------|
|**Image**|<ul><li>**JPEG/JPG**</li><li>**PNG**</li><li>**BMP**</li></ul>|  
|**Document**|<ul><li>**PDF** (If password-locked, remove the lock before submission.)</li></ul>|

### Supported file size

- The file size for analyzing documents is 20 MB
- The image dimensions must be between 50 pixels x 50 pixels and 10,000 pixels x 10,000 pixels
- The minimum height of the text to be extracted is 12 pixels for a 1024 x 768 pixel image. This dimension corresponds to about 8 point text at 150 dots per inch (DPI).
- For PDF documents, only the first 2,000 pages are processed.

## Model output

|Field|Description|
|----------|-----------|
|**Title**|Contract title| 
|**ContractId**|Contract identification code|  
|**Parties**|List of legal parties<ul><li>**Name**: Name of legal party</li><li>**Address**: Address of legal party</li><li>**ReferenceName**: Name used throughout the contract as reference to the legal party</li><li>**Clause**: Full description of the party</li></ul>|  
|**ExecutionDate**|Date when the agreement was fully signed and agreed upon by all parties|  
|**EffectiveDate**|Date when the contract starts to be in effect|  
|**ExpirationDate**|Date when the contract ends to be in effect|  
|**ContractDuration**|Contract terms|  
|**RenewalDate**|Date when the contract needs to be renewed by|  
|**Jurisdictions**|List of jurisdictions<ul><li>**Clause**: Full description of the jurisdiction</li><li>**Region**: Court location</li></ul>|

## Confidence score

|Field|Confidence score|
|----------|:-----------:|
|Title|✔|
|ContractId|✔|
|Parties| - |
|ExecutionDate|✔|
|EffectiveDate|✔|
|ExpirationDate|✔|
|ContractDuration|✔|
|RenewalDate|✔|
|Jurisdictions| - |

## Limits

|Action|Limit|Renewal period|
|:-----|:-----|-----:|
|Calls (per environment)|360|60 seconds|

<!--## Related information

placeholder-->