### Overview and terminology

* **Region**: geographical places where AWS services exist.
* **Availability Zone (AZ)**: AWS data center.
* A region contains 2 or more Availability Zones.
* **Content Delivery Network (CDN)**: globally distributed network of proxy servers
    deployed in multiple data centers. The goal of a CDN is to serve content to
    end-users with high availability and high performance.
* **CloudFront**: CDN for Amazon.
* **Edge Location**: physical locations for CloudFront.
* **Virtual Private Cloud (VPC)**: an on-demand configurable pool of shared computing
    resources allocated within a public cloud environment, providing a
    certain level of isolation between the different organizations
    using the resources. Basically, you can isolate a set of cloud resources
    into a network which can be interacted with and accessed as a single
    unit.
* **Domain Name System (DNS)**: a hierarchical decentralized naming system for
    computers, services, or other resources connected to the Internet or a
    private network. It associates various information with domain names
    assigned to each of the participating entities. Most prominently, it
    translates more readily memorized domain names to the numerical IP
    addresses needed for locating and identifying computer services and
    devices with the underlying network protocols.
* **Route 53**: Amazon's DNS service. Port 53 is the port through which it connects.
* **Direct Connect**: a service to directly connect to AWS. This is done if you
    need more performance or security.
* **Elastic Compute Cloud (EC2)**: general purpose virtual machines in the AWS.
* **EC2 Container Services (ECS)**: container management service that supports Docker
    containers and allows you to easily run applications on a managed cluster
    of Amazon EC2 instances
* **Elastic Beanstalk**: is a set of ready-to-use containers for specific app types
    such as rails apps, or .net apps, which allow you to deploy applications
    of the specific types without worrying about the infrastructure.
* **Lambda**: an event-driven, serverless computing platform provided by Amazon as
    a part of the Amazon Web Services. It is a compute service that runs code
    in response to events and automatically manages the compute resources required
    by that code.
* AWS Lambda functions can only run for a maximum of five minutes.
* **LightSail**: a virtual private server, that is easy to setup and deploy to. its
    a simple way to host a webpage that is mostly static, like a blog. Once a
    project gets large enough or popular enough, developers will often migrate
    to AWS. This is comparable to EC2, but with less of a focus on general
    computing and more focus on being a machine to serve your website on.
* **Simple Storage Service (S3)**: virtual disk to store flat files. This should not
    be used for installing apps or storing DBs.
* **Glacier**: archival data store. Getting files stored here is very slow (3-5 hours)
    however it is very cheap.
* **Elastic File System (EFS)**: Block storage where you would actually install apps.
* **Storage Gateway**: A service to connect S3 to a local virtual machine (not a
    cloud machine)
* **Relational Database System (RDS)**: provides access to many of the DB systems such
    as PostgreSQL, MySQL, Oracle, etc.
* **DynamoDB**: the NoSQL counterpart to RDS.
* **Redshift**: a hosted data warehouse product, forms part of the larger cloud-computing
    platform Amazon Web Services. Redshift differs from RDS in its ability to handle
    analytics workloads on large-scale datasets stored by a column-oriented DBMS
    principle. To be able to handle large scale datasets Amazon makes use of
    massive parallel processing.
* **ElastiCache**: a fully managed in-memory data store and cache service. The service
    improves the performance of web applications by retrieving information from
    managed in-memory caches, instead of relying entirely on slower disk-based
    databases. Built on memcached and redis.
* **Snowball**: Snowball is a petabyte-scale data transport solution that uses secure
    appliances to transfer large amounts of data into and out of the AWS cloud.
* **Database Migration Service (DMS)**: helps you migrate databases to AWS easily
    and securely. The source database remains fully operational during the
    migration, minimizing downtime to applications that rely on the database.
    This service can also migrate from one DB to another, e.g. from Oracle
    to MySql.
* **Server Migration Services (SMS)**: is an agentless service which makes it
    easier and faster for you to migrate thousands of on-premises workloads
    to AWS. AWS SMS allows you to automate, schedule, and track incremental
    replications of live server volumes, making it easier for you to coordinate
    large-scale server migrations.
