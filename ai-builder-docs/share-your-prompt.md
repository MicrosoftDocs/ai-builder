---
title: Share your prompt
description: Learn how to share your prompt.
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.collection: conceptual
ms.date: 12/18/2023
ms.author: plarrue
ms.reviewer: angieandrews
---

# Share your prompt

Newly created prompts are private by default. This means they're visible and usable in Power Automate, Power Apps, and Microsoft Copilot Studio only by the person who created them. This allows the maker the time to test and evaluate them in apps or workflows and ensure their accuracy before sharing them.

If you want other users of the environment or groups to use your prompt in Power Apps or Power Automate, you need to share it.

> [!IMPORTANT]
> - AI Builder prompts are running on GPT-3.5 Turbo model powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
> - This capability is [limited to some regions](availability-region.md#prompts).
> - This capability might be subject to usage limits or capacity throttling.

## Use the Share action

The Share action is available for every prompt owner on the **My prompts** page in Power Automate, Power Apps, and Microsoft Copilot Studio. It’s also available for the system administrator of the environment, or for any security role that has the share permissions. Sharing a prompt is performed by selecting **Share** for the respective prompt. You can add people as **Users** of your prompt so they can use your prompts in flows, apps, and chatbots.

## Understand the Share panel

When you select the **Share** action, a **Share** panel appears. This is where you select users or teams in your organization with whom you'll share your prompt.

### Prompt list views

The prompts visible to you appear in three different views on the Prompts page.

- **My prompts**: The prompts you created.
- **Shared with me**: The prompts that are shared with you.
- **All prompts**: All the prompts that you created or are shared with you.

## FAQ

This section contains frequently asked questions and their answers.

### Can I allow other users to edit my prompts?

No. When sharing a prompt with a user, they won't have the ability to edit or delete it.

### Can I stop sharing a prompt?

Yes. To stop sharing a prompt, select **Share** > <***user or team name***>. Then, select the **X** to stop sharing the prompt with user or team.

