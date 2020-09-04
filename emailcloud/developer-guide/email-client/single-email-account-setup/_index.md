---
title: "Single Email Account Setup"
type: docs
url: /single-email-account-setup/
description: "How to setup a single email account in Aspose.Email Cloud."
weight: 10
---

## **Introduction**
You should setup email accounts before using email client API.

Email account information should be stored on Storage as **\*.account** or **\*.multi.accoun**t file.

A single email account is storing on Storage in **\*.account** file. File with **.account** extension is used to store one email account.

**\*.account** is the internal file format developed by Aspose Company. This file format uses only for storing account’s settings on the Aspose Cloud Storage. It contains information about email server configuration (host, port, protocol, security options) and authentication data (login/password or OAuth credentials). 

You don't need to create **\*.account** file directly, you can do it via Aspose.Email Cloud API. To create **\*.account** file - follow instructions that are provided below. 



{{% alert color="primary" %}} 

If you want to know more about working with **Email Client** — take a look at the Aspose Email Cloud tutorial: [**Quick Start With Email Client**](/quick-start-with-email-client-html/).

{{% /alert %}} 
## **Save email account using Swagger-UI**
You can test this functional by using [API reference service](https://apireference.aspose.cloud/email/). To save email account to the [Aspose Storage](https://apireference.aspose.cloud/storage/), you should follow these steps:

1. Open link of  <https://apireference.aspose.cloud/email/>
1. Click the *"Authorize"* button, enter your AppKey and AppSid, obtained from the [dashboard](https://dashboard.aspose.cloud/), click *"Authorize"* dialog button
1. Open link <https://apireference.aspose.cloud/email/#/EmailClient/SaveEmailClientAccount> and click *"Try it out"* button
1. Enter JSON with email account information and click *"Execute"* button

{{% alert color="primary" %}} 

![todo:image\_alt\_text](/images/icons/grey\_arrow\_down.png)

You can use this JSON to save an email client account

```javascript

{

   "Value":{

      "Host":"smtp.gmail.com",

      "Port":465,

      "SecurityOptions":"SSLAuto",

      "ProtocolType":"SMTP",

      "Credentials":{

         "Password":"password",

         "Login":"example@gmail.com",

         "Discriminator":"EmailClientAccountPasswordCredentials"

      }

   },

   "StorageFile":{

      "FileName":"fileName.account",

      "Storage":"First Storage",

      "FolderPath":"account/folder/location/on/storage"

   }

}

```

{{% /alert %}} 
## **Get email account from storage using Swagger-UI**
You can get a saved .account file from storage and represent it as a JSON object:

1. Open link <https://apireference.aspose.cloud/email/#/EmailClient/GetEmailClientAccount> and click *"Try it out"* button
1. Enter information about file location on storage and click *"Execute"* button
## **Save and get email account using SDK**
**Save and get email account using SDK**

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Save-And-Get-Email-Account-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Save-And-Get-Email-Account-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Save-And-Get-Email-Account-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Save-And-Get-Email-Account-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Save-And-Get-Email-Account-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Save-And-Get-Email-Account-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}
## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/sdk-setup/).

{{% /alert %}}
