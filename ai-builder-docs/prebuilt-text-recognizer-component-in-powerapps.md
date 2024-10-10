---
title: Use the text recognizer component in Power Apps - AI Builder
description: Learn how to use the text recognizer component in Power Apps.
author: Phil-cmd
contributors:
  - Phil-cmd
  - v-aandrews
ms.topic: conceptual
ms.custom: 
ms.date: 06/25/2024
ms.author: plarrue
ms.reviewer: angieandrews
---

# Use the text recognizer component in Power Apps

Create a canvas app and add the text recognizer AI Builder component to your screen. This component takes a photo or loads an image from the local device, and then processes it to detect and extract text based on the text recognition prebuilt model. If it detects text in the image, the component outputs the text and identifies the instances by showing a rectangle for each instance in the image.

 > [!NOTE]
 > For information about canvas apps, see [What are canvas apps in Power Apps?](/powerapps/maker/canvas-apps/getting-started)

## Key properties

- **OriginalImage**: The original image before processing.

- **Results**: The list of detected text lines. For each object, these properties of extracted form fields and tables are available. At component initialization (AI model binding step), the potential fields and tables that can be extracted by the models are populated. These include:

  - **BoundingBox**: The coordinates for the detected text line.

  - **PageNumber**: The number of the page where the detected text line is located.

  - **Text**: The detected text line.

- **Selected**: The detected box selected by the user on the control.

  - **BoundingBox**: The coordinates for the detected text line selected by the user.

  - **PageNumber**: The number of the page where the detected text line selected by the user is located.

  - **Text**: The detected text line selected by the user.

> [!NOTE]
> Some of these property names changed with the April 2020 updates. If you aren't seeing these properties in your app, you'll have to manually update the property names. More information: [Property name changes in AI Builder components for canvas apps](use-in-powerapps-overview.md#property-name-changes-in-ai-builder-components-for-canvas-apps)

## Additional properties

- **Text**: Text that appears on the button that activates the text recognizer.

- **ImageDisplayed** (**Show image** in the properties panel): Determines whether the component displays the image. When set to **On**, rectangles are displayed around column values detected in the image.

- **DisplayMode**:

  - **Edit**: Allows user input.

  - **View**: Only displays data.

  - **Disabled** is disabled.

- **Height**: The height of the component.

- **Visible**: Whether the component appears or is hidden.

- **Width**: The width of the component.

- **X**: The distance between the left edge of the component and the left edge of its parent container or screen.

- **Y**: The distance between the top edge of the component and the top edge of the parent container or screen.

Additional design properties are available in the **Advanced** panel.

## Accessibility guidelines

These [guidelines](/powerapps/maker/canvas-apps/controls/control-button) for the Power Apps button control also apply to the text recognizer component.

## Use the formula bar to retrieve the text value from the selected item in the TextRecognizer control

Here are some examples.

This expression retrieves the full text recognized by TextRecognizer1.

```power-fx
TextRecognizer1.FullText
```

This expression retrieves the text value of the selected item from the `TextRecognizer1`.

```power-fx
TextRecognizer1.Selected.Text
```

This expression concatenates the values from the 'Text' property of the 'TextRecognizer1' control with a comma and space separator.

```power-fx
Concat(TextRecognizer1.Results,Text,", ")
```

## Related information

- [Text recognition model](prebuilt-text-recognition.md)  
- [Core properties in Power Apps](/powerapps/maker/canvas-apps/controls/properties-core)
- [Training: Recognize text with AI Builder (module)](/training/modules/get-started-with-ai-builder-text-recognition/) 

[!INCLUDE[footer-include](includes/footer-banner.md)]
