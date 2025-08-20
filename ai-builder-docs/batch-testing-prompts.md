---
title: Batch testing for prompts (preview)
description: Learn to use batch testing for prompts to validate and improve prompts used in AI tools across the platform.
author: antrodfr
contributors:
  - antrodfr
  - v-aangie
ms.topic: article
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 08/20/2025
ms.update-cycle: 180-days
ms.custom: build-2025
ms.author: antrod
ms.reviewer: angieandrews
---

# Batch testing for prompts (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

Prompts enable you to create custom generative AI tools for business automation and agents. Ensuring the accuracy, reliability, and efficiency of these tools is critical. Batch testing of prompts is designed to enable you to validate and improve prompts used in AI tools across the platform.

> [!IMPORTANT]
>- This is a production-ready preview feature.
>- Production-ready previews are subject to [supplemental terms of use](https://go.microsoft.com/fwlink/?linkid=2189520).
>- AI Builder prompts run on GPT models powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
>- This capability might not be available in your region yet. Learn more in the **Prompts** section in [Feature availability by region or US Government environment](availability-region.md#prompts).
>- This capability might be subject to usage limits or capacity throttling.

## Core features of batch testing

Batch testing provides a systematic approach for validating prompts on diverse datasets. You can:

- Upload or generate test datasets for comprehensive evaluation.
- Define evaluation criteria for judging the test results.
- Execute batch tests to assess prompt behavior across the test dataset.
- Compare outcomes over time to ensure continuous improvement.
- Review and adjust automatic evaluations to ensure alignment with your specific needs.

An accuracy score is calculated based on test results, giving you empirical data to trust your AI tools.

## How to use batch testing

Use the following steps to set up and run batch tests for your prompts.

### Define the test cases

1. Sign in to [Copilot Studio](https://copilotstudio.microsoft.com), [Power Apps](https://make.powerapps.com), or [Power Automate](https://make.powerautomate.com).
1. Access the list of prompts:
   - In Copilot Studio, select **Tools**, and then filter on prompts.
   - In Power Apps and Power Automate, select **AI hub**.

1. Next to the prompt name, select the ellipsis (**...**).
1. Select **Test hub (Preview)**.

    Here's an example of the **Tools** screen in Copilot Studio:

    :::image type="content" source="media/batch-testing-prompts/mcs-new-tool.png" alt-text="Screenshot of the menu with the 'Test hub - Preview' option.":::

    In Copilot Studio, the test hub looks like the following screenshot:

    :::image type="content" source="media/batch-testing-prompts/test-gub-get-started.png" alt-text="Screenshot of the Test hub screen.":::

1. Add your test cases using one the available options:
   - **Upload**: Allows you to upload test cases using a csv file. If you want to check the format of the file you need to upload, select Download test data schema.
   - **AI-generate**: Allows you to generate test cases using AI based on your prompt.
   - **Use activity data**: Allows you to pull the recent prompt activity to help you get started.
   - **Manually Add**: Allows you to create test cases manually.

   Any of the options help you create a list of test cases that you're able to run:

   :::image type="content" source="media/batch-testing-prompts/list-uploaded-test-case.png" alt-text="Screenshot of the uploaded test cases.":::

### Set evaluation criteria

1. After you create the test cases, select **Configure criteria** in the configuration section on the right:

    :::image type="content" source="media/batch-testing-prompts/configure-eval-criteria.png" alt-text="Screenshot of configure evaluation criteria.":::

1. Define the **Passing score**, which is the minimum score required for a response to pass.

1. Choose one of the following prebuilt criteria:
    - **Response quality**: Tests responses for clarity, helpfulness, and tone
    - **Response matches**: Tests responses for specific words and meanings
    - **JSON correctness**: Tests that responses follow your data schema

    :::image type="content" source="media/batch-testing-prompts/evaluation-criteria.png" alt-text="Screenshot of evaluation criteria.":::

    These criteria and passing score determine how test cases outputs are assessed during the evaluation process.

### Run batch tests

1. In the test cases screen, select **Run all** to run evaluation on all the test cases, or select the test cases to run and select **Run selected**.

    :::image type="content" source="media/batch-testing-prompts/run-tests.png" alt-text="Screenshot of tests to run.":::

   The test hub evaluates results against the defined criteria, providing insights into the prompt's performance.

1. Once the test cases evaluation is done, the result screen appears:

    :::image type="content" source="media/batch-testing-prompts/run-result.png" alt-text="Screenshot of tests results.":::

1. To access previous evaluation runs, select the prompt name at the top of the screen in Copilot Studio, or select **Run history** in Power Apps or Power Automate.

    :::image type="content" source="media/batch-testing-prompts/run-history.png" alt-text="Screenshot of run history.":::

1. To view details, select the evaluation run.

Run history allows you to monitor and analyze test results over time, including:

- Track accuracy score progression across multiple test runs.
- Compare outcomes from different runs to identify trends or regressions.
- Access details of why a certain test result was classified pass or fail, thus offering more details for diagnosis.

Iterate on the test cases evaluation and monitor any significant change between evaluation runs.

## Related information

[FAQ for prompts and text generation capabilities](faqs-text-generation.md)
