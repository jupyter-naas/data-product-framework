# Schedulers

## Description
The schedulers folder is an essential component of your data management system. It stores pipeline files that can be scheduled using the naas.scheduler feature. However, it's important to ensure that the execution time is lower than the cron time. If your pipeline lasts for 15 minutes and you want it to update every 10 minutes, you might encounter data issues. In this case, we recommend building smaller pipelines scheduled more frequently, along with a larger one scheduled 2-3 times a day. Of course, everything depends on your specific requirements.

By utilizing the schedulers folder, you can automate data-related tasks and ensure that your data is always up-to-date. This, in turn, can lead to better business decisions and improved operational efficiency.

You can refer to [our documentation](https://docs.naas.ai/features/scheduler) on how to schedule your notebooks using `naas.scheduler` feature or use the templates provided in the Naas folder in our [awesome-notebooks repository](https://github.com/jupyter-naas/awesome-notebooks/tree/master/Naas).

## Notebooks

### __pipeline__.ipynb

The **__pipeline__** file is a special file that specifies the order in which the notebooks inside your layers should be trained and evaluated.
This file is used to automate the model selection process, ensuring that the most accurate model is always used for a given task.

## Folder

### pipeline_executions

The pipeline_executions folder store all of the notebooks that are executed during your pipeline. 
For each execution, a new folder will be created with a unique timestamp and ID.

This folder is important because it allows you to easily track the progress of your pipeline and identify any issues that may arise. By examining the notebooks in the pipeline_executions folder, you can quickly identify which steps in the pipeline succeeded and which steps failed. This can be extremely helpful when debugging your pipeline or trying to understand why certain results were produced.

