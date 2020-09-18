---
title: "Get Email Document"
type: docs
url: /get-email-document/
weight: 30
---

## **Introduction**
Aspose.Email Cloud allows you to read properties from an Email Document uploaded to the Cloud. Aspose.Email Cloud provides the following API



{{% alert color="primary" %}} 

If you want to know more about working with emails — take a look at the Aspose Email Cloud tutorial: [**Email Message Files**](/emailcloud/email-message-files/).

{{% /alert %}} 
## **API Information**

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/email/{fileName}|GET|Read Email Document Properties|[GetEmail](https://apireference.aspose.cloud/email/#/Email/GetEmail)|
## **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X GET "https://api.aspose.cloud/v3.0/email/withAttachment.msg" -H "accept: application/json" -H "authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYmYiOjE1NzU5MjUwNDAsImV4cCI6MTU3NjAxMTQ0MCwiaXNzIjoiaHR0cHM6Ly9hcGkuYXNwb3NlLmNsb3VkIiwiYXVkIjpbImh0dHBzOi8vYXBpLmFzcG9zZS5jbG91ZC9yZXNvdXJjZXMiLCJhcGkucGxhdGZvcm0iLCJhcGkucHJvZHVjdHMiXSwiY2xpZW50X2lkIjoiNzg5NDZmYjQtM2JkNC00ZDNlLWIzMDktZjllMmZmOWFjNmY5IiwiY2xpZW50X2lkU3J2SWQiOiI2NTk5ODQiLCJzY29wZSI6WyJhcGkucGxhdGZvcm0iLCJhcGkucHJvZHVjdHMiXX0.JmM_z9oMwGwQj4F0NaQA7WItUz_UALIYRTbPMmutOdJfP1d4FPjpCnML4y8a_atM--jsXCp0aXO7QD5Vhe1QoKk_Xiwa1TrU08MpgGjapUdeTrXEVrMFuMp_dlN18futPUwB8muyYjFY0ljKQz7tTNQIO4VzHo6cqtFR1S88D7F49mztSTh3LdssKvYCTixzeEdzTj-vRCBRUYoS-dA3lxUnRB3Z7z7iDZRYIt2j7rJCEENG6z-4KduOTJnicLEz3HOUCcPyThTBYcVc2bJL8fdOQCYZhjUsqeMIoYcRxvced5JrJOEoIk6cbEenahUtmaJ89q-9mCKsn2qvuECUAA"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{ "links":null, "documentProperties":{ "link":{ "href":"/withAttachment.msg/documentproperties/", "rel":"self", "type":null, "title":null }, "list":[ { "link":{ "href":"/withAttachment.msg/documentproperties/Bcc", "rel":"self", "type":null, "title":null }, "name":"Bcc", "value":"" }, { "link":{ "href":"/withAttachment.msg/documentproperties/Body", "rel":"self", "type":null, "title":null }, "name":"Body", "value":"" }, { "link":{ "href":"/withAttachment.msg/documentproperties/CC", "rel":"self", "type":null, "title":null }, "name":"CC", "value":"" }, { "link":{ "href":"/withAttachment.msg/documentproperties/Date", "rel":"self", "type":null, "title":null }, "name":"Date", "value":"0001-01-01T00:00:00" }, { "link":{ "href":"/withAttachment.msg/documentproperties/DeliveryNotificationOptions", "rel":"self", "type":null, "title":null }, "name":"DeliveryNotificationOptions", "value":null }, { "link":{ "href":"/withAttachment.msg/documentproperties/From", "rel":"self", "type":null, "title":null }, "name":"From", "value":null }, { "link":{ "href":"/withAttachment.msg/documentproperties/To", "rel":"self", "type":null, "title":null }, "name":"To", "value":"" }, { "link":{ "href":"/withAttachment.msg/documentproperties/HtmlBody", "rel":"self", "type":null, "title":null }, "name":"HtmlBody", "value":"" }, { "link":{ "href":"/withAttachment.msg/documentproperties/IsBodyHtml", "rel":"self", "type":null, "title":null }, "name":"IsBodyHtml", "value":null }, { "link":{ "href":"/withAttachment.msg/documentproperties/MessageId", "rel":"self", "type":null, "title":null }, "name":"MessageId", "value":"9ddfa213c2504d16b5c2ec3dbac7d51a" }, { "link":{ "href":"/withAttachment.msg/documentproperties/Priority", "rel":"self", "type":null, "title":null }, "name":"Priority", "value":"Normal" }, { "link":{ "href":"/withAttachment.msg/documentproperties/Subject", "rel":"self", "type":null, "title":null }, "name":"Subject", "value":"" }, { "link":{ "href":"/withAttachment.msg/documentproperties/Attachments", "rel":"self", "type":null, "title":null }, "name":"Attachments", "value":[ { "name":"sample.vcf" } ] } ] } }

```

{{< /tab >}}

{{< /tabs >}}
## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/emailcloud/sdk-setup/).

{{% /alert %}} 




