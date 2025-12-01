---
title: Use the contract processing prebuilt model in Power Apps (preview)
description: Learn how to use the AI Builder contract processing prebuilt model in Power Apps.
author: phil-cmd
ms.topic: concept-article
ms.custom: 
ms.date: 06/27/2025
ms.author: plarrue
ms.reviewer: angieandrews
---

# Use the contract processing prebuilt model in Power Apps (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

AI Builder contract processing model combined with Power Fx lets you extract key details from a contract document like title, contract ID, list of legal parties, list of jurisdictions, execution date, effective date, expiration date, contract duration, and renewal date, quickly and accurately.

This low-code app simplifies contract document handling.

[!INCLUDE[cc_preview_features_definition](./includes/cc-preview-features-definition.md)]

**Supported document types**: Contract

## Requirements

Learn more about requirements in the [Supported language, format, and file size](prebuilt-contract-processing.md#supported-language-format-and-file-size) section in [Contract processing prebuilt model](prebuilt-contract-processing.md).

## Available fields

|Available fields|Type|
|---------------|-----|
|ContractDuration|Text|
|ContractId|Text|
|EffectiveDate|Text|
|ExecutionDate|Text|
|ExpirationDate|Text|
|RenewalDate|Text|
|Title|Text|

## Available table items

|Available fields|Type|
|---------------|-----|
|Jurisdictions|Text|
|Parties|Text|

## Build your canvas app

1. Sign in to [Power Apps](https://make.powerapps.com/).
1. On the navigation pane to the left, select **+Create.**
1. Select the **Start with a blank canvas** tile.
1. Select the size you would like to use for your canvas app&mdash;either **Responsive**, **Tablet size**, or **Phone size**.
1. In the app editor, from the left navigation pane, select **Data** > **Add data**, and then search **Contract model**.
1. Select **+Insert** > **Add picture**.
1. Select **+Insert** > **Text label**.
1. Select **Label1** and enter a formula like the following example, where `UploadedImage1` is the image container:

    ```power-fx
    'Contract Model'.Predict(UploadedImage1.Image).Fields.Title.Value.Text
    ```

    You can select your desired field from the available field.

    :::image type="content" source="media/use-prebuilt-contract-power-apps/power-fx-contract-select-fields.png" alt-text="Screenshot of all available text fields for a contract document.":::

1. Select **Save**, and then select the **Play** button.

    :::image type="content" source="media/use-prebuilt-contract-power-apps/power-fx-contract-select-fields-title.png" alt-text="Screenshot of a title text field for a contract document.":::

You can also use this formula to retrieve the first item from the result and extract the description of that item as a text string.

```power-fx
First('Contract Model'.Predict(UploadedImage1.Image).Tables.Parties.Rows).Clause.Value.Text
```

:::image type="content" source="media/use-prebuilt-contract-power-apps/power-fx-contract-first-clause-fields.png" alt-text="Screenshot of a first clause field for a contract document.":::

This expression concatenates the text values from the **Clause** field of each row in the prediction results of an image related to a contract document, and separates each value with a comma and a space.

```power-fx
Concat('Contract Model'.Predict(UploadedImage1.Image).Tables.Parties.Rows,Clause.Value.Text, Char(10))
```

:::image type="content" source="media/use-prebuilt-contract-power-apps/power-fx-contract-concatenate-clause-fields.png" alt-text="Screenshot of a first clause field with concatenated text values for a contract document.":::

## Related information

- [Contract processing prebuilt model](prebuilt-contract-processing.md)
- [Power Fx formula reference overview](/power-platform/power-fx/formula-reference-overview)