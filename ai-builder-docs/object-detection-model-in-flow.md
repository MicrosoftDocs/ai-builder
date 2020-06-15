---
title: Use object detection model in Power Automate -  AI Builder | Microsoft Docs
description: Provides information about how to use an object detection model in Power Automate
author: Dean-Haas

ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/12/2019
ms.author: v-dehaas
ms.reviewer: v-dehaas
---

# Use object detection model in Power Automate


> [!IMPORTANT]
 > To use AI Builder models in Power Automate, you have to create the flow inside a solution. The steps below won't work if you don't follow these instructions first: [Create a flow in a solution](/flow/create-flow-solution).

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, select **+Add an input**, select **File** as the input type, and set as input title **My Image**.
1.	Select **+ New step**, search for **AI Builder** in the Search for filters and actions box, and then select **Detect and count objects in images** in the list of actions.
1.	Select the object detection model you want to use, and in the **Image** field, specify **My Image** from the trigger:

    > [!div class="mx-imgBorder"]
    > ![Specify my image](media/flow-my-image-2.png "Specify my image")

1.	To retrieve the name of the detected object or objects on the image, use the **Detected object name** field.

Congratulations! You have created a flow that uses an object detection AI Builder model. Select **Save** on the top right, and then select **Test** to try out your flow.


## Example object detection flow

The following example shows the creation of a flow that is triggered by an image. This flow counts the number of green tea bottles in the image.

> [!div class="mx-imgBorder"]
> ![Green tea object detection flow example](media/green-tea-example-2.png "Example of an object detection flow")

To learn more about all the triggers and actions you can use, see [Power Automate documentation](/flow/getting-started).


## Parameters
### Input
|Name |Required |Type |Description |Values |
|---------|---------|---------|---------|---------|
|**AI Model** |Yes |model |Object detection model to use for analysis|Trained and published object detection models |
|**Image** |Yes |file |Image to process| |


### Output
|Name |Type |Description |Values |
|---------|---------|---------|---------|
|**Detected object name** |string |The detected object name|Among the tags defined at model creation |
|**Detected object ID** |string |The detected object ID| |
|**Confidence score** |float |How confident the model is in its prediction |Value in the range of 0 to 1. Values close to 1 indicate greater confidence that the extracted value is accurate |
|**Coordinates height** |float |Coordinates left of the object| |
|**Coordinates left** |float |Coordinates left of the object| |
|**Coordinates top** |float |Coordinates top of the object| |
|**Coordinates width** |float |Coordinates width of the object| |


## Related topic

[Object detection overview](object-detection-overview.md)
