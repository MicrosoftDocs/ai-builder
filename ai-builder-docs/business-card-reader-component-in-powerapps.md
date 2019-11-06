---
title: Use the business card reader component in canvas apps in PowerApps - AI Builder | Microsoft Docs
description: Provides information about the properties and information extracted by the business card reader component in a canvas app
author: alanabrito
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 10/03/2019
ms.author: alanab
ms.reviewer: v-dehaas
---

# Use the business card reader component in a canvas app

The business card reader component takes a photo or loads an image from the local device, and then scans it to find a business card. If it detects a business card, it extracts the information it finds.

> [!NOTE]
> - This component isn't supported in Internet Explorer.
> - For information about canvas apps, see [What are canvas apps in PowerApps](/powerapps/maker/canvas-apps/getting-started)?

## Licensing requirements

AI Builder is licensed as an add-on to your PowerApps or Power Automate licenses. For information about license capacity, pricing, and restrictions, see [AI Builder licensing](/ai-builder/administer-licensing).

## Role requirements

Users need to be entitled to the Common Data Service user role to be able to consume the business card reader.

## Key properties

If a business card is detected, the business card reader will try to extract information that it finds based on the following properties:

|Property |Definition  |
|---------|---------|
| **AddressCity**| The city address|
| **AddressCountry**| The country address|
| **AddressPostalCode**| The postal code address|
| **AddressStreet**| The street address|
| **BusinessPhone**| The first phone or fax number|
| **CleanedImage**| The image after processing where the business card appears cropped and enhanced from the original image|
| **CompanyName**| The company name|
| **Department**| The organization department found|
| **Email**| The contact email found in the business card, if any|
| **Fax**| The third phone or fax number|
| **FirstName**| The contact first name|
| **FullAddress**| The contact full address|
| **FullName**| The contact full name|
| **JobTitle**| The contact job title|
| **LastName**| The contact last name|
| **MobilePhone**| The second phone or fax number|
| **OriginalImage**| The original image before processing|
| **Website**| The website|

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
| **X**| The distance between the left edge of the component and the left edge of its parent container (screen if no parent container)|
| **Y**| The distance between the top edge of the component and the top edge of the parent container (screen if no parent container)|

Additional design properties are available in the **Advanced** panel.

## Accessibility guidelines

These [guidelines](/powerapps/maker/canvas-apps/controls/control-button) for the PowerApps button control also apply to the business card reader component.

### Related topic
[Core properties in PowerApps](/powerapps/maker/canvas-apps/controls/properties-core)
