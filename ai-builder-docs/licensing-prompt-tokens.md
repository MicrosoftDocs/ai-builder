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

**Check the credits display in the prompt builder**
When testing a prompt in AI Hub within Power Automate or Power Apps portal, you'll be able to see the credits consumed by your prompt (testing is free, so it's a theoritical value).

:::image type="content" source="media/credits-prompt-builder.png" alt-text="Credits display in Prompt builder":::

**Get the token count from a Power Automate flow**
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
todo

## Related information

- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Licensing FAQ for AI Builder](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
