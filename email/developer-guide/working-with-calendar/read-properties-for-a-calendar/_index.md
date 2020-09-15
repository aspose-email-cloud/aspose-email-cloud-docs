---
title: "Read Properties For a Calendar"
type: docs
url: /read-properties-for-a-calendar/
weight: 50
---

## **Introduction**
Aspose.Email Cloud allows you to read properties from a Calendar Document uploaded to the cloud.



{{% alert color="primary" %}} 

If you want to know more about working with **iCalendar files** — take a look at the Aspose Email Cloud tutorial: [**Quick Start With iCalendar API**](/emailcloud/quick-start-with-icalendar-api/).

{{% /alert %}} 


## **API Information**
Aspose.Email Cloud provides the following API:

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/email/Calendar/{name}/properties|GET|Read Calendar Properties|[GetCalendar](https://apireference.aspose.cloud/email/#/Calendar/GetCalendar)|

## **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X GET "https://api.aspose.cloud/v3.0/email/Calendar/sample.ics/properties" -H "accept: application/json" -H "authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYmYiOjE1NzU4MzA4NzksImV4cCI6MTU3NTkxNzI3OSwiaXNzIjoiaHR0cHM6Ly9hcGkuYXNwb3NlLmNsb3VkIiwiYXVkIjpbImh0dHBzOi8vYXBpLmFzcG9zZS5jbG91ZC9yZXNvdXJjZXMiLCJhcGkucGxhdGZvcm0iLCJhcGkucHJvZHVjdHMiXSwiY2xpZW50X2lkIjoiNzg5NDZmYjQtM2JkNC00ZDNlLWIzMDktZjllMmZmOWFjNmY5IiwiY2xpZW50X2lkU3J2SWQiOiI2NTk5ODQiLCJzY29wZSI6WyJhcGkucGxhdGZvcm0iLCJhcGkucHJvZHVjdHMiXX0.mp1drdo4pYso9TEv8VL0pNk5D\_oxNMFI1JevJCD3koIgC2kN8lFGVypkXwQVlEYLtOULaT5JlSEwB2dtomqTW1eGpy6SIHP\_o5g5npoj2tlyBMCEf3od-cU6oObwLkdiELGbjkJ9SHh--wZTjk81VeSudXyAoX48bPsFGlBwq0N240i7mShtxIno87U58DEFONJLteQME86rAg6PqwBmHkfVoLbDkkLWHo5s2VxOD6UPkBGRaqjdpQlkHL17mq5hz0iWHW2HLUnMo6-ET0g0e0RYaYZnu4VPRyoUj2j5a0WTVryKybMc-WgjmzDzfJ2Y1mQoZE9KvD177v2GKn5CBg"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{ "internalProperties": [ { "value": " Access-A-Ride to 900 Jay St., Brooklyn", "name": "DESCRIPTION", "type": "PrimitiveObject" }, { "value": "2013-08-02 15:04:00Z", "name": "ENDDATE", "type": "PrimitiveObject" }, { "value": "America/New\_York", "name": "ENDTIMEZONE", "type": "PrimitiveObject" }, { "value": "False", "name": "ISDESCRIPTIONHTML", "type": "PrimitiveObject" }, { "value": "1000 Broadway Ave., Brooklyn", "name": "LOCATION", "type": "PrimitiveObject" }, { "value": null, "name": "RECURRENCE", "type": "PrimitiveObject" }, { "internalProperties": [ { "index": 0, "internalProperties": [ { "value": "Display", "name": "REMINDERACTION", "type": "PrimitiveObject" }, { "value": "Pickup Reminder", "name": "REMINDERDESCRIPTION", "type": "PrimitiveObject" }, { "value": "0", "name": "REMINDERREPEAT", "type": "PrimitiveObject" }, { "internalProperties": [ { "value": "6000000000", "name": "REMINDERTRIGGERDURATION", "type": "PrimitiveObject" }, { "value": "Start", "name": "REMINDERTRIGGERRELATED", "type": "PrimitiveObject" } ], "name": "REMINDERTRIGGER", "type": "HierarchicalObject" } ], "name": "REMINDER", "type": "IndexedHierarchicalObject" } ], "name": "REMINDERS", "type": "HierarchicalObject" }, { "value": "3", "name": "SEQUENCEID", "type": "PrimitiveObject" }, { "value": "2013-08-02 14:34:00Z", "name": "STARTDATE", "type": "PrimitiveObject" }, { "value": "America/New\_York", "name": "STARTTIMEZONE", "type": "PrimitiveObject" }, { "value": "Confirmed", "name": "STATUS", "type": "PrimitiveObject" }, { "value": "Access-A-Ride Pickup", "name": "SUMMARY", "type": "PrimitiveObject" } ], "name": "CALENDAR", "type": "HierarchicalObject" } Response headers

```

{{< /tab >}}

{{< /tabs >}}


## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/emailcloud/sdk-setup/). 

{{% /alert %}} 




