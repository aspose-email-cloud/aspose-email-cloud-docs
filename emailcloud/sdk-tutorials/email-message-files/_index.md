---
title: "Email Message Files"
type: docs
url: /email-message-files/
description: " Aspose Email tutorial shows how to work with email files. Create emails, save emails, edit emails, send emails, receive emails and more."
weight: 20
---

## **How to Work With Email Message Files via Aspose.Email Cloud API**
[Aspose.Email Cloud API](https://products.aspose.cloud/email/family) supports email message files with EML, MSG, MHTML and HTML format. We have API for creating, editing, converting such files. Also, email message files can be used in the [built-in email client](/emailcloud/email-client/).

Our SDKs support two different ways of operating with email message files using [property sets](/emailcloud/working-with-email-properties/) and data transfer object EmailDto. This tutorial shows how to use an **EmailDto**.

{{% alert color="primary" %}} To see how to setup SDKs use the [SDK setup tutorial](/emailcloud/sdk-setup/). {{% /alert %}} 
## **Email Message Files**
Simply put, email message files are the files using to exchanging messages between people using electronic devices. Sounds simple, isn’t it? 

You may already know this. In our time, it’s hard to find a person who doesn't use email message. We use emails everywhere at our work, in a friendly conversation, etc.

There are many ways to send and retrieve emails, so, there are many file formats for these purposes.

Let's find out which email formats exist:

- [**EML**](https://wiki.fileformat.com/email/eml/) — using in Microsoft Outlook Express as well as some other email programs. An email message saved to a file in the MIME RFC 822 standard format. **EML** files usually contain plain ASCII text for the main message body, headers and hyperlinks and attachments.
- [**MSG**](https://wiki.fileformat.com/email/msg/) — using in Microsoft Outlook and Exchange. An **MSG** file can contain plain ASCII text as in **EML** files.
- [**HTML**](https://wiki.fileformat.com/web/html/) — the extension for web pages created for display in browsers. The HTML file format is very convenient to display emails on the web sites. 

As we have mentioned before, email message files are using for exchanging messages. With Aspose.Email Cloud API you can easily change the email’s data, attachments and other information. The API can help you to simplify the development of your product and achieve your goals. The Cloud approach provides you with the processing power of our servers, using them you do not need to process messages on your servers, provide this to us. User-friendly API provides security and ease of development.
## **How to Create Email Object and Save It as File on Storage**
The best way to work with emails is to use **EmailDto** objects. **EmailDto** object contains all email’s data:

{{% alert color="primary" %}} 

Email’s data that is contained in EmailDto

- Collection of alternate views of the message.
- Email message attachments.
- BCC recipients.
- Message subject.
- Sender address.
- The address collection that contains the recipients of a message.
- Email message body as plain text.
- Body encoding.
- The content type of message body. Enum, available values: PlainText, Html, Rtf.
- CC recipients.
- Message date.
- Delivery notifications. Items: Email delivery notification options.
- From address.
- Document headers.
- HTML body.
- Linked resources of a message.
- The list of addresses to reply to for the mail message.
- And other email’s data.

{{% /alert %}} 
## **Create Email File — EmailDto Object**
First, let's create an **EmailDto** object and save it as a file on the Storage.

To create an email file (EML, MSG, MHTML, HTML) you need to create [EmailDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/EmailDto.cs) object. To initialize [EmailDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/EmailDto.cs) object let’s define main fields: ***From*** (accepts [MailAddress](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/MailAddress.cs) object which contains the email address of a sender), ***To*** (accepts List of [MailAddress](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/MailAddress.cs) objects; parameter ***To*** can contain several email addresses), ***Subject*** (accepts a string with a subject of an email), ***Body*** (accepts a string with a body’s content).

After creating [EmailDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/EmailDto.cs) object we save it to [Storage](https://dashboard.aspose.cloud/#/storages). To save it we need to choose storage and folder where we want to save our created email file. Also, we need to create a name for this email file. [EmailApi](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md) class has a function called [*SaveEmailModelAsync*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#SaveEmailModelAsync) which requires one parameter — [*SaveEmailModelRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/SaveEmailModelRequest.cs). 

[SaveEmailModelRequest](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/SaveEmailModelRequest.cs) uses to define a file format (Enum, available values: EML, MSG, MsgUnicode, MHTML, HTML), name of an email file which we want to save on Storage (EmailDto) and the location of the email file on [Storage](https://dashboard.aspose.cloud/#/storages) ([StorageModelRqOfEmailDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/StorageModelRqOfEmailDto.cs) — has **2 required parameters**: [EmailDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/EmailDto.cs) object and StorageFolderLocation).

Look at the following code examples:

**How to create an EmailDto object and save it as a file on storage?**

{{< tabs tabTotal="6" tabID="1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-create-EmailDto-and-save-it-on-storage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-create-EmailDto-and-save-it-on-storage-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-create-email-file-and-save-it-on-storage-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-create-email-file-and-save-it-on-storage-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-create-email-file-and-save-it-on-storage-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-create-email-file-and-save-it-on-storage-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
 
  
You can edit the EmailDto object and save it again. If file name and location will be the same, the file will be overwritten.
## **How to Download Email File From Storage**
You can download files from the [Storage](https://dashboard.aspose.cloud/#/storages).

[EmailApi](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/EmailDto.cs) class has [DownloadFileAsync](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#DownloadFileAsync) function which allows to download files from [Storage](https://dashboard.aspose.cloud/#/storages) asynchronous as a Stream. This function has one required parameter —  [*DownloadFileRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/DownloadFileRequest.cs). To define it you need to pass **2 parameters** into it: a file’s path as a string and a name of [Storage](https://dashboard.aspose.cloud/#/storages) you want to download from.

To download the file that we created in the previous step from the Storage, use the following steps:

**How to download a file from the Storage?**

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-download-EmailDto-from-storage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-download-EmailDto-from-storage-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-download-EmailDto-from-storage-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-download-EmailDto-from-storage-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-download-EmailDto-from-storage-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-download-EmailDto-from-storage-1.php" >}}

{{< /tab >}}

{{< /tabs >}}

**Also, you can download a file in another format.**

Aspose.Email Cloud allows you to download email messages from [Storage](https://dashboard.aspose.cloud/#/storages) in many different file formats. For example, you have an EML file, you want to download it but in MSG. You can download it immediately without separate converting.

To download email file from [Storage](https://dashboard.aspose.cloud/#/storages) you need to call [*GetEmailAsFileAsync*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#GetEmailAsFileAsync)
 function from EmailApi. 
[GetEmailAsFileAsync](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#GetEmailAsFileAsync) accepts only one required parameter — 
[*GetEmailAsFileRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/GetEmailAsFileRequest.cs).

To initialize [*GetEmailAsFileRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/GetEmailAsFileRequest.cs) you need to pass **3 parameters** into it: a name of an email file on [Storage](https://dashboard.aspose.cloud/#/storages) as a string, a result file’s extension as an Enum (EML, MSG, MsgUnicode, MHTML, HTML), storage’s name as a string and a path to a folder on [Storage](https://dashboard.aspose.cloud/#/storages) where email file is.

If you do everything right you will get the email file as a Stream.

**How to download a file from the Storage in a different format?**

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-download-file-from-storage-in-any-format-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-download-file-from-storage-in-any-format-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-download-file-from-storage-in-any-format-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-download-file-from-storage-in-any-format-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-download-file-from-storage-in-any-format-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-download-file-from-storage-in-any-format-1.php" >}}

{{< /tab >}}

{{< /tabs >}}

**You can download the file as an EmailDto object:**

**EmailDto** provides you with an easier way to work with emails. It allows to change and get data from an email file in several code lines.

If you want to get an email from [Storage](https://dashboard.aspose.cloud/#/storages) as an [EmailDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailDto.md) object — you need to use [GetEmailModelAsync](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#getemailmodelasync) from [EmailApi](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/README.md). 

Unlike the previous case, here we need to pass [*GetEmailModelRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/GetEmailModelRequest.cs) 
into [GetEmailModelAsync](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#getemailmodelasync). 

[*GetEmailModelRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/GetEmailModelRequest.cs) accepts **2 required parameters**: 
an email document format as Enum (EML, MSG, MsgUnicode, MHTML, HTML), email document file name as a string; 
and 2 optional parameters: storage’s name as a string and a path to a folder on 
[Storage](https://dashboard.aspose.cloud/#/storages) where email file is as a string too.

After calling [*GetEmailModelAsync*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#getemailmodelasync) 
you get Task<[EmailDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailDto.md)> object.

**How to download a file as EmailDto object?**

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-download-file-from-storage-as-EmailDto-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-download-file-from-storage-as-EmailDto-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-download-file-from-storage-as-EmailDto-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-download-file-from-storage-as-EmailDto-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-download-file-from-storage-as-EmailDto-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-download-file-from-storage-as-EmailDto-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
## **How to Append Email Object to "INBOX" Folder of IMAP Account**
We can append this EmailDto object to the "INBOX" folder of an IMAP account:

{{% alert color="primary" %}} 

See how to setup and use email client in the [Quickstart with an email client](https://docs.aspose.cloud/display/LGIS/Quick+start+with+an+email+client)[ tutorial.](https://docs.aspose.cloud/display/LGIS/Quick+start+with+an+email+client)

{{% /alert %}} 



To append an email to the "INBOX" folder of an IMAP account, **you should create \*.account file with IMAP account credentials at first**. 
Then you need to call [*AppendEmailModelMessageAsync*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#AppendEmailModelMessageAsync) function from [EmailApi](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/README.md).

[AppendEmailModelMessageAsync](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#AppendEmailModelMessageAsync) has only one required parameter — [*AppendEmailModelMessageRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/AppendEmailModelMessageRequest.cs). This function requests an EmailDto object for append operation.

This needs an [*AppendEmailModelRq*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/AppendEmailModelRq.cs) object, which has 6 parameters:

1. First account storage file name for receiving emails (or use universal one) as a **string**.
1. Second account storage file name for sending emails (ignored if first is universal) as a **string**.
1. Storage folder location of account files as a **string**.
1. Email account folder to store a message as a **string**. For example, "INBOX".
1. Mark message as sent. Nullable bool parameter.
1. Email document. **EmailDto** object that we want to append to a folder.

As a result, you will add an email from model to a specified folder in an email account. 

**How to append EmailDto object to the "INBOX" folder of an IMAP account?**

{{< tabs tabTotal="6" tabID="5" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-append-EmailDto-to-IMAP-account-folder-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-append-EmailDto-to-IMAP-account-folder-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-append-EmailDto-to-IMAP-account-folder-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-append-EmailDto-to-IMAP-account-folder-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-append-EmailDto-to-IMAP-account-folder-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-append-EmailDto-to-IMAP-account-folder-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
## **How to Convert Email From One Format to Another**
If you don't want to use all these models and storages, and just want to convert email file from one format to another, use the fast and convenient Converter developed by Aspose.

To convert email file use [ConvertEmailAsync](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#ConvertEmailAsync) from [EmailApi](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/README.md). This function requires only one parameter — [*ConvertEmailRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/ConvertEmailRequest.cs) which requests a model for converting.

It has **2 required parameters**:

1. Email file format as Enum (EML, MSG, MsgUnicode, MHTML, HTML).
1. File to upload as a Stream.



**How to convert an email from one format to another?**

{{< tabs tabTotal="6" tabID="6" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-convert-email-to-another-fromat-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-convert-email-to-another-fromat-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-convert-email-to-another-fromat-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-convert-email-to-another-fromat-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-convert-email-to-another-fromat-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-convert-email-to-another-fromat-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
## **More Tutorials**
See more Aspose Email tutorials: 
