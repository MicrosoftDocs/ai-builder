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

AI Builder provides two kinds of Power Apps components, depending on the models you want to use:

- Components that use prebuilt AI models that are ready to use right way:
  - [Business card reader (canvas app)](business-card-reader-component-in-powerapps.md)
  - [Business card reader (model-driven app)](business-card-reader-component-model-driven.md)
  - [Text recognizer component (canvas app)](prebuilt-text-recognizer-component-in-powerapps.md)
- Components that use custom AI models that you build and train:
    - [Form processor](form-processor-component-in-powerapps.md)
    - [Object detector](object-detector-component-in-powerapps.md)

The AI Builder components for canvas apps are available in the Power Apps Studio, and appear in the **Insert** tab when you build your canvas app in Power Apps.

> [!div class="mx-imgBorder"]
> ![Power Apps Studio](media/canvas-studio.png "Power Apps Studio")

## Property name changes in AI Builder components for canvas apps

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
- [What are canvas apps?](https://docs.microsoft.com/powerapps/maker/canvas-apps/getting-started)
- [What are model-driven apps?](https://docs.microsoft.com/powerapps/maker/model-driven-apps/model-driven-app-overview)