* **Athena**: an interactive query service that makes it easy to analyze data in S3
    using standard SQL. Athena is serverless, so there is no infrastructure
    to manage, and you pay only for the queries that you run. Simply point to
    your data in Amazon S3, define the schema, and start querying using
    standard SQL.
* **Elastic Map-Reduce (EMR)**: provides a managed Hadoop framework that makes it
    easy, fast, and cost-effective to process vast amounts of data across
    dynamically scalable Amazon EC2 instances. Also works with Spark, Hbase,
    etc.
* **CloudSearch**: A service which allows for searching based solutions, such as
    setting a search engine for your website, or searching through all the
    user documents you own, etc. Fully managed and provisioned by Amazon.
* **Elasticsearch**: Similar to cloudsearch, except that is open source and not
    provisioned by Amazon, which mean that the user needs to set things up.
    It comes with Kibana, which allows you to visualize your searches and
    allows you to extract meaningful data out of your searches.
* **kinesis**: a platform for streaming data, offering services to make it
    easy to load and analyze streaming data, and also providing the ability
    for the user to build custom streaming data applications for specialized
    needs.
* **Data Pipeline**: A web service that helps you reliably process and move data
    between different AWS compute and storage services, as well as on-premise
    data sources, at specified intervals.
* **Quicksight**: a fast, cloud-powered business analytics service that makes it
    easy to build visualizations, perform ad-hoc analysis, and quickly get
    business insights from your data.
* **Identity Access Management (IAM)**: A service for signing into AWS services,
    assigning users to groups, creating roles to access various resources on
    the AWS cloud, enabling 2-factor authentication, and so forth.
* **Inspector**: An automated security assessment service that helps improve the
    security and compliance of applications deployed on AWS. Amazon Inspector
    automatically assesses applications for vulnerabilities or deviations from
    best practices.
* **Secure Sockets Layer (SSL)/Transport Layer Security (TLS) certificates**: used
    to secure network communications and establish the identity of websites over
    the Internet.
* **Certificate Manager**: a service that lets you easily provision, manage, and
    deploy Secure Sockets Layer/Transport Layer Security (SSL/TLS) certificates
    for use with AWS services
* **Active Directory**: Is a directory service that Microsoft developed for Windows
    domain networks. A server running Active Directory Domain Services (AD DS)
    is called a domain controller. It authenticates and authorizes all users
    and computers in a Windows domain type network—assigning and enforcing security
    policies for all computers and installing or updating software.
* **Directory Service**: enables your directory-aware workloads and AWS resources
    to use managed Active Directory in the AWS Cloud.
* **Web Application Firewall (WAF)**: helps protect your web applications from
    common web exploits that could affect application availability, compromise
    security, or consume excessive resources. AWS WAF gives you control over which
    traffic to allow or block to your web applications by defining customizable
    web security rules.
* **Artifact**: Provides on-demand access to AWS’ security and compliance documents,
    also known as audit artifacts. Examples of audit artifacts include Service
    Organization Control (SOC) reports, Payment Card Industry (PCI) reports, and
    certifications from accreditation bodies across geographies and compliance
    verticals that validate the implementation and operating effectiveness of AWS
    security controls.
* **CouldWatch**: a monitoring service for AWS cloud resources and the applications
    you run on AWS. You can use Amazon CloudWatch to collect and track metrics,
    collect and monitor log files, set alarms, and automatically react to changes
    in your AWS resources.
* **CloudFormation**: Gives developers and systems administrators an easy way to create
    and manage a collection of related AWS resources, provisioning and updating
    them in an orderly and predictable fashion. To do this you would create a
    template to describe the AWS resources, and any associated dependencies or
    runtime parameters, required to run your application.
- **CloudTrail**: Is a service that enables governance, compliance, operational
    auditing, and risk auditing of your AWS account. With CloudTrail, you can log,
    continuously monitor, and retain events related to API calls across your AWS
    infrastructure.
