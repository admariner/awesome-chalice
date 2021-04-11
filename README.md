<a href="https://github.com/chalice-dev/awesome-chalice"><img alight="right" src="https://end4gy838edhwnq.m.pipedream.net" align="right" height="20"></a><a href="https://github.com/aws/chalice"><img src="https://user-images.githubusercontent.com/80226595/110259005-4ec13080-7f5a-11eb-98eb-f84dbac2c736.png" height="20" align="right"></a><a href="https://github.com/sindresorhus/awesome"><img src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg" align="right" height="20"></a>[![Analytics](https://ga-beacon.appspot.com/UA-191636151-1/awesome-chalice?useReferer&pixel)](https://github.com/igrigorik/ga-beacon)
# Awesome Chalice
> List of resources for using AWS Chalice

[AWS Chalice](https://aws.github.io/chalice/)<a href="https://aws.github.io/chalice/"><img src="https://aws.github.io/chalice/_static/img/chalice-logo-icon-small.png" height="20"></a> (join us in our [community Slack channel](https://join.slack.com/t/chalicedev/shared_invite/zt-naadmddi-MRwgFq40Ge3qfcPJR_RaDQ)) is Amazon Web Services' premier solution to writing infinitely scalable serverless Python applications based on AWS Lambda. Chalice provides an extensible build process via <code>chalice generate-pipeline</code>, allowing you to orchestrate the deployment (<code>chalice deploy</code>) of any dependencies or outputs, such as infrastructure code written in the CDK, executable artifacts, backend APIs or front-end applications. Chalice is suited for:
- Writing https APIs that wrap infrastructure on AWS.
- Building libraries of Ops functions (DevOps, DevSecOps, NetDevOps, NetOps, NetSecOps, CI/CD Pipeline, ChatOps, etc.).
- Managing AWS accounts programmatically.
- Creating web applications with your favorite front-end toolkit, just as [jQuery UI](https://jqueryui.com/) or [AWS Amplify](https://aws.amazon.com/amplify/).
- Providing the web API backend layer to cross-platform Win/Mac/Linux/Android/iOS desktop and mobile applications written in Qt for Python (PySide6).

Chalice's design is based on decorators. It is written by the AWS Chalice team. Think of Chalice as your primary entry point to whatever it is that you want to do on AWS, or in the cloud.

## Contents
- [AWS Projects](#aws-projects)
- [AWS Python SDKs](#aws-python-sdks)
- [AWS Samples for Python](#aws-samples-for-python)
- [AWS Labs](#aws-labs)
- [3rd Party Tools](#3rd-party-tools)
- [Tooling for Writing Chalice Code](#tooling-for-writing-chalice-code)
- [Blog Posts and Feature Releases](#blog-posts-and-feature-releases)
- [Built on Chalice](#built-on-chalice)
- [Miscellaneous Awesomeness](#miscellaneous-awesomeness)

## AWS Projects
- [AWS Data Wrangler](https://github.com/awslabs/aws-data-wrangler) - "Pandas on AWS": *Easy integration with Athena, Glue, Redshift, Timestream, QuickSight, Chime, CloudWatchLogs, DynamoDB, EMR, SecretManager, PostgreSQL, MySQL, SQLServer and S3 (Parquet, CSV, JSON and EXCEL).*
- [AWS SDK for JavaScript](https://aws.amazon.com/sdk-for-javascript/) - With the AWS SDK for JavaScript, you can authenticate your users on the front-end using Cognito, and from there code up a management interface for much of AWS. Note however that not all AWS services are supported yet. You can see which servics are supported in [aws-sdk-js/clients/all.js](https://github.com/aws/aws-sdk-js/blob/master/clients/all.js).
- [AWS Cloud Development Kit (CDK)](https://aws.amazon.com/cdk/) - The AWS CDK is written in JavaScript and, via JSii, is available to Python. With the <code>chalice-cdk</code> CDK Construct for Chalice you can deploy your Chalice application via `cdk deploy`. Alternately, with Chalice's <code>chalice generate-pipeline</code> extensible build process, you can deploy your CDK infrastructure when you deploy your Chalice application. In other words, you can either use the CDK to deploy your Chalice application, or use Chalice to deploy your CDK application. If you primarily write Chalice applications, you can use the CDK primarily for deploying your infrastructure layer.
- [AWS Solutions Constructs Patterns](https://aws.amazon.com/solutions/constructs/patterns/) - These are vetted architectural patterns for the AWS CDK that allow you to easily chain together multiple products per solutions construct, and to also chain those patterns together. Many of the patterns are serverless in nature.
- [AWS Serverless Application Repository](https://serverlessrepo.aws.amazon.com/applications) - Weave these serverless applications into your Chalice application, such as the [AthenaDynamoDBConnector](https://serverlessrepo.aws.amazon.com/applications/us-east-1/292517598671/AthenaDynamoDBConnector) which allows you to query DynamoDB using SQL via Athena. Take note that while many are published by AWS teams, some of these applications are published by third parties and should be evaluated before being put into production.
- [JSii](https://github.com/aws/jsii) - JSii is the library that enables the AWS CDK to generalize from JavaScript to Python. You can use JSii to call CDK code that may not have been interfaced to Python in a CDK Construct yet.
- [DynamoDB Global Tables](https://aws.amazon.com/dynamodb/global-tables/) - A fully managed extension to DynamoDB for global NoSQL scale-out of your Chalice application.
- [Aurora Serverless Global Database 2](https://aws.amazon.com/rds/aurora/serverless/) - A serverless OLTP database for your Chalice application that scales out to hundreds of thousands of transactions per second, with secondary cluster replications in up to 5 regions. Rumor has it that it runs Amazon.com.
- [AWS Amplify](https://docs.amplify.aws/) - In particular the Amplify UI Components, written in JavaScript. Chalice makes it easy to create routing-based APIs that wrap the heavy lifting, while Amplify helps with the front-end JavaScript, such as reactive programming based on React. You can use Chalice's built-in support for authorization via Cognito user pools. You can also use Amplify CLI to deploy your Chalice application.
- [Amazon Athena Federated Query](https://docs.aws.amazon.com/athena/latest/ug/connect-to-a-data-source.html) - This allows you to write Athena "data source connector" Lambda functions that can be used to query across hybrid data sources achieving a mesh topology for your ad-hoc Data Lake. You can write these data source connectors with Chalice using its ability to create pure Lambda functions, and run your federated queries from Chalice in SQL using a third party module such as SQLAlchemy.

## AWS Python SDKs
- [AWS SDK for Python (boto3)](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html) - In addition to providing Python interfaces to most AWS services, Amazon will often release setup/teardown code for new services as boto3 scripts (i.e. AWS Detective and AWS GuardDuty. before they are available in CloudFormation or the CDK. You can modify these scripts to be run from Chalice. There is also an asynchronous version of boto3 available, aioboto3, that is compatible with Python 3's built-in  <code>async</code> and <code>await</code> asynchronous programming keywords. With aioboto3 you can, for example, perform massively parallel writes and reads to S3 or DynamoDB.
- [AWS X-Ray SDK for Python](https://docs.aws.amazon.com/xray/latest/devguide/xray-sdk-python.html) - The X-Ray SDK for Python is a must have for using the X-Ray console to trace and visualize your Chalice-based microservices architecture. In addition, this SDK can dynamically instrument tracing into other libraries that are useful for Chalice, such as boto3, aioboto3, pynamodb, sqlite3, psycopg2, pymongo and PyMySQL using `from aws_xray_sdk.core import patch_all;patch_all();`.
- [AWS IoT SDK for Python](https://github.com/aws/aws-iot-device-sdk-python-v2) - Add Internet of Things support to your Chalice application. This pairs well with Chalice's built-in support for events based on Kinesis Streams. There is also a Python SDK for Greengrass, which runs Lambda functions ON Greengrass IoT edge devices. These functions can trigger application logic in Chalice via IoT --> Kinesis Streams.
- [AWS C Common Runtime](https://github.com/awslabs/aws-c-common) - The most high performance Python-on-AWS applications may make use of the AWS C Common Runtime, which is written in C. You'll need to use the AWS CRT Python module to make the magic happen.
- [AWS Encryption SDK for Python](https://github.com/aws/aws-encryption-sdk-python/) - This is a client-side encryption library, meaning a library for using hard encryption hosted by AWS, in your application logic.
- [AWS SageMaker SDK for Python](https://github.com/aws/sagemaker-python-sdk) - This SDK allows you to train and deploy machine learning models in Python, from Chalice, in frameworks such as TensorFlow, MXNet, or models that you created in SageMaker. It also supports hosting Apache SparkML models, allowing you to integrate with your AWS EMR cluster.
- [AWS Step Functions Data Science SDK for Python](https://github.com/aws/aws-step-functions-data-science-sdk-python) - This SDK is for data scientists who want to create workflows that train and publish machine learning models, as orchestrated by AWS Step Functions, without having to worry about provisioning infrastructure.
- [AWS Braket SDK for Python](https://github.com/aws/amazon-braket-sdk-python) - This SDK allows you to interact with D-Wave quantum computing devices on AWS Braket from Chalice, enabling applications from quantum annealing to random number generation.
- [AWS DynamoDB Encryption SDK for Python](https://github.com/aws/aws-dynamodb-encryption-python) - This client-side SDK helps you encrypt your sensitive data before sending it to DynamoDB.

## AWS Samples for Python
AWS Samples are example solution architectures created by AWS and published on GitHub. Here is [the complete list of 500+ Python samples](https://github.com/aws-samples?q=&type=&language=python&sort=). This section contains the best serverless samples, which you can use as inspiration.

- [AWS Control Tower Account Creation Automation](https://github.com/aws-samples/aws-control-tower-automate-account-creation) 
- [AWS Serverless Ecommerce Platform](https://github.com/aws-samples/aws-serverless-ecommerce-platform)
- [Recurring Security Hub Summary Email](https://github.com/aws-samples/aws-security-hub-summary-email)
- [SQS dead letter queue replay with backoff and jitter](https://github.com/aws-samples/amazon-sqs-dlq-replay-backoff)
- [Tokenization and Encryption of Sensitive Data](https://github.com/aws-samples/aws-serverless-tokenization)
- [AWS ParallelCluster serverless API](https://github.com/aws-samples/aws-parallelcluster-serverless-api)
- [Amazon WorkMail Lambda Templates](https://github.com/aws-samples/amazon-workmail-lambda-templates)
- [S3 Glacier Bulk Retrieval](https://github.com/aws-samples/s3-glacier-bulk-retrieval)
- [AutoML with AutoGluon, Amazon SageMaker, and AWS Lambda](https://github.com/aws-samples/automl-pipeline-with-autogluon-sagemaker-lambda)
- [Processing ML Workloads asynchronously in Batch using SageMaker Batch Transform](https://github.com/aws-samples/aws-asynchronous-ml-processing)
- [Serverless Tracking Pixel](https://github.com/aws-samples/aws-serverless-tracking-pixel)
- [Serverless Reference Architecture: Real-time File Processing](https://github.com/aws-samples/lambda-refarch-fileprocessing)
- [Serverless Reference Architecture: IoT Backend](https://github.com/aws-samples/lambda-refarch-iotbackend)
- [AWS X-Ray Serverless Samples](https://github.com/aws-samples/aws-xray-serverless-samples)

## AWS Labs
Sample serverless solution architectures code in Python from AWS Labs, which tends to be more feature complete than AWS Samples.

- [Serverless Data Lake Framework (SDLF)](https://github.com/awslabs/aws-serverless-data-lake-framework)
- [Media Insights Engine](https://github.com/awslabs/aws-media-insights-engine)
- [Serverless Transit Network Orchestrator](https://github.com/awslabs/serverless-transit-network-orchestrator)
- [Amazon Aurora Postgres Advanced Monitoring](https://github.com/awslabs/amazon-aurora-postgres-monitoring)
- [AWS Serverless Twitter Event Source](https://github.com/awslabs/aws-serverless-twitter-event-source)
- [Serverless Subtitles](https://github.com/awslabs/serverless-subtitles)
- [AWS Serverless Financial Functions](https://github.com/awslabs/aws-serverless-financial-functions)

## 3rd Party Tools
- [3M Falcano](https://github.com/3mcloud/falcano) - Falcano provides a PynamoDB-like interface that allows for single table designs. 
- [PynamoDB: A Pythonic wrapper for DynamoDB](https://github.com/pynamodb/PynamoDB) - PynamoDB is a pythonic interface to DynamoDB for data modelling. Example: [terraform-registry](https://github.com/zeroae/terraform-registry).
- [S3Fs](https://s3fs.readthedocs.io/en/latest/) - A filesystem-like interface to S3 built on `botocore`.
- [PySide6](https://www.qt.io/blog/qt-for-python-6-released) - PySide6 is the official Qt module for Python, for writing cross-platform Win/Mac/Linux/Android/iOS applications. With PySide6 and QtQuick you can very quickly write desktop Python applications that integrate with Chalice. You can use Chalice to authenticate via Cognito user pools, and to write an API layer for your application that is backed by any AWS service. You can use Chalice's extensible build system to create and publish cross-platform Qt executables.
- [Hy: A lisp written in Python](https://docs.hylang.org/en/master/tutorial.html) - Hy is a multi-paradigm general-purpose programming language in the Lisp family, inspired by Clojure and written in Python. You can use it to pipeline Chalice λ functions together (functional programming), achieving lambda-based programming that is as effortless as Bash pipelines on the Linux command line. You can mix Hy and Python in the same file.
- [Toolz: A set of utility functions for iterators, functions, and dictionaries](https://github.com/pytoolz/toolz) - Toolz is a python module that allows you to import functional programming primitives, going beyond Python's built-in map-reduce-filter idioms.
- [AWS Limit Checker](https://github.com/jantman/awslimitchecker) - Python code for automatically detecting when you are about to run up against AWS limits.

## Tooling for Writing Chalice Code
- [Cloudviz](https://cloudviz.io/) - Cloudviz is the software that most AWS employees use to create diagrams.
- [CloudMoji™](https://cloudmoji.com/) - CloudMoji has the 2021 icon packs for AWS, Azure and GCP.
- [AWS Toolkit for PyCharm](https://aws.amazon.com/pycharm/) - Amazon has thrown its weight behind the PyCharm IDE with this AWS Toolkit, which enables you to seamlessly switch between accounts, to use a proxy, and other features, from inside the PyCharm editor. There is also the AWS Toolkit for VSCode, IntelliJ IDEA, Eclipse and JetBrains.
- [Anaconda Python Distribution](https://www.anaconda.com/products/individual/download-success) - Anaconda provides a consistent Python development environment. You can use Anaconda on AWS Lambda if you mount an EFS filesystem that has it, or if you use a container image for your Lambda functions. This is not yet tightly integrated with Chalice, however, it works very well for local development.

## Blog Posts and Feature Releases
- [Python support GA: improving Python code quality using Amazon CodeGuru Reviewer](https://aws.amazon.com/blogs/devops/python-support-ga-improving-python-code-quality-using-amazon-codeguru-reviewer/)
- [Amplify Flutter is Now Generally Available: Build Beautiful Cross-Platform Apps](https://aws.amazon.com/blogs/aws/amplify-flutter-is-now-generally-available-build-beautiful-cross-platform-apps/)
- [Using container images to run PyTorch models in AWS Lambda](https://aws.amazon.com/blogs/machine-learning/using-container-images-to-run-pytorch-models-in-aws-lambda/)
- [AWS Chalice adds support for the AWS CDK](https://aws.amazon.com/blogs/developer/aws-chalice-adds-support-for-the-aws-cdk/)
- [Packaging AWS Lambda functions as container images](https://acloudguru.com/blog/engineering/packaging-aws-lambda-functions-as-container-images)
- [New for AWS Lambda – 1ms Billing Granularity Adds Cost Savings](https://aws.amazon.com/blogs/aws/new-for-aws-lambda-1ms-billing-granularity-adds-cost-savings/)
- [Implementing version control using Amazon DynamoDB](https://aws.amazon.com/blogs/database/implementing-version-control-using-amazon-dynamodb/) - Includes code on `GitHub`: [Amazon DynamoDB Design Patterns](https://github.com/aws-samples/amazon-dynamodb-design-patterns)
- [Introducing Middleware Stack in Modular AWS SDK for JavaScript](https://aws.amazon.com/blogs/developer/middleware-stack-modular-aws-sdk-js/)
- [How do I give internet access to a Lambda function that's connected to an Amazon VPC?](https://aws.amazon.com/premiumsupport/knowledge-center/internet-access-lambda-function/)
- [AWS Lambda Extensions: What are they and why do they matter](https://lumigo.io/blog/aws-lambda-extensions-what-are-they-and-why-do-they-matter/) - Extensions allow you to monitor your Lambda functions, such as CPU and network utilization.
- [AWS Chalice now supports Amazon Kinesis and Amazon DynamoDB Streams](https://aws.amazon.com/blogs/developer/aws-chalice-now-supports-amazon-kinesis-and-amazon-dynamodb-streams/) - By integrating Chalice with DynamoDB streams, you can create sophisticated business logic using DynamoDB's ablity to trigger lambda functions based on events.
- [Using AWS Lambda Layers with AWS Chalice](https://aws.amazon.com/blogs/developer/using-aws-lambda-layers-with-aws-chalice/) - With automatic lambda layers, you don't have to wait for your large lambda layer to upload every time you deploy your application.
- [Following serverless best practices with AWS Chalice and Lambda Powertools](https://aws.amazon.com/blogs/developer/following-serverless-best-practices-with-aws-chalice-and-lambda-powertools/) - Allows you to ie trace with AWS X-Ray, and to create middleware - code that is called before, during and after each lambda invocation.
- [Automatically deploy a Serverless REST API from GitHub with AWS Chalice](https://aws.amazon.com/blogs/developer/automatically-deploy-a-serverless-rest-api-from-github-with-aws-chalice/)
- [Creating low-latency, high-volume APIs with Provisioned Concurrency](https://aws.amazon.com/blogs/compute/creating-low-latency-high-volume-apis-with-provisioned-concurrency/) - Chalice does not yet support Provisioned Concurrency out of the box, [but it plans to.](https://github.com/aws/chalice/issues/1322)
- [Configuring custom domain names with AWS Chalice](https://aws.amazon.com/blogs/developer/configuring-custom-domain-names-with-aws-chalice/)
- [AWS Chalice Now Supports YAML Templates](https://aws.amazon.com/blogs/developer/aws-chalice-now-supports-yaml-templates/) - Allows you to deploy Chalice using the AWS Serverless Application model, for integration with CloudFormation.
- [AWS Solutions Constructs – A Library of Architecture Patterns for the AWS CDK](https://aws.amazon.com/blogs/aws/aws-solutions-constructs-a-library-of-architecture-patterns-for-the-aws-cdk/)
- [Using Amazon EFS for AWS Lambda in your serverless applications](https://aws.amazon.com/blogs/compute/using-amazon-efs-for-aws-lambda-in-your-serverless-applications/) - A building block for mounting an Elastic File System with Chalice, which should be combined with CDK support.
- [Introducing the AWS Chalice test client](https://aws.amazon.com/blogs/developer/introducing-the-new-test-client-for-aws-chalice/)
- [Use Amazon DynamoDB Accelerator (DAX) from AWS Lambda to increase performance while reducing costs](https://aws.amazon.com/blogs/database/how-to-increase-performance-while-reducing-costs-by-using-amazon-dynamodb-accelerator-dax-and-aws-lambda/)
- [Painless AWS Chalice Application Debug](https://medium.com/cyberark-engineering/painless-aws-chalice-application-debug-90534e33cf76)
- [Modularizing a Chalice Application for Teams](https://medium.com/tensoriot/modularizing-a-chalice-application-for-teams-f716f496b94b) - How to leverage the `chalicelib` directory to enable a team of developers to work on Chalice.
- [Getting started with the AWS Cloud Development Kit and Python](https://aws.amazon.com/blogs/developer/getting-started-with-the-aws-cloud-development-kit-and-python/)
- [Run your Python Scripts as Slack Commands (ChatOps)](https://medium.com/@yogeshingale94/run-your-python-scripts-as-slack-commands-chatops-63bc334b74cd)
- [Building Serverless Python Apps Using AWS Chalice](https://realpython.com/aws-chalice-serverless-python/)

## Built on Chalice
- [Coworks Microframework](https://github.com/gdoumenc/coworks) - Coworks is a complete microservices framework for Chalice that utilizes AWS Step Functions for implementing business logic, as an alternative to DynamoDB event triggers.
- [Agave: REST API for Chalice BluePrints](https://github.com/cuenca-mx/agave)
- [aws-chalice-swagger: AWS Chalice template project with Swagger UI](https://github.com/samuelkhtu/aws-chalice-swagger) - Chalice comes with Swagger support, this project shows you how to use it.
- [Lambda Multi-threading in Chalice](https://github.com/vumdao/multithread-in-lambda) - Lambda functions can have up to 6 vCPU cores and 10GB RAM, this simple example shows how to use a map/reduce across cores in Chalice.
- [chalice-cicd-app: Deploy Chalice using AWS CodeStar via the AWS CDK](https://github.com/folksgl/chalice-cicd-app)
- [aws-chalice-boilerplate](https://github.com/GabrielTavares99/aws-chalice-boilerplate) - Among other things, demonstrates how to use `chalice.cli.CLIFactory`.
- [chalice_dockerized: How to deploy Chalice with docker-compose](https://github.com/vanderlvoff/chalice_dockerized)
- [Chalice-GraphQL: Adds Facebook's GraphQL support to your Chalice application](https://github.com/jrbeilke/chalice-graphql)
- [Chalice + LocalStack](https://github.com/localstack/chalice-local)
- [chalice-extended-action: Automated deployment of your Chalice application via GitHub Actions](https://github.com/jayef0/chalice-extended-action)
- [pytest-chalice: A set of py.test fixtures for AWS Chalice](https://github.com/studio3104/pytest-chalice)
- [chalice-cognito-auth: A library for setting up login routes in a Chalice app](https://github.com/stealthycoin/chalice-cognito-auth) - Connect Chalice to a Cognito user pool for single-sign on (SSO).
- [Domovoi - Extension to Chalice that supports Automatic Load Balancing](https://github.com/cloud-utils/domovoi)
- [Damn Vulnerable Functions as a Service](https://github.com/we45/DVFaaS-Damn-Vulnerable-Functions-as-a-Service) - Example insecure FaaS repository built on Chalice.

## Miscellaneous Awesomeness

- [Using APISpec to enable using Swagger with Chalice](https://stackoverflow.com/questions/63048401/any-framework-or-tool-is-available-to-achieve-swagger-definition-as-the-auto-gen)
- [AWS IAM Policy required for AWS Chalice](https://stackoverflow.com/questions/63781304/aws-iam-policy-required-for-aws-chalice)
- [Calling a Lambda from a Lambda in Chalice without going through API Gateway again](https://stackoverflow.com/questions/62815740/how-to-directly-invoke-a-chalice-lambda-from-another-lambda-without-going-throug)
- [How to create pure Lambda functions in Chalice](https://aws.github.io/chalice/topics/purelambda)
- [Continuous Deployment with Chalice](https://aws.github.io/chalice/topics/cd) - Chalice has support for dev/stage/prod out-of-the-box, in addition to CodeBuild, CodeDeploy and CodePipeline.
- [Configuration File](https://aws.github.io/chalice/topics/configfile.html) - By setting `api_gateway_endpoint_type` you can deploy into a VPC.
- [sentry-python: application monitoring platform to diagnose, fix, and optimize code performance](https://github.com/getsentry/sentry-python/blob/af163ff176b2c22952443dc5ec535aed98656fc2/tests/integrations/chalice/test_chalice.py)
- [Lumigo Python agent for distributed tracing and performance monitoring](https://github.com/lumigo-io/python_tracer/blob/1ab55406befe494aa61384576339b49a1e681623/src/lumigo_tracer/examples/chalice.py)
- [IOpipe Analytics & Distributed Tracing Agent for Python](https://github.com/iopipe/iopipe-python#chalice)
- [PySide6, Qt Quick, Material Design, VS Code And Python 3.9.1 - Tutorial Modern GUI - Part 1](https://www.youtube.com/watch?v=Jn0PpzB14Y8)
- [Building your first REST API with AWSs Open Data Sets and Chalice - Christian Weber](https://www.youtube.com/watch?v=VKUoL3IL3-w)
- [AWS Chalice Hands-On Walkthrough, a Python Serverless Microframework for AWS](https://www.youtube.com/watch?v=q3eayufwmMg)
- [AWS Chalice - Walkthrough of the Media Query Sample Application](https://www.youtube.com/watch?v=UCZXJpI1dKw&ab_channel=AmazonWebServices)
- [Udemy Online Course - AWS Chalice: Build Serverless REST APIs on AWS](https://www.udemy.com/course/aws-chalice-build-serverless-rest-apis-on-aws/?ranMID=39197&ranEAID=Gw%2FETjJoU9M&ranSiteID=Gw_ETjJoU9M-gPreRA73w_.wS1U96fuiKw&utm_source=aff-campaign&utm_medium=udemyads&LSNPUBID=Gw%2FETjJoU9M)
- [chalice.dev Slack channel](https://chalice.dev/)
- [cdk.dev Slack channel](https://cdk.dev/)
- [AWS Nuke](https://github.com/rebuy-de/aws-nuke) - Attempts to delete all resources in an AWS account.
- [Steampipe](https://steampipe.io/) - Steampipe allows you to query your AWS infrastructure, IAM policies, etc., using SQL.
- [Click](https://click.palletsprojects.com/en/7.x/) - You can pair Flask's Click project to decorate your Chalice apps so as to have a CLI.
- [AWS CDK Patterns](https://github.com/cdk-patterns/serverless)
- [Metaflow S3](https://github.com/Netflix/metaflow/blob/master/metaflow/datatools/s3.py) - Achieve 20 gigabit throughput with S3 using this python module from Netflix.
