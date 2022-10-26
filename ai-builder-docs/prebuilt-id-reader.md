---
title: ID reader prebuilt model - AI Builder
description: Learn about the ID reader prebuilt AI Builder model.
author: JoeFernandezMS
contributors:
  - JoeFernandezMS
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.custom: 
ms.date: 10/26/2022
ms.author: jofernan
ms.reviewer: angieandrews
---

# ID reader prebuilt model

You can use the identity document (ID) reader prebuilt model to extract information from passports and US driver licenses, social security, and green cards. The model will extract information such as the person’s first name, date of birth, or gender.

Images such as scans or pictures of the identity documents are deleted once processed by the model.

> [!NOTE]
> - The design and format of identity documents vary widely. AI Builder is constantly improving the accuracy of the ID reader prebuilt model, but it's possible there could be inaccurate or missing information in some cases. It's a good idea to verify that the output is as you expect.
> - The ID reader prebuilt model only supports Latin character extraction at this time.

## Licensing requirements

AI Builder is licensed as an add-on to your Power Apps or Power Automate licenses. For information about license capacity, pricing, and restrictions, see [AI Builder licensing](./administer-licensing.md).

## Role requirements

Users need to have the Basic User role to consume the ID reader prebuilt model.

<!-- H2 **Use in Power Apps** (we’ll light up this section when Power Apps will show the ID reader)
If you want to use this prebuilt model in Power Apps, you use the business card reader component. More information: Use the business card reader component in canvas apps and Use the business card reader component in model-driven apps -->

## Use in Power Automate

If you want to use this model in Power Automate, you can find more information in [Use the ID reader prebuilt model in Power Automate](id-reader.md).

## Supported language, format, and size

The images you can process with the ID reader prebuilt model must have these characteristics:

- Format:
    - jpg
    - png
    - pdf
- Size: 20 MB maximum (use small images for fastest processing time)
- For PDF documents, only the first 2,000 pages are processed.

## Model output

If a valid identity document is detected, the model will try to locate and extract the following properties.

|Property  |Note  |
|---------|---------|
|First name     |    N/A     |
|Last name     |   N/A      |
|Gender     |    N/A     |
|Date of birth     |    N/A     |
|Place of birth     |    N/A     |
|Region     | US driver license only        |
|Country     |    N/A     |
|Nationality     | Passport only        |
|Street address     | US driver license only        |
|Identity document number     |    N/A     |
|Date of issue    |    N/A     |
|Identity document expiration date     |    N/A     |
|Category code     |    US green card only    |

## Limits

|Action|Limit|Renewal period|
|--|--|--|
|Identity document reader calls (per environment)|24|60 seconds|


### See also

[Use the ID reader prebuilt model in Power Automate](id-reader.md)
