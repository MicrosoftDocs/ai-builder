---
title: Model selection and temperature settings
description: Learn about the settings parameter in prompt builder.
author: ashbhati
contributors:
  - ashbhati
  - Phil-cmd
  - Antoine2F
  - v-aangie
ms.topic: conceptual
ms.date: 03/10/2025
ms.author: ashbhati
ms.reviewer: angieandrews
---

# Model selection and temperature settings

When you create a prompt action in prompt builder, the panel on the right includes a **Settings** section. This section allows you to set these parameters:

- Version of the generative AI model
- Temperature

This article explores the impact of these parameters.

## Generative AI model versions

The dropdown menu allows you to select among the generative AI models, which generate the answer to your custom prompt.

The default model as of November 2024 is GPT-4o Mini (general availability, or GA). You can also use the more powerful GPT-4o model (GA), and o1 model (paid preview). The exact minor versions of these models might change.

When you use prompt actions in Power Apps or Power Automate, they consume AI Builder credits.

### Choose a model

Choose between the models based on status and licensing rules.

|GPT model  |Status   |Licensing rules   | Functionalities| Region availabilities |
|---------|---------|---------|---------|---------|
|GPT 4o Mini | GA - Default model	| Consumes credits in Power Apps and Power Automate. More information: [Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130)  | Trained on data up to December 2023. Context allowed up to 128k tokens. | [Feature availability by regions for prompts](availability-region.md)
| GPT 4 | GA | Consumes credits in Power Apps and Power Automate. More information: [Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130)  | GPT 4o has knowledge up to October 2023 and has a context length of 128k tokens. | [Feature availability by regions for prompts](availability-region.md)|
| o1 | Paid Preview | Consumes credits in Power Apps and Power Automate. More information: [Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130). o1 model consumes 140 credits for 1K input tokens and 560 credits for 1K output tokens. Consumes message in Copilot Studio starting April 7th. More information: [Message in Copilot Studio](https://go.microsoft.com/fwlink/?linkid=2307400)  | o1 has knowledge up to October 2023 and has a context length of 128k tokens. | [Feature availability by regions for prompts](availability-region.md)|

Choose between the model based on capabilities and scenarios.

### Comparison of GPT-4o Mini, GPT-4o, and o1

| Factors                     | GPT-4o Mini                          | GPT-4o                               | o1
|---------------------------|--------------------------------------|--------------------------------------|--------------------------------------|
| **Cost**                  | Lower, more cost-effective           | Higher, premium pricing              | Higher, premium pricing (paid preview) |
| **Performance**           | Good for most tasks                  | Superior for complex tasks           | Trained for reasoning tasks          |
| **Speed**                 | Faster processing                    | Might be slower due to complexity    | Slower as it reasons before responding |
| **Use Cases**             | Summarization, information tasks | Image and document processing, as well complex content creation tasks |  Complex data analysis and reasoning tasks |

## Decision Narrative

When you need a cost-effective solution for moderately complex tasks, have limited computational resources, or require faster processing, choose GPT-4o Mini. It's ideal for projects with budget constraints and applications like customer support or efficient code analysis.

When you're dealing with highly complex, multimodal tasks that require superior performance and detailed analysis, choose GPT-4o. It's the better choice for large-scale projects where accuracy and advanced capabilities are crucial. Another scenario where it's a better choice is when you have the budget and computational resources to support it. GPT-4o is also preferable for long-term projects that might grow in complexity over time.

For projects requiring advanced reasoning capabilities, the o1 model excels. It's suitable for scenarios that demand sophisticated problem-solving and critical thinking. The o1 model excels in environments where nuanced reasoning, complex decision-making, and detailed analysis are important. 

### Use of AI prompts in context of Microsoft Copilot Studio

AI prompts don't consume AI Builder credits in the Copilot Studio but consume messages.

Learn more about message consumption in the [Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130).

## Temperature

The slider allows you to select the temperature of the generative AI model. It varies between 0 and 1, and guides the generative AI model about how much creativity (1) vs deterministic answer (0) it should provide.

Temperature is a parameter that controls the randomness of the output generated by the AI model. A lower temperature results in more predictable and conservative outputs. To compare, a higher temperature allows for more creativity and diversity in the responses. It’s a way to fine-tune the balance between randomness and determinism in the model’s output.

By default, the temperature is 0, as in previously created prompts.

|Temperature  |Functionality| Use in|
|---------|---------|---------|
|0| More predictable and conservative outputs.<br>Responses are more consistent.| Prompts that require high accuracy and less variability.|
|1| More creativity and diversity in the responses. <br> More varied and sometimes more innovative responses.| Prompts that create new out-of-the-box content |

Adjusting the temperature can influence the model’s output, but it doesn’t guarantee a specific result. The AI’s responses are inherently probabilistic and can vary even with the same temperature setting. 

> [!NOTE]
> The temperature setting isn't available for the o1 model, so the slider is disabled when the o1 model is selected.
