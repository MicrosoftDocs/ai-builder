---
title: Use the form processor component in Power Apps - AI Builder | Microsoft Docs
description: Provides information about how to use the form processor component in Power Apps
author: JoeFernandezMS
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 12/31/2019
ms.author: jofernan
ms.reviewer: kvivek
---

# Use the form processor component in Power Apps

You can add the AI Builder form processor component to your screen in your canvas apps. This component takes a photo or loads your image. Then it extracts text based on your trained AI model. If it detects a form that the AI model is trained for, the form processor extracts the field values and identifies them by using rectangles.

 > [!NOTE]
 > For more information about creating a new form processing model, see [Get started with Form processing in AI Builder](/learn/modules/get-started-with-form-processing/)
 >
 > For more information about canvas apps, see [What are canvas apps in Power Apps?](/powerapps/maker/canvas-apps/getting-started).

## Prerequisites

This component requires a published AI Builder form-processing model. Then that model must be bound to the component by using the AI model property in the properties panel.

When you add the component to the screen, it automatically opens the AI models pane. There, you select a model that has been published in your environment. The component is initialized after an AI model is bound to it.

## Key properties

- **ModelId** ("AI model" in the properties panel): AI model information to which the component is bound.

- **OriginalImage**: The original image before processing.

- **Fields**: The extracted fields by the AI model.

- **Tables**: The extracted tables by the AI model. 

- **Results**: Contains all the outputs returned by the AI Model along with advanced properties. For each value returned by the AI model, you can access:

  - **BoundingBox** The coordinates on the form for the extracted field.

  - **Confidence** How confident the model is in its prediction of the extracted text.

  - **PageNumber** The number of the page where the extracted text is located.

  - **Value** The extracted text value.

    > [!NOTE]
    > Some of these property names changed with the April 2020 updates. If you aren't seeing these properties in your app, you'll have to manually update the property names. More information: [Property name changes in AI Builder components for canvas apps](use-in-powerapps-overview.md#property-name-changes-in-ai-builder-components-for-canvas-apps)

## Additional properties

- **Text**: Text that appears on the button that activates the form processor.

- **ImageDisplayed** (**Show image** in the properties panel): Determines whether the component displays the image. When set to **On**, rectangles are displayed around field values detected in the image.

  Three different colors can be used to draw the rectangle depending on the confidence level:
  - **Red**: Confidence level is between 0 percent and 39 percent.
  - **Orange**: Confidence level is between 40 percent and 59 percent.
  - **Blue**: Confidence level is between 60 percent and 100 percent.

- **ShowConfidence** (**Show confidence** in the properties panel): Determines whether the component displays confidence levels along with the rectangles in the image.

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
These [guidelines](/powerapps/maker/canvas-apps/controls/control-button) for the Power Apps button control also apply to the form processor component.

### See also

[Overview of the object detection model](object-detection-overview.md)  
[Core properties in Power Apps](/powerapps/maker/canvas-apps/controls/properties-core)


[!INCLUDE[footer-include](includes/footer-banner.md)]