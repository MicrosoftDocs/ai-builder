---
title: Prompt tokens
description: Learn about prompt tokens and licensing in AI Builder.
author: antrod
contributors:
  - antrod
  - v-aangie
ms.topic: how-to
ms.collection: 
    - bap-ai-copilot
ms.date: 03/04/2025
ms.update-cycle: 180-days
ms.author: antrod
ms.reviewer: angieandrews
---

# Prompt tokens

A prompt model doesn't operate on words or characters as units of text, but instead uses something in-between: tokens.
- A token can be a single character, fraction of a word, or an entire word.
    - Many common words are represented by a single token.
    - Less common words are represented by multiple tokens.
- When images or documents are included in a prompt instruction, they're translated into tokens following [conversion rules](#how-image-or-documents-are-translated-into-tokens).

## Tokens consumed by a prompt

When you create a prompt instruction and run it, the following happens:

- The prompt instruction gets deconstructed into a sequence of tokens called the *input tokens*.
- The model generates an answer as a sequence of tokens called the *output tokens*.

The input tokens are a sum of the tokens coming from:

- The system metaprompt from Microsoft. This system prompt isn't visible and is essential for the safety of your prompt response. It represents a few hundred tokens.
- The prompt instruction.
- If any, the input values.
- If any, the knowledge data retrieved.

The output tokens are the tokens coming from the model response.

## How tokens impact licensing

The combination of input tokens, output tokens, and the model version allows you to compute the cost of your prompt run. Learn more in the **AI Builder rate card** section in the [Microsoft Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130) downloadable PDF file.

When you build solutions that include prompts, it can be important for you to assess the average cost of a prompt. The two possibilities to achieve that goal are explained in the following sections.

### Credits count in prompt builder

When you test a prompt in AI Hub within the Power Automate or Power Apps portal, you're able to display the credits consumed by your prompt. Testing is free, so it's a projected value.

:::image type="content" source="media/licensing-prompt-tokens/credits-prompt-builder.png" alt-text="Screenshot of credits displayed in prompt builder.":::

### Token count from a Power Automate flow

When you call a prompt action in a flow, you can get the associated input and tokens using formulas.

#### Input tokens

```
outputs('Run_a_prompt')?['body/responsev2/predictionOutput/promptTokens']
```

#### Output tokens

```
outputs('Run_a_prompt')?['body/responsev2/predictionOutput/completionTokens']
```

:::image type="content" source="media/licensing-prompt-tokens/tokens-prompt-input-output-flow.png" alt-text="Screenshot of token formulas input and output in a Power Automate cloud flow.":::

## How image or documents are translated into tokens

When you pass an image to a prompt, it gets converted into tokens.

When you pass a PDF document into a prompt, it first gets converted into images at one image per page, and then into tokens.

The tokens-to-image conversion fully applies the [Azure OpenAI logic](/azure/ai-services/openai/overview#image-tokens).

We use the [**auto**](/azure/ai-services/openai/how-to/gpt-with-vision?tabs=rest#detail-parameter-settings-in-image-processing-low-high-auto) setting when passing images to Azure OpenAI. This means the token cost of an image depends on its initial resolution.

### Low resolution image

Images with resolution lower than 512 x 512 pixels have the flat conversion rate of 85 tokens per image, regardless of size.

### High resolution images

For images with resolution higher than 512 x 512 pixels, the token conversion happens in two steps. The steps are described in the following table.

| Step | Description | Conversion process |
|------|-------------|---------------------|
| 1 | Resize the image | The image is resized to fit within a 2048 x 2048 pixel square. If the shortest side is larger than 768 pixels, the image is further resized so that the shortest side is 768 pixels long. The aspect ratio is preserved during resizing. |
| 2 | Tokens conversion | The resized image is divided into 512 x 512 pixel tiles. Any partial tiles are rounded up to a full tile. The number of tiles determines the total token cost: Each 512 x 512 pixel tile costs 170 tokens. An extra 85 base tokens are added to the total. |

## Related information

- [Licensing and credit management](credit-management.md)
- [Microsoft Power Platform Licensing Guide (PDF)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Add text, image, or document input to a prompt](add-inputs-prompt.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
