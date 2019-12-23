---
title: Use an object detection component in Power Apps -  AI Builder | Microsoft Docs
description: Provides information about how to use an object detection component in Power Apps
author: amina196
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/06/2019
ms.author: aminab
ms.reviewer: v-dehaas
---

# Use an object detection component in Power Apps

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

Use the object detection component to take a photo or choose an image file to perform an object detection scan. On a mobile device, the user is presented with the device's interface to choose between taking a photo or selecting one already available. When an image is selected, the component automatically performs a scan to identify objects in the image.

 > [!NOTE]
 >
 > - Find more information about canvas apps in the [What are canvas apps in PowerApps?](/powerapps/maker/canvas-apps/getting-started).

## Prerequisites

You need a trained and published AI Builder object detection model to get started. Then you need to bind that model to the component using the AI model property in the **Properties** panel. When you add it to the screen, the component will automatically open the AI models pane so you can select a model from those that are published in that environment.

The component is initialized once an AI model is bound to it.

## Properties

### Key properties

 - **ModelId** (“AI model” in the properties panel): AI model information to which the component is bound.
 - **OriginalImage**: The original image before processing.
 - **VisionObjects**: The details of detected objects. For each object, these properties are available:
    - **id** (populated at AI model binding)
    - **displayName** (populated at AI model binding)
    - **count** (populated after a detection)

### Additional properties
 - **Text**: Text that appears on the button that activates the object detector.
 - **ImageDisplayed** (“Show image” in the properties panel): Whether the component displays the image or not.
 - **DisplayMode**:
    - **Edit**: Allows user input.
    - **View**: Only displays data. 
    - **Disabled** is disabled.
 - **Height**: The height of the component.
 - **Visible**: Whether the component appears or is hidden.
 - **Width**: The width of the component.
 - **X**: The distance between the left edge of the component and the left edge of its parent container (screen if no parent container).
 - **Y**: The distance between the top edge of the component and the top edge of the parent container (screen if no parent container).

Additional design properties are available in the Advanced panel.

## Accessibility guidelines
These [guidelines](/powerapps/maker/canvas-apps/controls/control-button) for the Power Apps button control also apply to the form processor component.

### Related topics
[Object detection overview](object-detection-overview.md)

[Use an object detection model in Power Automate](object-detection-model-in-flow.md)

[Core properties in Power Apps](/powerapps/maker/canvas-apps/controls/properties-core)
