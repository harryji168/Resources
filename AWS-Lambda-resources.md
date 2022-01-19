# AWS Lambda

AWS Lambda is an event-driven, serverless computing platform provided by Amazon as a part of Amazon Web Services. It is a computing service that runs code in response to events and automatically manages the computing resources required by that code. It was introduced in November 2014.[1]

Node.js, Python, Java, Go,[2] Ruby,[3] and C# (through .NET) are all officially supported as of 2018. In late 2018, custom runtime support[4] was added to AWS Lambda.

AWS Lambda supports running native Linux executables via calling out from a supported runtime such as Node.js.[5] For example, Haskell code can be run on Lambda.[6]

AWS Lambda was designed for use cases such as image or object uploads to Amazon S3, updates to DynamoDB tables, responding to website clicks, or reacting to sensor readings from an IoT connected device. AWS Lambda can also be used to automatically provision back-end services triggered by custom HTTP requests, and "spin down" such services when not in use, to save resources. These custom HTTP requests are configured in AWS API Gateway, which can also handle authentication and authorization in conjunction with AWS Cognito.

Unlike Amazon EC2, which is priced by the hour but metered by the second, AWS Lambda is metered by rounding up to the nearest millisecond with no minimum execution time.

In 2019, at AWS' annual cloud computing conference (AWS re:Invent), the AWS Lambda team announced "Provisioned Concurrency", a feature that "keeps functions initialized and hyper-ready to respond in double-digit milliseconds."[7] The Lambda team described Provisioned Concurrency as "ideal for implementing interactive services, such as web and mobile backends, latency-sensitive microservices, or synchronous APIs."[8]

 

