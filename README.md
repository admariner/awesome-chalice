<a href="https://github.com/chalice-dev/awesome-chalice"><img alight="right" src="https://end4gy838edhwnq.m.pipedream.net" align="right" height="20"></a><a href="https://github.com/aws/chalice"><img src="https://user-images.githubusercontent.com/80226595/110259005-4ec13080-7f5a-11eb-98eb-f84dbac2c736.png" height="20" align="right"></a><a href="https://github.com/sindresorhus/awesome"><img src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg" align="right" height="20"></a>[![Analytics](https://ga-beacon.appspot.com/UA-191636151-1/awesome-chalice?useReferer&pixel)](https://github.com/igrigorik/ga-beacon)
# Awesome Chalice
> List of resources for using AWS Chalice

[AWS Chalice](https://aws.github.io/chalice/)<a href="https://aws.github.io/chalice/"><img src="https://aws.github.io/chalice/_static/img/chalice-logo-icon-small.png" height="20"></a> ([join us in our community Slack channel](https://join.slack.com/t/chalicedev/shared_invite/zt-naadmddi-MRwgFq40Ge3qfcPJR_RaDQ)) is Amazon Web Services' premier solution to writing infinitely scalable serverless Python applications based on AWS Lambda and decorators. Chalice is suited for:
- Writing HTTPS APIs that wrap AWS infrastructure.
- Building libraries of Ops functions.
- Managing AWS accounts programmatically.
- Creating web applications with your favorite front-end toolkit.
- Providing the web API backend layer to cross-platform desktop and mobile applications written in Qt for Python.

## Contents
- [AWS Projects that integrate with Chalice](#aws-projects-that-integrate-with-chalice)
- [AWS Python SDKs](#aws-python-sdks)
- [AWS Samples for Python](#aws-samples-for-python)
- [AWS Labs](#aws-labs)
- [3rd Party Tools](#3rd-party-tools)
- [Tooling for Writing Chalice Code](#tooling-for-writing-chalice-code)
- [Blog Posts and Feature Releases](#blog-posts-and-feature-releases)
- [Built on Chalice](#built-on-chalice)
- [Miscellaneous Awesomeness](#miscellaneous-awesomeness)

## AWS Projects that work with Chalice
- [AWS Data Wrangler](https://github.com/awslabs/aws-data-wrangler) - This AWS ProServ project integrates Pandas with nearly every major AWS backend store.
- [AWS SDK for JavaScript](https://aws.amazon.com/sdk-for-javascript/) - Chalice's front-end partner, you can include it in your HTML like so: ` <script src="https://sdk.amazonaws.com/js/aws-sdk-2.879.0.min.js"></script>` 
- [AWS Cloud Development Kit (CDK)](https://aws.amazon.com/cdk/) - The CDK can author and deploy Chalice applications, or Chalice can deploy CDK applications.
- [AWS Solutions Constructs Patterns](https://aws.amazon.com/solutions/constructs/patterns/) - Architectural patterns for the CDK that can be chained together.
- [AWS Serverless Application Repository](https://serverlessrepo.aws.amazon.com/applications) - Serverless AWS applications. 
- [JSii](https://github.com/aws/jsii) - Enables the CDK to be used from Python.
- [DynamoDB Global Tables](https://aws.amazon.com/dynamodb/global-tables/) - NoSQL database.
- [Aurora Serverless Global Database 2](https://aws.amazon.com/rds/aurora/serverless/) - Serverless OLTP database.
- [AWS Amplify](https://docs.amplify.aws/) - Front-end toolkit.
- [Amazon Athena Federated Query](https://docs.aws.amazon.com/athena/latest/ug/connect-to-a-data-source.html) - Author `data source connectors` as pure lambda functions.

## AWS Python SDKs
- [AWS SDK for Python (boto3)](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html) - See also `aioboto3` for the asynchronous version.
- [AWS X-Ray SDK for Python](https://docs.aws.amazon.com/xray/latest/devguide/xray-sdk-python.html) - Ddynamically instrument your application with `from aws_xray_sdk.core import patch_all;patch_all();`.
- [AWS IoT SDK for Python](https://github.com/aws/aws-iot-device-sdk-python-v2) - Can talk to Chalice via Kinesis Streams. 
- [AWS C Common Runtime](https://github.com/awslabs/aws-c-common) - Use the AWS CRT Python module to take advantage of this fast AWS backend library written in C.
- [AWS Encryption SDK for Python](https://github.com/aws/aws-encryption-sdk-python/) - Hard encryption in your application logic.
- [AWS SageMaker SDK for Python](https://github.com/aws/sagemaker-python-sdk) - Train and deploy machine learning models. Integrate with your EMR cluster.
- [AWS Step Functions Data Science SDK for Python](https://github.com/aws/aws-step-functions-data-science-sdk-python) - Similar to above, but with managed infrastructure.
- [AWS Braket SDK for Python](https://github.com/aws/amazon-braket-sdk-python) - Leverage D-Wave quantum computing devices.
- [AWS DynamoDB Encryption SDK for Python](https://github.com/aws/aws-dynamodb-encryption-python) - Encrypt data before sending it to DynamoDB.

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
- [3M Falcano](https://github.com/3mcloud/falcano) - Similar to PynamoDB, but allows for single table designs, following official guidelines. 
- [PynamoDB: A Pythonic wrapper for DynamoDB](https://github.com/pynamodb/PynamoDB) - ORM for DynamoDB.
- [S3Fs](https://s3fs.readthedocs.io/en/latest/) - Use S3 like a filesystem.
- [PySide6](https://www.qt.io/blog/qt-for-python-6-released) - Official Qt module for Python.
- [Hy: A lisp written in Python](https://docs.hylang.org/en/master/tutorial.html) - A lisp that can you can use in your Python code, for FP.
- [Toolz: A set of utility functions for iterators, functions, and dictionaries](https://github.com/pytoolz/toolz) - Functional programming primitives.
- [AWS Limit Checker](https://github.com/jantman/awslimitchecker) - Automatically detecting when you are about to run up against AWS limits.

## Tooling for Writing Chalice Code
- [AWS Toolkit for PyCharm](https://aws.amazon.com/pycharm/) - Tightly integrated editor, for repl-driven development.
- [Anaconda Python Distribution](https://www.anaconda.com/products/individual/download-success) - Consistent Python development environment for local dev.
- [Cloudviz](https://cloudviz.io/) - Create official looking diagrams.
- [CloudMoji™](https://cloudmoji.com/) - CloudMoji has the 2021 AWS icon pack.

## Blog Posts and Feature Releases
Blog posts, mostly from AWS, that are critical background reading for using Chalice.
- [Python support GA: improving Python code quality using Amazon CodeGuru Reviewer](https://aws.amazon.com/blogs/devops/python-support-ga-improving-python-code-quality-using-amazon-codeguru-reviewer/)
- [Amplify Flutter is Now Generally Available: Build Beautiful Cross-Platform Apps](https://aws.amazon.com/blogs/aws/amplify-flutter-is-now-generally-available-build-beautiful-cross-platform-apps/)
- [Using container images to run PyTorch models in AWS Lambda](https://aws.amazon.com/blogs/machine-learning/using-container-images-to-run-pytorch-models-in-aws-lambda/)
- [AWS Chalice adds support for the AWS CDK](https://aws.amazon.com/blogs/developer/aws-chalice-adds-support-for-the-aws-cdk/)
- [Packaging AWS Lambda functions as container images](https://acloudguru.com/blog/engineering/packaging-aws-lambda-functions-as-container-images)
- [New for AWS Lambda – 1ms Billing Granularity Adds Cost Savings](https://aws.amazon.com/blogs/aws/new-for-aws-lambda-1ms-billing-granularity-adds-cost-savings/)
- [Implementing version control using Amazon DynamoDB](https://aws.amazon.com/blogs/database/implementing-version-control-using-amazon-dynamodb/)
- [Introducing Middleware Stack in Modular AWS SDK for JavaScript](https://aws.amazon.com/blogs/developer/middleware-stack-modular-aws-sdk-js/)
- [How do I give internet access to a Lambda function that's connected to an Amazon VPC?](https://aws.amazon.com/premiumsupport/knowledge-center/internet-access-lambda-function/)
- [AWS Lambda Extensions: What are they and why do they matter](https://lumigo.io/blog/aws-lambda-extensions-what-are-they-and-why-do-they-matter/)
- [AWS Chalice now supports Amazon Kinesis and Amazon DynamoDB Streams](https://aws.amazon.com/blogs/developer/aws-chalice-now-supports-amazon-kinesis-and-amazon-dynamodb-streams/) - By integrating Chalice with DynamoDB streams, you can create sophisticated business logic using DynamoDB's ablity to trigger lambda functions based on events.
- [Using AWS Lambda Layers with AWS Chalice](https://aws.amazon.com/blogs/developer/using-aws-lambda-layers-with-aws-chalice/) - With automatic lambda layers, you don't have to wait for your large lambda layer to upload every time you deploy your application.
- [Following serverless best practices with AWS Chalice and Lambda Powertools](https://aws.amazon.com/blogs/developer/following-serverless-best-practices-with-aws-chalice-and-lambda-powertools/)
- [Automatically deploy a Serverless REST API from GitHub with AWS Chalice](https://aws.amazon.com/blogs/developer/automatically-deploy-a-serverless-rest-api-from-github-with-aws-chalice/)
- [Configuring custom domain names with AWS Chalice](https://aws.amazon.com/blogs/developer/configuring-custom-domain-names-with-aws-chalice/)
- [AWS Chalice Now Supports YAML Templates](https://aws.amazon.com/blogs/developer/aws-chalice-now-supports-yaml-templates/)
- [AWS Solutions Constructs – A Library of Architecture Patterns for the AWS CDK](https://aws.amazon.com/blogs/aws/aws-solutions-constructs-a-library-of-architecture-patterns-for-the-aws-cdk/)
- [Using Amazon EFS for AWS Lambda in your serverless applications](https://aws.amazon.com/blogs/compute/using-amazon-efs-for-aws-lambda-in-your-serverless-applications/)
- [Introducing the AWS Chalice test client](https://aws.amazon.com/blogs/developer/introducing-the-new-test-client-for-aws-chalice/)
- [Use Amazon DynamoDB Accelerator (DAX) from AWS Lambda to increase performance while reducing costs](https://aws.amazon.com/blogs/database/how-to-increase-performance-while-reducing-costs-by-using-amazon-dynamodb-accelerator-dax-and-aws-lambda/)
- [Painless AWS Chalice Application Debug](https://medium.com/cyberark-engineering/painless-aws-chalice-application-debug-90534e33cf76)
- [Modularizing a Chalice Application for Teams](https://medium.com/tensoriot/modularizing-a-chalice-application-for-teams-f716f496b94b)
- [Getting started with the AWS Cloud Development Kit and Python](https://aws.amazon.com/blogs/developer/getting-started-with-the-aws-cloud-development-kit-and-python/)
- [Run your Python Scripts as Slack Commands (ChatOps)](https://medium.com/@yogeshingale94/run-your-python-scripts-as-slack-commands-chatops-63bc334b74cd)
- [Building Serverless Python Apps Using AWS Chalice](https://realpython.com/aws-chalice-serverless-python/)

## Built on Chalice
- [Coworks Microframework](https://github.com/gdoumenc/coworks) - Complete microservices framework based on Step Functions.
- [Agave: REST API for Chalice BluePrints](https://github.com/cuenca-mx/agave) - REST APIs for your managed routes.
- [aws-chalice-swagger](https://github.com/samuelkhtu/aws-chalice-swagger) - How to use Swagger support.
- [Lambda Multi-threading in Chalice](https://github.com/vumdao/multithread-in-lambda) - Map/reduce across your Lambda cores.
- [aws-chalice-boilerplate](https://github.com/GabrielTavares99/aws-chalice-boilerplate) - How to use `chalice.cli.CLIFactory`.
- [chalice_dockerized](https://github.com/vanderlvoff/chalice_dockerized) - Dockerize your application.
- [Chalice-GraphQL](https://github.com/jrbeilke/chalice-graphql) - Add a GraphQL API.
- [Chalice + LocalStack](https://github.com/localstack/chalice-local) - Dev against local versions of DynamoDB, AWS Lambda, API Gateway, etc.
- [chalice-extended-action](https://github.com/jayef0/chalice-extended-action) - Deploy with GitHub Actions.
- [pytest-chalice](https://github.com/studio3104/pytest-chalice) - py.test fixtures.
- [chalice-cognito-auth: A library for setting up login routes in a Chalice app](https://github.com/stealthycoin/chalice-cognito-auth) - SSO with a Cognito user pool.
- [Damn Vulnerable Functions as a Service](https://github.com/we45/DVFaaS-Damn-Vulnerable-Functions-as-a-Service) - Insecure FaaS repository.

## Miscellaneous Awesomeness

- [Using APISpec to enable using Swagger with Chalice](https://stackoverflow.com/questions/63048401/any-framework-or-tool-is-available-to-achieve-swagger-definition-as-the-auto-gen)
- [AWS IAM Policy required for AWS Chalice](https://stackoverflow.com/questions/63781304/aws-iam-policy-required-for-aws-chalice)
- [Calling a Lambda from a Lambda in Chalice without going through API Gateway again](https://stackoverflow.com/questions/62815740/how-to-directly-invoke-a-chalice-lambda-from-another-lambda-without-going-throug)
- [How to create pure Lambda functions in Chalice](https://aws.github.io/chalice/topics/purelambda)
- [Continuous Deployment with Chalice](https://aws.github.io/chalice/topics/cd) - Chalice has support for dev/stage/prod out-of-the-box, in addition to CodeBuild, CodeDeploy and CodePipeline.
- [Configuration File](https://aws.github.io/chalice/topics/configfile.html) - Deploy into a VPC by setting `api_gateway_endpoint_type`.
- [sentry-python](https://github.com/getsentry/sentry-python/blob/af163ff176b2c22952443dc5ec535aed98656fc2/tests/integrations/chalice/test_chalice.py) Paid tracing.
- [Lumigo Python agent](https://github.com/lumigo-io/python_tracer/blob/1ab55406befe494aa61384576339b49a1e681623/src/lumigo_tracer/examples/chalice.py) Paid tracing.
- [IOpipe](https://github.com/iopipe/iopipe-python#chalice) Paid tracing.
- [PySide6](https://www.youtube.com/watch?v=Jn0PpzB14Y8) Video demonstrating Qt for Python (PySide6).
- [Building your first REST API](https://www.youtube.com/watch?v=VKUoL3IL3-w) Tutorial video.
- [Hands-On Walkthrough](https://www.youtube.com/watch?v=q3eayufwmMg) Tutorial video.
- [Udemy Online Course](https://www.udemy.com/course/aws-chalice-build-serverless-rest-apis-on-aws/?ranMID=39197&ranEAID=Gw%2FETjJoU9M&ranSiteID=Gw_ETjJoU9M-gPreRA73w_.wS1U96fuiKw&utm_source=aff-campaign&utm_medium=udemyads&LSNPUBID=Gw%2FETjJoU9M) Udemy course.
- [AWS Nuke](https://github.com/rebuy-de/aws-nuke) - Delete all resources in an AWS account.
- [Steampipe](https://steampipe.io/) - Query your AWS infrastructure, IAM policies, etc., using SQL.
- [Click](https://click.palletsprojects.com/en/7.x/) - Create a CLI.
- [AWS CDK Patterns](https://github.com/cdk-patterns/serverless) - CDK architecture patterns.
- [Netflix' Metaflow S3](https://github.com/Netflix/metaflow/blob/master/metaflow/datatools/s3.py) - Achieve 20 gigabit S3 throughput.
