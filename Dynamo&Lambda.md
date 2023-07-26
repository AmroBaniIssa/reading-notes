What is Amazon API Gateway?
 Amazon API Gateway is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend business logic. It also handles authentication, access control, monitoring, and tracing of API requests.

Why is Amazon API Gateway an important part of the Serverless ecosystem?
 Within the Serverless ecosystem, API Gateway is the piece that ties together Serverless functions and API definitions. Being able to trigger the execution of a Serverless function directly in response to an HTTP request is the key reason why API Gateway is so valuable in Serverless setups: it enables a truly serverless architecture for web applications. When using API Gateway together with other AWS services, it’s possible to build a fully functional customer-facing web application without maintaining a single server yourself.

 This brings the advantages of the serverless model—scalability, low maintenance, and low cost due to low overhead—to mainstream web applications.


How does API Gateway integrate with other AWS services?
    - Invoking an AWS Lambda function.
    - Invoking another HTTP endpoint, with or without VPC Link.
    - Making an HTTP call against the API of any AWS service that provides an HTTP API.
    - Returning a mock response generated within API Gateway without calling out to other services.

What are the some benefits of using Amazon API Gateway?
    - Efficient API development
    - Performance at any scale
    - Cost savings at scale
    - Easy monitoring
    - Flexible security controls
    - RESTful API options


What is DynamoDB?
 DynamoDB is a hosted NoSQL database offered by Amazon Web Services (AWS). It offers:

    - reliable performance even as it scales;
    - a managed experience, so you won't be SSH-ing into servers to upgrade the crypto libraries;
    - a small, simple API allowing for simple key-value access as well as more advanced query patterns.

Under what circumstances would you recommend DynamoDB over MongoDB?
   
    DynamoDB is a particularly good fit for the following use cases:

     - Applications with large amounts of data and strict latency requirements. As your amount of data scales, JOINs and advanced SQL operations can slow down your queries. With DynamoDB, your queries have predictable latency up to any size, including over 100 TBs!

     - Serverless applications using AWS Lambda. AWS Lambda provides auto-scaling, stateless, ephemeral compute in response to event triggers. DynamoDB is accessible via an HTTP API and performs authentication & authorization via IAM roles, making it a perfect fit for building Serverless applications.

     - Data sets with simple, known access patterns. If you're generating recommendations and serving them to users, DynamoDB's simple key-value access patterns make it a fast, reliable choice.

What is Dynamoose?
   Dynamoose is a modeling tool for Amazon's DynamoDB. Dynamoose is heavily inspired by Mongoose, which means if you are coming from Mongoose the syntax will be very familiar.


What are some key features of Dynamoose?
   - Type safety
   - High level API
   - Easy to use syntax
   - DynamoDB Single Table Design Support
   - Ability to transform data before saving or retrieving items
   - Strict data modeling (validation, required attributes, and more)
   - Support for DynamoDB Transactions
   - Powerful Conditional/Filtering Support
   - Callback & Promise support
   - AWS Multi-region support