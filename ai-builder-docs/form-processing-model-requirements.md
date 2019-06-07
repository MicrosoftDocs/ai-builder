---
title: Requirements and limitations -  AI Builder | Microsoft Docs
description: Describes the requirements and limitations form processing models in AI Builder.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/07/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Form processing AI model requirements and limitations

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

> [!NOTE]
>
> - Make sure your administrator has assigned you a security role with all organization privileges over the entity **Note** from **Core Records**, and read privilege over the entity you are using to select object names.
> - For best results, use a data set that is smaller than 1.5 gb. When your data set exceeds 1.5 gb, AI Builder only uses 1.5 gb of your data to train and predict. Since you can’t control which data exceeding the 1.5 gb limit is not used, you should optimize your data to stay under 1.5 gb.

Form processing works on input documents that meet the following requirements:

- JPG, PNG, or PDF format (text or scanned). Text embedded PDFs are preferable because there is no possibility of error in character extraction and location.
- File size must be less than 4 megabytes (MB)
- For images, dimensions must be between 50x50 and 4200x4200 pixels
- If scanned from paper documents, scans should be high-quality images.
- Must use the Latin alphabet (English characters)
- Printed data (not handwritten)
- Must contain keys and values (e.g.: “company: Contoso” works, “Contoso” without a key label is not supported). 
- Keys can appear above or to the left of the values, but not below or to the right.

 > [!NOTE] 
 > AI Builder does not currently support the following types of form processing input data:
 >
 > - Complex tables (nested tables, merged headers or cells, and so on)
 > - Checkboxes or radio buttons
 > - PDF documents longer than 50 pages

### Next steps

[Create a form processing model](create-form-processing-model.md)
