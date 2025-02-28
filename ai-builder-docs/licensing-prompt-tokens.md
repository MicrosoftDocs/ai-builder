---
title: Prompt tokens
description: Learn about licensing and credit management in AI Builder.
author: antrod
contributors:
  - antrod
  - v-aangie
ms.topic: conceptual
ms.collection: 
    - bap-ai-copilot
ms.date: 02/26/2025
ms.author: antrod
ms.reviewer: angieandrews
---

# Prompt tokens
## What are tokens
The prompt model don't operate on words or characters as units of text, but instead use something in-between: tokens.
- A token can be a single character, fraction of a word, or an entire word (many common words are represented by a single token, less common words are represented by multiple tokens).
- When images or documents are included in a prompt instruction, they are translated into tokens following [conversion rules](#conversion-rules-for-images-and-documents).

## Tokens consumed by a prompt
When creating a prompt instruction and runing it, the following will happen:
- The prompt instruction gets deconstructed into a sequence of tokens, called the input tokens.
- The model generates an answer as a sequence of tokens, called the output tokens. 

The input tokens are a sum of the tokens coming from:
- The system metaprompt from Microsoft. This system prompt is not visible and is essential for the safety of your prompt response. It represents few hundreds of tokens.
- The prompt instruction.
- If any, the input values.
- If any, the knowledge data retrieved.

The output tokens are the tokens coming from the model response.

## How tokens impact licensing
The combination of input tokens, output tokens and the model version allows to compute the cost of your prompt run. You can refer to the AI Builder rate card in the [Microsoft Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130) (pdf).

When building solutions that include prompts, it can be important for you to assess the average cost of a prompt. Here are two possibilities to achieve that goal:

### Check the credits display in the prompt builder
When testing a prompt in AI Hub within Power Automate or Power Apps portal, you'll be able to see the credits consumed by your prompt (testing is free, so it's a theoritical value).

:::image type="content" source="media/credits-prompt-builder.png" alt-text="Credits display in Prompt builder":::

### Get the token count from a Power Automate flow
When calling a prompt action in a flow, you can see the associated input and tokens using formulas.

Input tokens:
```
outputs('Create_text_with_GPT_using_a_prompt')?['body/responsev2/predictionOutput/promptTokens']
```

Output tokens:
```
outputs('Create_text_with_GPT_using_a_prompt')?['body/responsev2/predictionOutput/completionTokens']
```

:::image type="content" source="media/tokens-prompt-flow.png" alt-text="Tokens formulas in Power Automate":::

## How image or documents are translated into tokens
When you pass an image to a prompt, it gets converted into tokens.
When you pass a PDF document into a prompt, it gets first conerted into images (1 image per page) and then into tokens.

We are using the [**auto**](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/gpt-with-vision?tabs=rest#detail-parameter-settings-in-image-processing-low-high-auto) setting when passing images to Azure OpenAI. This means the token cost of an image depend on the initial resoution of the image.

### Low resolution image
Images with resolution lower than 512 x 512 pixels have the flat conversion rate of 85 tokens per image, regardless of size.

### High resolution images
For images with resolution higher than 512 x 512 pixel, the token conversion happens in two steps:

**Image resize**
The image is resized to fit within a 2048 x 2048 pixel square. If the shortest side is larger than 768 pixels, the image is further resized so that the shortest side is 768 pixels long. The aspect ratio is preserved during resizing.

**Tokens conversion**
Once resized, the image is divided into 512 x 512 pixel tiles. Any partial tiles are rounded up to a full tile. The number of tiles determines the total token cost: Each 512 x 512 pixel tile costs 170 tokens. An extra 85 base tokens are added to the total.

[See more details and examples](https://learn.microsoft.com/en-us/azure/ai-services/openai/overview#image-tokens) on Azure OpenAI Image to tokens conversion.

## Related information

- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Licensing FAQ for AI Builder](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
