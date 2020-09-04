---
title: "Email Client Operations"
type: docs
url: /email-client-operations/
description: " Aspose.Email Cloud API provides you with numerous number of email client operations that you can implement in your projects. How to work with Email Client?"
weight: 30
---

## **Introduction**
When email account information is uploaded to the storage, it can be used for email client operations. To use email account file, you should specify account file location on storage. This file can be a single .account file or a multi-account.

The email client has different APIs for some operations. For example, there are 3 ways for sending email message:

- [Send an email from *.eml file located on storage](https://apireference.aspose.cloud/email/#/EmailClient/SendEmail)
- [Send an email specified by base64 string in the request](https://apireference.aspose.cloud/email/#/EmailClient/SendEmailMime)
- [Send an email specified by a model in request ](https://apireference.aspose.cloud/email/#/EmailClient/SendEmailModel)

Use SDK reference documentation to see all available API methods: [C#](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/README.md), [Java](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/master/docs/README.md), [Python](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/master/sdk/docs/README.md), [Ruby](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/master/docs/README.md), [Typescript](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/master/doc/README.md), [PHP](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/master/doc/README.md).



{{% alert color="primary" %}} 

If you want to know more about working with **Email Client** — take a look at the Aspose Email Cloud tutorial: [**Quick Start With Email Client**](/quick-start-with-email-client-html/).

{{% /alert %}} 
## **Send email**
Send email operation will throw an error if sending emails is not supported by specified protocol (IMAP, POP3), or sender account is not set (EmailClientMultiAccount.SendAccount is null)
### **Send email using Swagger UI**
-----
You can test this functional by using [API reference service](https://apireference.aspose.cloud/email/). You can send a test email. *To send an email, you should follow these steps*:

1. Open link <https://apireference.aspose.cloud/email/>
1. Click *"Authorize"* button, enter your AppKey and AppSid, obtained from the [dashboard](https://dashboard.aspose.cloud/), click *"Authorize"* dialog button
1. Open link <https://apireference.aspose.cloud/email/#/EmailClient/SendEmailModel> and click *"Try it out"* button
1. Enter JSON with an email message and account information, then click *"Execute"* button

{{% alert color="primary" %}} 

![todo:image\_alt\_text](/images/icons/grey\_arrow\_down.png)

You can use this JSON to send an email

```javascript

{

   "Message":{

      "Body":"Some body",

      "From":{

         "DisplayName":"From address",

         "Address":"from@aspose.com"

      },

      "Subject":"Some subject",

      "To":[

         {

            "DisplayName":"To address",

            "Address":"to@aspose.com"

         }

      ]

   },

   "FirstAccount":"emailAccount.account",

   "StorageFolder":{

      "Storage":"First Storage",

      "FolderPath":"emailAccount/location/on/storage"

   }

}

```

File *"emailAccount.account"* should be available on storage in folder *"emailAccount/location/on/storage"*

{{% /alert %}} 
### **Send email using SDK**
-----
**Send email using SDK**

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Send-Email-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Send-Email-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Send-Email-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Send-Email-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Send-Email-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Send-Email-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}
## **Search messages**
Use search methods to find email messages by the subject, body, from, to fields, etc. Use virtual multi-account, to search messages in several accounts by one API request. If an account has no specified folder, it will be skipped when multi-account is used. There is no folder support in POP3 accounts, so folder field will be ignored for it.

Search message methods return only basic information about messages like from, to, subject, unique id, date, but nobody. Use **Fetch** methods to get the full message by finding a unique identifier.
### **Search messages using Swagger UI**
-----
You can test this functional by using [API reference service](https://apireference.aspose.cloud/email/). To find email messages in your files in [Aspose Storage](https://apireference.aspose.cloud/storage/)*,* you should follow these steps:

1. Open link <https://apireference.aspose.cloud/email/#/EmailClient/ListEmailModels> and click *"Try it out"* button
1. Enter email folder, query, account file location
1. You can set the *"recursive"* field to search in all child folders
1. Click the *"Execute"* button
### **Search messages using SDK**
-----
**Search messages using SDK**

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Search-Messages-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Search-Messages-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Search-Messages-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Search-Messages-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Search-Messages-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Search-Messages-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}
## **Delete message by id**
Messages found using email client API can be deleted by identifier EmailDto.MessageId. The virtual multi-account client adds extra information to MessageId, to identify from which account message was obtained. So when you delete a message using multi-account, you can be sure that it will be removed only from one account.
### **Delete message using Swagger UI**
-----


You can test this functional by using [API reference service](https://apireference.aspose.cloud/email/). To delete an email message from your files in [Aspose Storage](https://apireference.aspose.cloud/storage/)*,* you should follow these steps:



1. Open link <https://apireference.aspose.cloud/email/#/EmailClient/https://apireference.aspose.cloud/email/#/EmailClient/DeleteEmailMessage> and click *"Try it out"* button
1. Enter JSON to specify account and message to delete
1. Click the *"Execute"* button

{{% alert color="primary" %}} 

![todo:image\_alt\_text](/images/icons/grey\_arrow\_down.png)

You can use this JSON to delete a message

```javascript

{

  "firstAccount": "email.multi.account",

  "storageFolder": {

    "storage": "First storage",

    "folderPath": "email/account/location/on/storage"

  },

  "messageId": "<put your message identifier here>",

  "deletePermanently": true

}

```

{{% /alert %}} 
### **Delete message using SDK**
**Delete message using SDK**

{{< tabs tabTotal="6" tabID="5" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Delete-Messages-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Delete-Messages-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Delete-Messages-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Delete-Messages-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Delete-Messages-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Delete-Messages-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}
## **Fetch message by id**
Email client API provides fetch methods to get the full message by identifier. Use message identifiers from message search results (EmailDto.MessageId field)
### **Fetch message using Swagger UI**
-----


You can test this functional by using [API reference service](https://apireference.aspose.cloud/email/). To get the full message by identifier from your files in [Aspose Storage](https://apireference.aspose.cloud/storage/)*,* you should follow these steps:



1. Open link <https://apireference.aspose.cloud/email/#/EmailClient/FetchEmailModel> and click *"Try it out"* button
1. Enter message id and account file location
1. Click the *"Execute"* button
### **Fetch message using SDK**
-----
**Fetch message using SDK**

{{< tabs tabTotal="6" tabID="6" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Fetch-Message-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Fetch-Message-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Fetch-Message-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Fetch-Message-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Fetch-Message-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Fetch-Message-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}
## **Append emails**
Email messages can be appended to any folder if it is supported by account. POP3, SMTP and virtual multi-accounts do not support this feature.
### **Append email using Swagger UI**
-----
You can test this functional by using [API reference service](https://apireference.aspose.cloud/email/). To append messages to any folder if it is supported by account*,* you should follow these steps:

1. Open link <https://apireference.aspose.cloud/email/#/EmailClient/AppendEmailModelMessage> and click *"Try it out"* button
1. Enter JSON with an email message, folder and account information, then click *"Execute"* button

{{% alert color="primary" %}} 

![todo:image\_alt\_text](/images/icons/grey\_arrow\_down.png)

Use this JSON to append a message

```javascript

{

  "firstAccount": "email.account",

  "storageFolder": {

    "storage": "First storage",

    "folderPath": "email/account/location/on/storage"

  },

  "folder": "EmailAccountFolderName",

  "markAsSent": true,

  "message":{

    "body":"Some body",

    "from":{

       "displayName":"From address",

       "address":"from@aspose.com"

    },

    "subject":"Some subject",

    "to":[

       {

          "displayName":"To address",

          "address":"to@aspose.com"

       }

    ]

  }

}

```

{{% /alert %}} 
### **Append email using SDK**
**Append email using SDK**

{{< tabs tabTotal="6" tabID="8" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Email-Client-Append-Email-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Email-Client-Append-Email-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Email-Client-Append-Email-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Email-Client-Append-Email-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Email-Client-Append-Email-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Email-Client-Append-Email-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}
## **Mark message as read**
Email messages can be marked as read or unread.
### **Mark message as read using Swagger UI**
-----


You can test this functional by using [API reference service](https://apireference.aspose.cloud/email/). To mark messages as read or unread*,* you should follow these steps:



1. Open link <https://apireference.aspose.cloud/email/#/EmailClient/SetEmailReadFlag> and click *"Try it out"* button
1. Enter JSON with an email message, folder and account information, then click *"Execute"* button

{{% alert color="primary" %}} 

![todo:image\_alt\_text](/images/icons/grey\_arrow\_down.png)

Use this JSON to mark message as unread

```javascript

{

  "firstAccount": "email.account",

  "storageFolder": {

    "storage": "First storage",

    "folderPath": "email/account/location/on/storage"

  },

  "messageId": "<put your message identifier here>",

  "isRead": false

}

```

{{% /alert %}} 
### **Mark message as read using SDK**
**Mark message as read using SDK**

{{< tabs tabTotal="6" tabID="10" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Email-Client-Mark-Message-As-Read-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Email-Client-Mark-Message-As-Read-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Email-Client-Mark-Message-As-Read-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Email-Client-Mark-Message-As-Read-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Email-Client-Mark-Message-As-Read-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Email-Client-Mark-Message-As-Read-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}
## **Folders support**
The email client supports 3 operations with folders: Get a list of folders, create and delete folders. POP accounts do not support these operations, virtual multi-accounts support only getting folder lists.

In multi-account, all folders are merged by name. So, if you have 3 accounts and all of them have "INBOX" folder, you will get only one such folder. If one of the accounts has a unique folder, you will get it also.
### **Processing folders with Swagger UI**
-----
#### **Get folders**
You can test this functional by using [API reference service](https://apireference.aspose.cloud/email/). To get folders*,* you should follow these steps:

1. Open link <https://apireference.aspose.cloud/email/#/EmailClient/ListEmailFolders> and click *"Try it out"* button
1. Enter parent folder name (if it is not a root folder) and account information, then click *"Execute"* button
#### **Create folder**
You can test this functional by using [API reference service](https://apireference.aspose.cloud/email/). To create folders*,* you should follow these steps:

1. Open link <https://apireference.aspose.cloud/email/#/EmailClient/CreateEmailFolder> and click *"Try it out"* button
1. Enter JSON and click *"Execute"* button

{{% alert color="primary" %}} 

![todo:image\_alt\_text](/images/icons/grey\_arrow\_down.png)

Use this JSON to create a new folder

```javascript

{

  "firstAccount": "email.account",

  "storageFolder": {

    "storage": "First storage",

    "folderPath": "email/account/location/on/storage"

  },

  "folder": "NewFolderName"

}

```

{{% /alert %}} 
#### **Delete folder**
You can test this functional by using [API reference service](https://apireference.aspose.cloud/email/). To delete folders*,* you should follow these steps:

1. Open link <https://apireference.aspose.cloud/email/#/EmailClient/DeleteEmailFolder> and click *"Try it out"* button
1. Enter JSON and click *"Execute"* button

{{% alert color="primary" %}} 

![todo:image\_alt\_text](/images/icons/grey\_arrow\_down.png)

Use this JSON to delete a folder from previous example

```javascript

{

  "firstAccount": "email.account",

  "storageFolder": {

    "storage": "First storage",

    "folderPath": "email/account/location/on/storage"

  },

  "folder": "NewFolderName",

  "deletePermanently": true

}

```

{{% /alert %}} 
### **Processing folders with SDK**
-----
**Processing folders with SDK**

{{< tabs tabTotal="6" tabID="13" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Email-Client-Processing-Emails-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Email-Client-Processing-Emails-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Email-Client-Processing-Emails-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Email-Client-Processing-Emails-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Email-Client-Processing-Emails-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Email-Client-Processing-Emails-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}
## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/sdk-setup/).

{{% /alert %}}
