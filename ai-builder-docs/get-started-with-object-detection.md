---
title: Build your object detection model - AI Builder | Microsoft Docs
description: This topic lays out the first steps you'll perform to build an object detection AI model. 
author: amina196
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 10/20/2020
ms.author: aminab
ms.reviewer: v-dehaas
---

# Build your object detection model

1. Sign in to [Power Apps](https://make.powerapps.com), and then in the left pane, select the down arrow to expand **AI Builder**. Select the **Object Detection** AI model type.

2. Enter a name for your model, and then select **Create**.

## Select the model domain

The first thing you'll do when you create an AI Builder object detection model is to define its domain. The domain optimizes the model for specific use cases. There are three domains:

- **Common objects:** The default value. Use this if your use cases doesn't fit the specific applications below.
- **Objects on retail shelves:** Detects products densely packed on shelves.
- **Brand logo:** Optimized for logo detection.

> [!NOTE]
> Domain specific object detection uses more AI Builder credits than common object detection, and therefore costs more to use. To estimate the impact of using domain specific vs. common object on your organization, use the [AI Builder calculator](https://powerapps.microsoft.com/ai-builder-calculator/).

## Provide object names

Next, provide the names of the items you want to detect. You can provide up to 500 object names per model.

There are two ways to provide object names:

- Enter object names directly in AI Builder.
- Select names from your Common Data Service entity.

In the top action bar, select the input mode you want to use.

> [!IMPORTANT]
> If you change input mode, you lose any existing object names. In other words: if you type object names in AI Builder and then change to selecting from a database, all object names typed and their associated bounding boxes are deleted from your model. This is not recoverable. The same applies if you switch from selecting object names from a database to typing object names.

### Enter names in AI Builder

To provide object names directly in AI Builder, just enter the name in the space where the object is detected in the image. Then press **Enter** or select **Add new object** to continue.

- To edit an object name, select the object name and then make your change.
- To remove an object name, select the trashcan icon.

### Select names from a database

If your data isn't in Common Data Service, see [Prerequisites](build-model.md#prerequisites) for information about how to import data into Common Data Service.

1. Select **Select from database** to see entities in your environment.
2. In the right-side pane, find the entity that contains your object names. Look through the list, or use the search bar, and then select that entity.
3. Locate the field that contains the names of your objects. Select that field, and then select **Select Field** at the bottom of the screen.
4. From the list of strings in your table, select the ones that represent the objects you want to detect. 
5. Select **Next** at the bottom of the screen.

## Upload images

Now let's move on to the image upload step. The pictures you collected ahead of time will now come in handy because you need to upload them to AI Builder.

1. Prepare your images in the storage location where you want to add them from. Currently you can add images from local storage, SharePoint, or Azure Blob Storage.
1. Make sure your images follow the qualitative and quantitative [guidance](collect-images.md).
1. In AI Builder, select **+Add Images**.
1. Select the data source where your images are stored, and then select the images that contain your objects.
1. Confirm the images that appear in AI Builder before you finish uploading them. Deselect any image you want to exclude.

   > [!div class="mx-imgBorder"]
   > ![Select images screen](media/select-images.png "Select images screen")

1. Select **Upload images**.
1. When the upload is complete, select **Close**.

## Tag images

This section explains the tagging process that's a key part of object detection. You draw rectangles around the objects of interest, and then assign a name to the rectangle that you want the model to associate with this object.

1. On the **Tag object in your images** screen, select the first image in your gallery.
1. Draw a rectangle around the object: Press and hold your mouse at the upper-left corner of the object and then drag down to the lower-right corner of the object. The rectangle should fully encompass the object you want your model to recognize.

   > [!div class="mx-imgBorder"]
   > ![Tag images screen](media/tag-images.png "Tag images screen")

1. After you draw a rectangle, you can associate a name to the object from the list of names you already selected.

   > [!div class="mx-imgBorder"]
   > ![Associate name screen](media/tag-image-associate-name.png "Associate name screen")

1. Your tag is created when you see it surrounding an object.

   > [!div class="mx-imgBorder"]
   > ![Tag created screen](media/tag-created.png "Tag created screen")

1. Navigate from image to image, and tag at least 15 images per object name to build a model.
1. After you're done tagging your images, select **Done Tagging**. Your data is saved as you create rectangles.
1. In the grid view, you can view a summary of all the tags you created and which images you created. This lets you know how much more work is needed to move forward.
1. Until you reach the minimum for content quantity, you can't move forward. After you have at least 15 images per object name, you'll be able to select **Next** at the bottom of the screen.

That's it! Congratulations, you've created a training set for object detection.

### Next step

[Train and publish your object detection model](object-detection-train-model.md)

### See also

[Use an object detection model in Power Automate](object-detection-model-in-flow.md) 
