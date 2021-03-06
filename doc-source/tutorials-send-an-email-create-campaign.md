# Step 5: Create a Campaign<a name="tutorials-send-an-email-create-campaign"></a>

After you create a segment, you can create a *campaign* and schedule Amazon Pinpoint to send it to your segment\.

In Amazon Pinpoint, a campaign refers to a single message that you send to a segment\. If you've used other digital user engagement tools in the past, you might have used phrases like "tactics" or "campaign elements" to refer to the same concept\.

**To create a new campaign**

1. In the navigation pane, choose **Campaigns**, and then choose **New campaign**\.

1. For **Campaign name**, type a name for the campaign\. 

1. Under **What messaging channel do you want to use**, choose **Email**\.

1. Under **Choose the campaign type**, choose **Standard campaign**, and then choose **Next step**\.

1. On the **Segment** page, choose **Use a previously defined segment**\. Then, for **Segment**, choose the segment that you created in the previous section\. Choose **Next step**\.

1. On the **Message** page, do the following:

   1. For **From address**, type the address that you want to send the email from\.

   1. For **Subject**, type the subject line of the email\. 

   1. For **Message**, type the body of the email\.
**Tip**  
You can modify the HTML body of your message directly by choosing the **edit HTML** \(![\[Image NOT FOUND\]](http://docs.aws.amazon.com/pinpoint/latest/userguide/images/campaigns_email_editor_edit_html.png)\) button in the message editor\.  
You can also include personalized content in your message\. You do this by adding the name of an attribute from the spreadsheet that you imported into Amazon Pinpoint\. When you specify an attribute in this way, surround the attribute name with two sets of curly braces\. For example, you could include the recipient's first name in the body of the message by typing `{{User.UserAttributes.FirstName}}` in the body of the message\.

   1. When you finish, choose **Next step**\.

1. On the **Schedule** page, choose **Immediate**, and then choose **Next step**\.
**Note**  
You can also choose to schedule the delivery of your message for a specific date and time\. To schedule the delivery of your message, choose **Once**, and then specify the date and time when you want Amazon Pinpoint to send the email\.   
If you want to send the message on a recurring basis, choose one of the other schedule options \(**Hourly**, **Daily**, **Weekly**, or **Monthly**\), and then specify the start and end times\.

1. On the **Review and launch** page, choose **Launch campaign**\.

**Next:** [Next Steps »](tutorials-send-an-email-next-steps.md)