* **OpsWorks**: Is a configuration management service that uses Chef, an automation
    platform that treats server configurations as code. OpsWorks uses Chef to
    automate how servers are configured, deployed, and managed across your
    Amazon Elastic Compute Cloud (Amazon EC2) instances or on-premises compute
    environments
* **Config**: A fully managed service that provides you with an AWS resource
    inventory, configuration history, and configuration change notifications to
    enable security and governance. Config Rules enables you to create rules that
    automatically check the configuration of AWS resources recorded by AWS Config.
* **Trusted Advisor**: An online resource to help you reduce cost, increase
    performance, and improve security by optimizing your AWS environment, Trusted
    Advisor provides real time guidance to help you provision your resources
    following AWS best practices.
* **Simple Workflow Service (SWF)**: Helps developers build, run, and scale
    background jobs that have parallel or sequential steps. You can think of
    Amazon SWF as a fully-managed state tracker and task coordinator in the
    Cloud. Can interleave tasks here with human tasks which must be completed
    before the next step and so on.
* **Step Functions**: coordinate the components of distributed applications
    and microservices using visual workflows. This differs from SWF as each step
    is serverless.
* **API Gateway**: A fully managed service that makes it easy for developers to
    create, publish, maintain, monitor, and secure APIs at any scale. You can
    create an API that acts as a “front door” for applications to access data,
    business logic, or functionality from your back-end services, such as
    sworkloads running on Amazon Elastic Compute Cloud (Amazon EC2), code running
    on AWS Lambda, or any Web application
* **AppStream 2.0**: A fully managed, secure application streaming service that
    allows you to stream desktop applications from AWS to any device running a
    web browser, without rewriting them.
* **Elastic Transcoder**: Media transcoding in the cloud. Convert (or “transcode”)
    media files from their source format into versions that will playback on
    devices like smartphones, tablets and PCs.
* **Code [Commit | Build | Deploy]**: Services to do things with code which is exactly
    what it sounds like.
* **Code Pipeline**: A continuous integration and continuous delivery service
    for fast and reliable application and infrastructure updates. CodePipeline
    builds, tests, and deploys your code every time there is a code
    change, based on the release process models you define.
* **Workspaces**: A fully managed, secure desktop computing service which runs
    on the AWS cloud. Amazon WorkSpaces allows you to easily provision
    cloud-based virtual desktops and provide your users access to the documents,
    applications, and resources they need from any supported device, including
    Windows and Mac computers, Chromebooks, iPads, Fire tablets, Android tablets,
    and Chrome and Firefox web browsers.
* **Lex**: service for building conversational interfaces into any application
    using voice and text. Lex provides the advanced deep learning functionalities
    of automatic speech recognition (ASR) for converting speech to text, and
    natural language understanding (NLU) to recognize the intent of the text,
    to enable you to build applications with highly engaging user experiences
    and lifelike conversational interactions.
* **Polly**: A service that turns text into lifelike speech. Polly lets you
    create applications that talk, enabling you to build entirely new
    categories of speech-enabled products
* **Machine Learning**: A service that makes it easy for developers of all
    skill levels to use machine learning technology. Amazon Machine Learning
    provides visualization tools and wizards that guide you through the
    process of creating machine learning (ML) models without having to
    learn complex ML algorithms and technology.
* **Rekognition**: A service that makes it easy to add image analysis to
    your applications. With Rekognition, you can detect objects, scenes,
    and faces in images. You can also search and compare faces.
    Rekognition’s API enables you to quickly add sophisticated deep
    learning-based visual search and image classification to your
    applications.
* **Simple Notification Service (SNS)**: fully managed push notification service that
    lets you send individual messages or to fan-out messages to large
    numbers of recipients.
* **Simple Queue Services (SQS)**: fully-managed message queuing service for
    reliably communicating among distributed software components and microservices
* **Simple Email Service (SES)**: Send emails etc.
