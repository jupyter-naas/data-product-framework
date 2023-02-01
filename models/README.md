# Models

## Description
The /models folder stores any files that transform inputs into outputs (notebook, Python, SQL files)

## Notebooks

### __pipeline__.ipynb

The **__pipeline__** file is a special file that specifies the order in which the models in the Bronze, Silver, and Gold categories should be trained and evaluated.
This file is used to automate the model selection process, ensuring that the most accurate model is always used for a given task.

## Layers

### l1_bronze
The Bronze layer should contain models that have been trained on a limited dataset and have achieved relatively low accuracy. These models may be useful for initial testing and prototyping, but may not be suitable for use in production environments.

### l2_silver
The Silver layer should contain models that have been trained on a larger dataset and have achieved moderate accuracy. These models may be suitable for use in certain production environments, but may not be the most accurate option available.

### l3_gold
The Gold layer should contain the most accurate models that have been trained on the largest and most diverse dataset available. These models are suitable for use in the most demanding production environments and are the top choice for mission-critical tasks.

### l4_insights
The Insights layer should contain any additional information or analysis related to the models in the Bronze, Silver, and Gold categories. This may include performance metrics, error analysis, and other useful insights.
