# Schedule Job

## Overview

Scheduling a job to run at a specific time is a common task in data science. This can be used to automate data collection, model training, or model deployment. In this guide we will use AWS Lambda to schedule a job to run at a specific time.

## How we do this:

1. Create a Lambda function that will run our job (see [guide](https://github.com/CodesmithLLC/aws-cloud-guides/lambda.md))

2. Configure Lambda to be triggered by [Cloudwatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/ScheduledEvents.html)

## Assumptions/Considerations

As our dataset evolve the performance of our models may deteriorate due to [data drift](https://www.datacamp.com/tutorial/understanding-data-drift-model-drift). Data drift is a common problem in data science. This is when the data we are using to train our model changes over time. This can lead to our model becoming less accurate over time. We can use a scheduled job to retrain our model on a regular basis to account for data drift.

## Variations/Alternatives

There are many ways you can schedule a job to run at a specific time:

- [AWS Step Functions](https://aws.amazon.com/step-functions/)
- [Airflow](https://airflow.apache.org/)
- [Local Cron Job](https://pypi.org/project/local-crontab/#:~:text=local%2Dcrontab%20is%20a%20Python,because%20of%20Daylight%20Saving%20Time.)