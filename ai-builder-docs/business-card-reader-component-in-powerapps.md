---
title: Use the business card reader component in canvas apps in Power Apps - AI Builder
description: Learn about the properties and information extracted by the business card reader component in a canvas app.
author: joefernandezms
contributors:
  - joefernandezms
  - phil-cmd
  - v-angie
ms.topic: conceptual
ms.custom: 
ms.date: 06/18/2024
ms.author: jofernan
ms.reviewer: angieandrews
---

# Use the business card reader component in a canvas app in Power Apps

Use the AI Builder business card reader component to detect business cards and extract their information. You can take photos directly in the component or load images that you took. Data is extracted and identified by using the properties listed in the [Key properties](#key-properties) section in this article.

To learn more about canvas apps, go to [What are canvas apps in Power Apps?](/powerapps/maker/canvas-apps/getting-started)

## Licensing requirements

AI Builder is licensed as an add-on to your Power Apps or Power Automate licenses. To learn more about license capacity, pricing, and restrictions, go to [AI Builder licensing](./administer-licensing.md).

## Role requirements

You need the Basic User role to use the business card reader.

## Key properties

If a business card is detected, the business card reader extracts information that it finds based on the following properties.

|Property |Definition  |
|---------|---------|
| **AddressCity**| City |
| **AddressCountry**| Country |
| **AddressPostalCode**| Postal code |
| **AddressPostOfficeBox**| Post office box |
| **AddressState**| State address |
| **AddressStreet**| Street address|
| **BusinessPhone**| The first phone or fax number|
| **CleanedImage** (deprecated)| The image after processing, where the business card appears cropped and enhanced from the original image|
| **CompanyName**| Company name|
| **Department**| Organization department |
| **Email**| The contact's email address, if any|
| **Fax**| The third phone or fax number|
| **FirstName**| The contact's first name|
| **FullAddress**| The contact's full address|
| **FullName**| The contact's full name|
| **JobTitle**| The contact's job title|
| **LastName**| The contact's last name|
| **MobilePhone**| Second phone or fax number|
| **OriginalImage**| The original image, before processing|
| **Website**| Website|

## Additional properties

|Name |Definition  |
|---------|---------|
| **Text**| Text that appears on the button that activates the business card reader|
| **ImageDisplayed** (**Show image** in the properties panel)| Whether the component displays the image|
|**DisplayMode (Edit)**| Allows user input|
|**DisplayMode (View)**| Only displays data|
|**DisplayMode (Disabled)**| Is disabled|
| **Height**| The height of the component|
| **Visible**| Whether the component appears or is hidden|
| **Width**| The width of the component|
| **X**| The distance between the left edge of the component and the left edge of its parent container or screen|
| **Y**| The distance between the top edge of the component and the top edge of the parent container or screen |

More design properties are available in the **Advanced** panel.

## Accessibility guidelines

The guidelines in [Button control in Power Apps](/power-apps/maker/canvas-apps/controls/control-button) also apply to the business card reader component.

### Use the BusinessCardReader control

Use the formula bar to retrieve the text value from the selected item in the BusinessCardReader control.

Here are some examples:

This expression retrieves the value of the 'FullName' property from the 'BusinessCardReader1' variable.

`BusinessCardReader1.FullName`

This expression concatenates the CompanyName, FullName, JobTitle, FullAddress, and Email properties of the BusinessCardReader1 variable, separated by a special character represented by the Char(Float(10)) function.

`BusinessCardReader1.CompanyName & Char(10) & BusinessCardReader1.FullName & Char(10) & BusinessCardReader1.JobTitle & Char(10) & BusinessCardReader1.FullAddress & Char(10) &
BusinessCardReader1.Email`

### See also

- [Core properties in Power Apps](/powerapps/maker/canvas-apps/controls/properties-core)
- [Training: Extract information from business cards with AI Builder (module)](/training/modules/get-started-with-ai-business-card-reader/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
