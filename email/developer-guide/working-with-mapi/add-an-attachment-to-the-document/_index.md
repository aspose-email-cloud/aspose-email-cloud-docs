---
title: "Add an Attachment To The Document"
type: docs
url: /add-an-attachment-to-the-document/
description: " Add an attachment to the document using MAPI with Aspose.Email Cloud API."
weight: 10
---

## **Add an attachment to the document**
Aspose.Email Cloud API allows you to add an attachment to the document using MAPI.
## **API Information**

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/email/Mapi/{name}/attachments/{attachment}|PUT|Add an attachment to document|[**AddMapiAttachment**](https://apireference.aspose.cloud/email/#/Mapi/AddMapiAttachment)|
## **cURL Examples**
You can try this here: [**AddMapiAttachment**](https://apireference.aspose.cloud/email/#/Mapi/AddMapiAttachment). 
Click on "*Try it out*" button to use this function. 

**Specify storage folders for MAPI and attachment with Swagger UI**

Use this JSON to specify storage folders for MAPI and attachment:

{{< tabs tabTotal="1" tabID="1" tabName1="JSON" >}}

{{< tab tabNum="1" >}}

```java

{

   "DocumentFolder":{

      "Storage":"First Storage",

      "FolderPath":"document/location/on/storage"

   },

   "AttachmentFolder":{

      "Storage":"First Storage",

      "FolderPath":"attachment/location/on/storage"

   }

}

```

{{< /tab >}}

{{< /tabs >}}

## SDK Examples ##

**Add an attachment to the document**

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

[**AddMapiAttachment**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/docs/EmailApi.md#addmapiattachment) - Add an attachment to the document.

[**AddAttachmentRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/docs/AddAttachmentRequest.md) - Add attachment request.

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Add-Attachment-To-Document-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

[**addMapiAttachment**](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/a980be836c9f0d9f80a317a3ef9c1efbe9844f25/docs/EmailApi.md#addmapiattachment) - Add an attachment to the document.

[**AddAttachmentRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/a980be836c9f0d9f80a317a3ef9c1efbe9844f25/docs/AddAttachmentRequest.md) - Add attachment request.

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Add-Attachment-To-Document-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

[**AddMapiAttachment**](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/855a1287594376de3de5c2cbf96fb896c39073a7/doc/EmailApi.md#addmapiattachment) - Add an attachment to the document.

[**AddAttachmentRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/855a1287594376de3de5c2cbf96fb896c39073a7/doc/AddAttachmentRequest.md) - Add attachment request.

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Add-Attachment-To-Document-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

[**add_mapi_attachment**](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/e66b9a7b649e94e34a23856ae706ec10ad25eb4e/sdk/docs/EmailApi.md#add_mapi_attachment) - Add an attachment to the document.

[**AddAttachmentRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/e66b9a7b649e94e34a23856ae706ec10ad25eb4e/sdk/docs/AddAttachmentRequest.md) - Add attachment request.

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Add-Attachment-To-Document-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

[**add_mapi_attachment**](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/10345091853eaf62bbf6b083dd861d0771efa3e3/docs/EmailApi.md#add_mapi_attachment) - Add an attachment to the document.

[**AddAttachmentRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/10345091853eaf62bbf6b083dd861d0771efa3e3/docs/AddAttachmentRequest.md) - Add attachment request.

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Add-Attachment-To-Document-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

[**addMapiAttachment**](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/37bfaf209b850defb882d5de9e832485275726c8/doc/EmailApi.md#addmapiattachment) - Add an attachment to the document.

[**AddAttachmentRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/37bfaf209b850defb882d5de9e832485275726c8/doc/AddAttachmentRequest.md) - Add attachment request.

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Add-Attachment-To-Document-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}
## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/email/sdk-setup/).

{{% /alert %}}
