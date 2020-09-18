---
title: "CalendarDto Model To Represent iCalendar Files"
type: docs
url: /calendardto-model-to-represent-icalendar-files/
weight: 10
---

## **Introduction**
The **Internet Calendaring and Scheduling Core Object Specification** (**iCalendar**) is a [MIME type](https://en.wikipedia.org/wiki/MIME_type "MIME type") that allows users to store and exchange calendaring and scheduling information such as events, to-dos, journal entries, and free/busy information. The iCalendar files formatted according to the specification usually have an extension of [.ics](https://wiki.fileformat.com/email/ics/). In the previous version, it was only property sets based API. 



{{% alert color="primary" %}} 

If you want to know more about working with **iCalendar files** — take a look at the Aspose Email Cloud tutorial: [**Quick Start With iCalendar API**](/emailcloud/quick-start-with-icalendar-api/).

{{% /alert %}} 

So in order to create iCalendar file using .Net SDK, you had to use the following code:

**Create iCalendar using property sets API**

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Email-Create-iCalendar-Property-sets-1.cs" >}}
## **cURL Example**
{{< tabs tabTotal="2" tabID="2" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/email/AiBcr/parse-storage" -H "accept: application/json" -H "authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYmYiOjE1ODI2NjMzMTMsImV4cCI6MTU4Mjc0OTcxMywiaXNzIjoiaHR0cHM6Ly9hcGkuYXNwb3NlLmNsb3VkIiwiYXVkIjpbImh0dHBzOi8vYXBpLmFzcG9zZS5jbG91ZC9yZXNvdXJjZXMiLCJhcGkucGxhdGZvcm0iLCJhcGkucHJvZHVjdHMiXSwiY2xpZW50X2lkIjoiRTMxREYyOTctOTY1NS00RjYxLUIxQzgtRUM1MkUxMEIxODg4IiwiY2xpZW50X2lkU3J2SWQiOiI1MzgzMiIsInNjb3BlIjpbImFwaS5wbGF0Zm9ybSIsImFwaS5wcm9kdWN0cyJdfQ.Y76YJx64rafsN5qljoL5MZtOHW-5TXr0mQlm0MjhKtzan8yYMgK4beADQBW0Jge8LPJwqa0kjmVSW9uDhX7k6xrH_S0BssR1HXtSOpCkDunP_84k_ehXUe07_k9RIRwasZaxO2rgGjcf7APbMzDxSf_LaWyLJ3QH-rkyiupwI1mg_9Dp80fSr67-pIIjPoRWqZ7zX-cmLUWNMmtLYW2Y3GlONTHw66dfhvBUZr55j2y8w6nLwjLVzCggTpJ_0Csaqamld8mF2GvF70RisXXLak-3g1qP7iUBeFUHtdgXW2Nr6qjs88BSPmkwOgehF7KpuY5hpoR1A7xMCLAoqgTbIw" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{ \"options\": { \"languages\": \"string\", \"countries\": \"string\" }, \"images\": [ { \"isSingle\": true, \"file\": { \"storage\": \"string\", \"folderPath\": \"string\", \"fileName\": \"string\" } } ], \"outFolder\": { \"storage\": \"string\", \"folderPath\": \"string\" }}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

{ "value": [ { "storage": "string", "folderPath": "string", "fileName": "string" } ] }

{{< /tab >}}

{{< /tabs >}}
## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/emailcloud/sdk-setup/).

{{% /alert %}}
