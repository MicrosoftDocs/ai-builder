---
title: Use text recognizer component in Power Apps -  AI Builder | Microsoft Docs
description: Provides information about how to use the text recognizer component in Power Apps
author: alanabrito
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/19/2019
ms.author: alanabrito
ms.reviewer: v-dehaas
---

# Use the text recognizer component in Power Apps

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

Create a canvas app and add the text recognizer AI Builder component to your screen. This component takes a photo or loads an image from the local device, and then processes it to detect and extract text based on the text recognition prebuilt AI model. If it detects text in the image, the component outputs the text and identifies the instances with rectangles in the image.

 > [!NOTE]
 >
 > - Display of PDF files is not included in the initial preview.
 > - Find more information about canvas apps [here](/powerapps/maker/canvas-apps/getting-started).

## Key properties

 - **OriginalImage**: The original image before processing. 
 - **OcrObjects**: The list of detected text lines. For each object, these properties are available of extracted form fields and tables. At component initialization (AI model binding step), the potential fields and tables that can be extracted by the models are populated:
     - **text**: The detected text line.
 - **SelectedText**: The text line selected by the user.
 
## Additional properties

 - **Text**: Text that appears on the button that activates the text recognizer.
 - **ImageDisplayed** (“Show image” in the properties panel): Whether the component displays the image or not. When set to ON, rectangles are displayed around field values detected in the image.
 - **DisplayMode**:
     - **Edit**: Allows user input.
     - **View**: Only displays data.
     - **Disabled** is disabled.
 - **Height**: The height of the component.
 - **Visible**: Whether the component appears or is hidden.
 - **Width**: The width of the component.
 - **X**: The distance between the left edge of the component and the left edge of its parent container or screen.
 - **Y**: The distance between the top edge of the component and the top edge of the parent container or screen.

Additional design properties are available in the Advanced panel.

## Accessibility guidelines
These [guidelines](/powerapps/maker/canvas-apps/controls/control-button) for the Power Apps button control also apply to the text recognizer component.

### Related topics

[Text recognition overview](prebuilt-text-recognition.md)

[Core properties in Power Apps](/powerapps/maker/canvas-apps/controls/properties-core)
