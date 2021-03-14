
<a href="https://github.com/chalice-dev/awesome-chalice"><img alight="right" src="https://end4gy838edhwnq.m.pipedream.net" align="right" height="20"></a><a href="https://github.com/aws/chalice"><img src="https://user-images.githubusercontent.com/80226595/110259005-4ec13080-7f5a-11eb-98eb-f84dbac2c736.png" height="20" align="right"></a><a href="https://github.com/sindresorhus/awesome"><img src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg" align="right" height="20"></a>[![Analytics](https://ga-beacon.appspot.com/UA-191636151-1/awesome-chalice?useReferer&pixel)](https://github.com/igrigorik/ga-beacon)
# Awesome AWS Chalice 
[AWS Chalice](https://aws.github.io/chalice/)<a href="https://aws.github.io/chalice/"><img src="https://aws.github.io/chalice/_static/img/chalice-logo-icon-small.png" height="20"></a> (join us in our [community Slack channel](https://join.slack.com/t/chalicedev/shared_invite/zt-naadmddi-MRwgFq40Ge3qfcPJR_RaDQ)) is Amazon Web Services' premier solution to writing infinitely scalable serverless Python applications based on AWS Lambda. Chalice provides an extensible build process via <code>chalice generate-pipeline</code>, allowing you to orchestrate the deployment (<code>chalice deploy</code>) of any dependencies or outputs, such as infrastructure code written in the CDK, executable artifacts, backend APIs or front-end applications. Chalice is suited for:
- Writing https APIs that wrap infrastructure on AWS.
- Building libraries of Ops functions (DevOps, DevSecOps, NetDevOps, NetOps, NetSecOps, CI/CD Pipeline, ChatOps, etc.).
- Managing AWS accounts programatically.
- Creating web applications with your favorite front-end toolkit (or AWS Amplify).
- Providing the web API backend layer to cross-platform Win/Mac/Linux/Android/iOS desktop and mobile applications written in Qt for Python (PySide6).

Chalice's design is based on decorators. It is written by the AWS Chalice team. Think of Chalice as your primary entry point to whatever it is that you want to do on AWS, or in the cloud.

## AWS Projects
- [AWS Cloud Development Kit (CDK)](https://aws.amazon.com/cdk/) `aws.amazon.com`
  - The AWS CDK is written in Javascript and, via JSii, is available to Python. With the <code>chalice-cdk</code> CDK Construct for Chalice you can deploy your Chalice application via `cdk deploy`. Alternately, with Chalice's <code>chalice generate-pipeline</code> extensible build process, you can deploy your CDK infrastructure when you deploy your Chalice application. In other words, you can either use the CDK to deploy your Chalice application, or use Chalice to deploy your CDK application. If you primarily write Chalice applications, you can use the CDK primarily for deploying your infrastructure layer. 
- [AWS Solutions Constructs Patterns](https://aws.amazon.com/solutions/constructs/patterns/) `aws.amazon.com`
  - These are vetted architectural patterns for the AWS CDK that allow you to easily chain together multiple products per solutions construct, and to also chain those patterns together. Many of the patterns are serverless in nature.
- [AWS Serverless Application Repository](https://serverlessrepo.aws.amazon.com/applications) `aws.amazon.com`
  - Weave these serverless applications into your Chalice application, such as the [AthenaDynamoDBConnector](https://serverlessrepo.aws.amazon.com/applications/us-east-1/292517598671/AthenaDynamoDBConnector) which allows you to query DynamoDB using SQL via Athena. Take note that while many are published by AWS teams, some of these applications are published by third parties and should be evaluated before being put into production.
- [JSii](https://github.com/aws/jsii) `GitHub`
  - JSii is the library that enables the AWS CDK to generalize from Javascript to Python. You can use JSii to call CDK code that may not have been interfaced to Python in a CDK Construct yet.
- [DynamoDB Global Tables](https://aws.amazon.com/dynamodb/global-tables/) `aws.amazon.com`
  - A fully managed extension to DynamoDB for global NoSQL scale-out of your Chalice application. 
- [Aurora Serverless Global Database 2](https://aws.amazon.com/rds/aurora/serverless/) `aws.amazon.com`
  - A serverless OLTP database for your Chalice application that scales out to hundreds of thousands of transactions per second, with secondary cluster replications in up to 5 regions. Rumor has it that it runs Amazon.com.
- [AWS Amplify](https://docs.amplify.aws/) `docs.amplify.aws`
  - In particular the [Amplify UI Components](https://docs.amplify.aws/ui), written in Javascript. Chalice makes it easy to create routing-based APIs that wrap the heavy lifting, while Amplify helps with the front-end Javascript, such as reactive programming based on React. You can use Chalice's [built-in support for authorization via Cognito user pools](https://aws.github.io/chalice/topics/authorizers.html), and you can pair Amplify's support for GraphQL with the [Chalice-GraphQL](https://github.com/jrbeilke/chalice-graphql) 3rd-party library. You can also use Amplify CLI to deploy your Chalice application. 
- [Amazon Athena Federated Query](https://docs.aws.amazon.com/athena/latest/ug/connect-to-a-data-source.html) `docs.aws.amazon.com`
  - This allows you to write Athena -data source connector- Lambda functions that can be used to query across hybrid data sources achieving a mesh topology for your ad-hoc Data Lake. You can write these data source connectors with Chalice using its ability to create [pure Lambda functions](https://aws.github.io/chalice/topics/purelambda), and run your federated queries from Chalice in SQL using a third party module such as [SQLAlchemy](https://www.sqlalchemy.org/).

## AWS Python SDKs
- [AWS SDK for Python (boto3)](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html) `boto3.amazonaws.com`
  - In addition to providing Python interfaces to most AWS services, Amazon will often release setup/teardown code for new services as boto3 scripts (i.e. [AWS Detective](https://github.com/aws-samples/amazon-detective-multiaccount-scripts) and [AWS GuardDuty](https://github.com/aws-samples/amazon-guardduty-multiaccount-scripts/blob/master/enableguardduty.py)) before they are available in CloudFormation or the CDK. You can modify these scripts to be run from Chalice. There is also an -asynchronous- version of boto3 available, [aioboto3](https://github.com/terrycain/aioboto3), that is compatible with Python 3's built-in  <code>async</code> and <code>await</code> asynchronous programming keywords. With aioboto3 you can, for example, perform massively parallel writes and reads to S3 or DynamoDB.
- [AWS X-Ray SDK for Python](https://docs.aws.amazon.com/xray/latest/devguide/xray-sdk-python.html)  `docs.aws.amazon.com`
  - The X-Ray SDK for Python is a must have for using the X-Ray console to trace and visualize your Chalice-based microservices architecture. In addition, this SDK can dynamically instrument tracing into other libraries that are useful for Chalice, such as [boto3](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html), [aioboto3](https://aioboto3.readthedocs.io/en/latest/usage.html), [pynamodb](https://github.com/pynamodb/PynamoDB), [sqlite3](https://docs.python.org/3/library/sqlite3.html), [psycopg2](https://www.psycopg.org/), [pymongo](https://pymongo.readthedocs.io/en/stable/) and [PyMySQL](https://github.com/PyMySQL/PyMySQL) using `from aws_xray_sdk.core import patch_all;patch_all();`
- [AWS IoT SDK for Python](https://github.com/aws/aws-iot-device-sdk-python-v2) `GitHub`
  - Add Internet of Things support to your Chalice application. This pairs well with Chalice's [built-in support for events based on Kinesis Streams](https://aws.amazon.com/blogs/developer/aws-chalice-now-supports-amazon-kinesis-and-amazon-dynamodb-streams/). There is also a [Python SDK for Greengrass](https://aws.github.io/aws-greengrass-core-sdk-python/), which runs Lambda functions ON Greengrass IoT edge devices. These functions can trigger application logic in Chalice via IoT --> Kinesis Streams.
- [AWS C Common Runtime](https://github.com/awslabs/aws-c-common) `GitHub`
  - The most high performance Python-on-AWS applications may make use of the AWS C Common Runtime, which is written in.. C! You'll need to use the [AWS CRT Python](https://github.com/awslabs/aws-crt-python) module to make the magic happen.
- [AWS Encryption SDK for Python](https://github.com/aws/aws-encryption-sdk-python/) `GitHub`
  - This is a client-side encryption library, meaning a library for using hard encryption hosted by AWS, in your application logic.
- [AWS SageMaker SDK for Python](https://github.com/aws/sagemaker-python-sdk) `GitHub`
  - This SDK allows you to train and deploy machine learning models in Python, from Chalice, in frameworks such as TensorFlow, MXNet, or models that you created in SageMaker. It also supports hosting Apache SparkML models, allowing you to integrate with your AWS EMR cluster.
- [AWS Step Functions Data Science SDK for Python](https://github.com/aws/aws-step-functions-data-science-sdk-python) `GitHub`
  - This SDK is for data scientists who want to create workflows that train and publish machine learning models, as orchestrated by AWS Step Functions, without having to worry about provisioning infrastructure.
- [AWS Braket SDK for Python](https://github.com/aws/amazon-braket-sdk-python) `GitHub`
  - This SDK allows you to interact with D-Wave quantum computing devices on AWS Braket from Chalice, enabling applications from quantum annealing to random number generation.
- [AWS DynamoDB Encryption SDK for Python](https://github.com/aws/aws-dynamodb-encryption-python) `GitHub`
  - This client-side SDK helps you encrypt your sensitive data before sending it to DynamoDB.

## AWS Samples for Python
AWS Samples are example solution architectures created by AWS and published on GitHub. Here is [the complete list of 500+ Python samples](https://github.com/aws-samples?q=&type=&language=python&sort=). This section contains the best serverless samples, which you can use as inspiration.

- [AWS Control Tower Account Creation Automation](https://github.com/aws-samples/aws-control-tower-automate-account-creation) `GitHub`
- [AWS Serverless Ecommerce Platform](https://github.com/aws-samples/aws-serverless-ecommerce-platform) `GitHub`
- [Recurring Security Hub Summary Email](https://github.com/aws-samples/aws-security-hub-summary-email) `GitHub`
- [SQS dead letter queue replay with backoff and jitter](https://github.com/aws-samples/amazon-sqs-dlq-replay-backoff) `GitHub`
- [Tokenization and Encryption of Sensitive Data](https://github.com/aws-samples/aws-serverless-tokenization) `GitHub`
- [AWS ParallelCluster serverless API](https://github.com/aws-samples/aws-parallelcluster-serverless-api) `GitHub`
- [Amazon WorkMail Lambda Templates](https://github.com/aws-samples/amazon-workmail-lambda-templates) `GitHub`
- [S3 Glacier Bulk Retrieval](https://github.com/aws-samples/s3-glacier-bulk-retrieval) `GitHub`
- [AutoML with AutoGluon, Amazon SageMaker, and AWS Lambda](https://github.com/aws-samples/automl-pipeline-with-autogluon-sagemaker-lambda) `GitHub`
- [Processing ML Workloads asynchronously in Batch using SageMaker Batch Transform](https://github.com/aws-samples/aws-asynchronous-ml-processing) `GitHub`
- [Serverless Tracking Pixel](https://github.com/aws-samples/aws-serverless-tracking-pixel) `GitHub`
- [Serverless Reference Architecture: Real-time File Processing](https://github.com/aws-samples/lambda-refarch-fileprocessing) `GitHub`
- [Serverless Reference Architecture: IoT Backend](https://github.com/aws-samples/lambda-refarch-iotbackend) `GitHub`
- [AWS X-Ray Serverless Samples](https://github.com/aws-samples/aws-xray-serverless-samples) `GitHub`

## AWS Labs
Sample serverless solution architectures code in Python from AWS Labs, which tends to be more feature complete than AWS Samples.
- [Serverless Data Lake Framework (SDLF)](https://github.com/awslabs/aws-serverless-data-lake-framework) `GitHub`
- [Media Insights Engine](https://github.com/awslabs/aws-media-insights-engine) `GitHub`
- [Serverless Transit Network Orchestrator](https://github.com/awslabs/serverless-transit-network-orchestrator) `GitHub`
- [Amazon Aurora Postgres Advanced Monitoring](https://github.com/awslabs/amazon-aurora-postgres-monitoring) `GitHub`
- [AWS Serverless Twitter Event Source](https://github.com/awslabs/aws-serverless-twitter-event-source) `GitHub`
- [Serverless Subtitles](https://github.com/awslabs/serverless-subtitles) `GitHub`
- [AWS Serverless Financial Functions](https://github.com/awslabs/aws-serverless-financial-functions) `GitHub`

## 3rd Party Tools
- [PynamoDB: A Pythonic wrapper for DynamoDB](https://github.com/pynamodb/PynamoDB) `GitHub`
  - PynamoDB is a pythonic interface to DynamoDB for data modelling. Example: [terraform-registry](https://github.com/zeroae/terraform-registry). `GitHub`
- [PySide6](https://www.qt.io/blog/qt-for-python-6-released) `qt.io`
  - PySide6 is the official Qt module for Python, for writing cross-platform Win/Mac/Linux/Android/iOS applications. With PySide6 and [QtQuick](https://doc-snapshots.qt.io/qt6-dev/qtquick-index.html) you can very quickly write desktop Python applications that integrate with Chalice. You can use Chalice to authenticate via Cognito user pools, and to write an API layer for your application that is backed by any AWS service. You can use Chalice's extensible build system to create and publish cross-platform Qt executables.
- [Hy: A lisp written in Python](https://docs.hylang.org/en/master/tutorial.html) `hylang.org`
  - Hy is a multi-paradigm general-purpose programming language in the Lisp family, inspired by Clojure and written in Python. You can use it to pipeline Chalice λ functions together (functional programming), achieving lambda-based programming that is as effortless as Bash pipelines on the Linux command line. You can mix Hy and Python in the same file.
- [Toolz: A set of utility functions for iterators, functions, and dictionaries](https://github.com/pytoolz/toolz) `GitHub`
  - Toolz is a python module that allows you to import functional programming primitives, going beyond Python's built-in map-reduce-filter idioms.

## Tooling for Writing Chalice Code
- [Lucidchart](https://lucid.app/) `lucid.app`
  - Lucid is the premier tool for hand-crafting AWS Solutions Architecture diagrams. They have the 2017 and 2019 AWS icon packs by default, and you can also [download the latest AWS Architecture Icons from Amazon](https://aws.amazon.com/architecture/icons/) and upload them to Lucidchart.
- [AWS Toolkit for PyCharm](https://aws.amazon.com/pycharm/) `aws.amazon.com`
  - Amazon has thrown its weight behind the [PyCharm IDE](https://www.jetbrains.com/pycharm/) with this AWS Toolkit, which enables you to seamlessly switch between accounts, to use a proxy, and other features, from inside the PyCharm editor. There is also the [AWS Toolkit for VSCode](https://aws.amazon.com/visualstudiocode/), [IntelliJ IDEA](https://aws.amazon.com/intellij/), [Eclipse](https://aws.amazon.com/eclipse/) and [JetBrains](https://docs.aws.amazon.com/toolkit-for-jetbrains/).
- [Anaconda Python Distribution](https://www.anaconda.com/products/individual/download-success). `anaconda.com`
  - Anaconda provides a consistent Python development environment. You can use Anaconda on AWS Lambda if you [mount an EFS filesystem](https://docs.aws.amazon.com/efs/latest/ug/mounting-fs.html) that has it, or if you [use a container image](https://aws.amazon.com/blogs/aws/new-for-aws-lambda-container-image-support/) for your Lambda functions. This is not yet tightly integrated with Chalice, however, it works very well for local development.

## Blog Posts and Feature Releases
- `02-2021` [Amplify Flutter is Now Generally Available: Build Beautiful Cross-Platform Apps](https://aws.amazon.com/blogs/aws/amplify-flutter-is-now-generally-available-build-beautiful-cross-platform-apps/) `AWS Blog`
- `02-2021` [Using container images to run PyTorch models in AWS Lambda](https://aws.amazon.com/blogs/machine-learning/using-container-images-to-run-pytorch-models-in-aws-lambda/) `AWS Blog`
- `01-2021` [AWS Chalice adds support for the AWS CDK](https://aws.amazon.com/blogs/developer/aws-chalice-adds-support-for-the-aws-cdk/) `AWS Blog`
- `12-2020` [Packaging AWS Lambda functions as container images](https://acloudguru.com/blog/engineering/packaging-aws-lambda-functions-as-container-images) `A Cloud Guru`
- `12-2020` [New for AWS Lambda – 1ms Billing Granularity Adds Cost Savings](https://aws.amazon.com/blogs/aws/new-for-aws-lambda-1ms-billing-granularity-adds-cost-savings/) `AWS Blog`
- `12-2020` [Implementing version control using Amazon DynamoDB](https://aws.amazon.com/blogs/database/implementing-version-control-using-amazon-dynamodb/) `AWS Blog`
  - Includes code on `GitHub`: [Amazon DynamoDB Design Patterns](https://github.com/aws-samples/amazon-dynamodb-design-patterns)
- `10-2020` [AWS Lambda Extensions: What are they and why do they matter](https://lumigo.io/blog/aws-lambda-extensions-what-are-they-and-why-do-they-matter/) `Lumigo`
  - Extensions allow you to monitor your Lambda functions, such as CPU and network utilization.
- `10-2020` [AWS Chalice now supports Amazon Kinesis and Amazon DynamoDB Streams](https://aws.amazon.com/blogs/developer/aws-chalice-now-supports-amazon-kinesis-and-amazon-dynamodb-streams/) `AWS Blog`
  - By integrating Chalice with DynamoDB streams, you can create sophisticated business logic using DynamoDB's ablity to trigger lambda functions based on events.
- `09-2020` [Using AWS Lambda Layers with AWS Chalice](https://aws.amazon.com/blogs/developer/using-aws-lambda-layers-with-aws-chalice/) `AWS Blog`
  - With automatic lambda layers, you don't have to wait for your large lambda layer to upload every time you deploy your application.
- `08-2020` [Following serverless best practices with AWS Chalice and Lambda Powertools](https://aws.amazon.com/blogs/developer/following-serverless-best-practices-with-aws-chalice-and-lambda-powertools/) `AWS Blog`
  - Allows you to ie trace with AWS X-Ray, and to create middleware - code that is called before, during and after each lambda invocation.
- `08-2020` [Automatically deploy a Serverless REST API from GitHub with AWS Chalice](https://aws.amazon.com/blogs/developer/automatically-deploy-a-serverless-rest-api-from-github-with-aws-chalice/) `AWS Blog`
- `07-2020` [Creating low-latency, high-volume APIs with Provisioned Concurrency](https://aws.amazon.com/blogs/compute/creating-low-latency-high-volume-apis-with-provisioned-concurrency/) `GitHub`
  - Chalice does not yet support Provisioned Concurrency out of the box, [but it plans to.](https://github.com/aws/chalice/issues/1322) `GitHub`
- `07-2020` [Configuring custom domain names with AWS Chalice](https://aws.amazon.com/blogs/developer/configuring-custom-domain-names-with-aws-chalice/) `AWS Blog`
- `06-2020` [AWS Chalice Now Supports YAML Templates](https://aws.amazon.com/blogs/developer/aws-chalice-now-supports-yaml-templates/) `AWS Blog`
  - Allows you to deploy Chalice using the AWS Serverless Application model, for integration with CloudFormation.
- `06-2020` [AWS Solutions Constructs – A Library of Architecture Patterns for the AWS CDK](https://aws.amazon.com/blogs/aws/aws-solutions-constructs-a-library-of-architecture-patterns-for-the-aws-cdk/) `AWS Blog`
- `06-2020` [Using Amazon EFS for AWS Lambda in your serverless applications](https://aws.amazon.com/blogs/compute/using-amazon-efs-for-aws-lambda-in-your-serverless-applications/) `AWS Blog`
  - A building block for mounting an Elastic File System with Chalice, which should be combined with CDK support.
- `05-2020` [Introducing the AWS Chalice test client](https://aws.amazon.com/blogs/developer/introducing-the-new-test-client-for-aws-chalice/) `AWS Blog`
- `04-2020` [Use Amazon DynamoDB Accelerator (DAX) from AWS Lambda to increase performance while reducing costs](https://aws.amazon.com/blogs/database/how-to-increase-performance-while-reducing-costs-by-using-amazon-dynamodb-accelerator-dax-and-aws-lambda/) `GitHub`
- `02-2020` [Painless AWS Chalice Application Debug](https://medium.com/cyberark-engineering/painless-aws-chalice-application-debug-90534e33cf76) `Medium`
- `03-2019` [Modularizing a Chalice Application for Teams](https://medium.com/tensoriot/modularizing-a-chalice-application-for-teams-f716f496b94b) `Medium`
  - How to leverage the `chalicelib` directory to enable a team of developers to work on Chalice.
- `03-2019` [Run your Python Scripts as Slack Commands (ChatOps)](https://medium.com/@yogeshingale94/run-your-python-scripts-as-slack-commands-chatops-63bc334b74cd) `Medium`
- `12-2018` [Building Serverless Python Apps Using AWS Chalice](https://realpython.com/aws-chalice-serverless-python/) `Real Python Blog`

## Built on Chalice
- `current` [Coworks Microframework](https://github.com/gdoumenc/coworks)
  - Coworks is a complete microservices framework for Chalice that utilizes AWS Step Functions for implementing business logic, as an alternative to DynamoDB event triggers.
- `current` [Agave: REST API for Chalice BluePrints](https://github.com/cuenca-mx/agave)
- `current` [aws-chalice-swagger: AWS Chalice template project with Swagger UI](https://github.com/samuelkhtu/aws-chalice-swagger) `GitHub`
  - Chalice comes with Swagger support, this project shows you how to use it.
- `01-2021` [Lambda Multi-threading in Chalice](https://github.com/vumdao/multithread-in-lambda) `GitHub` ![#2BBA9C](https://via.placeholder.com/15/2BBA9C/000000?text=+)
  - Lambda functions can have up to 6 vCPU cores and 10GB RAM, this simple example shows how to use a map/reduce across cores in Chalice.
- `12-2020` [chalice-cicd-app: Deploy Chalice using AWS CodeStar via the AWS CDK](https://github.com/folksgl/chalice-cicd-app) `GitHub`
- `11-2020` [aws-chalice-boilerplate](https://github.com/GabrielTavares99/aws-chalice-boilerplate) `GitHub`
  - Among other things, demonstrates how to use `chalice.cli.CLIFactory`.
- `11-2020` [chalice_dockerized: How to deploy Chalice with docker-compose](https://github.com/vanderlvoff/chalice_dockerized) `GitHub`
- `11-2020` [Chalice-GraphQL: Adds Facebook's GraphQL support to your Chalice application](https://github.com/jrbeilke/chalice-graphql)
- `11-2020` ~~[Chalice + LocalStack (doesn't work yet)](https://github.com/localstack/chalice-local)~~
- `08-2020` [chalice-extended-action: Automated deployment of your Chalice application via GitHub Actions](https://github.com/jayef0/chalice-extended-action) `GitHub`
- `06-2020` [pytest-chalice: A set of py.test fixtures for AWS Chalice](https://github.com/studio3104/pytest-chalice)
- `02-2020` [chalice-cognito-auth: A library for setting up login routes in a Chalice app](https://github.com/stealthycoin/chalice-cognito-auth)  ![#2BBA9C](https://via.placeholder.com/15/2BBA9C/000000?text=+)
  - Connect Chalice to a Cognito user pool for single-sign on (SSO).
- `10-2019` [Domovoi - Extension to Chalice that supports Automatic Load Balancing](https://github.com/cloud-utils/domovoi) `GitHub`
- `01-2019` [Damn Vulnerable Functions as a Service](https://github.com/we45/DVFaaS-Damn-Vulnerable-Functions-as-a-Service) `GitHub`
  - Example insecure FaaS repository built on Chalice

# Miscellaneous Awesomeness

## Stack Overflow
- `10-2020` [Using APISpec to enable using Swagger with Chalice](https://stackoverflow.com/questions/63048401/any-framework-or-tool-is-available-to-achieve-swagger-definition-as-the-auto-gen)
- `09-2020` [AWS IAM Policy required for AWS Chalice](https://stackoverflow.com/questions/63781304/aws-iam-policy-required-for-aws-chalice)
- `07-2020` [Calling a Lambda from a Lambda in Chalice without going through API Gateway again](https://stackoverflow.com/questions/62815740/how-to-directly-invoke-a-chalice-lambda-from-another-lambda-without-going-throug)

## Chalice Documentation

- [How to create pure Lambda functions in Chalice](https://aws.github.io/chalice/topics/purelambda)
- [Continuous Deployment with Chalice](https://aws.github.io/chalice/topics/cd) ![#2BBA9C](https://via.placeholder.com/15/2BBA9C/000000?text=+)
  - Chalice has support for dev/stage/prod out-of-the-box, in addition to CodeBuild, CodeDeploy and CodePipeline.
- [Configuration File](https://aws.github.io/chalice/topics/configfile.html) ![#2BBA9C](https://via.placeholder.com/15/2BBA9C/000000?text=+)
  - By setting `api_gateway_endpoint_type` you can deploy into a VPC. 

## Paid Tracing
- [sentry-python: application monitoring platform to diagnose, fix, and optimize code performance](https://github.com/getsentry/sentry-python/blob/af163ff176b2c22952443dc5ec535aed98656fc2/tests/integrations/chalice/test_chalice.py) `GitHub`
- [Lumigo Python agent for distributed tracing and performance monitoring](https://github.com/lumigo-io/python_tracer/blob/1ab55406befe494aa61384576339b49a1e681623/src/lumigo_tracer/examples/chalice.py) `GitHub`
- [IOpipe Analytics & Distributed Tracing Agent for Python](https://github.com/iopipe/iopipe-python#chalice) `GitHub`

## Videos
- `10-2020` [Building your first REST API with AWS’s Open Data Sets and Chalice - Christian Weber](https://www.youtube.com/watch?v=VKUoL3IL3-w) `YouTube`
- `09-2020` [AWS Chalice Hands-On Walkthrough, a Python Serverless Microframework for AWS](https://www.youtube.com/watch?v=q3eayufwmMg) `YouTube`
- `04-2019` [Udemy Online Course - AWS Chalice : Build Serverless REST APIs on AWS](https://www.udemy.com/course/aws-chalice-build-serverless-rest-apis-on-aws/?ranMID=39197&ranEAID=Gw%2FETjJoU9M&ranSiteID=Gw_ETjJoU9M-gPreRA73w_.wS1U96fuiKw&utm_source=aff-campaign&utm_medium=udemyads&LSNPUBID=Gw%2FETjJoU9M) `Udemy`

## Support
- [chalice.dev Slack channel](https://chalice.dev/) `chalice.dev`
- [cdk.dev Slack channel](https://cdk.dev/) `cdk.dev`

## Misc
- [Steampipe](https://steampipe.io/) `steampipe.io` ![#2BBA9C](https://via.placeholder.com/15/2BBA9C/000000?text=+)
  - Steampipe allows you to query your AWS infrastructure, IAM policies, etc., using SQL. 
- [Click](https://click.palletsprojects.com/en/7.x/) `PalletsProjects` ![#2BBA9C](https://via.placeholder.com/15/2BBA9C/000000?text=+)
  - You can pair Flask's Click project to decorate your Chalice apps so as to have a CLI.
- [AWS CDK Patterns](https://github.com/cdk-patterns/serverless) `GitHub` ![#2BBA9C](https://via.placeholder.com/15/2BBA9C/000000?text=+)
