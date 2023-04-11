# Webhooks

## Description
The webhooks folder is another crucial component of your data management system. It stores pipeline files that can be triggered using the naas.webhook feature. With our webhook feature, you can build smaller pipelines that can be triggered inside a third-party tool or by a human by clicking on the naas link or using our Chrome extension. This allows end-users to have refreshed data without waiting for scheduled refreshing. Webhooks can have a response time below one minute or return a 500 error, which is the limit fixed by naas. This error won't stop the execution of your webhook, but it won't allow you to get the expected response.

To address this issue, you can use the pipeline feature on.error to manage longer webhook execution and get the result of the execution by creating a status file that can store the webhook status. If you want to learn more about this feature, please contact florent@naas.ai.

To learn more about how to use naas.webhook feature, you can refer to [our documentation](https://docs.naas.ai/features/webhook) or use the templates provided in the Naas folder in our [awesome-notebooks repository](https://github.com/jupyter-naas/awesome-notebooks/tree/master/Naas).

## Notebooks

### __pipeline__.ipynb

The **__pipeline__** file is a special file that specifies the order in which the models in the Bronze, Silver, and Gold categories should be trained and evaluated.
This file is used to automate the model selection process, ensuring that the most accurate model is always used for a given task.

## Folder

### pipeline_executions

The pipeline_executions folder store all of the notebooks that are executed during your pipeline. 
For each execution, a new folder will be created with a unique timestamp and ID.

This folder is important because it allows you to easily track the progress of your pipeline and identify any issues that may arise. By examining the notebooks in the pipeline_executions folder, you can quickly identify which steps in the pipeline succeeded and which steps failed. This can be extremely helpful when debugging your pipeline or trying to understand why certain results were produced.

