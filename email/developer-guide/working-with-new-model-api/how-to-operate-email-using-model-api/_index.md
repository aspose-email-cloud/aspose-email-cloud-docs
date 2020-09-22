---
title: "How To Operate Email Using Model API"
type: docs
url: /how-to-operate-email-using-model-api/
weight: 30
---

## **Introduction**
{{% alert color="primary" %}} [EML](https://wiki.fileformat.com/email/eml/) file format represents email messages saved using Outlook and other relevant applications. Almost all emailing clients support this file format for its compliance with RFC-822 Internet Message Format Standard. {{% /alert %}} 
## **Model API**
When using Model API, the files are represented using models.

Email Model API supports:

- Get email document (EML/MHT/MSG/HTML) from storage as EmailDto ([GetEmailModel](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#GetEmailModel))
- Save EmailDto to file on storage, using one of the supported formats ([SaveEmailModel](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#SaveEmailModel))
- Get the list of email documents from Storage folder ([GetEmailModelList](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#GetEmailModelList))
- Send email using a built-in client ([SendEmailModel](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#SendEmailModel))
- Add an email to a specified folder in email account ([AppendEmailModelMessage](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#AppendEmailModelMessage))
- Fetch message from email account ([FetchEmailModel](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#FetchEmailModel))
- Get messages from email account folder ([ListEmailModels](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#ListEmailModels))

Create [EmailDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailDto.md) object with [AlternateView](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/AlternateView.md). The conversion details can be found over [How to operate iCalendar using Model API](/email/how-to-operate-icalendar-using-model-api/):



**Create EmailDto object with AlternateView** 

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Email-Create-CalendarDto-Object-1.cs" >}}

The email variable now represents an email message with iCalendar in it. This email can be saved to a .eml file.

**Save Email as .eml file**

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Email-Save-Email-As-EMLFormat-1.cs" >}}

Once an email has been created, the email can be sent to [attendee@aspose.com](/email/mailto-attendee@aspose-com/) using built-in email client: 

**Send email using builtin client**

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Email-Send-Email-Using-Client-1.cs" >}}
## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/email/sdk-setup/).

{{% /alert %}}
