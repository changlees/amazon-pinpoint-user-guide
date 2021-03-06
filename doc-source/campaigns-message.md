# Step 3: Write the Message<a name="campaigns-message"></a>

Write the message that your campaign delivers to your audience segment\. If you chose to create a standard campaign, you write a single message, which you can revise after you launch the campaign\.

If you chose to create an A/B test for your campaign's message, you define two or more *treatments*, which are variations of your message that the campaign sends to different portions of the segment\. You cannot revise your treatments after you launch the campaign\.

**Prerequisite**  
Before you begin, complete [Step 2: Specify the Audience Segment for the Campaign](campaigns-segment.md)\.

## Writing a Mobile Push Message<a name="campaigns-message-mobile"></a>

If you chose **Mobile push** as the channel type, write the push notification that your campaign sends to your user segment, and choose the action that occurs when a user opens the notification\.

**Choose the notification type**
+ Choose the type of notification that your campaign delivers:  
![\[The options to create a standard notification or a silent notification.\]](http://docs.aws.amazon.com/pinpoint/latest/userguide/images/campaigns_messagetype.png)![\[The options to create a standard notification or a silent notification.\]](http://docs.aws.amazon.com/pinpoint/latest/userguide/)![\[The options to create a standard notification or a silent notification.\]](http://docs.aws.amazon.com/pinpoint/latest/userguide/)
  + **Standard notification** – A push notification with a title and message\. Users are alerted by their mobile devices when they receive the notification\.
  + **Silent notification** – A custom JSON attribute\-value pair that Amazon Pinpoint sends to your app without alerting users\. Use silent notifications to send data that your app code is designed to receive and handle, for example to update the app's configuration or to show messages in the app\.

**To write a standard notification**

1. If you previously saved a template that you want to use for your message, load it by choosing **Load template**\. The **Title** and **Message** are populated with the contents of the template\.

1. For **Title**, type the title you want to display above the message\.

1. For **Message**, type the message body\. Your push notification can have up to 200 characters\. A character counter below the right edge of the field counts down from 200 as you enter the text of the message\.

   When you finish writing your message, you can save it as a template for later use by choosing **Save as template**\.

1. \(Optional\) For **Time To Live**, specify the length of time \(in seconds\) that the message is stored by the push notification services to which Amazon Pinpoint sends the message\. These services can include Apple Push Notification service \(APNs\), Firebase Cloud Messaging \(FCM\), and Google Cloud Messaging \(GCM\)\.

   While storing the message, the push notification service attempts to deliver it until the delivery succeeds\. If you specify **0**, the message is not stored and delivery is attempted only once\. If this delivery fails, the message is discarded\.

1. For **Action**, select the action you want to occur if the user opens the notification:
   + **Open app** – Your app launches, or it becomes the foreground app if it has been sent to the background\.
   + **Go to URL** – The default mobile browser on the user's device launches and opens a web page at the URL you specify\. For example, this action can be useful for sending users to a blog post\.
   + **Deep link** – Your app opens and displays a designated user interface\. Deep link is an iOS and Android feature\. For example, this action can be useful to direct users to special promotions for in\-app purchases\.

1. \(Optional\) In the **Media URLs** section, you can optionally provide URLs that point to media files that are displayed in your push notification\. The URLs must be publicly accessible so that the push notification services for Android or iOS can retrieve the images\.

1. If you are creating an A/B test for the campaign message, complete steps under *Creating a Message A/B Test*\. Otherwise, choose **Next step**\.

## Writing an Email Message<a name="campaigns-message-email"></a>

If you chose **Email** as the channel type, write the email that your campaign sends to your user segment\.

1. If you previously saved a template that you want to use for your message, load it by choosing **Load template**\. The **Subject** and **Message** are populated with the contents of the template\.

1. For **Subject**, type the subject for your email\.

1. For **Message**, type the email body\. You can use the rich text editor to format your message:  
![\[The icons in the email message rich text editor.\]](http://docs.aws.amazon.com/pinpoint/latest/userguide/images/campaigns_email_editor.png)![\[The icons in the email message rich text editor.\]](http://docs.aws.amazon.com/pinpoint/latest/userguide/)![\[The icons in the email message rich text editor.\]](http://docs.aws.amazon.com/pinpoint/latest/userguide/)

   To write your message body as HTML, choose the source icon:  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/pinpoint/latest/userguide/images/campaigns_email_source.png)![\[Image NOT FOUND\]](http://docs.aws.amazon.com/pinpoint/latest/userguide/)![\[Image NOT FOUND\]](http://docs.aws.amazon.com/pinpoint/latest/userguide/)

   When you finish writing your message, you can save it as a template for later use by choosing **Save as template**\.

1. \(Optional\) Under **Plain text message**, type a version of your message for email clients that accept only plain text emails\.

1. If you are creating an A/B test for the campaign message, complete steps under *Creating a Message A/B Test*\. Otherwise, choose **Next step**\.

## Writing an SMS Message<a name="campaigns-message-sms"></a>

If you selected **SMS** as the channel type, write the text message that your campaign sends to your user segment\.

1. If you previously saved a template that you want to use for your message, load it by choosing **Load template**\. The **Message** is populated with the contents of the template\.

1. For **Message type**, choose one of the following:
   + **Promotional** – Noncritical messages, such as marketing messages\. Amazon Pinpoint optimizes the message delivery to incur the lowest cost\.
   + **Transactional** – Critical messages that support customer transactions, such as one\-time passcodes for multi\-factor authentication\. Amazon Pinpoint optimizes the message delivery to achieve the highest reliability\.

   This campaign\-level setting overrides your default message type, which you set on the **Settings** page\.

1. For **Message**, type the message body\. 

   Your text message can have up to 160 characters\. A character counter below the right edge of the field counts down from 160 as you enter the text of the message\.

   When you finish writing your message, you can save it as a template for later use by choosing **Save as template**\.

1. \(Optional\) For **Sender ID**, type a custom ID that contains up to 11 alphanumeric characters, including at least one letter and no spaces\. The sender ID is displayed as the message sender on the receiving device\. For example, you can use your business brand to make the message source easier to recognize\.

   Support for sender IDs varies by country or region\. For more information, see [Supported Countries and Regions](channels-sms-countries.md)\.

   This message\-level sender ID overrides your default sender ID, which you set on the **Settings** page\.

1. If you are creating an A/B test for the campaign message, complete steps under *Creating a Message A/B Test*\. Otherwise, choose **Next step**\.

## Creating a Message A/B Test<a name="campaigns-message-abtest"></a>

For a campaign that includes an A/B test of the message, define two or more message treatments\.

1. To help you start, Amazon Pinpoint provides two treatments\. If you want more treatments, choose **Add more**\.  
![\[Amazon Pinpoint provides two treatments to get you started, and you can add more.\]](http://docs.aws.amazon.com/pinpoint/latest/userguide/images/campaigns_allocation.png)![\[Amazon Pinpoint provides two treatments to get you started, and you can add more.\]](http://docs.aws.amazon.com/pinpoint/latest/userguide/)![\[Amazon Pinpoint provides two treatments to get you started, and you can add more.\]](http://docs.aws.amazon.com/pinpoint/latest/userguide/)

1. For each treatment, do the following:

   1. Customize the treatment name to make it easy to recognize later\.

   1. Define the message settings and write the message content\.

   1. Set the **Treatment allocation** to specify the percentage of users in the segment who will receive the message for the treatment\.

      As you set the allocation for each treatment, the **Holdout** value adjusts to represent the total percentage of users who will not receive messages delivered by this campaign\.

1. When you finish defining your treatments, choose **Next step**\.

## Testing Messages<a name="campaigns-message-test"></a>

Amazon Pinpoint can display a preview of a message that you can view before you schedule the message to be sent\. You can also send a test message to a small group of recipients for testing purposes\. You can send test messages for email, SMS, and mobile push campaigns\.

When you send test messages, consider the following factors:
+ You're charged for sending test messages as if they were regular campaign messages\. For example, if you send 10,000 test emails in a month, you're charged USD $1\.00 for sending the test emails\. For more information about pricing, see [Amazon Pinpoint Pricing](https://aws.amazon.com/pinpoint/pricing/)\.
+ Test messages count toward your account's sending limits\. For example, if your account is authorized to send 10,000 emails per 24\-hour period, and you send 100 test emails, you can send up to 9,900 additional emails in the same 24\-hour period\.
+ When you send a test message to specific users, you can specify up to 10 addresses\. Use commas to separate multiple addresses\.
**Note**  
The word "address" \(as it's used in this section\) can refer to any of the following: an email address, a mobile phone number, an endpoint ID, or a device token\.
+ When you send a test SMS message to specific phone numbers, the numbers must be listed in E\.164 format\. That is, they must include a plus sign \(\+\), the country code without a leading zero, and the complete subscriber number, including area code\. E\.164\-formatted numbers shouldn't contain parentheses, periods, hyphens, or any symbols other than the plus sign\. E\.164 phone numbers can have a maximum of 15 digits\.
+ When you send a test push notification, the addresses must be either endpoint IDs or device tokens\.
+ When you send a test message to a segment, you can only choose one segment\. Additionally, you can only choose segments that contain 100 endpoints or fewer\.
+ When you send a test message to a segment, Amazon Pinpoint creates a campaign for that test\. The name of the campaign contains the word "test", followed by four random alphanumeric characters, followed by the name of the campaign\. These campaigns aren't counted toward the maximum number of active campaigns that your account can contain\. Amazon Pinpoint doesn't create a new campaign when you send a test message to specific recipients\.
+ Events that are associated with test messages are counted in the metrics for the parent campaign\. For example, the Delivered chart in the Campaign dashboard includes the number of test messages that were successfully delivered\.

### Sending a Test Message<a name="campaigns-message-test-send"></a>

It's often helpful to send a test message to actual recipients in order to make sure that your message appears correctly when your customers receive it\. By sending a test version of a message, you can test incremental improvements to the content and appearance of your message without impacting the status of your campaign\.

There are two ways to send a test message: you can send it to an existing segment, or you can send it to a list of addresses that you specify\. The method you choose depends on your use case\. For example, if you have a regular group of people who test your messages, you might find it helpful to create a segment that contains all of their endpoints\. If you need to send to a group of testers that changes regularly, or to a dynamically generated address, you might find it easier to manually specify your recipients\.

**To send a test message to a segment**

1. Under the message editor, choose **Test campaign message**\.

1. On the **Test campaign** dialog box, under **Send test to**, choose **A segment**\.

1. Use the drop\-down list to choose the segment you want to send the test message to\.
**Note**  
Amazon Pinpoint automatically removes all segments that contain 100 endpoints or more from this list\.

1. Choose **Send test campaign**\.

**To send a test message to specific recipients**

1. Under the message editor, choose **Send a test message**\.

1. On the **Test campaign** dialog box, under **Send test to**, choose one of the options in the following table\.    
[\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/pinpoint/latest/userguide/campaigns-message.html)

1. Choose **Send test campaign**\.

### Previewing an Email Without Sending It<a name="campaigns-message-test-preview"></a>

Amazon Pinpoint can generate a preview of an email message without sending it\. This feature is helpful when you want to quickly verify that a message renders as you expect it to before you send a test\. 

Note that this preview only shows how the message would appear if it were rendered by your web browser\. As a best practice, you should still send test emails to several recipients and view those test messages using a variety of devices and email clients\.

**To preview an email**
+ Under the message editor, choose **Preview message**\. A preview of your email appears in a new window\.

## Message Templates<a name="campaigns-message-templates"></a>

To save your message and reuse it in a separate campaign or direct message, choose **Save as template** and provide a template name\. Then, you can load the template for any message by choosing **Load template** and selecting it from a list of saved templates\. Amazon Pinpoint populates your message with the template's content\. Then, you can send the message as\-is or customize as needed\.

You can base a template on any supported message type, and you can use the same template for other message types\. For example, you can write a push notification message, save it as a template, and use that template for an SMS message\. Note that if you use a single template for multiple message types, Amazon Pinpoint loads the content differently for each type\. For example, if you base a template on a mobile push message, and you load this template for an email message, the push notification *title* is used as the email *subject*\. The correlations between message parts are as follows:


**Mobile push templates**  

| The mobile push \. \. \.  | Is used as the email \. \. \. | Is used as the SMS \. \. \. | 
| --- | --- | --- | 
| Title | Subject | Not used | 
| Message body | Plain text message | Message body | 


**Email templates**  

| The email \. \. \. | Is used as the mobile push \. \. \.  | Is used as the SMS \. \. \. | 
| --- | --- | --- | 
| Subject | Title | Not used | 
| Message body \(HTML\) | Not used | Not used | 
| Plain text message | Message body | Message body | 


**SMS templates**  

| The SMS \. \. \. | Is used as the mobile push \. \. \.  | Is used as the email \. \. \. | 
| --- | --- | --- | 
| Message type | Title | Subject | 
| Message body | Message body | Plain text message | 

### Email Template Restrictions<a name="campaigns-message-templates-restrictions"></a>

Email templates can only include the HTML elements and attributes listed in the following table\.


| Allowed Elements | Allowed Attributes | 
| --- | --- | 
| a | dir, href, style, title | 
| b | dir, style, title | 
| blockquote | cite, dir, style, title | 
| br | dir, style, title | 
| caption | dir, style, title | 
| cite | dir, style, title | 
| code | dir, style, title | 
| col | dir, span, style, title | 
| colgroup | dir, span, style, title | 
| dd | dir, style, title | 
| div | dir, style, title | 
| dl | dir, style, title | 
| dt | dir, style, title | 
| em | dir, style, title | 
| h1 | dir, style, title | 
| h2 | dir, style, title | 
| h3 | dir, style, title | 
| h4 | dir, style, title | 
| h5 | dir, style, title | 
| h6 | dir, style, title | 
| i | dir, style, title | 
| img | alt, dir, height, src, style, title, width | 
| li | dir, style, title, value | 
| ol | dir, reversed, start, style, title, type | 
| p | dir, style, title | 
| pre | dir, style, title | 
| q | cite, dir, style, title | 
| small | dir, style, title | 
| span | dir, style, title | 
| strike | dir, style, title | 
| strong | dir, style, title | 
| sub | dir, style, title | 
| sup | dir, style, title | 
| table | dir, style, title | 
| tbody | dir, style, title | 
| td | colspan, dir, rowspan, style, title | 
| tfoot | dir, style, title | 
| th | abbr, colspan, dir, rowspan, scope, sorted, style, title | 
| thead | dir, style, title | 
| tr | dir, style, title | 
| u | dir, style, title | 
| ul | dir, style, title | 

Additionally, some attributes—such as `src` or `href`—allow you to specify a protocol\. If your HTML templates include these attributes, they can only specify certain protocols\. The allowed protocols for these attributes are listed in the following table\.


| Element/attribute | Allowed protocols | 
| --- | --- | 
| <a href="\.\.\."> | ftp, http, https, mailto | 
| <blockquote cite="\.\.\."> | http, https | 
| <img src="\.\.\."> | http, https | 
| <q cite="\.\.\."> | http, https | 

## Message Variables<a name="campaigns-message-variables"></a>

To create a message that is personalized for each recipient, use message variables\. Message variables refer to specific *endpoint* attributes\. These attributes can include characteristics that you add to the endpoint resource, such as the recipient's name, city, device, or operating system\. When Amazon Pinpoint sends the message, it substitutes the variables with the corresponding attribute values for the receiving endpoint\.

For the attributes, see [Endpoint Attributes](http://docs.aws.amazon.com/pinpoint/latest/apireference/rest-api-endpoints.html#rest-api-endpoints-attributes)\.

To include a variable in your message, enclose the attribute name in double brackets, as in `{{Demographic.AppVersion}}`\.

Often, the most useful endpoint attribute for message variables is `{{Attributes.customAttributeName}}`, where `customAttributeName` refers to custom attributes that you add to the endpoint\. By using custom attributes for your variables, you can display personalized messages that are unique for each recipient\.

For example, if your app is a fitness app for runners and it includes custom attributes for the user's name, activity, and personal record, you could use variables in the following message:

`Hey {{Attributes.userName}}, congratulations on your new {{Attributes.activity}} PR of {{Attributes.personalRecord}}!`

When Amazon Pinpoint delivers this message, the content varies for each recipient after the variables are substituted\. Possible final messages are:

`Hey Jane Doe, congratulations on your new half marathon PR of 1:42:17!`

Or:

`Hey John Doe, congratulations on your new 5K PR of 20:52!`

For examples of custom attributes for your app's code, see the [iOS example](http://docs.aws.amazon.com/pinpoint/latest/developerguide/mobile-sdk-ios-register.html#mobile-sdk-ios-custom-attributes) or the [Android example](http://docs.aws.amazon.com/pinpoint/latest/developerguide/mobile-sdk-android-register.html#mobile-sdk-android-custom-attributes)\.

**Next**  
[Step 4: Set the Campaign Schedule](campaigns-schedule.md)