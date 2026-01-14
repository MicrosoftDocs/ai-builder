---
title: Health insurance card processing prebuilt model (preview)
description: Learn about the health insurance card processing prebuilt model in AI Builder.
author: phil-cmd
ms.topic: concept-article
ms.custom: 
ms.date: 01/14/2026
ms.author: plarrue
ms.reviewer: angieandrews
---

# Health insurance card processing prebuilt model (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

The health insurance card processing prebuilt model uses Optical Character Recognition (OCR) capabilities to analyze and extract key information from a US health insurance card. It extracts information from US health insurance card images.

The model extracts information such as insurer, member, prescription, group number, and more.

[!INCLUDE[cc_preview_features_definition](./includes/cc-preview-features-definition.md)]

## Learn how to use the health insurance card prebuilt model

To learn how to use the health insurance card processing prebuilt model, select from the following articles:

- **Power Apps**: [Use the health insurance card processing prebuilt model in Power Apps](use-prebuilt-health-insurance-card-power-apps.md)
- **Power Automate**: [Use the health insurance card processing prebuilt model in Power Automate](use-prebuilt-health-insurance-card-power-automate.md)

## Supported language, format, and size

### Supported language

|Language Locale code|Default|
|--------------------|-------|
|English (United States)|English (United States) en-US|

### Supported format

For best results, provide one clear photo or high-quality scan per document.

|Supported file types|Format|
|-----|--------|
|**Image**|<ul><li>**JPEG/JPG**</li><li>**PNG**</li><li>**BMP**</li></ul>|  
|**Document**|<ul><li>**PDF** (If password-locked, remove the lock before submission.)</li></ul>|

### Supported size

- The file size for analyzing documents is 20 MB.
- The image dimensions must be between 50 pixels x 50 pixels and 10,000 pixels x 10,000 pixels.
- The minimum height of the text to be extracted is 12 pixels for a 1024 x 768 pixel image. This dimension corresponds to about 8 point text at 150 dots per inch (DPI).

## Model output

If a health insurance card is detected, the health insurance card processing model outputs the following information:

|Field|Description|
|-----|------------|
|**Insurer**|Health insurance provider name.|
|**Member**|Member information extracted from the health insurance card.<ul><li>**Name**: Member name.</li><li>**BirthDate**: Member date of birth.</li><li>**Employer**: Member employer.</li><li>**Gender**: Member gender.</li><li>**IdNumberSuffix**: Identification Number Suffix as it appears on some health insurance cards.</li></ul>|
|**Dependents**|Array holding a list of dependents, ordered where possible by membership suffix value.<ul><li>**Name**: Dependent name.</li></ul>|
|**IdNumber**|Identification number details.<ul><li>**Prefix**: Identification Number Prefix as it appears on some health insurance cards.</li><li>**Number**: Identification Number.</li></ul>|
|**GroupNumber**|Insurance Group Number.|
|**PrescriptionInfo**|Prescription-related details.<ul><li>**Issuer**: ANSI issuer identification number (IIN).</li><li>**RxBIN**: Prescription issued BIN number.</li><li>**RxPCN**: Prescription processor control number.</li><li>**RxGrp**: Prescription group number.</li><li>**RxId**: Prescription identification number. If not present, defaults to membership ID number.</li><li>**RxPlan**: Prescription Plan number.</li></ul>|
|**Pbm**|Pharmacy Benefit Manager for the plan.|
|**EffectiveDate**|Date from which the plan is effective.|
|**Copays**|Array holding a list of CoPay Benefits.<ul><li>**Benefit**: Co-Pay Benefit name.</li><li>**Amount**: Co-Pay required amount.</li></ul>|
|**Payer**|Payer details.<ul><li>**Id**: Payer Id Number.</li><li>**Address**: Payer address.</li><li>**PhoneNumber**: Payer phone number.</li></ul>|
|**Plan**|Plan details.<ul><li>**Number**: Plan number.</li><li>**Name**: Plan name - If "Medicaid" is mentioned, then it's a Medicaid plan.</li><li>**Type**: Plan type.</li></ul>|
|**MedicareMedicaidInfo**|Medicare or Medicaid information.<ul><li>**Id**: Medicare or Medicaid number.</li><li>**PartAEffectiveDate**: Effective date of Medicare Part A.</li><li>**PartBEffectiveDate**: Effective date of Medicare Part B.</li></ul>|

## Limits

|Action|Limit|Renewal period|
|:-----|:-----|-----:|
|Calls (per environment)|360|60 seconds|


