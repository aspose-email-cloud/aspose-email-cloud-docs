---
title: "Update a Calendar Property"
type: docs
url: /update-a-calendar-property/
weight: 60
---

## **Introduction**
Aspose.Email Cloud allows you to update properties from a Calendar Document uploaded to the cloud.



{{% alert color="primary" %}} 

If you want to know more about working with **iCalendar files** — take a look at the Aspose Email Cloud tutorial: [**Quick Start With iCalendar API**](/emailcloud/quick-start-with-icalendar-api/).

{{% /alert %}} 


## **API Information**
Aspose.Email Cloud provides the following API:

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/email/Calendar/{name}/properties|PUT|Update a Calendar Properties|[UpdateCalendarProperties](https://apireference.aspose.cloud/email/#/Calendar/UpdateCalendarProperties)|

## **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "https://api.aspose.cloud/v3.0/email/Calendar/sample.ics/properties" -H "accept: application/json" -H "authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYmYiOjE1NzU4MzA4NzksImV4cCI6MTU3NTkxNzI3OSwiaXNzIjoiaHR0cHM6Ly9hcGkuYXNwb3NlLmNsb3VkIiwiYXVkIjpbImh0dHBzOi8vYXBpLmFzcG9zZS5jbG91ZC9yZXNvdXJjZXMiLCJhcGkucGxhdGZvcm0iLCJhcGkucHJvZHVjdHMiXSwiY2xpZW50X2lkIjoiNzg5NDZmYjQtM2JkNC00ZDNlLWIzMDktZjllMmZmOWFjNmY5IiwiY2xpZW50X2lkU3J2SWQiOiI2NTk5ODQiLCJzY29wZSI6WyJhcGkucGxhdGZvcm0iLCJhcGkucHJvZHVjdHMiXX0.mp1drdo4pYso9TEv8VL0pNk5D_oxNMFI1JevJCD3koIgC2kN8lFGVypkXwQVlEYLtOULaT5JlSEwB2dtomqTW1eGpy6SIHP_o5g5npoj2tlyBMCEf3od-cU6oObwLkdiELGbjkJ9SHh--wZTjk81VeSudXyAoX48bPsFGlBwq0N240i7mShtxIno87U58DEFONJLteQME86rAg6PqwBmHkfVoLbDkkLWHo5s2VxOD6UPkBGRaqjdpQlkHL17mq5hz0iWHW2HLUnMo6-ET0g0e0RYaYZnu4VPRyoUj2j5a0WTVryKybMc-WgjmzDzfJ2Y1mQoZE9KvD177v2GKn5CBg" -H "Content-Type: application/json" -d "{ \"hierarchicalObject\": { \"name\": \"CALENDAR\", \"type\": \"HierarchicalObject\", \"internalProperties\": [ { \"value\":\"Updated Access-A-Ride to 900 Jay St., Brooklyn\", \"name\":\"DESCRIPTION\", \"type\":\"PrimitiveObject\" } ] }}"

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




