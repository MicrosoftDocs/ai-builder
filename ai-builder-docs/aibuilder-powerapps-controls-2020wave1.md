---
title: Power Apps Canvas AI Builder controls 2020 release wave 1 update -  AI Builder | Microsoft Docs
description: Updated on AI Builder Power Apps canvas controls on the 2020 release wave 1 update
author: jofernan
manager: kvivek
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 03/06/2020
ms.author: jofernan
ms.reviewer: v-dehaas
---

# Power Apps Canvas AI Builder controls 2020 release wave 1 update

With the [announced improvements](https://powerapps.microsoft.com/en-us/blog/ai-builder-february-update/) to the AI Builder controls in the Power Apps canvas studio, some of the property names will change. Your existing apps will automatically update to use the new property names with no action required. If the automatic update is unsuccessful for some reason, here are the changes that would need to be made to your app:

For the **Form Processor** control:

|Previous property name | New Property name |
|:-------|:-------:|
|{Control Name}.FormContent.Fields |{Control Name}.Fields |
|{Control Name}.FormContent.Tables |{Control Name}.Tables |

For the **Text Recognizer** control:

|Previous property name | New Property name |
|:-------|:-------:|
|{Control Name}.SelectedText |{Control Name}.Selected.Text |
|{Control Name}.OcrObjects.text |{Control Name}.Results.Text |

For the **Object Detector** control:

|Previous property name | New Property name |
|:-------|:-------:|
|{Control Name}.VisionObjects.id |{Control Name}.GroupedResults.TagId |
|{Control Name}.VisionObjects.displayName |{Control Name}.GroupedResults.TagName |
|{Control Name}.VisionObjects.count |{Control Name}.GroupedResults.ObjectCount |

If  your app uses a **Data table** control to display results from the **Object Detector** control, and you don’t see the content after this update,  remove the **Data table** control from your app, and then add it again.  Then, reset the Item’s property to correctly display the content from the Object Detector control. 
