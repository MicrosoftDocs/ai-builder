---
title: Use the business card reader component in PowerApps | Microsoft Docs
description: Provides information about how to use the business card reader component in PowerApps 
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/10/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---

# Use the business card reader component in PowerApps 

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

Business card reader component

## Overview

Takes a photo or loads an image from the local device and then scans it to find a business card. If a business card is detected, it extracts contact information it finds. 

## Properties
### Key properties
If a business card is detected, the business card reader will try to extract and expose the below information:
- **CleanedImage**: Output property that contains the image after processing where the business card appears cropped and enhanced from the original image.
- **CompanyName**: Output property that contains the company name in the business card if any found.
- **Department**: Output property that contains the organization department found in the business card if any found.
- **Email**: Output property that contains the contact email found in the business card if any.
- **FirstName**: Output property that contains the contact first name in the business card if any found.
- **FullAddress**: Output property that contains the contact full address in the business card if any found.
- **FullName**: Output property that contains the contact full name in the business card if any found.
- **JobTitle**: Output property that contains the contact job title in the business card if any found.
- **LastName**: Output property that contains the contact last name in the business card if any found.
- **OriginalImage**: Output property that contains the original image before processing.
- **Phone1**: Output property that contains the first phone or fax number detected in the business card if any found.
- **Phone2**: Output property that contains the second phone or fax number detected in the business card if any found.
- **Phone3**: Output property that contains the third phone or fax number detected in the business card if any found.
- **Website**: Output property that contains the website detected in the business card if any found.


### Additional properties
- **Text**: Text that appears on the button that activates the business card reader.
- **ImageDisplayed** (“Show image” in the properties panel): Whether the component displays the image or not.
- **DisplayMode**:
    - **Edit**: Allows user input
    - **View**: Only displays data 
    - **Disabled** is disabled.
- **Height**: The height of the component.
- **Visible**: Whether the component appears or is hidden.
- **Width**: The width of the component.
- **X**: The distance between the left edge of the component and the left edge of its parent container (screen if no parent container).
- **Y**: The distance between the top edge of the component and the top edge of the parent container (screen if no parent container).

Additional design properties are available in the Advanced panel.

## Accessibility guidelines
These guidelines for the PowerApps [Button control](/powerapps/maker/canvas-apps/controls/control-button) also apply to the form processor component.



### Related topics
[AI Builder Release Notes](/power-platform-release-notes/october19/ai-builder)<br/>
[Core properties in PowerApps](/powerapps/maker/canvas-apps/controls/properties-core)
