---
title: Batch testing for prompts
description: Batch testing for prompts
author: antrodfr
contributors:
  - antrodfr
ms.topic: article
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 05/20/2025
ms.custom: build-2025
ms.author: antrod
ms.reviewer: angieandrews
---

# Batch testing for prompts (preview)
[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

Prompts enable you to create custom generative AI tools for business automation and agents. Ensuring the accuracy, reliability, and efficiency of these tools is critical. Batch testing of Prompts is designed to enable you to validate, and improve prompts used in AI tools across the platform. 

> [!IMPORTANT]
> - AI Builder prompts run on GPT models powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
> - This capability is [limited to some regions](availability-region.md#prompts).
> - This capability might be subject to usage limits or capacity throttling.

> [!IMPORTANT]
> - This is a production-ready preview feature.
>- Production-ready previews are subject to [supplemental terms of use](https://go.microsoft.com/fwlink/?linkid=2189520).

## Core features of batch testing

Batch testing provides a systematic approach for validating prompts on diverse datasets. Users can:
- Upload or generate test datasets for comprehensive evaluation.
- Define evaluation criteria for judging the test results.
- Execute batch tests to assess prompt behavior across the test dataset.
- Compare outcomes over time to ensure continuous improvement.
- Ability for you to review and adjust automatic evaluations, ensuring alignment with your specific needs.

An accuracy score is calculated based on test results, giving users empirical data to trust their AI tools. 

## Test dataset management

You can create and manage test datasets in multiple ways:
- Import historical data from past prompt interactions.
- Upload pre-labeled datasets in CSV format.
- Leverage AI-generated synthetic test data for diverse scenarios.
- Manually create or refine test cases within the interface.

## Evaluation criteria
The framework offers flexibility in defining evaluation criteria:
- Prebuilt Criteria: Includes options for tasks like JSON validation, exact match, semantic similarity and response quality check.
- Passing Score: You can tailor the passing score to fit unique use case depending upon the threshold that you set when a test result should be considered as pass or fail.

## Run History Insights
Run history allows users to monitor and analyze test results over time, including:
- Tracking accuracy score progression across multiple test runs.
- Comparing outcomes from different runs to identify trends or regressions.
- Accessing details of why a certain test result was classified pass or fail thus offering more detailed for diagnosis.

## How to Use the Test Framework
### Step 1: Define the Test Dataset
1.	Open **Test hub**
:::image type="content" source="media/batch-testing/test-gub-get-started.png" alt-text="Screenshot of Test hub.":::

1.	You can add test cases individually by selecting on **Add test case**
:::image type="content" source="media/batch-testing/add-test-case.png" alt-text="Screenshot of adding a test case.":::

1.	You can also a set upload test cases by selecting on **Upload test case**. If you want to check the format of the file you need to upload, click on **Download test data schema**.
:::image type="content" source="media/batch-testing/upload-test-case.png" alt-text="Screenshot of adding a test case.":::

    Select the test lines to keep and save to generate the test cases.
    :::image type="content" source="media/batch-testing/list-uploaded-test-case.png" alt-text="Screenshot of uploaded test cases.":::

Users can also define define datasets by generating synthetic datasets using AI, selecting **Generate**, or from past activity, selecting **Create from activity**.

### Step 2: Set evaluation criteria
In the **Test hub** screen, select **Evaluation criteria**.
:::image type="content" source="media/batch-testing/evaluation-criteria.png" alt-text="Screenshot of evaluation criteria.":::

Choose from prebuilt criteria like semantic similarity, selecting **Response quality**, or JSON validation, selecting **JSON correctness**. Adjust the pass score threshold tailored to specific needs. These criteria and passing score determine how outputs will be assessed during the evaluation process.

### Step 3: Run batch tests
Select the test cases to run and click on **Run selected**. The framework evaluates results against the defined criteria, providing insights into the prompt's performance.

:::image type="content" source="media/batch-testing/run-tests.png" alt-text="Screenshot of tests to run.":::

### Step 4: Review test results
Users can:
- View test responses, accuracy scores, and evaluation details.
- Refine evaluation metrics to suit their needs.
- Identify areas for improvement and optimize their prompt.

1. Select **Run history** to access previous runs.
:::image type="content" source="media/batch-testing/run-history.png" alt-text="Screenshot of run history.":::

1. Select the run to view details
:::image type="content" source="media/batch-testing/run-details.png" alt-text="Screenshot of run details.":::

### Step 4: Monitor and iterate
Utilize the run history to track performance over time. Continuously improve prompts through iterative testing and evaluation.

Key Benefits:
- Improved confidence and trust in AI tool outcomes.
- Standardized and repeatable testing processes.
- Enhanced efficiency through automation and AI-assisted tools.
- Customizable evaluation options for diverse business scenarios.


## Related information
- [FAQ for prompts and text generation capabilities](faqs-text-generation.md)
