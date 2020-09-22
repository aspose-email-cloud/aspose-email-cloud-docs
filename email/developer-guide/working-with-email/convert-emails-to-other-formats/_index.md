---
title: "Convert Emails to Other Formats"
type: docs
url: /convert-emails-to-other-formats/
weight: 10
---

## **Introduction**
Aspose.Email Cloud supports different Email message file formats:

- EML
- MSG
- MHTML
- HTML



{{% alert color="primary" %}} 

If you want to know more about working with emails — take a look at the Aspose Email Cloud tutorial: [**Email Message Files**](/email/email-message-files/).

{{% /alert %}} 
## **Resource URI**
 [Swagger UI](https://apireference.aspose.cloud/email/#/Email/ConvertEmail) lets you call this REST API directly from the browser. The description of the API and its parameters are also given there.
## **cURL Example**


{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X GET "https://api.aspose.cloud/v3.0/email/test.eml/as-file/MSG" -H "accept: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

File stream in specified format

```

{{< /tab >}}

{{< /tabs >}}


## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/email/sdk-setup/).

{{% /alert %}} 
## **SDK Examples**
 Aspose.Email Cloud now also provides you the capabilities to interconvert supported file formats. The following example shows how to convert an email message (EML to MSG) file from disk to the desired format by using [GetEmailAsFileAsync](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#GetEmailAsFileAsync) method:

**EML to MSG conversion**

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-EML-to-MSG-Conversion-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-EML-to-MSG-Conversion-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-EML-to-MSG-Conversion-1.py" >}}

{{< /tab >}}

{{< /tabs >}}
\
Email message files can be downloaded from the Storage in any of the supported formats while using [GetEmailAsFile](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#GetEmailAsFile). 

**Download Email Message from Storage**

{{< tabs tabTotal="3" tabID="5" tabName1="C#" tabName2="Java" tabName3="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Download-Email-From-Storage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Download-Email-From-Storage-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Download-Email-From-Storage-1.py" >}}

{{< /tab >}}

{{< /tabs >}}