*   [AWS Serverless Application Model](http://docs.aws.amazon.com/lambda/latest/dg/deploying-lambda-apps.html#serverless_app) - Natively supported with CloudFormation
*   [Apex](http://apex.run/) - Go/Java/JavaScript/Python/(Others) - Hookable build process, supports deploying infrastructure using Terraform - Go
*   [Chalice](https://github.com/awslabs/chalice) - Python2.7 - Written by AWS, still in preview - Python
*   [Gordon](https://github.com/jorgebastida/gordon) - Go/Java/JavaScript/Python/Scala - Automatically packages dependencies, integration with pip/npm/gradle, Deploys resources using CloudFormation - Python
*   [Serverless](https://github.com/serverless/serverless) - Java/JavaScript/Python/Scala - Lots of Plugins, Deploys resources using CloudFormation - JavaScript
*   [Zappa](https://github.com/Miserlou/Zappa) - Python
*   [Backand](https://www.backand.com) - Node.JS/JavaScript - A serverless development platform built to make AWS Lambda easier. Create your own Lambda functions, or connect your AWS account to use your Lambda functions in the Lambda Launcher tool, providing easy access to running your Lambda functions
*   [FuseLess](https://fuseless.org) - CFML/ColdFusion - a toolkit for running Lambda functions written in CFML.

[](#reference-architectures)Reference Architectures
---------------------------------------------------

*   [lambda-refarch-webapp](https://github.com/awslabs/lambda-refarch-webapp/tree/master/lambda-functions) - Java - Java Webapp
*   [lambda-refarch-mobilebackend](https://github.com/awslabs/lambda-refarch-mobilebackend) - JavaScript - Mobile App Backend
*   [lambda-refarch-mapreduce](https://github.com/awslabs/lambda-refarch-mapreduce) - JavaScript/Python - Running MapReduce jobs on Lambda
*   [aws-serverless-auth-reference-app](https://github.com/awslabs/aws-serverless-auth-reference-app) - TypeScript - App and Backend API with Authentication and Authorization
*   [lambda-refarch-iotbackend](https://github.com/awslabs/lambda-refarch-iotbackend) - JavaScript - IoT Backend
*   [lambda-refarch-fileprocessing](https://github.com/awslabs/lambda-refarch-fileprocessing) - JavaScript - Real-time File Processing
*   [lambda-refarch-streamprocessing](https://github.com/awslabs/lambda-refarch-streamprocessing) - JavaScript - Real-time Stream Processing

[](#functions)Functions
-----------------------

*   [WAV to MP3 Email Transcoder](https://github.com/jrstarke/email-audio-convert) - Python - Converts WAV attachments to MP3 before forwarding them
*   [File Based AWS WAF Updater](https://github.com/SilkStart/lambda-functions/tree/master/waf-file-based-ip-set) - Python - Updates a WAF list based on changes to a block file
*   [Kinesis Streams to Kinesis Firehose](https://github.com/awslabs/lambda-streams-to-firehose) - JavaScript - Pushes all events passing through a Kinesis Stream on to a Kinesis Firehose
*   [CloudFront Security Group Updater](https://github.com/SilkStart/aws-cloudfront-samples/tree/master/update_security_groups_lambda) - Python - Updates a security group based on all CIDRs for CloudFront Endpoints
*   [Congrats You Broke The Build](https://github.com/nikolalsvk/congrats-you-broke-the-build) - Node.js - AWS Lambda function for notifying a user who breaks the build on Semaphore CI
*   [Slack Police](https://medium.com/@farski/learn-aws-api-gateway-with-the-slack-police-ca8d636e9fc0#.8txdk7mph) - Javascript - Using API Gateway & Lambda to create a "ok lets move this coversation" slash command in Slack.
*   [Slack Channel as a AWS SNS Subscriber](https://medium.com/cohealo-engineering/how-set-up-a-slack-channel-to-be-an-aws-sns-subscriber-63b4d57ad3ea#.8wdbdzllh) - Javascript - Ping Slack when an Elastic Beanstalk deploy happens via SNS & Lambda
*   [Cloudwatch Alarms to Slack](http://notes.webutvikling.org/send-aws-cloudwatch-alarms-to-slack/) - Javascript (really the Lambda itself is this gist: [https://gist.github.com/tomfa/b33f768908b0a83987d26f269e377e95](https://gist.github.com/tomfa/b33f768908b0a83987d26f269e377e95)). Send Cloudwatch alerts to a Slack channel
*   [Slack Integration Blueprints for AWS Lambda](https://aws.amazon.com/blogs/aws/new-slack-integration-blueprints-for-aws-lambda/) - Python & Others - using AWS Lambda to power chatops
*   [AWS Server Chatbot Sample](https://github.com/awslabs/aws-serverless-chatbot-sample) - Python/JavaScript - A sample to get you started with your own Slackbot lambda integration
*   [CloudTrail Deactivation Remediation](https://github.com/awslabs/aws-security-automation/tree/master/CloudTrailRemediation) - Python - Automatically remediate CloudTrail Deactivations
*   [AWS CIS Benchmark Compliance Check](https://github.com/awslabs/aws-security-benchmark) - Python - A Lambda for benchmarking checking compliance against the AWS CIS Benchmark
*   [Express Application Example](https://github.com/awslabs/aws-serverless-express) - JavaScript - A Library and example on how to run an Express application on Lambda
*   [CRUD Example](https://github.com/awslabs/aws-serverless-crud-sample) - JavaScript - Mobile Backend for movies Database
*   [Configuration Management](https://github.com/awslabs/lambda-runcommand-configuration-management) - Python - Execute RunCommand from Lambda to perform SSHless Server Configuration Management
*   [Alexa skill for running Lambda functions](https://github.com/backand/alexa_function_runner_skill) - Node.js - Allows for execution of arbitrary Lambda functions using Backand.
*   [Alexa restaurant lambda skill](https://github.com/backand/alexa_lambda_skill_demo) - Node.js - Three Lambda functions that can be used to implement a simple restaurant-related Alexa conversation. Hits Yelp and OpenTable APIs.
*   [PBKDF2 hash Validator](http://dchua.com/2016/03/22/writing-a-serverless-python-microservice-with-aws-lambda-and-aws-api-gateway/) - More of a tutorial than a real Lambda example, but gives a good overview of putting a lambda behind API Gateway to quickly build a very scalable web API.
*   [AWS Lambda Test Runner](https://github.com/automatictester/lambda-test-runner) - Java - Runs your unit tests with Maven or SBT directly on AWS Lambda.
*   [AWS IoT Button logger to git](https://github.com/kachkaev/aws-iot-button-logger-to-git/) - TypeScript + git binary - Logs events from IoT devices into a git repository of your choice. Beginner-friendly, highly customisable.