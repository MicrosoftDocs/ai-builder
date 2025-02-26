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

## How tokens impact licensing
When creating a prompt instruction and runing it, the following will happen:
- The prompt instruction gets deconstructed into a sequence of tokens, called the input tokens.
- The model generates an answer as a sequence of tokens, called the output tokens. 

The combination of input tokens, output tokens and the model version allows to compute the cost of your prompt run. You can refer to the AI Builder rate card in the [Microsoft Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130) (pdf).

## Estimate tokens for my prompt
To estimate the total tokens of your prompt you should consider:
- The hidden system metaprompt from Microsoft. This represents tens to few hundreds of tokens and is essential for the safety of your prompt response.
- The prompt instruction.
- If any, the input values.
- If any, the knowledge data retrieved.
- The response ot the prompt model.




## Related information

- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Licensing FAQ for AI Builder](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
