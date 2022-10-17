---
title: Business card prebuilt AI model- AI Builder | Microsoft Docs
description: Describes the business card prebuilt AI Builder model.
author: alanabrito
ms.topic: conceptual
ms.custom: 
ms.date: 03/29/2021
ms.author: alanab
ms.reviewer: angieandrews
---

# Business card prebuilt model

You can use the business card prebuilt model to extract information from business card images. If it detects a business card in the image, the AI model extracts information such as the person's name, job title, address, email, company, and phone numbers.

 > [!NOTE]
>
> - The design and format of business cards varies widely. AI Builder is constantly improving the accuracy of the business card AI model, but it's possible there could be inaccurate or missing information in some cases. It's a good idea to verify that the output is as you expect.
> - The prebuilt business card reader only supports English & Japanese languages extraction at this time. Check back to see what languages are supported going forward.

## Licensing requirements

AI Builder is licensed as an add-on to your Power Apps or Power Automate licenses. For information about license capacity, pricing, and restrictions, see [AI Builder licensing](administer-licensing.md).

## Role requirements

Users need to have the Basic User role to consume the business card reader.

## Use in Power Apps

If you want to use this prebuilt model in Power Apps, you use the business card reader component. More information: [Use the business card reader component in canvas apps](business-card-reader-component-in-powerapps.md) and [Use the business card reader component in model-driven apps](business-card-reader-component-model-driven.md)

## Use in Power Automate

If you want to use this prebuilt model in Power Automate, you can find more information in [Use the business card reader prebuilt model in Power Automate](flow-business-card-reader.md).

## Supported language, format, and size

The images you can process with the business card model must have these characteristics:

- Languages: English & Japanese
- Format:
  - JPG
  - PNG
  - BMP
- Size: 50 MB maximum

## Model output

If a business card is detected, the business card model will try to locate and extract the following properties.

|Property |Definition  |
|---------|---------|
| **AddressCity**| The city address|
| **AddressCountry**| The country address|
| **AddressPostalCode**| The postal code address|
| **AddressPostOfficeBox**| The post office box address|
| **AddressState**| The state address|
| **AddressStreet**| The street address|
| **BusinessPhone**| The first phone or fax number|
| **CleanedImage**| The image after processing, where the business card appears cropped and enhanced from the original image|
| **CompanyName**| The company name|
| **Department**| The organization department found|
| **Email**| The contact email found in the business card, if any|
| **Fax**| The third phone or fax number|
| **FirstName**| The contact's first name|
| **FullAddress**| The contact's full address|
| **FullName**| The contact's full name|
| **JobTitle**| The contact's job title|
| **LastName**| The contact's last name|
| **MobilePhone**| The second phone or fax number|
| **OriginalImage**| The original image before processing|
| **Website**| The website|

## Limits

|**Action**|**Limit**|**Renewal period**|
|:-----|:-----|-----:|
|Business card reader calls (per environment)|24|60 seconds|


[!INCLUDE[footer-include](includes/footer-banner.md)]
