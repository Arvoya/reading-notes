# AWS: API, Dynamo, and Lambda

## Questions & Answers

[AWS API Gateway Overview](https://www.serverless.com/amazon-api-gateway)

1. What is Amazon API Gateway?
  A way for requests to be routed to the correct services.
2. Why is Amazon API Gateway an important part of the Serverless ecosystem?
  You can use it to connect with Lambda functions, so in the context of serverless
  applications, it is a key component.
3.How does API Gateway integrate with other AWS services?j
  It can be used to connect with Lambda functions, DynamoDB, and other services.
  The lambda function can be triggered based on the gatway's configuration. Then
  the lambda function can be used to interact with other services including more
  lambda functions.

[AWS API Gateway](https://aws.amazon.com/api-gateway/)

1. What are the some benefits of using Amazon API Gateway?
  It can be used to create, publish, maintain, monitor, and secure APIs at any scale.
2. What two API types might you choose from?
  RESTful APIs and WebSocket APIs.

[AWS DynamoDB Guide](https://www.dynamodbguide.com/what-is-dynamo-db/)

1. What is DynamoDB?
  Amazon's key-value and document database.
2. Under what circumstances would you recommend DynamoDB over MongoDB?
  If you are using AWS already it might be nice to keep it all in the same ecosystem.

[AWS DynamoDB](https://aws.amazon.com/dynamodb/)

1. Explain to a non-technical friend how DynamoDB works.
  Databases are ways to store various types of data. DynamoDB is a service provided
  by Amaazon that allows you to store data in a way that is scalable and reliable.

[Dynamoose](https://dynamoosejs.com/getting_started/Introduction)

1. What is Dynamoose?
  Dynamoose is a modeling tool for Amazon's DynamoDB. Dynamoose is heavily inspired
  by Mongoose, which means if you are coming from Mongoose the syntax will be very
  familiar.
2. What are some key features of Dynamoose?
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
