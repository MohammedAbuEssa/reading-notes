# AWS: Events

### [AWS SQS vs SNS](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)

1. What is the difference betweeen SQS and SNS?

SQS is a message queue service for decoupling components, while SNS is a pub/sub service for broadcasting messages to multiple subscribers. SQS uses point-to-point communication, whereas SNS follows a publish/subscribe model. SQS retains messages in the queue, while SNS doesn't retain messages.

2. What are some use cases for both SNS and SQS?

SNS (Simple Notification Service) Use Cases:

- Real-time notifications.
- Fan-out messaging.
- Email and SMS alerts.

SQS (Simple Queue Service) Use Cases:

- Load leveling.
- Task decoupling.
- Reliable message delivery.

---

### [AWS SNS and SQS](https://www.youtube.com/watch?v=mXk0MNjlO7A)

1. Describe how to use SQS and SNS in a “fanout” pattern.

- Create an SNS topic (e.g., "Credit card").
- Add subscribers, such as SQS queues or other endpoints, to the SNS topic.
- Publish messages to the SNS topic.
- Each subscriber (SQS queue, etc.) receives a copy of the message and processes it independently.
- SNS will automatically distribute the message to all subscribers.

2. Explain how “push notifications” work, using SNS.

- Register devices with unique tokens for each platform (e.g., iOS, Android) on SNS.

- Create an SNS platform application for the specific platform (e.g., APNs for iOS, FCM for Android).

- Link registered device tokens to the platform application.

- Publish push notifications to the platform application.

- SNS delivers the notifications to the registered devices in real-time.

---

### [SQS and SNS Basics](https://www.youtube.com/watch?v=UesxWuZMZqI)

1. How might a large scale, distributed application make use of a Queue system like SQS?

- Load balance and scale components.
- Decouple application services.
- Handle asynchronous processing.
- Ensure fault tolerance and durability.
- Implement rate limiting.
- Reduce resource contentions.

---

Bookmark and Review

### [SNS Javascript SDK](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SNS.html)

### [SQS Javascript SDK](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SQS.html)

## [Main Page](../README.md)
