---
title: Use the object detection component in Power Apps - AI Builder | Microsoft Docs
description: Provides information about how to use an object detection component in Power Apps
author: Raj-Virk
ms.topic: conceptual
ms.custom: intro-internal
ms.date: 04/09/2021
ms.author: rajvirk
ms.reviewer: angieandrews
---

# Use the object detection component in Power Apps

The object detection component takes a photo or loads an image file to do an object detection scan. On a mobile device, the user chooses between taking a photo or selecting one already available in the device user interface. When an image is selected, the component automatically scans it to identify objects.

 > [!NOTE]
 > For information about canvas apps, see [What are canvas apps in Power Apps?](/powerapps/maker/canvas-apps/getting-started).

## Prerequisites

To start, you need a trained and published AI Builder object detection model. You bind that model to the component using **AI Model** in the **Properties** panel. When you add it to the screen, the component automatically opens the AI models pane. There you select a model from the models published in that environment.

The component is initialized after an AI model is bound to it.

## Properties

### Key properties

- **ModelId** (**AI model** in the properties panel): AI model information to which the component is bound.

- **OriginalImage**: The original image before processing.

- **GroupedResults**: The details of detected objects. For each object, these properties are available:

  - **TagId** The ID of the object detected.

  - **TagName** The name of the object detected.

  - **ObjectCount** The number of times the object is present on the image.

- **Results**: Contains all the outputs returned by the model.

  - **BoundingBox** The coordinates on the image of the object detected.

  - **Confidence** How confident the model is in its prediction of the object detected.

  - **TagId** The ID of the object detected.

  - **TagName** The name of the object detected.

> [!NOTE]
> Some of these property names changed with the April 2020 updates. If you aren't seeing these properties in your app, you'll have to manually update the property names. More information: [Property name changes in AI Builder components for canvas apps](use-in-powerapps-overview.md#property-name-changes-in-ai-builder-components-for-canvas-apps)

### Additional properties

- **Text**: Text that appears on the button that activates the object detector.

- **ImageDisplayed** (**Show image** in the properties panel): Determines whether the component displays the image.

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
[Use the object detection model in Power Automate](object-detection-model-in-flow.md)  
[Core properties in Power Apps](/powerapps/maker/canvas-apps/controls/properties-core)


[!INCLUDE[footer-include](includes/footer-banner.md)]