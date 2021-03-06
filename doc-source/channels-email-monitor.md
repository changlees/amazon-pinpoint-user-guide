# Monitoring Email Activity with Amazon Pinpoint<a name="channels-email-monitor"></a>

For emails that you send as part of a campaign, Amazon Pinpoint provides options for monitoring your email activity\.

**Note**  
To monitor email activity, you must use a campaign\. You cannot monitor email activity outside of a campaign\.

## Streaming Email Event Data<a name="w3ab1c15c16c17b9"></a>

To monitor data, such as successful and failed email deliveries, configure Amazon Pinpoint to stream email event data to Amazon Kinesis Data Streams or Amazon Kinesis Data Firehose\. Then, you can use the Kinesis platform to analyze this email data\. For more information, see [Streaming Amazon Pinpoint Events to Kinesis](analytics-streaming.md#analytics-streaming-kinesis)\.

For examples of the event data that Amazon Pinpoint streams to Kinesis, see [Event Data](http://docs.aws.amazon.com/pinpoint/latest/developerguide/analytics-streaming.html#analytics-streaming-data) in the *Amazon Pinpoint Developer Guide*\.

## Amazon Pinpoint Analytics<a name="w3ab1c15c16c17c11"></a>

On the **Analytics** page in the Amazon Pinpoint console, you can view metrics for the number of active targetable users that you can engage with the email channel\. 