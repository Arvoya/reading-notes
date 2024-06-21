# AWS: Events

## Questions & Answers

[AWS SQS vs SNS](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)

1. What is the difference betweeen SQS and SNS?
SNS is a distributed publish-subscribe service
SQS is distributed message queuing service
  
2. What are some use cases for both SNS and SQS?
SNS is used for push notificaitons like sending emails to a large number of users.
SQS requires a consumer to poll the queue, and it has some persistence.

[AWS SNS and SQS](https://www.youtube.com/watch?v=mXk0MNjlO7A)

1. Describe how to use SQS and SNS in a “fanout” pattern.
You start with SNS which can go to a variety of SQS queues or other services. This
approach prevents single points of failure, allowing for the other SQS queues to
continue to work even if one fails.

2. Explain how “push notifications” work, using SNS.
SNS can can be used to send multiple notifications when it is triggered, it goes
out to all the subscribers.

[SQS and SNS Basics](https://www.youtube.com/watch?v=UesxWuZMZqI)

1. How might a large scale, distributed application make use of a Queue system like
SQS?
