What is the difference betweeen SQS and SNS?
   Entity Type
    SQS: Queue (similar to JMS, MSMQ).
    SNS: Topic-Subscriber (Pub/Sub system).

   Message consumption
    SQS: Pull Mechanism — Consumers poll messages from SQS.
    SNS: Push Mechanism — SNS pushes messages to consumers.

   Persistence
    SQS: Messages are persisted for some duration is no consumer available. The retention period value is from 1 minute to 14 days. The default is 4 days.
    SNS: No persistence. Whichever consumer is present at the time of message arrival, gets the message and the message is deleted. If no consumers available then the message is lost.

    In SQS message delivery is guaranteed but in SNS it is not.

   Consumer Type
    SQS: All the consumers are supposed to be identical and hence process the messages in exact same way.
    SNS: All the consumers are (supposed to be) processing the messages in different ways.

What are some use cases for both SNS and SQS?
  Use Cases
   Choose SNS if:
    - You would like to be able to publish and consume batches of messages.
    - You would like to allow same message to be processed in multiple ways.
    - Multiple subscribers are needed.

Choose SQS if:
    - You need a simple queue with no particular additional requirements.
    - Decoupling two applications and allowing parallel asynchronous processing.
    - Only one subscriber is needed.

Describe how to use SQS and SNS in a “fanout” pattern.
   you can use SNS to send a message to many receivers. the receiver could be an SQS system that maybe use your message to analyze things, or it can be a lambda function that will do some logic based on your message.

