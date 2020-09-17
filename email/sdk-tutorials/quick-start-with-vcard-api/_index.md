---
title: "Quick Start With VCard API"
type: docs
url: /quick-start-with-vcard-api/
description: "Aspose Email tutorial — how to work with contact card files using Aspose.Email Cloud. Create, edit, process VCard, scan business card images to VCard."
weight: 50
---

## **VCard API**
[Aspose.Email Cloud API](https://products.aspose.cloud/email/family) supports working with VCard files. You can use our API to read, edit and save VCard files. Also, you can use our Business card recognition API to parse VCard file from image.

The SDKs support two different ways of operating with VCard files using property sets and data transfer object ContactDto. This tutorial shows how to use ContactDto.

{{% alert color="primary" %}} To see how to setup SDKs use the [SDK setup](/emailcloud/sdk-setup/) tutorial. {{% /alert %}} 
## **How to Create Contact File Object and Save It to Storage**
**ContactDto** object contains all contact’s information such as gender, surname, email addresses, phone numbers, etc.

Let’s create a **ContactDto** object and save it to the Storage as **.vcf** or **.msg** file.

To save **ContactDto** use [**SaveContactModelAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#SaveContactModelAsync) from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). 
This method requires **1 parameter** — [**SaveContactModelRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/SaveContactModelRequest.cs), which is a request for this operation.

[**SaveContactModelRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/SaveContactModelRequest.cs) has **3 parameters**:

- *Format —* Contact document format. Enum, available values: VCard, WebDav, Msg.
- *Name* — Contact document file name.
- *Rq* — Create contact request. This parameter accepts [**StorageModelRqOfContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/StorageModelRqOfContactDto.cs), 
to initialize this model you should define 2 parameters: *Value —* ContacDto object and StorageFolder — [**StorageFolderLocation**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/StorageFolderLocation.cs) object. 

**How to create ContactDto object and save it to the Storage?**

{{< tabs tabTotal="6" tabID="1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Create-ContactDto-Save-To-Storage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Create-ContactDto-Save-To-Storage-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Create-ContactDto-Save-To-Storage-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Create-ContactDto-Save-To-Storage-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Create-ContactDto-Save-To-Storage-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Create-ContactDto-Save-To-Storage-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
## **How to Download VCard File From Storage**
You can find the saved file on [Aspose.Cloud Dashboard](https://dashboard.aspose.cloud/#/files), or download it using SDK.

To find the contact card file on Storage use [**DownloadFileAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#DownloadFileAsync) 
from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). 
This method requires **1 parameter** — [**DownloadFileRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/DownloadFileRequest.cs), which is a request for this operation.

[**DownloadFileRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/DownloadFileRequest.cs) has **3 parameters**:

- *Path* — File path e.g. "/folder/contact_card".
- *StorageName* — Storage name.
- *VersionId* [**optional**] — File version ID to download

**How to download VCard file from the Storage?**

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Download-ContactDto-From-Storage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Download-ContactDto-From-Storage-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Download-ContactDto-From-Storage-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Download-ContactDto-From-Storage-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Download-ContactDto-From-Storage-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Download-ContactDto-From-Storage-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
## **How to Get VCard File From Storage as ContactDto Object**
Let's get this file from storage as a ContactDto object.

To get a contact card file from Storage as **ContactDto** use [**GetContactModelAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#GetContactModelAsync) from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). This method requires **1 parameter** — [**GetContactModelRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/GetContactModelRequest.cs), which is a request for this operation.

[**GetContactModelRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/GetContactModelRequest.cs) has **4 parameters**:

- *Format —* Contact document format. Enum, available values: VCard, WebDav, Msg.
- *Name* — VCard file name in storage.
- *Folder* — Path to the folder in storage.
- *Storage* — Storage name.

**How to get VCard file from the Storage as a ContactDto object?**

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Download-Contact-Card-File-From-Storage-As-ContactDto-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Download-Contact-Card-File-From-Storage-As-ContactDto-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Download-Contact-Card-File-From-Storage-As-ContactDto-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Download-Contact-Card-File-From-Storage-As-ContactDto-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Download-Contact-Card-File-From-Storage-As-ContactDto-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Download-Contact-Card-File-From-Storage-As-ContactDto-1.php" >}}

{{< /tab >}}

{{< /tabs >}}

You can change model fields and save it again. The file will be rewritten if you don't change file name and location.
## **How to Use Business Card Recognition API**
{{% alert color="primary" %}} To get more information take a look at the [Business Cards Recognition API](/emailcloud/business-cards-recognition-api/). {{% /alert %}} 

Now, let's use our **Business Card Recognition API**.

First, we need an image of a business card. Something like this:

![todo:image_alt_text](quick-start-with-vcard-api_1.png)

This file should be placed somewhere on the disk, for example at "*/tmp/alex.png*". To use our parsing API, we should read the file. We need to convert it to the base64 string and send it to parser using our SDK.

To parse an image of a contact card use [**AiBcrParseModelAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#AiBcrParseModelAsync) from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). This method requires **1 parameter** — [**AiBcrParseModelRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/AiBcrParseModelRequest.cs), which is a request for this operation.

To initialize this request define [**AiBcrBase64Rq**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/AiBcrBase64Rq.cs) object.

[**AiBcrBase64Rq**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/AiBcrBase64Rq.cs) has **2 parameters**:

- *Options —* Recognition options. [**AiBcrOptions**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/AiBcrOptions.cs) has **2 parameters**:
  - *Languages —* Comma-separated ISO-639 codes of languages (either 639-1 or 639-3; i.e. "it" or "ita" for Italian); it's "" by default.
  - *Countries —* Comma-separated codes of countries.
- *Images* — Vcard file name in storage.  List of [**AiBcrBase64Image**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/AiBcrBase64Image.cs) has **2 parameters**:
  - *IsSingle* — Determines that image contains single VCard or more. Ignored in the current version.
  - *Base64Data* — Image data in base64.

**How to parse an image of business card to VCard?**

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Parse-Image-Of-Business-Card-To-VCard-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Parse-Image-Of-Business-Card-To-VCard-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Parse-Image-Of-Business-Card-To-VCard-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Parse-Image-Of-Business-Card-To-VCard-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Parse-Image-Of-Business-Card-To-VCard-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Parse-Image-Of-Business-Card-To-VCard-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
## **How to Get a List of VCard Files From One Folder**
You can get a list of VCard files stored in one folder on storage using a single API request. Files will be filtered by an extension (**.msg** for Msg format and **.vcf** for VCard) and read to list of ContactDto object. The method supports pagination.

To get a list of VCard files use [**GetContactModelListAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#GetContactModelListAsync) from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). This method requires **1 parameter** — [**GetContactModelListRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/GetContactModelListRequest.cs), which is a request for this operation.

[**GetContactModelListRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/GetContactModelListRequest.cs) has **4 parameters**:

- *Format —* Contact document format. Enum, available values: VCard, WebDav, Msg.
- *Folder* — Path to the folder in storage.
- *Storage* — Storage name.
- *ItemsPerPage* — Count of items on page.
- *PageNumber* — Page number.

**How to get a list of VCard files stored in one folder?**

{{< tabs tabTotal="6" tabID="5" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Get-List-Of-VCards-From-Storage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Get-List-Of-VCards-From-Storage-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Get-List-Of-VCards-From-Storage-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Get-List-Of-VCards-From-Storage-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Get-List-Of-VCards-From-Storage-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Get-List-Of-VCards-From-Storage-1.php" >}}

{{< /tab >}}

{{< /tabs >}}


## **More Tutorials**
See more Aspose Email tutorials: 


