---
title: "Working with New Model API"
type: docs
url: /working-with-new-model-api/
description: "Operate with Eml/VCard/iCalendar by property sets or Model API (part of Aspose.Email Cloud API, which is easy to use)."
weight: 40
---

## **Introduction**
{{% alert color="primary" %}} **iCalendar** is a MIME type that allows users to exchange and store calendaring and scheduling information such as general entries, events, free/busy information, and ToDo, etc. {{% /alert %}} 

There are 2 ways to operate with Eml/VCard/iCalendar files available in Aspose.Email Cloud. The first one is Property Sets and the other one is the Model API. 
### **Property sets**
First is operating files as property sets. For example, to create iCalendar file using the property set ([CreateCalendarAsync](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#CreateCalendarAsync)):
### **Model API**
And the second way is **Model API**, where files are represented using models.
#### **Operate iCalendar using Model API**
iCalendar Model API supports:

- Get iCalendar file from Storage as CalendarDto ([GetCalendarModel](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#GetCalendarModel))
- Save CalendarDto to file on Storage ([SaveCalendarModel](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#SaveCalendarModel))
- Get the list of iCalendar files from Storage folder ([GetCalendarModelList](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#GetCalendarModelList))
- Get iCalendar file from Storage as AlternateView ([GetCalendarModelAsAlternate](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#GetCalendarModelAsAlternate))
- Convert CalendarDto to AlternateView ([ConvertCalendarModelToAlternate](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#ConvertCalendarModelToAlternate))
## **API Information**
Aspose.Email Cloud provides the following API:

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/email/Calendar/{name}|PUT|Create calendar file|[CreateCalendar](https://apireference.aspose.cloud/email/#/Calendar/CreateCalendar)|
## **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "https://api.aspose.cloud/v3.0/email/Calendar/sample.ics/properties" -H "accept: application/json" -H "authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYmYiOjE1NzU4MzA4NzksImV4cCI6MTU3NTkxNzI3OSwiaXNzIjoiaHR0cHM6Ly9hcGkuYXNwb3NlLmNsb3VkIiwiYXVkIjpbImh0dHBzOi8vYXBpLmFzcG9zZS5jbG91ZC9yZXNvdXJjZXMiLCJhcGkucGxhdGZvcm0iLCJhcGkucHJvZHVjdHMiXSwiY2xpZW50X2lkIjoiNzg5NDZmYjQtM2JkNC00ZDNlLWIzMDktZjllMmZmOWFjNmY5IiwiY2xpZW50X2lkU3J2SWQiOiI2NTk5ODQiLCJzY29wZSI6WyJhcGkucGxhdGZvcm0iLCJhcGkucHJvZHVjdHMiXX0.mp1drdo4pYso9TEv8VL0pNk5D\_oxNMFI1JevJCD3koIgC2kN8lFGVypkXwQVlEYLtOULaT5JlSEwB2dtomqTW1eGpy6SIHP\_o5g5npoj2tlyBMCEf3od-cU6oObwLkdiELGbjkJ9SHh--wZTjk81VeSudXyAoX48bPsFGlBwq0N240i7mShtxIno87U58DEFONJLteQME86rAg6PqwBmHkfVoLbDkkLWHo5s2VxOD6UPkBGRaqjdpQlkHL17mq5hz0iWHW2HLUnMo6-ET0g0e0RYaYZnu4VPRyoUj2j5a0WTVryKybMc-WgjmzDzfJ2Y1mQoZE9KvD177v2GKn5CBg" -H "Content-Type: application/json" -d "{ \"hierarchicalObject\": { \"name\": \"CALENDAR\", \"type\": \"HierarchicalObject\", \"internalProperties\": [ { \"value\":\"Updated Access-A-Ride to 900 Jay St., Brooklyn\", \"name\":\"DESCRIPTION\", \"type\":\"PrimitiveObject\" } ] }}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

Returns 200 if update is successful


```

{{< /tab >}}

{{< /tabs >}}
## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/emailcloud/sdk-setup/). 

{{% /alert %}} 
## **Articles in this section**
