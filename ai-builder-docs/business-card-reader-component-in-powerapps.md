---
title: Use the business card reader component in PowerApps -  AI Builder | Microsoft Docs
description: Provides information about the properties and information extracted by the business card reader component in PowerApps 
author: Dean-Haas
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 06/07/2019
ms.author: v-dehaas
ms.reviewer: kvivek
---


# Use the business card reader component in PowerApps 

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

 > [!NOTE]
 >
 > - This component is not supported in Internet Explorer.
 > - Import/export of PowerApps with Business Card Reader control is not currently supported.
 > - Find more information about [canvas apps](/powerapps/maker/canvas-apps/getting-started).


The business card reader component takes a photo or loads an image from the local device, and then scans it to find a business card. If it detects a business card, it extracts the information it finds.

## Key properties

If a business card is detected, the business card reader will try to extract the following information:

 - **CleanedImage**: The image after processing where the business card appears cropped and enhanced from the original image.
 - **CompanyName**: The company name in the business card, if found.
 - **Department**: The organization department found in the business card, if found.
 - **Email**: The contact email found in the business card, if any.
 - **FirstName**: The contact first name in the business card, if found.
 - **FullAddress**: The contact full address in the business card, if found.
 - **FullName**: The contact full name in the business card, if found.
 - **JobTitle**: The contact job title in the business card, if found.
 - **LastName**: The contact last name in the business card, if found.
 - **OriginalImage**: The original image before processing.
 - **Phone1**: The first phone or fax number detected in the business card, if found.
 - **Phone2**: The second phone or fax number detected in the business card, if found.
 - **Phone3**: The third phone or fax number detected in the business card, if found.
 - **Website**: The website detected in the business card, if found.


## Additional properties

 - **Text**: Text that appears on the button that activates the business card reader.
 - **ImageDisplayed** (“Show image” in the properties panel): Whether the component displays the image.
 - **DisplayMode**:
    - **Edit**: Allows user input.
    - **View**: Only displays data. 
    - **Disabled**: Is disabled.
 - **Height**: The height of the component.
 - **Visible**: Whether the component appears or is hidden.
 - **Width**: The width of the component.
 - **X**: The distance between the left edge of the component and the left edge of its parent container (screen if no parent container).
 - **Y**: The distance between the top edge of the component and the top edge of the parent container (screen if no parent container).

Additional design properties are available in the **Advanced** panel.



## Accessibility guidelines
These [guidelines](/powerapps/maker/canvas-apps/controls/control-button) for the PowerApps button control also apply to the form processor component.



### Related topic
[Core properties in PowerApps](/powerapps/maker/canvas-apps/controls/properties-core)
