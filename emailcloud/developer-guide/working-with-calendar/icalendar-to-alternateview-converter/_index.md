---
title: "iCalendar To AlternateView Converter"
type: docs
url: /icalendar-to-alternateview-converter/
keywords: "iCalendar, AlternateView converter"
description: "iCalendar to AlternateView converter description"
weight: 30
---

## **Introduction**
Starting with the release of [Aspose.Email Cloud 20.1](/emailcloud/aspose-email-cloud-20-1-release-notes/), we have introduced the capability to convert iCalendar to AlternateView.

{{% alert color="primary" %}}  [AlternateView](https://docs.microsoft.com/en-us/dotnet/api/system.net.mail.alternateview?view=netframework-4.8) specifies copies of an email message in different formats. For example, if you send a message in HTML, you might also want to provide a plain text version in case some of the recipients use email readers that cannot display HTML content. {{% /alert %}} 

Once the email message has been converted to AlternateView, it can easily be attached to an email message.

**iCalendar to AlternateView Converter**

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-iCalendar-to-AlternateView-Converter-1.cs" >}}



{{% alert color="primary" %}} 

If you want to know more about working with **iCalendar files** — take a look at the Aspose Email Cloud tutorial: [**Quick Start With iCalendar API**](/emailcloud/quick-start-with-icalendar-api/).

{{% /alert %}} 


## **API Information**
**Aspose.Email Cloud** provides the following API:

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/email/CalendarModel/as-alternate|PUT|Convert iCalendar to AlternateView|[ConvertCalendarModelToAlternate](https://apireference.aspose.cloud/email/#/CalendarModel/ConvertCalendarModelToAlternate)|
## **cURL Example**
{{< tabs tabTotal="2" tabID="2" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```html

curl -X PUT "https://api.aspose.cloud/v3.0/email/CalendarModel/as-alternate" -H "accept: application/json" -H "authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYmYiOjE1ODI4MjUwNDIsImV4cCI6MTU4MjkxMTQ0MiwiaXNzIjoiaHR0cHM6Ly9hcGkuYXNwb3NlLmNsb3VkIiwiYXVkIjpbImh0dHBzOi8vYXBpLmFzcG9zZS5jbG91ZC9yZXNvdXJjZXMiLCJhcGkucGxhdGZvcm0iLCJhcGkucHJvZHVjdHMiXSwiY2xpZW50X2lkIjoiRTMxREYyOTctOTY1NS00RjYxLUIxQzgtRUM1MkUxMEIxODg4IiwiY2xpZW50X2lkU3J2SWQiOiI1MzgzMiIsInNjb3BlIjpbImFwaS5wbGF0Zm9ybSIsImFwaS5wcm9kdWN0cyJdfQ.ItwtPLglUiQAT2uRbGaPVxAlI-4UluyxlgGTyt\_jmv1wZev4fOeylqirvmo-BbqLXC2v4sqpZ4qlwW4UER8FwZKWOp2EhQXOpqC8K\_MdR4TA3KRxL\_D6GvGM4XKMoPU0hU1RfPQQ\_d9M1wRGaIF533ubD1tdqjDalcPoCALgnFizxh4Ev1wNPI9xWICx7rnKlMrRTw-qQ1GAStkK4V9OprZcTVy-iP2Yy9pn2g8ZpDVQ2TAPIoSOv9nhL5oMvJBd9GpldJCNm4OZJRT5XmHPQsh6rpkRYGojAWBboOL1vTTuSqMg\_g3Xue1rlX2ukClNElTrvbPV7xUC-JHbvb3JwA" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{ \"value\": { \"attachments\": [ { \"base64Data\": \"string\", \"contentId\": \"string\", \"contentType\": { \"boundary\": \"string\", \"charSet\": \"string\", \"mediaType\": \"string\", \"name\": \"string\", \"parameters\": [ { \"name\": \"string\", \"value\": \"string\" } ] }, \"headers\": { \"additionalProp1\": \"string\", \"additionalProp2\": \"string\", \"additionalProp3\": \"string\" }, \"contentDisposition\": \"string\", \"isEmbeddedMessage\": true, \"name\": \"string\", \"nameEncoding\": \"string\", \"preferredTextEncoding\": \"string\" } ], \"attendees\": [ { \"displayName\": \"string\", \"address\": \"string\", \"participationStatus\": \"string\" } ], \"description\": \"string\", \"endDate\": \"2020-02-27T19:24:42.400Z\", \"endTimeZone\": \"string\", \"flags\": [ \"string\" ], \"isDescriptionHtml\": true, \"location\": \"string\", \"method\": \"string\", \"microsoftBusyStatus\": \"string\", \"microsoftIntendedStatus\": \"string\", \"optionalAttendees\": [ { \"displayName\": \"string\", \"address\": \"string\", \"participationStatus\": \"string\" } ], \"organizer\": { \"displayName\": \"string\", \"address\": \"string\", \"participationStatus\": \"string\" }, \"recurrenceString\": \"string\", \"reminders\": [ { \"action\": \"string\", \"attachments\": [ \"string\" ], \"attendees\": [ { \"address\": \"string\" } ], \"description\": \"string\", \"duration\": 0, \"repeat\": 0, \"summary\": \"string\", \"trigger\": { \"dateTime\": \"2020-02-27T19:24:42.400Z\", \"duration\": 0, \"related\": \"string\" } } ], \"sequenceId\": \"string\", \"startDate\": \"2020-02-27T19:24:42.400Z\", \"startTimeZone\": \"string\", \"status\": \"string\", \"summary\": \"string\", \"transparency\": \"string\" }, \"action\": \"string\", \"sequenceId\": \"string\"}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```html

{ "base64Data": "string", "contentId": "string", "contentType": { "boundary": "string", "charSet": "string", "mediaType": "string", "name": "string", "parameters": [ { "name": "string", "value": "string" } ] }, "headers": { "additionalProp1": "string", "additionalProp2": "string", "additionalProp3": "string" }, "baseUri": "string", "linkedResources": [ { "base64Data": "string", "contentId": "string", "contentType": { "boundary": "string", "charSet": "string", "mediaType": "string", "name": "string", "parameters": [ { "name": "string", "value": "string" } ] }, "headers": { "additionalProp1": "string", "additionalProp2": "string", "additionalProp3": "string" }, "contentLink": "string" } ] }

```

{{< /tab >}}

{{< /tabs >}}
## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/emailcloud/sdk-setup/).

{{% /alert %}}
