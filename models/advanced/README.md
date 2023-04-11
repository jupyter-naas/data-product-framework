# Models - Advanced

## How do you want to organize your naas data product?
Effective data management is critical for businesses to make informed decisions, achieve operational efficiency, and remain competitive in today's market. As data volumes continue to increase, managing data becomes more complex and challenging. That's why it's essential to establish a structured and organized folder system right from the beginning.

As you start working with data, it's crucial to establish a structured folder system to avoid things from becoming too messy. A basic folder structure may work for a small amount of data, but as your data grows, it can quickly become difficult to manage. Organizing your data makes it easy to locate and access specific datasets when needed, saving you time and reducing the risk of errors.

In addition to facilitating easy data access, a structured folder system also enables you to automate data-related tasks using triggers. With triggers, you can automate data ingestion, transformation, and analysis, making the data management process much more efficient. By streamlining your workflow, you can focus on the more critical aspects of your business while ensuring that your data remains accurate and up-to-date.

To establish a structured folder system, we recommend dividing the models/advanced folder into six subfolders. These subfolders should include four layers folders and two triggers, specifically schedulers and folders. The four layers folders should be organized by data type, making it easy to locate specific datasets. The triggers will help automate tasks such as data ingestion and transformation.

We recommend dividing the models/advanced folder into six subfolders:
- 4 layers folders
- 2 triggers (schedulers and folders)"

## Layers

### l1_bronze
The Bronze layer should contain models that have been trained on a limited dataset and have achieved relatively low accuracy.
These models may be useful for initial testing and prototyping, but may not be suitable for use in production environments.

### l2_silver
The Silver layer should contain models that have been trained on a larger dataset and have achieved moderate accuracy.
These models may be suitable for use in certain production environments, but may not be the most accurate option available.

### l3_gold
The Gold layer should contain the most accurate models that have been trained on the largest and most diverse dataset available.
These models are suitable for use in the most demanding production environments and are the top choice for mission-critical tasks.

### l4_insights
The Insights layer should contain any additional information or analysis related to the models in the Bronze, Silver, and Gold categories.
This may include performance metrics, error analysis, and other useful insights.

## Triggers

### Schedulers

The schedulers folder is an essential component of your data management system. It stores pipeline files that can be scheduled using the naas.scheduler feature. However, it's important to ensure that the execution time is lower than the cron time. If your pipeline lasts for 15 minutes and you want it to update every 10 minutes, you might encounter data issues. In this case, we recommend building smaller pipelines scheduled more frequently, along with a larger one scheduled 2-3 times a day. Of course, everything depends on your specific requirements.

By utilizing the schedulers folder, you can automate data-related tasks and ensure that your data is always up-to-date. This, in turn, can lead to better business decisions and improved operational efficiency.

You can refer to [our documentation](https://docs.naas.ai/features/scheduler) on how to schedule your notebooks using `naas.scheduler` feature or use the templates provided in the Naas folder in our [awesome-notebooks repository](https://github.com/jupyter-naas/awesome-notebooks/tree/master/Naas).

### Webhooks

The webhooks folder is another crucial component of your data management system. It stores pipeline files that can be triggered using the naas.webhook feature. With our webhook feature, you can build smaller pipelines that can be triggered inside a third-party tool or by a human by clicking on the naas link or using our Chrome extension. This allows end-users to have refreshed data without waiting for scheduled refreshing. Webhooks can have a response time below one minute or return a 500 error, which is the limit fixed by naas. This error won't stop the execution of your webhook, but it won't allow you to get the expected response.

To address this issue, you can use the pipeline feature on.error to manage longer webhook execution and get the result of the execution by creating a status file that can store the webhook status. If you want to learn more about this feature, please contact florent@naas.ai.

To learn more about how to use naas.webhook feature, you can refer to [our documentation](https://docs.naas.ai/features/webhook) or use the templates provided in the Naas folder in our [awesome-notebooks repository](https://github.com/jupyter-naas/awesome-notebooks/tree/master/Naas).


