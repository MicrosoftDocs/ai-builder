---
title: Use the health insurance card processing prebuilt model in Power Apps
description: Learn how to use the AI Builder health insurance card prebuilt model in Power Apps.
author: phil-cmd
ms.topic: conceptual
ms.custom: 
ms.date: 09/05/2025
ms.author: plarrue
ms.reviewer: angieandrews
---

# Use the health insurance card processing prebuilt model in Power Apps

AI Builder health insurance card model combined with Power Fx lets you extract key details from health insurance card like Insurer, Member, IdNumber, Group Number, Prescription Info, Effective Date, Medicare or Medicaid Info, and more, quickly and accurately. This low-code app simplifies health insurance card handling.

**Supported document types**: US health insurance card

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

1. Sign in to [Power Apps](https://make.powerapps.com/).
1. On the navigation pane to the left, select **+Create**.
1. Select the **Start with a blank canvas** tile.
1. Name your app, and select either **Responsive**, **Tablet size**, or **Phone size**.
1. In the app editor, from the navigation pane on the left, select **Data** > **Add data**, and then search **Health insurance card processing model**.
1. Select **+Insert** > **Add picture**.
1. Select **+Insert** > **Text label**.
1. Select **Label1** and enter a formula like the following example, where `UploadedImage1` is the image container:

    ```power-fx
    'Health insurance card Model'.Predict(UploadedImage1.Image).Fields.Insurer.Value.Text
    ```
    You can select your desired field from the available field.

    :::image type="content" source="media/use-prebuilt-health-insurance-card-power-apps/power-fx-select-fields-health-insurance-card.png" alt-text="Screenshot of all available text fields for a health insurance card.":::

1. Select **Save**, and then select the play button.

    :::image type="content" source="media/use-prebuilt-health-insurance-card-power-apps/power-fx-select-fields-health-insurance-save.png" alt-text="Screenshot of an insurer text field for a health insurance card.":::

You can also use this formula to retrieve the first item from the result and extract the name of that item as a text string.

```power-fx
First('Health insurance card Model'.Predict(UploadedImage1.Image).Tables.Member.Rows).Name.Value.Text
```

:::image type="content" source="media/use-prebuilt-health-insurance-card-power-apps/power-fx-first-row-table-name-fields-health-insurance.png" alt-text="Screenshot of a first member field for a health insurance card.":::

This expression concatenates the text values from the CoPay Benefits field of each row in the prediction results of an image related to a health insurance card, and separates each value.

```power-fx
Concat(
    'Health insurance card Model'.Predict(UploadedImage1.Image).Tables.Copays.Rows,Benefit.Value.Text & ": " & Amount.Value.Text & Char(10)
)
```

:::image type="content" source="media/use-prebuilt-health-insurance-card-power-apps/power-fx-concat-table-name-fields-copays-health-insurance.png" alt-text="Screenshot of Copays benefits fields amount and benefit for a health insurance card.":::

## Related information

- [Health insurance card processing prebuilt model](prebuilt-health-insurance-card.md)
- [Power Fx formula reference overview](/power-platform/power-fx/formula-reference-overview)