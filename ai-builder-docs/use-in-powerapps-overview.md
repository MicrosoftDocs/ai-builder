---
title: Overview of AI Builder in Power Apps -  AI Builder | Microsoft Docs
description: Provides an overview of the AI Builder components that are available to use with canvas and model-driven apps in Power Apps
author: mustlaz
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/30/2019
ms.author: mustlaz
ms.reviewer: v-dehaas
---

# AI Builder in Power Apps overview

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

AI Builder comes with:
- A ready-to-use business card reader available in canvas as well as in [model-driven apps](/powerapps/maker/model-driven-apps/model-driven-app-overview). 
    - [Business card reader (Canvas)](business-card-reader-component-in-powerapps.md)
    - [Business card reader (Model-driven)](business-card-reader-component-model-driven.md)
- Additional canvas components to leverage your AI Builder form processing or object detection models [canvas apps](/powerapps/maker/canvas-apps/getting-started).
    - [Form processor](form-processor-component-in-powerapps.md)
    - [Object detector](object-detector-component-in-powerapps.md)

> [!div class="mx-imgBorder"]
> ![Canvas studio screen](media/canvas-studio.png "Canvas studio screen")

The canvas components are available in the canvas studio and appear in the **Insert** tab when you build your canvas app in Power Apps.

## Property name changes in AI Builder components in canvas apps

With the [AI Builder component improvements](https://powerapps.microsoft.com/blog/ai-builder-february-update/) released in April 2020, some of the property names in the components have changed. In most cases, your existing apps will be automatically updated to use the new property names without any action required from you. However, in cases where the automatic updates to your app is unsuccessful, here are the property name changes you must make in your apps:


- For the [form processor](form-processor-component-in-powerapps.md) component:

    |Previous property name | New Property name |
    |:-------|:-------|
    |{Control Name}.FormContent.Fields |{Control Name}.Fields |
    |{Control Name}.FormContent.Tables |{Control Name}.Tables |


- For the [text recognizer](prebuilt-text-recognizer-component-in-powerapps) component:

    |Previous property name | New Property name |
    |:-------|:-------|
    |{Control Name}.SelectedText |{Control Name}.Selected.Text |
    |{Control Name}.OcrObjects.text |{Control Name}.Results.Text |

- For the [object detector](object-detector-component-in-powerapps) component:

    |Previous property name | New Property name |
    |:-------|:-------|
    |{Control Name}.VisionObjects.id |{Control Name}.GroupedResults.TagId |
    |{Control Name}.VisionObjects.displayName |{Control Name}.GroupedResults.TagName |
    |{Control Name}.VisionObjects.count |{Control Name}.GroupedResults.ObjectCount |

If  your app uses a **data table** component to display results from the **object detector** component, and you don't see the content after this update, remove the **data table** component from your app, and then add it again. Next, reset the item's property to correctly display the content from the **object detector** component.

### Related content

- [Feature availability by region](availability-region.md)
- [AI Builder in Power Automate](use-in-flow-overview.md)
- [Prerequisites](use-in-flow-prereq.md)
