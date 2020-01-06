---
title: Use the business card reader component in canvas apps in Power Apps - AI Builder | Microsoft Docs
description: Provides information about the properties, and information extracted by the business card reader component in a canvas app.
author: alanabrito
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/27/2019
ms.author: alanab
ms.reviewer: v-dehaas
---

# Use the business card reader component in a canvas app

Use the AI Builder business card reader component to detect business cards, and extract their information. You can take photos directly in the component, or load images that you've taken. Data is identified and extracted using the properties listed below.

For information about canvas apps, see [What are canvas apps in Power Apps?](/powerapps/maker/canvas-apps/getting-started)

## Licensing requirements

AI Builder is licensed as an add-on to your Power Apps or Power Automate licenses. For information about license capacity, pricing, and restrictions, see [AI Builder licensing](/ai-builder/administer-licensing).

## Role requirements

You need the Common Data Service user role to use the business card reader.

## Key properties

If a business card is detected, the business card reader will extract information that it finds based on the following properties:

|Property |Definition  |
|---------|---------|
| **AddressCity**| City |
| **AddressCountry**| Country |
| **AddressPostalCode**| Postal code |
| **AddressStreet**| Street address|
| **BusinessPhone**| The first phone or fax number|
| **CleanedImage**| The image after processing where the business card appears cropped and enhanced from the original image|
| **CompanyName**| Company name|
| **Department**| Organization department |
| **Email**| Contact email address, if any|
| **Fax**| The third phone or fax number|
| **FirstName**| Contact first name|
| **FullAddress**| Contact full address|
| **FullName**| Contact full name|
| **JobTitle**| Contact job title|
| **LastName**| Contact last name|
| **MobilePhone**| Second phone or fax number|
| **OriginalImage**| The original image before processing|
| **Website**| Website|

## Additional properties

|Name |Definition  |
|---------|---------|
| **Text**| Text that appears on the button that activates the business card reader|
| **ImageDisplayed** (“Show image” in the properties panel)| Whether the component displays the image|
|**DisplayMode (Edit)**| Allows user input|
|**DisplayMode (View)**| Only displays data|
|**DisplayMode (Disabled)**| Is disabled|
| **Height**| The height of the component|
| **Visible**| Whether the component appears or is hidden|
| **Width**| The width of the component|
| **X**| The distance between the left edge of the component and the left edge of its parent container or screen|
| **Y**| The distance between the top edge of the component and the top edge of the parent container or screen |

Additional design properties are available in the **Advanced** panel.

## Accessibility guidelines

These [guidelines](/powerapps/maker/canvas-apps/controls/control-button) for the Power Apps button control also apply to the business card reader component.

### Related topic
[Core properties in Power Apps](/powerapps/maker/canvas-apps/controls/properties-core)
