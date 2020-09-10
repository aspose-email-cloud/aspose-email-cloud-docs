---
title: "Quick Start With iCalendar API"
type: docs
url: /quick-start-with-icalendar-api/
description: "Aspose Email tutorial shows how to work with iCalendar files using Aspose.Email Cloud. Create calendars, edit calendars, process appointments, etc."
weight: 40
---

## **iCalendar API**
[Aspose.Email Cloud API](https://products.aspose.cloud/email/family) supports working with iCalendar files. You can use our API to read, edit and save iCalendar (.ics) files. Also, you can convert them to [**AlternateView**](/icalendar-to-alternateview-converter/) and add them to email messages.

Our SDKs support two different ways of operating with iCalendar files using [property sets](/create-icalendar-file-using-the-property-set/) and data transfer object **CalendarDto**. This tutorial shows how to use **CalendarDto**.

{{% alert color="primary" %}} To see how to setup SDKs use the [SDK setup](/sdk-setup/) tutorial. {{% /alert %}} 


## **Create Calendar File Object and Save It to Storage**
[**CalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/CalendarDto.cs)
 object contains all information about an appointment including attendees, start date, end date, description and etc.

First, let’s create a **CalendarDto** object and save it to Storage.

To save a **CalendarDto** to Storage use [**SaveCalendarModelAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#SaveCalendarModelAsync) 
from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). 
This method requires **1 parameter** — 
[**SaveCalendarModelRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/SaveCalendarModelRequest.cs), which is a request model for this operation. 

[**SaveCalendarModelRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/SaveCalendarModelRequest.cs) requires **2 parameters**: 
*Name —* iCalendar file name in storage and [***StorageModelRqOfCalendarDto***](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/StorageModelRqOfCalendarDto.cs) object — calendar properties update request. 

[**StorageModelRqOfCalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/StorageModelRqOfCalendarDto.cs) has 2 parameters:

- *Value* — [**CalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/CalendarDto.cs) object.
- *StorageFolder* — [**StorageFolderLocation**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/StorageFolderLocation.cs) object.

**How to create a CalendarDto object and save it to the Storage?**

{{< tabs tabTotal="6" tabID="1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Create-iCalendar-Save-To-Storage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Create-iCalendar-Save-To-Storage-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Create-iCalendar-Save-To-Storage-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Create-iCalendar-Save-To-Storage-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Create-iCalendar-Save-To-Storage-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Create-iCalendar-Save-To-Storage-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
## **Download iCalendar File From Storage**
You can find the saved file on [Aspose.Cloud Dashboard](https://dashboard.aspose.cloud/#/files), or download it using SDK.

To download a file from the storage use [**DownloadFileAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#SaveCalendarModelAsync) from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). This method requires 1 parameter — [**DownloadFileRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/DownloadFileRequest.cs), which is a request for this operation.

[**DownloadFileRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/DownloadFileRequest.cs) has **3 parameters**:

- *Path* — File path e.g. "/folder/file.ext".
- *StorageName* — Storage name.
- *VersionId* [**optional**] — File version ID to download.

**How to download iCalendar file from the Storage?**

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Download-CalendarDto-From-Storage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Download-CalendarDto-From-Storage-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Download-CalendarDto-From-Storage-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Download-CalendarDto-From-Storage-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Download-CalendarDto-From-Storage-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Download-CalendarDto-From-Storage-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
## **Get Calendar File From Storage as CalendarDto Object**
Let's get this file from storage as a **CalendarDto** object.

To get a calendar file from Storage use [**GetCalendarModelAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#GetCalendarModelAsync) 
from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). 
This method requires **1 parameter** — 
[**GetCalendarModelRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/GetCalendarModelRequest.cs), which is a request for this operation.

[**GetCalendarModelRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/GetCalendarModelRequest.cs) has **3 parameters**:

- *Name* — iCalendar file name in storage.
- *Folder* — Path to the folder in storage.
- *Storage* — Storage name.

**How to get a file from the Storage as a CalendarDto object?**

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Download-Calendar-File-From-Storage-As-CalendarDto-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Download-Calendar-File-From-Storage-As-CalendarDto-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Download-Calendar-File-From-Storage-As-CalendarDto-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Download-Calendar-File-From-Storage-As-CalendarDto-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Download-Calendar-File-From-Storage-As-CalendarDto-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Download-Calendar-File-From-Storage-As-CalendarDto-1.php" >}}

{{< /tab >}}

{{< /tabs >}}

\
You can change model fields and save it again. The file will be rewritten if you don't change file name and location.
## **Convert Calendar Object to AlternateView**
We also provide API methods for converting **CalendarDto** to an **AlternateView**. **AlternateView** can be added to **EmailDto**, which can be saved as **EML** file or sent using a built-in email client.

{{% alert color="primary" %}} 

To get more information about built-in email client — take a look at the [Email Client tutorial](https://docs.aspose.cloud/display/LGIS/Quick+start+with+the+email+client).

{{% /alert %}} 



To convert a **CalendarDto** object to **AlternateView** use [**ConvertCalendarModelToAlternateAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#ConvertCalendarModelToAlternateAsync) from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). This method requires **1 parameter** — [**ConvertCalendarModelToAlternateRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/ConvertCalendarModelToAlternateRequest.cs), which is a request for this operation. This request has 1 parameter — [**CalendarDtoAlternateRq**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/CalendarDtoAlternateRq.cs) (iCalendar document as AlternateView request).

[**CalendarDtoAlternateRq**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/CalendarDtoAlternateRq.cs) has **3 parameters**:

- *Value* — iCalendar document model.
- *Action* — iCalendar actions. Enum, available values: Create, Update, Cancel.
- *SequenceId* — iCalendar sequence id.

**How to convert CalendarDto to an AlternateView?**

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Convert-CalendarDto-To-AlternateView-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Convert-CalendarDto-To-AlternateView-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Convert-CalendarDto-To-AlternateView-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Convert-CalendarDto-To-AlternateView-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Convert-CalendarDto-To-AlternateView-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Convert-CalendarDto-To-AlternateView-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
## **Get a List of iCalendar Files From One Folder**
You can get a list of iCalendar files stored in one folder on storage using a single API request. Files will be filtered by ".ics" extension and read to list of CalendarDto object. The method supports pagination.

To get a list of iCalendar files use [**GetCalendarModelListAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#GetCalendarModelListAsync) from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). This method requires **1 parameter** — [**GetCalendarModelListRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/GetCalendarModelListRequest.cs), which is a request for this operation.

[**GetCalendarModelListRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/GetCalendarModelListRequest.cs) has **4 parameters**:

- *Folder* — Path to the folder in storage.
- *ItemsPerPage* — Count of items on page.
- *PageNumber* — Page number.
- *Storage* — Storage name.

**How to get a list of iCalendar files stored in one folder?**

{{< tabs tabTotal="6" tabID="5" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Get-List-Of-CalendarDto-From-Storage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Get-List-Of-CalendarDto-From-Storage-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Get-List-Of-CalendarDto-From-Storage-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Get-List-Of-CalendarDto-From-Storage-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Get-List-Of-CalendarDto-From-Storage-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Get-List-Of-CalendarDto-From-Storage-1.php" >}}

{{< /tab >}}

{{< /tabs >}}


## **More Tutorials**
See more Aspose Email tutorials: 
