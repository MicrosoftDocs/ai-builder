---
title: Use the health insurance card processing prebuilt model in Power Apps
description: Learn how to use the AI Builder health insurance card prebuilt model in Power Apps.
author: phil-cmd
ms.topic: conceptual
ms.custom: 
ms.date: 08/08/2025
ms.author: plarrue
ms.reviewer: angieandrews
---

# Use the health insurance card processing prebuilt model in Power Apps

AI Builder health insurance card model combined with Power Fx lets you extract key details from health insurance card like Insurer, Member, IdNumber, Group Number, Prescription Info, Effective Date, Medicare or Medicaid Info, and more, quickly and accurately. This low-code app simplifies health insurance card handling.

Supported document types: US health insurance card

## Requirements

Learn about requirements in [Supported language, format, and size](prebuilt-health-insurance-card.md#supported-language-format-and-size).

## Available fields

|Available fields|	Type|
|-----------------|-----|
|Insurer|Text|
|Member|Text|
|Dependents|Text|
|IdNumber|Text|
|GroupNumber|Text|
|PrescriptionInfo|Text|
|Pbm|Text|
|EffectiveDate|Text|
|Copays|Text|
|Payer|Text|
|Plan|Text|
|MedicareMedicaidInfo|Text|
|MedicareMedicaidInfo.PartAEffectiveDate|Date|
|MedicareMedicaidInfo.PartBEffectiveDate	|Date|

## Build your canvas app

- Sign in to [Power Apps](https://make.powerapps.com/).

- On the left-side navigation pane, select **+Create**.

- Select the **Start with a blank canvas** tile.

- Name your app, select either **Responsive**, **Tablet size**, or **Phone size**.

- In the app editor, from the left navigation pane, select **Data** > **Add data**, and then search **Health insurance card processing model**.

- Select +Insert > Add picture.

- Select +Insert > Text label.

- Select Label1 and enter a formula like the following example, where UploadedImage1 is the image container:

 ```power-fx
'Health insurance card Model'.Predict(UploadedImage1.Image).Fields.Insurer.Value.Text
```
You can select your desired field from the available field.

:::image type="content" source="media/use-prebuilt-health-insurance-card-power-apps/powerfx-select-fields-health-insurance-card.png" alt-text="Screenshot of all available text fields for a health insurance card.":::

-  Select Save, and then select the play button.

    :::image type="content" source="media/use-prebuilt-health-insurance-card-power-apps/powerfx-select-fields-health-insurance-save.png" alt-text="Screenshot of an insurer text field for a health insurance card.":::

You can also use this formula to retrieve the first item from the result and extract the name of that item as a text string.

```power-fx
First('Health insurance card Model'.Predict(UploadedImage1.Image).Tables.Member.Rows).Name.Value.Text
```

:::image type="content" source="media/use-prebuilt-health-insurance-card-power-apps/powerfx-first-row-table-name-fields-health-insurance.png" alt-text="Screenshot of a first member field for a health insurance card.":::

This expression concatenates the text values from the CoPay Benefits field of each row in the prediction results of an image related to a health insurance card, and separates each value.

```power-fx
Concat(
    'Health insurance card Model'.Predict(UploadedImage1.Image).Tables.Copays.Rows,Benefit.Value.Text & ": " & Amount.Value.Text & Char(10)
)
```

:::image type="content" source="media/use-prebuilt-health-insurance-card-power-apps/powerfx-concat-table-name-fields-copays-health-insurance.png" alt-text="Screenshot of Copays benefits fields amount and benefit for a health insurance card.":::

## Related information

- [Health insurance card processing prebuilt model](prebuilt-health-insurance-card.md)
- [Power Fx formula reference overview](/power-platform/power-fx/formula-reference-overview)