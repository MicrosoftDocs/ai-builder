---
title: Requirements and limitations | Microsoft Docs
description: Describes the requirements and limitations form processing models in AI Builder.
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/10/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Form processing AI model requirements and limitations

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

Form processing works on input documents that meet the following requirements:
-	JPG, PNG, or PDF format (text or scanned). Text embedded PDFs are preferable because there is no possibility of error in character extraction and location.
-	File size must be less than 4 megabytes (MB)
-	For images, dimensions must be between 50x50 and 4200x4200 pixels
-	If scanned from paper documents, scans should be high-quality images.
-	Must use the Latin alphabet (English characters)
-	Printed data (not handwritten)
-	Must contain keys and values (e.g.: “company: Contoso” works, “Contoso” without a key label is not supported). 
-	Keys can appear above or to the left of the values, but not below or to the right.

 > [!NOTE] 
 > AI Builder does not currently support the following types of form processing input data:
 > -	Complex tables (nested tables, merged headers or cells, and so on)
 > -	Checkboxes or radio buttons
 > -	PDF documents longer than 50 pages

### Next steps
[Create a form processing model](create-form-processing-model.md)
