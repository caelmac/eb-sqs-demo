# Serverless Demo Framework using SQS, EventBridge, and Lambda
This is a serverless demo framework using SQS, EventBridge, and Lambda architectures. It is built on AWS and allows for easy integration of these services in a serverless environment. The serverless.yml file in this repository is an example configuration for the demo.

## Getting Started
To get started, you will need an AWS account and the Serverless Framework installed on your local machine. Once you have the Serverless Framework installed, you can deploy this demo by doing the following:

## Clone this repository to your local machine.
In the root of the repository, run npm install to install the necessary dependencies.
In the serverless.yml file, update the provider.region field to the AWS region you want to deploy to.
Deploy the demo using the Serverless Framework: serverless deploy
Once the deployment is complete, you can test the demo by sending a message to the SQS queue using the AWS console or the AWS CLI. The message should trigger the processEventLambda function, which will in turn publish an event to the EventBridge. The putEventsLambda function will then receive this event and log it.

## Architecture
This demo framework uses the following AWS services:

* Amazon Simple Queue Service (SQS): A fully managed message queuing service.
* Amazon EventBridge: A serverless event bus that makes it easy to connect applications using data from your own applications, integrated Software-as-a-Service (SaaS) applications, and AWS services.
* AWS Lambda: A serverless compute service that runs your code in response to events and automatically manages the underlying compute resources.
The serverless.yml file in this repository defines the following resources:

* An SQS queue: This is where messages are sent to trigger the processEventLambda function.
* An EventBridge event bus: This is used to publish events from the processEventLambda function to the putEventsLambda function.
* Two Lambda functions: The processEventLambda function is triggered by messages sent to the SQS queue, and the putEventsLambda function is triggered by events published to the EventBridge event bus.


License
This demo framework is licensed under the MIT License. See the LICENSE file for more information.
