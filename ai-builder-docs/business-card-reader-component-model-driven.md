---
title: Use the business card reader component in PowerApps - AI Builder | Microsoft Docs
description: Provides information about how to setup and use the AI Builder business card reader in model-driven apps 
author: mustlaz
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/30/2019
ms.author: mustlaz
ms.reviewer: v-dehaas
---


# Use the business card reader in model-driven applications

 The business card reader takes a photo or loads an image from the local device, and then scans it to find a business card. If it detects a business card, it extracts the information it finds.

## Licensing requirements

AI Builder is licensed as an add-on to your PowerApps or Flow licenses. For information about license capacity, pricing, and restrictions, see [AI Builder licensing](/ai-builder/administer-licensing).

## Role requirements

Users need to be entitled to the **common data service user** role to be able to consume the business card reader.

## Add the business card reader

Add the business card reader to an existing contact or lead form in the form editor, and through binding to a placeholder**SingleLine.Text** or **Multiple** field.

1. Select the placeholder field, and then open the properties dialog.
2. Select the **Controls** tab.
3. Select **Add Control...**.
4. Select **AI Builder Business Card Control**.

> [!div class="mx-imgBorder"]
> ![Form editor add control screen](media/Form-editor-add-control.PNG "Form editor add control screen")

> [!NOTE]
>
> - The **Company Name** property cannot be bound to a field of type **Lookup.Customer**. The only supported type is **SingleLine.Text**.
> - Find more information about [adding components to model-driven apps](/powerapps/developer/component-framework/add-custom-controls-to-a-field-or-entity).

## Configure the business card reader

After having selected in which platform (Web, Phone, Tablet) the business card reader should display, you can then bind the component properties that you need.

> [!div class="mx-imgBorder"]
> ![Form editor binding properties screen](media/Form-editor-binding-properties.PNG "Form editor binding properties screen")

## Key properties

If a business card is detected, the business card reader will try to extract information based on the following properties:

|Property |Definition  |Type  |
|---------|---------|---------|
 |**Full Name**| The contact full name| **SingleLine.Text**|
 |**First Name**| The contact first name|**SingleLine.Text**|
 |**Last Name**| The contact last name|**SingleLine.Text**|
 |**Job Title**| The contact job title|**SingleLine.Text**|
 |**Mobile Phone**| The mobile phone number detected| **SingleLine.Phone**|
 |**Business Phone**| The business phone number detected| **SingleLine.Phone**|
 |**Fax**| The fax number detected| **SingleLine.Phone**|
 |**Email**| The contact email found in the business card, if any. **SingleLine.Email**|
 |**Company Name**| The company name|**SingleLine.Text**|
 |**Website**| The website detected| **SingleLine.URL**|
 |**Department**| The organization department found|**SingleLine.Text**|
 |**Full Address**| The contact full address|**SingleLine.TextArea, Multiple**|
 |**Address Street**| The street address detected|**SingleLine.Text**|
 |**Address City**| The city address detected|**SingleLine.Text**|
 |**Address PostalCode**| The postal code address detected|**SingleLine.Text**|
 |**Address Country**| The country address detected|**SingleLine.Text**|
 |**Cleaned Image**| The image after processing where the business card appears cropped and enhanced from the original image.|**Multiple**|

## Customization properties

The following properties are available for advanced customization:

|Property |Definition  |
|---------|---------|
 |**Default Image**| To replace the default placeholder image with a different one. The image (jpeg or png) should be encoded with base-64 digits.
 |**Text**| To override the default button text.
