---
title: "Multi Email Account Setup"
type: docs
url: /multi-email-account-setup/
description: "How to setup multi email account with Aspose.Email Cloud API. What is .multi.account file format?"
weight: 20
---

## **Introduction**
You should setup email accounts before using email client API.

Email account information should be stored on Storage as **\*.account** or **\*.multi.accoun**t file.

File with **.multi.account** extension is used to store multiple email accounts. This file should be used for virtual multi-account client feature.

One email account contains information about email server configuration (host, port, security options, protocol) and authentication data (login/password or OAuth credentials).  To get more information about **.account** file - take a look at the  [Single Email Account setup](https://docs.aspose.cloud/display/LGIS/Single+Email+Account+setup) article.

**.multi.account** is the internal file format developed by Aspose Company. This file format uses only for storing account’s settings on the Aspose Cloud Storage. 

You don't need to create **.multi.account** file directly, you can do it via Aspose.Email Cloud API. To create **.multi.account** file - follow instructions that are provided below.

{{% alert color="primary" %}} 

If you want to know more about working with **Email Client** — take a look at the Aspose Email Cloud tutorial: [**Quick Start With Email Client**](/emailcloud/quick-start-with-email-client/).

{{% /alert %}} 
## **Save multi email account using Swagger-UI**
You can test this functional by using [API reference service](https://apireference.aspose.cloud/email/). To save **multi email** **account** to the [Aspose Storage](https://apireference.aspose.cloud/storage/), you should follow these steps:

1. Open [link](https://apireference.aspose.cloud/email/)
1. Click *"Authorize"* button, enter your AppKey and AppSid, obtained from the [dashboard](https://dashboard.aspose.cloud/), click *"Authorize"* dialog button
1. Open [link](https://apireference.aspose.cloud/email/#/EmailClient/SaveEmailClientMultiAccount) and click *"Try it out"* button
1. Enter JSON with email account information and click *"Execute"* button


You can use this JSON to save a multi email account

```javascript

{

   "Value":{

      "ReceiveAccounts":[

         {

            "Host":"imap.gmail.com",

            "Port":993,

            "SecurityOptions":"SSLAuto",

            "ProtocolType":"IMAP",

            "Credentials":{

               "ClientId":"client-id",

               "ClientSecret":"clientSecret",

               "RefreshToken":"refreshToken",

               "Login":"example@gmail.com",

               "Discriminator":"EmailClientAccountOauthCredentials"

            }

         },

         {

            "Host":"exchange.outlook.com",

            "Port":443,

            "SecurityOptions":"SSLAuto",

            "ProtocolType":"EWS",

            "Credentials":{

               "Password":"password",

               "Login":"example@outlook.com",

               "Discriminator":"EmailClientAccountPasswordCredentials"

            }

         }

      ],

      "SendAccount":{

         "Host":"smtp.gmail.com",

         "Port":465,

         "SecurityOptions":"SSLAuto",

         "ProtocolType":"SMTP",

         "Credentials":{

            "ClientId":"client-id",

            "ClientSecret":"clientSecret",

            "RefreshToken":"refreshToken",

            "Login":"example@gmail.com",

            "Discriminator":"EmailClientAccountOauthCredentials"

         }

      }

   },

   "StorageFile":{

      "FileName":"fileName.multi.account",

      "Storage":"First Storage",

      "FolderPath":"folder/on/storage"

   }

}

```

## **Get email multi-account from storage using Swagger-UI**
You can get saved .multi.account file from storage and represent it as a JSON object:

1. Open [link](https://apireference.aspose.cloud/email/#/EmailClient/GetEmailClientMultiAccount) and click *"Try it out"* button
1. Enter information about file location on storage and click *"Execute"* button
## **Save and get email multi-account using SDK**
**Save and get email multi-account using SDK**

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Save-And-Get-Email-Multi-Account-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Save-And-Get-Email-Multi-Account-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Save-And-Get-Email-Multi-Account-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Save-And-Get-Email-Multi-Account-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Save-And-Get-Email-Multi-Account-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Save-And-Get-Email-Multi-Account-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}
## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/emailcloud/sdk-setup/).

{{% /alert %}}
