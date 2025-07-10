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
ms.date: 05/20/2025
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

## Test dataset management

You can create and manage test datasets in multiple ways:

- Import historical data from past prompt interactions.
- Upload pre-labeled datasets in CSV format.
- Leverage AI-generated synthetic test data for diverse scenarios.
- Manually create or refine test cases within the interface.

## Evaluation criteria

The framework offers you flexibility in defining evaluation criteria:

- **Prebuilt criteria**: Includes options for tasks like JSON validation, exact match, semantic similarity, and response quality check.
- **Passing score**: You can tailor the passing score to fit unique use case depending upon the threshold that you set when a test result should be considered as pass or fail.

## Run history insights

Run history allows you to monitor and analyze test results over time, including:

- Track accuracy score progression across multiple test runs.
- Compare outcomes from different runs to identify trends or regressions.
- Access details of why a certain test result was classified pass or fail thus offering more detailed for diagnosis.

## How to use the Test framework

Use the following steps to set up and run batch tests for your prompts.

### Define the Test dataset

Step 1 in the batch testing process is to define the test dataset.

1. Sign in to [Power Apps](https://make.powerapps.com) or [Power Automate](https://make.powerautomate.com).
1. On the navigation pane to the left, select **AI hub**.
1. Under **Recently created**, select **Prompts**.

    :::image type="content" source="media/batch-testing-prompts/ai-hub-prompts.png" alt-text="Screenshot of recently created prompts.":::

1. Next to the prompt name, select the vertical ellipsis (&vellip;).
1. Select **Test hub (Preview)**.

    :::image type="content" source="media/batch-testing-prompts/more.png" alt-text="Screenshot of the 'More' menu with the 'Test hub - Preview' option.":::

    The Test hub (preview) opens.

    :::image type="content" source="media/batch-testing-prompts/test-gub-get-started.png" alt-text="Screenshot of the Test hub screen.":::

1. To add test cases individually, select **Add test case**.

    :::image type="content" source="media/batch-testing-prompts/add-test-case.png" alt-text="Screenshot of adding a test case.":::

1. To set upload test cases, select **Upload**.

    If you want to check the format of the file you need to upload, select **Download test data schema**.

    :::image type="content" source="media/batch-testing-prompts/upload-test-case.png" alt-text="Screenshot of uploading or downloading test data schema.":::

1. To generate synthetic datasets using AI, select **Generate**.
1. Select the test lines to keep and then select **Save**.
  
    :::image type="content" source="media/batch-testing-prompts/list-uploaded-test-case.png" alt-text="Screenshot of the uploaded test cases.":::

You can also define datasets by selecting the following in the **Test hub** menu. To choose from past activity, select **Create from activity**.

### Set evaluation criteria

Step 2 in the batch testing process involves defining the evaluation criteria for the test cases.

1. In the **Test hub** screen, select **Evaluation criteria**.
1. Choose from the following prebuilt criteria:
    - For semantic similarity, select **Response quality**.
    - For JSON validation, select **JSON correctness**.
1. Adjust the pass score threshold tailored to specific needs.

    :::image type="content" source="media/batch-testing-prompts/evaluation-criteria.png" alt-text="Screenshot of evaluation criteria.":::

    These criteria and passing score determine how outputs are assessed during the evaluation process.

### Run batch tests

Step 3 in the batch testing process is to run the batch tests.

1. Select the test cases to run.
1. Select **Run selected**.

    The framework evaluates results against the defined criteria, providing insights into the prompt's performance.

    :::image type="content" source="media/batch-testing-prompts/run-tests.png" alt-text="Screenshot of tests to run.":::

### Review test results

Step 4 in the batch testing process is to review the test results.

You can:
- View test responses, accuracy scores, and evaluation details.
- Refine evaluation metrics to suit their needs.
- Identify areas for improvement and optimize their prompt.

1. To access previous runs, select **Run history**.

    :::image type="content" source="media/batch-testing-prompts/run-history.png" alt-text="Screenshot of run history.":::

1. To view details, select the run.

    :::image type="content" source="media/batch-testing-prompts/run-details.png" alt-text="Screenshot of run details.":::

### Monitor and iterate

Step 5 in the batch testing process is to monitor and iterate. To track performance over time, use the run history. Continuously improve prompts through iterative testing and evaluation.

The following list contains the key benefits:
- Improved confidence and trust in AI tool outcomes.
- Standardized and repeatable testing processes.
- Enhanced efficiency through automation and AI-assisted tools.
- Customizable evaluation options for diverse business scenarios.

## Related information

[FAQ for prompts and text generation capabilities](faqs-text-generation.md)
