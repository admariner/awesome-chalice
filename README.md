<a href="https://join.slack.com/t/chalicedev/shared_invite/zt-naadmddi-MRwgFq40Ge3qfcPJR_RaDQ"><img align="right" height="20px" src="https://img.shields.io/badge/Slack-4A154B?logo=slack&logoColor=white"></a><img align="right" src="https://end4gy838edhwnq.m.pipedream.net"><a href="http://magnataur.com"><img src="https://magnataur.com/favicon.ico" align="right" height="20"></a><a href="https://github.com/aws/chalice"><img src="chalice.png" height="20" align="right"></a><a href="https://github.com/sindresorhus/awesome"><img src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg" align="right" height="20"></a><br/><br/>

AWS Chalice is a Python library for serverless application development on AWS Lambda. It enables developers to easily create and manage HTTPS APIs, build libraries of operational functions, manage AWS accounts programmatically, create web applications with popular front-end toolkits, and serve as the backend for cross-platform desktop and mobile applications written in Qt for Python. This is the community documentation for AWS Chalice.

## AWS Projects
Supercharge your app.

- [AWS Data Wrangler](https://github.com/awslabs/aws-data-wrangler) - Pandas on AWS - Easy integration with Athena, Glue, Redshift, Timestream, QuickSight, Chime, CloudWatchLogs, DynamoDB, EMR, SecretManager, PostgreSQL, MySQL, SQLServer and S3 (Parquet, CSV, JSON and EXCEL).
- [AWS AutoGluon](https://github.com/awslabs/autogluon) - Automate machine learning training and deployment.
- [AWS Lambda Powertools](https://github.com/awslabs/aws-lambda-powertools-python) - A suite of utilities for AWS Lambda functions to ease adopting best practices such as tracing, structured logging, custom metrics async, parameters and secrets management, idempotency, and more.
- [AWS Cloud Development Kit (CDK)](https://aws.amazon.com/cdk/) - The CDK can deploy Chalice apps, or Chalice can deploy CDK apps.
- [AWS Solutions Constructs Patterns](https://aws.amazon.com/solutions/constructs/patterns/) - Architectural patterns for the CDK that can be chained together.
- [AWS Serverless Application Repository](https://serverlessrepo.aws.amazon.com/applications) - Serverless AWS applications. 
- [DynamoDB Global Tables](https://aws.amazon.com/dynamodb/global-tables/) - NoSQL database.
- [Aurora Serverless Global Database 2](https://aws.amazon.com/rds/aurora/serverless/) - OLTP database.
- [AWS Amplify](https://docs.amplify.aws/) - Front-end toolkit.
- [Amazon Athena Federated Query](https://docs.aws.amazon.com/athena/latest/ug/connect-to-a-data-source.html) - Author pure lambda functions for ad-hoc datalakes.
- [AWS SDK for JavaScript](https://aws.amazon.com/sdk-for-javascript/) - Combine with Brython or Pyodide for front-end Python development.
- [QLDB Python Driver](https://github.com/awslabs/amazon-qldb-driver-python) - A Python implementation of a driver for Amazon Quantum Ledger Database.
- [AWS CloudWatch Embedded Metrics](awslabs/aws-embedded-metrics-python) - Amazon CloudWatch Embedded Metric Format Client Library.

## AWS Python SDKs
Every SDK in one place.

- [AWS SDK for Python (boto3)](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html) - See `aioboto3` for the async version.
- [AWS X-Ray SDK for Python](https://docs.aws.amazon.com/xray/latest/devguide/xray-sdk-python.html) - Instrument with `from aws_xray_sdk.core import patch_all;patch_all();`.
- [AWS IoT SDK for Python](https://github.com/aws/aws-iot-device-sdk-python-v2) - Can talk to Chalice via Kinesis Streams. 
- [AWS C Common Runtime](https://github.com/awslabs/aws-c-common) - Use with the AWS CRT Python module.
- [AWS Encryption SDK for Python](https://github.com/aws/aws-encryption-sdk-python/) - Hard encryption in your application logic.
- [AWS SageMaker SDK for Python](https://github.com/aws/sagemaker-python-sdk) - Train and deploy machine learning models. Integrate with your EMR cluster.
- [AWS Step Functions Data Science SDK for Python](https://github.com/aws/aws-step-functions-data-science-sdk-python) - Managed AI/ML infrastructure.
- [AWS Braket SDK for Python](https://github.com/aws/amazon-braket-sdk-python) - Leverage D-Wave quantum computing devices.
- [AWS DynamoDB Encryption SDK for Python](https://github.com/aws/aws-dynamodb-encryption-python) - Encrypt data before sending it to DynamoDB.
- [AWS Transcribe Streaming SDK for Python](https://github.com/awslabs/amazon-transcribe-streaming-sdk) - Convert audio into text.
- [AWS Data API SDK for Python](https://github.com/awslabs/aws-data-api-python-sdk) - HTTP interface to your non-transactional data lake, made with Chalice.
- [AWS Config Rules Development Kit for Python](https://github.com/awslabs/aws-config-rdk) - The AWS Config Rules Development Kit helps developers set up, author and test custom Config rules. It contains scripts to enable AWS Config, create a Config rule and test it with sample ConfigurationItems.
- [AWS Streamer SDK for Python](https://github.com/awslabs/aws-streamer) - A collection of video processing and streaming tools for the AWS platform.


## 3rd-party Python

- [Dask](https://dask.org/) - Disributed DataFrames built on Pandas
- [3M Falcano](https://github.com/3mcloud/falcano) - DynamoDB ORM, allowing for single table designs. Successor to PynamoDB.
- [S3Fs](https://s3fs.readthedocs.io/en/latest/) - Use S3 like a filesystem.
- [PySide2](https://wiki.qt.io/Qt_for_Python) - Official Qt module for Python.
- [Hy: A lisp written in Python](https://docs.hylang.org/en/master/tutorial.html) - A lisp that can you can use in your Python code, for FP.
- [Toolz: A set of utility functions for iterators, functions, and dictionaries](https://github.com/pytoolz/toolz) - FP primitives.
- [AWS Limit Checker](https://github.com/jantman/awslimitchecker) - Detect when you are about to run up against AWS limits.
- [Click](https://click.palletsprojects.com/en/7.x/) - Create a CLI.
- [Netflix Metaflow S3](https://github.com/Netflix/metaflow/blob/master/metaflow/datatools/s3.py) - Achieve 20 gigabit S3 throughput.
- [Slack Bolt](https://github.com/slackapi/bolt-python) - Enable AWS ChatOps with Slack's built-in Chalice support.
- [Troposphere](https://github.com/cloudtools/troposphere) - Write CloudFormation using Python.
- [Scepter](https://github.com/Sceptre/sceptre) - CloudFormation deployment library.
- [taskcat](https://github.com/aws-quickstart/taskcat) - CloudFormation testing library from AWS.
- [PyCognito](https://github.com/pvizeli/pycognito) - Manage and use Cognito user pools.
- [mrjob](https://github.com/Yelp/mrjob) - Run MapReduce jobs on your EMR cluster.

## 3rd-party Python (ChatGPT)
This section generated by ChatGPT.

- [boto3](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html): This is the official AWS SDK for Python, which allows you to interact with AWS services in a programmatic way.
[requests](https://pypi.org/project/requests/): This is a popular library for making HTTP requests in Python. It can be used to make requests to external APIs, which can be useful when building serverless applications with AWS Chalice.
- [jsonpickle](https://jsonpickle.github.io/): This library provides an easy way to convert Python objects to and from JSON. This can be useful when working with JSON data in AWS Lambda functions.
- [PyJWT](https://pyjwt.readthedocs.io/en/stable/): This library allows you to encode and decode JSON Web Tokens (JWT) in Python. This can be useful for authentication and authorization in serverless applications built with AWS Chalice.
- [Flask-Cors](https://flask-cors.readthedocs.io/en/latest/): This library is an extension for Flask that allows you to easily configure CORS headers for your API. This can be useful when building serverless applications that need to support cross-origin requests.
- [PyYAML](https://pypi.org/project/PyYAML/): This library allows you to parse and work with YAML files in Python. This can be useful for loading configuration files for your serverless application built with AWS Chalice.
- [Pandas](https://pandas.pydata.org/): This library provides fast, flexible, and expressive data structures designed to make working with “relational” or “labeled” data both easy and intuitive. It can be useful when working with data in AWS Lambda functions
- [Loguru](https://github.com/Delgan/loguru): This library provides a simple and lightweight way to log messages in Python. It can be useful for debugging and troubleshooting issues in your serverless application built with AWS Chalice
- [PyMySQL](https://pypi.org/project/PyMySQL/): This library is a pure-Python MySQL client library, which allows you to interact with a MySQL database from your Python code. This can be useful for connecting to a MySQL database in your serverless application built with AWS Chalice.
- [Flask-RESTful](https://flask-restful.readthedocs.io/en/latest/): This library is an extension for Flask that makes it easy to build RESTful APIs with Flask. This can be useful when building serverless applications that expose an API.
- [Pytest](https://pytest.org): This library is a popular testing framework for Python. It can be used to write unit tests for your serverless application built with AWS Chalice.
- [Flask-SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/): This library is an extension for Flask that adds support for SQLAlchemy to your application. This can be useful when working with a relational database in your serverless application built with AWS Chalice.
- [Flask-Uploads](https://pythonhosted.org/Flask-Uploads/): This library is an extension for Flask that provides flexible and efficient upload handling for Flask. This can be useful when building serverless applications that need to handle file uploads.
- [pytz](https://pypi.org/project/pytz/): This library provides a library for using those timezones, and it's a dependency of many libraries, including dateutil and pytzdata. It can be useful when working with time and date in your serverless application built with AWS Chalice.
- [PyMySQL](https://pypi.org/project/PyMySQL/): This library is a pure-Python MySQL client library, which allows you to interact with a MySQL database from your Python code. This can be useful for connecting to a MySQL database in your serverless application built with AWS Chalice.
- [Flask-RESTful](https://flask-restful.readthedocs.io/en/latest/): This library is an extension for Flask that makes it easy to build RESTful APIs with Flask. This can be useful when building serverless applications that expose an API.
- [Pytest](https://docs.pytest.org/en/7.2.x/): This library is a popular testing framework for Python. It can be used to write unit tests for your serverless application built with AWS Chalice.
- [Flask-SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/en/3.0.x/): This library is an extension for Flask that adds support for SQLAlchemy to your application. This can be useful when working with a relational database in your serverless application built with AWS Chalice.
- [Flask-Uploads](https://pythonhosted.org/Flask-Uploads/): This library is an extension for Flask that provides flexible and efficient upload handling for Flask. This can be useful when building serverless applications that need to handle file uploads.
- [PyS3](https://pypi.org/project/pys3/): This library is a simple interface to Amazon S3 for Python. This can be useful for working with files and data stored on S3 in your serverless application built with AWS Chalice.
- [DynamoDB-Geo](https://www.npmjs.com/package/dynamodb-geo): This library is a Python library for working with Amazon DynamoDB and geospatial data. This can be useful for building serverless applications that need to work with geospatial data stored in DynamoDB.
- [PyVault](https://pypi.org/project/pyvault/): This library is a simple Python library for interacting with HashiCorp Vault. This can be useful for securely storing and accessing sensitive data in your serverless application built with AWS Chalice.
- [PyAthena](https://pypi.org/project/pyathena/): This library is a simple Python library for interacting with Amazon Athena. This can be useful for running SQL queries on data stored in S3 in your serverless application built with AWS Chalice.

## Tooling
Create diagrams, write code.

- [AWS Toolkit for PyCharm](https://aws.amazon.com/pycharm/) - Tightly integrated editor, for repl-driven development.
- [Anaconda Python Distribution](https://www.anaconda.com/products/individual/download-success) - Consistent Python environment for local dev.
- [Chalice + LocalStack](https://github.com/localstack/chalice-local) - Dev against local versions of DynamoDB, AWS Lambda, API Gateway, etc.
- [LucidCharts](https://lucid.app) - Create diagrams in the official style.

## Made with Chalice
Example GitHub repos.

- [Coworks Microframework](https://github.com/gdoumenc/coworks) - Based on Step Functions.
- [Agave: REST API for Chalice BluePrints](https://github.com/cuenca-mx/agave) - REST APIs for your managed routes.
- [aws-chalice-swagger](https://github.com/samuelkhtu/aws-chalice-swagger) - How to use Swagger support.
- [Lambda Multi-threading in Chalice](https://github.com/vumdao/multithread-in-lambda) - Map/reduce across your Lambda cores.
- [aws-chalice-boilerplate](https://github.com/GabrielTavares99/aws-chalice-boilerplate) - How to use `chalice.cli.CLIFactory`.
- [chalice_dockerized](https://github.com/vanderlvoff/chalice_dockerized) - Dockerize your application.
- [Chalice-GraphQL](https://github.com/jrbeilke/chalice-graphql) - Add a GraphQL API.
- [chalice-extended-action](https://github.com/jayef0/chalice-extended-action) - Deploy with GitHub Actions.
- [pytest-chalice](https://github.com/studio3104/pytest-chalice) - Py.test fixtures.
- [chalice-cognito-auth](https://github.com/stealthycoin/chalice-cognito-auth) - SSO with a Cognito user pool.
- [Chalice PynamoDB Docker Starter Kit](https://github.com/DevOps-Nirvana/Chalice-PynamoDB-Docker-Starter-Kit) - A starter kit to begin using Chalice and PynamoDB easily


## Articles
Critical background reading.
- [Use AWS Lambda with AWS Control Tower Audit account to inspect your multi-account setup](https://aws.amazon.com/blogs/mt/use-aws-lambda-with-aws-control-tower-audit-account-to-inspect-your-multi-account-setup/)
- [Introducing AWS Lambda Extensions](https://aws.amazon.com/blogs/aws/getting-started-with-using-your-favorite-operational-tools-on-aws-lambda-extensions-are-now-generally-available/)
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
- [AWS Chalice now supports Amazon Kinesis and Amazon DynamoDB Streams](https://aws.amazon.com/blogs/developer/aws-chalice-now-supports-amazon-kinesis-and-amazon-dynamodb-streams/)
- [Using AWS Lambda Layers with AWS Chalice](https://aws.amazon.com/blogs/developer/using-aws-lambda-layers-with-aws-chalice/)
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

## AWS Serverless Architectures
Inspiration for your app. [Complete list of 500+ sample architectures](https://github.com/aws-samples?q=&type=&language=python&sort=). 

- [AWS Glue ETL Code Samples](https://github.com/aws-samples/aws-glue-samples)
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
More inspiration from AWS Labs, closer to production-ready. [Complete list of 100+ Labs solutions](https://github.com/awslabs?q=&type=&language=python&sort=stargazers).

- [AWS Control Tower Customizations](https://github.com/awslabs/aws-control-tower-customizations)
- [Serverless Data Lake Framework (SDLF)](https://github.com/awslabs/aws-serverless-data-lake-framework)
- [Media Insights Engine](https://github.com/awslabs/aws-media-insights-engine)
- [Serverless Transit Network Orchestrator](https://github.com/awslabs/serverless-transit-network-orchestrator)
- [Amazon Aurora Postgres Advanced Monitoring](https://github.com/awslabs/amazon-aurora-postgres-monitoring)
- [AWS Serverless Twitter Event Source](https://github.com/awslabs/aws-serverless-twitter-event-source)
- [Serverless Subtitles](https://github.com/awslabs/serverless-subtitles)
- [AWS Serverless Financial Functions](https://github.com/awslabs/aws-serverless-financial-functions)

## Related Awesome Lists
- [Awesome AWS](https://github.com/donnemartin/awesome-aws#readme)
- [Awesome Alexa](https://github.com/miguelmota/awesome-amazon-alexa#readme)
- [Awesome Amplify](https://github.com/dabit3/awesome-aws-amplify#readme)
- [Awesome AppSync](https://github.com/aws/aws-appsync-community#readme)
- [Awesome IAM](https://github.com/kdeldycke/awesome-iam#readme)
- [Awesome CDK](https://github.com/kolomied/awesome-cdk#readme)
- [Awesome CloudFormation](https://github.com/aws-cloudformation/awesome-cloudformation#readme)
- [Awesome EC2 Spot](https://github.com/nadaahm/awesome-ec2-spot)
- [Awesome ECS](https://github.com/nathanpeck/awesome-ecs#readme)
- [Awesome EKS](https://github.com/realvz/awesome-eks#readme)
- [Awesome Lambda Layers](https://github.com/mthenw/awesome-layers)
- [Awesome AWS Research](https://github.com/randyridgley/awesome-aws-research#readme)
- [Awesome AWS Security](https://github.com/jassics/awesome-aws-security)
- [AWS Security Arsenal](https://github.com/toniblyx/my-arsenal-of-aws-security-tools)
- [Awesome Cloud Security](https://github.com/RyanJarv/awesome-cloud-sec#readme)
- [AWSome Websites](https://github.com/StanForever/AWSome-websites)
- [The Open Guide to Amazon Web Services](https://github.com/open-guides/og-aws)

## Related Projects
- [Goblet](https://github.com/anovis/goblet) - Like Chalice, but for GCP.
