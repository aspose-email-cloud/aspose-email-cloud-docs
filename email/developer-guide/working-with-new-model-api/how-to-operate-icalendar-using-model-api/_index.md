---
title: "How To Operate iCalendar Using Model API"
type: docs
url: /how-to-operate-icalendar-using-model-api/
description: "Aspose.Email Cloud API allows you to operate iCalendar files. Create ICS file, edit ICS file, convert ICS to AletrnateView, save iCalendar as ICS."
weight: 20
---

## **Introduction**
The **Internet Calendaring and Scheduling Core Object Specification** ([iCalendar](https://wiki.fileformat.com/email/ics/)) is a [MIME type](https://en.wikipedia.org/wiki/MIME_type "MIME type") which allows users to store and exchange calendaring and scheduling information such as events, to-dos, journal entries, and free/busy information.



{{% alert color="primary" %}} 

If you want to know more about working with **iCalendar files** — take a look at the Aspose Email Cloud tutorial: [**Quick Start With iCalendar API**](/emailcloud/quick-start-with-icalendar-api/).

{{% /alert %}} 


## **Model API**
When using Model API, the files are represented using models.

**iCalendar Model API supports:**

- Get iCalendar file from Storage as CalendarDto ([GetCalendarModel](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#GetCalendarModel))
- Save CalendarDto to file on Storage ([SaveCalendarModel](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#SaveCalendarModel))
- Get the list of iCalendar files from Storage folder ([GetCalendarModelList](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#GetCalendarModelList))
- Get iCalendar file from Storage as AlternateView ([GetCalendarModelAsAlternate](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#GetCalendarModelAsAlternate))
- Convert CalendarDto to AlternateView ([ConvertCalendarModelToAlternate](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#ConvertCalendarModelToAlternate))


## **Create iCalendar**
When using this model, we need to follow certain steps. As specified in examples below. Let’s start with creating [CalendarDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarDto.md) object:

**Create iCalendar — CalendarDto object:**
{{% alert color="primary" %}} 

[**CalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarDto.md) - The model contains properties that are describing iCalendar;

[**MailAddress**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/docs/MailAddress.md) - Contains mail address properties.

{{% /alert %}} 
{{< tabs tabTotal="6" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Email-Create-CalendarDto-Object-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{% alert color="primary" %}} 

[**CalendarDto](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/37ee732853b3f483c1af14402662fe790ad5aaf9/docs/CalendarDto.md) **-** The model contains properties that are describing iCalendar;

[**MailAddress](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/37ee732853b3f483c1af14402662fe790ad5aaf9/docs/MailAddress.md) **-** Contains mail address properties.

{{% /alert %}} 

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Email-Create-CalendarDto-Object-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{% alert color="primary" %}} 

[**CalendarDto](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/3a5c2c35a31629493aa484b65870622165570db8/doc/CalendarDto.md) **-** The model contains properties that are describing iCalendar;

[**MailAddress](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/3a5c2c35a31629493aa484b65870622165570db8/doc/MailAddress.md) **-** Contains mail address properties.

{{% /alert %}} 

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Email-Create-CalendarDto-Object-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{% alert color="primary" %}} 

[**CalendarDto](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/22a14eb5f9ca38fcf2e79193a2890d3018fbaf84/sdk/docs/CalendarDto.md) **-** The model contains properties that are describing iCalendar;

[**MailAddress](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/22a14eb5f9ca38fcf2e79193a2890d3018fbaf84/sdk/docs/MailAddress.md) **-** Contains mail address properties.

{{% /alert %}} 

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Email-Create-CalendarDto-Object-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{% alert color="primary" %}} 

[**CalendarDto](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/22a14eb5f9ca38fcf2e79193a2890d3018fbaf84/sdk/docs/CalendarDto.md) **-** The model contains properties that are describing iCalendar;

[**MailAddress](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/22a14eb5f9ca38fcf2e79193a2890d3018fbaf84/sdk/docs/MailAddress.md) **-** Contains mail address properties.

{{% /alert %}} 

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Email-Create-CalendarDto-Object-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{% alert color="primary" %}} 

[**CalendarDto](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/0d0ec4f4a9ca1beb87e3c194f1ac69630d5205fe/doc/CalendarDto.md) **-** The model contains properties that are describing iCalendar;

[**MailAddress](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/0d0ec4f4a9ca1beb87e3c194f1ac69630d5205fe/doc/MailAddress.md) **-** Contains mail address properties.

{{% /alert %}} 

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Ndoe-Email-Create-CalendarDto-Object-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}


## **Save iCalendar as ICS File**
Once **CalendarDto** has been created, the next step is to **save iCalendar file as a .ics file**. 

**Save CalendarDto object as .ICS file**

{{% alert color="primary" %}} 

[**SaveCalendarModel**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/docs/EmailApi.md#savecalendarmodel) - Save iCalendar.

**SaveCalendarModelRequest** - Request model for saveCalendarModel operation.

[**StorageModelRqOfCalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/docs/StorageModelRqOfCalendarDto.md) - Calendar properties update request.

{{% /alert %}} 

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}


{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Email-Save-CalendarDto-As-ICS-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{% alert color="primary" %}} 

[**saveCalendarModel](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/37ee732853b3f483c1af14402662fe790ad5aaf9/docs/EmailApi.md#savecalendarmodel) **-** Save iCalendar.

**SaveCalendarModelRequest** - Request model for saveCalendarModel operation.

[**StorageModelRqOfCalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/37ee732853b3f483c1af14402662fe790ad5aaf9/docs/StorageModelRqOfCalendarDto.md) - Calendar properties update request.

{{% /alert %}} 

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Email-Save-CalendarDto-As-ICS-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{% alert color="primary" %}} 

[**saveCalendarModel](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/3a5c2c35a31629493aa484b65870622165570db8/doc/EmailApi.md#savecalendarmodel) **-** Save iCalendar.

**SaveCalendarModelRequest** - Request model for saveCalendarModel operation.

[**StorageModelRqOfCalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/3a5c2c35a31629493aa484b65870622165570db8/doc/StorageModelRqOfCalendarDto.md) - Calendar properties update request.

{{% /alert %}} 

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Email-Save-CalendarDto-As-ICS-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{% alert color="primary" %}} 

[**save_calendar_model](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/22a14eb5f9ca38fcf2e79193a2890d3018fbaf84/sdk/docs/EmailApi.md#save_calendar_model) **-** Save iCalendar.

**SaveCalendarModelRequest** - Request model for saveCalendarModel operation.

[**StorageModelRqOfCalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/22a14eb5f9ca38fcf2e79193a2890d3018fbaf84/sdk/docs/StorageModelRqOfCalendarDto.md) - Calendar properties update request.

{{% /alert %}} 

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Email-Save-CalendarDto-As-ICS-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{% alert color="primary" %}} 

[**save_calendar_model](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/f3225bb43730f601716d5aa26c0f5e1734a64833/docs/EmailApi.md#save_calendar_model) **-** Save iCalendar.

**SaveCalendarModelRequest** - Request model for saveCalendarModel operation.

[**StorageModelRqOfCalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/f3225bb43730f601716d5aa26c0f5e1734a64833/docs/StorageModelRqOfCalendarDto.md) - Calendar properties update request.

{{% /alert %}} 

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Email-Save-CalendarDto-As-ICS-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{% alert color="primary" %}} 

[**saveCalendarModel](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/0d0ec4f4a9ca1beb87e3c194f1ac69630d5205fe/doc/EmailApi.md#savecalendarmodel) **-** Save iCalendar.

**SaveCalendarModelRequest** - Request model for saveCalendarModel operation.

[**StorageModelRqOfCalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/0d0ec4f4a9ca1beb87e3c194f1ac69630d5205fe/doc/StorageModelRqOfCalendarDto.md) - Calendar properties update request.

{{% /alert %}} 

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Email-Save-CalendarDto-As-ICS-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}


## **Convert iCalendar To AlternateView**
Or, you get an option to convert iCalendar to an [AlternateView](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/AlternateView.md): 

**Save CalendarDto model as AlternateView:**

{{% alert color="primary" %}} 

[**ConvertCalendarModelToAlternateAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/docs/EmailApi.md#convertcalendarmodeltoalternateasync) - Convert iCalendar to AlternateView. Returns [**AlternateView**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/docs/AlternateView.md).

**ConvertCalendarModelToAlternateRequest** - Request to convert iCalendar to AlternateView. 

[**CalendarDtoAlternateRq**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/docs/CalendarDtoAlternateRq.md) - iCalendar to AlternateView request. List of properties:

- **Value** ([CalendarDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/docs/CalendarDto.md)) - iCalendar document model;
- **Action (string)** - iCalendar actions. Enum, available values: Create, Update, Cancel;
- **SequenceId (string)** [Optional]- iCalendar sequence id.

{{% /alert %}} 

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Email-Convert-CalendarDto-as-AlternateView-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{% alert color="primary" %}} 

[**convertCalendarModelToAlternate](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/37ee732853b3f483c1af14402662fe790ad5aaf9/docs/EmailApi.md#convertcalendarmodeltoalternate) **-** Convert iCalendar to AlternateView. Returns [**AlternateView](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/37ee732853b3f483c1af14402662fe790ad5aaf9/docs/AlternateView.md)**.**

**ConvertCalendarModelToAlternateRequestData** - Request to convert iCalendar to AlternateView. 

[**CalendarDtoAlternateRq**](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/37ee732853b3f483c1af14402662fe790ad5aaf9/docs/CalendarDtoAlternateRq.md) - iCalendar to AlternateView request. List of properties:

- **value ([CalendarDto](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/37ee732853b3f483c1af14402662fe790ad5aaf9/docs/CalendarDto.md)) -** iCalendar document model;
- **action (string) -** iCalendar actions. Enum, available values: Create, Update, Cancel;
- **sequenceId (string)** [Optional] **-** iCalendar sequence id.

{{% /alert %}} 

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Email-Convert-CalendarDto-as-AlternateView-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{% alert color="primary" %}} 

[**convertCalendarModelToAlternate](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/3a5c2c35a31629493aa484b65870622165570db8/doc/EmailApi.md#convertcalendarmodeltoalternate) **-** Convert iCalendar to AlternateView. Returns [**AlternateView](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/3a5c2c35a31629493aa484b65870622165570db8/doc/AlternateView.md)**.**

**ConvertCalendarModelToAlternateRequest** - Request to convert iCalendar to AlternateView. 

[**CalendarDtoAlternateRq**](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/3a5c2c35a31629493aa484b65870622165570db8/doc/CalendarDtoAlternateRq.md) - iCalendar to AlternateView request. List of properties:

- **value ([CalendarDto](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/3a5c2c35a31629493aa484b65870622165570db8/doc/CalendarDto.md)) -** iCalendar document model;
- **action (string) -** iCalendar actions. Enum, available values: Create, Update, Cancel;
- **sequence\_id (string)** [Optional] **-** iCalendar sequence id.

{{% /alert %}} 

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Email-Convert-CalendarDto-as-AlternateView-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{% alert color="primary" %}} 

[**convert_calendar_model_to_alternate](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/22a14eb5f9ca38fcf2e79193a2890d3018fbaf84/sdk/docs/EmailApi.md#convert_calendar_model_to_alternate) **-** Convert iCalendar to AlternateView. Returns [**AlternateView](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/22a14eb5f9ca38fcf2e79193a2890d3018fbaf84/sdk/docs/AlternateView.md)**.**

**ConvertCalendarModelToAlternateRequest** - Request to convert iCalendar to AlternateView. 

[**CalendarDtoAlternateRq**](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/22a14eb5f9ca38fcf2e79193a2890d3018fbaf84/sdk/docs/CalendarDtoAlternateRq.md) - iCalendar to AlternateView request. List of properties:

- **value ([CalendarDto](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/22a14eb5f9ca38fcf2e79193a2890d3018fbaf84/sdk/docs/CalendarDto.md)) -** iCalendar document model;
- **action (str) -** iCalendar actions. Enum, available values: Create, Update, Cancel;
- **sequence\_id (str)** [Optional] **-** iCalendar sequence id.

{{% /alert %}} 

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Email-Convert-CalendarDto-as-AlternateView-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{% alert color="primary" %}} 

[**convert_calendar_model_to_alternate](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/f3225bb43730f601716d5aa26c0f5e1734a64833/docs/EmailApi.md#convert_calendar_model_to_alternate) **-** Convert iCalendar to AlternateView. Returns [**AlternateView](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/f3225bb43730f601716d5aa26c0f5e1734a64833/docs/AlternateView.md)**.**

**ConvertCalendarModelToAlternateRequestData** - Request to convert iCalendar to AlternateView. 

[**CalendarDtoAlternateRq**](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/f3225bb43730f601716d5aa26c0f5e1734a64833/docs/CalendarDtoAlternateRq.md) - iCalendar to AlternateView request. List of properties:

- **value ([CalendarDto](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/f3225bb43730f601716d5aa26c0f5e1734a64833/docs/CalendarDto.md)) -** iCalendar document model;
- **action (string) -** iCalendar actions. Enum, available values: Create, Update, Cancel;
- **sequence\_id (string)** [Optional] **-** iCalendar sequence id.

{{% /alert %}} 

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Email-Convert-CalendarDto-as-AlternateView-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{% alert color="primary" %}} 

[**convertCalendarModelToAlternate](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/0d0ec4f4a9ca1beb87e3c194f1ac69630d5205fe/doc/EmailApi.md#convertcalendarmodeltoalternate) **-** Convert iCalendar to AlternateView. Returns **AlternateView.**

**ConvertCalendarModelToAlternateRequest** - Request to convert iCalendar to AlternateView. 

[**CalendarDtoAlternateRq**](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/0d0ec4f4a9ca1beb87e3c194f1ac69630d5205fe/doc/CalendarDtoAlternateRq.md) - iCalendar to AlternateView request. List of properties:

- **value ([CalendarDto](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/0d0ec4f4a9ca1beb87e3c194f1ac69630d5205fe/doc/CalendarDto.md)) -** iCalendar document model;
- **action (string) -** iCalendar actions. Enum, available values: Create, Update, Cancel;
- **sequenceId (string)** [Optional] **-** iCalendar sequence id.

{{% /alert %}} 

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Email-Convert-CalendarDto-as-AlternateView-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}
\
Finally, the **AlternateView** can be added to [EmailDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailDto.md) object, which is also a part of the Model API.

## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/emailcloud/sdk-setup/).

{{% /alert %}} 


## **Articles in This Section**
Please take a look at the following examples to see how it works:

