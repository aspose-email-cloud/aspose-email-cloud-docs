---
title: "Quick Start With Email Client"
type: docs
url: /quick-start-with-email-client/
description: " Aspose Email tutorial shows how to work with your email clients using Aspose.Email Cloud API. Send emails, receive emails, process emails in your way."
weight: 30
---

## **Built-In Email Client**
[Aspose.Email Cloud API ](https://products.aspose.cloud/email/family)contains a built-in email client.

{{% alert color="primary" %}} 

To get more information about the built-in email client, take a look at the [Email Client](/email-client/) article. 

{{% /alert %}} 



The built-in email client supports:

- **SMTP**
- **POP3**
- **IMAP**
- **EWS**
- **WebDav**
- **Virtual multi-account**

Virtual multi-account is a fast and convenient way to set up multiple email accounts and use them as a single one.

{{% alert color="primary" %}} 

To see how to setup SDKs use the [SDK setup](/sdk-setup/) tutorial.

{{% /alert %}} 


## **How to Work With Email Client**
Before we start, we should set up an email account. This allows you to process your messages with [built-in Email Client](/email-client/) which is developed by [Aspose.Email Cloud](https://products.aspose.cloud/email/family).

The **created email account will be saved on storage**, so you don't have to repeat this operation later.
### **Create Email Account File**
You can create an email account online using Swagger UI or follow the instructions from these guides: [Single Email Account Setup](/single-email-account-setup/) and [Multi Email Account Setup](/multi-email-account-setup/).

1. Open [link](https://apireference.aspose.cloud/email/#/EmailClient/SaveEmailClientAccount) and click *"Try it out"* button
1. Enter JSON with email account information and click *"Execute"* button

{{< tabs tabTotal="1" tabID="1" tabName1="Swagger UI" >}}

{{< tab tabNum="1" >}}


```javascript

{ "Value":{ "Host":"imap.gmail.com", "Port":993, "SecurityOptions":"SSLAuto", "ProtocolType":"IMAP", "Credentials":{ "Password":"password", "Login":"example@gmail.com", "Discriminator":"EmailClientAccountPasswordCredentials" } }, "StorageFile":{ "FileName":"imap.account", "Storage":"First Storage", "FolderPath":"folder/on/storage" } }

```

{{< /tab >}}

{{< /tabs >}}

### **Setup email account**
First of all, you need to set up your email account’s credentials with [**EmailClientAccountPasswordCredentials**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/EmailClientAccountPasswordCredentials.cs) class. Define two fields: *Login* (Email client account login) and *Password* (Email client account password).

Then you need to initialize [**EmailClientAccount**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/EmailClientAccount.cs) object. Let’s define the following parameters:

- *Host* — Mail server hostname or IP address.
- *Port* — Mail server port.
- *ProtocolType* — Type of connection protocol. Enum, available values: IMAP, POP3, SMTP, EWS, WebDav.
- *SecurityOptions* — Email account security mode Enum, available values: None, SSLExplicit, SSLImplicit, SSLAuto, Auto.
- *Credentials* — Email client account credentials that we have created before.

To save your email account use [**SaveEmailClientAccountAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#SaveEmailClientAccountAsync) from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). You should create a request for this operation using [**SaveEmailClientAccountRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/SaveEmailClientAccountRequest.cs). To use this request you need to pass into it [**StorageFileRqOfEmailClientAccount**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/StorageFileRqOfEmailClientAccount.cs) model, which has **2 parameters**:

- *Value* — Object we want to save on Storage.
- StorageFile — [**StorageFileLocation**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/StorageFileLocation.cs) object, which contains IMAP account’s file location information, including **storage name**, a path to an **account folder**, name of the file with **IMAP account’s** configurations.

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Set-Up-Email-Account-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Set-Up-Email-Account-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Set-Up-Email-Account-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Set-Up-Email-Account-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Set-Up-Email-Account-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Set-Up-Email-Account-1.php" >}}

{{< /tab >}}

{{< /tabs >}}


### **Search Emails**
**Search Emails with Swagger UI**

Before you start, please try to search emails in your email account’s folders to see how it works. To do this use Swagger UI and follow instructions below:

1. Open [link](https://apireference.aspose.cloud/email/#/EmailClient/ListEmailModels) and click *"Try it out"* button
1. Enter email folder, query, account file location:
   1. folder = "INBOX"
   1. firstAccount: "imap.account"
   1. queryString: "('From' Contains '.com')"
   1. secondAccount should be empty
   1. storage: "First storage"
   1. storageFolder: "folder/on/storage"
   1. recursive: true
1. Click the *"Execute"* button.

**Search Emails Using Aspose.Email Cloud SDKs**

To search for emails in your email account’s folders you need to call [**ListEmailModelsAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#ListEmailModelsAsync) from [**EmailAPI**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). This method has one parameter — [**ListEmailModelsRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/ListEmailModelsRequest.cs), which is a request model for this operation. In this model you should define the following fields:

- *Folder* — A folder in email account.
- *QueryString* — A MailQuery search string.
- *FirstAccount* — Email account.
- *SecondAccount* [**optional**] — Additional email account (should be specified for POP/IMAP accounts and should be SMTP account).
- *Storage* — Storage name where account file(s) located.
- *StorageFolder* — Folder in storage where account file(s) located.
- *Recursive* [**optional**] — Specifies that should message be searched in subfolders recursively.

After that, you will get a list of messages matching your search criteria as [**ListResponseOfEmailDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/ListResponseOfEmailDto.cs).

**Now you can search emails**

{{< tabs tabTotal="6" tabID="5" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Search-Emails-In-INBOX-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Search-Emails-In-INBOX-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Search-Emails-In-INBOX-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Search-Emails-In-INBOX-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Search-Emails-In-INBOX-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Search-Emails-In-INBOX-1.php" >}}

{{< /tab >}}

{{< /tabs >}}


### **Fetch Message By Id**
**Fetch Message By Id With Swagger UI**

Try to fetch email by its Id from your email account’s folders to see how it works. To do this use Swagger UI and follow instructions below:

- Open [link](https://apireference.aspose.cloud/email/#/EmailClient/FetchEmailModel) and click *"Try it out"* button
- Enter message id and account file location
  - messageId: <message identifier>
  - firstAccount: "imap.account"
  - secondAccount should be empty
  - storage: "First storage"
  - storageFolder: "folder/on/storage"
- Click the *"Execute"* button




**Fetch Email By Id Using Aspose.Email Cloud SDKs**

In the previous step, we have got a list of emails. Let’s fetch one of them by its Id.

To do this you should use the **email’s Id**, obviously, and [**FetchEmailModelAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#FetchEmailModelAsync) method from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). This method requires **1 parameter** — [**FetchEmailModelRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/FetchEmailModelRequest.cs), 
which is a request model for this operation. 
[**FetchEmailModelRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/FetchEmailModelRequest.cs) has the following parameters:

- *MessageId* — Message identifier. 
- *FirstAccount* — Email account.
- *SecondAccount* [**optional**] — Additional email account (should be specified for POP/IMAP accounts and should be SMTP account).
- *Storage* — Storage name where account file(s) located.
- *StorageFolder* — Folder in storage where account file(s) located.

Аfter this operation you will receive an email as [**EmailDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/Model/EmailDto.cs).

**Fetch found message by id**

{{< tabs tabTotal="6" tabID="7" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Fetch-Message-By-Id-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Fetch-Message-By-Id-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Fetch-Message-By-Id-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Fetch-Message-By-Id-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Fetch-Message-By-Id-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Fetch-Message-By-Id-1.php" >}}

{{< /tab >}}

{{< /tabs >}}


### **Mark Message as Read**
Using API you are able to mark a message as read by its Id. Try to do this with **Swagger UI**:


1. Open [link](https://apireference.aspose.cloud/email/#/EmailClient/SetEmailReadFlag) and click *"Try it out"* button.
2. Use this JSON example in Swagger UI to do this operation:

{{< tabs tabTotal="1" tabID="8" tabName1="JSON" >}}
{{< tab tabNum="1" >}}

```javascript

{

  "firstAccount": "imap.account",

  "storageFolder": {

    "storage": "First storage",

    "folderPath": "folder/on/storage"

  },

  "messageId": "<message identifier>",

  "isRead": true

}

```

{{< /tab >}}

{{< /tabs >}}

\
**Mark Message as Read Using Aspose.Email Cloud SDKs**

You need to know message’s Id to mark it as read. We have done it in previous steps.

To mark a message as read use [**SetEmailReadFlagAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#SetEmailReadFlagAsync) from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). This method requires **1 parameter** — [**SetEmailReadFlagRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/SetEmailReadFlagRequest.cs), which requests a model for this operation.

The request accepts only **1 parameter** — [**SetMessageReadFlagAccountBaseRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/SetMessageReadFlagAccountBaseRequest.cs), which is a request to set a message as read.

[**SetMessageReadFlagAccountBaseRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/SetMessageReadFlagAccountBaseRequest.cs) has **5 parameters**:

- *FirstAccount* — First account storage file name for receiving emails (or universal one).
- *SecondAccount* [**oprional**] — Second account storage file name for sending emails (ignored if first is universal).
- *StorageFolder* — Storage folder location of account files.
- *MessageId* — Message identifier.
- *IsRead* — Specifies that message should be marked read or unread.

**Mark message as read**

{{< tabs tabTotal="6" tabID="10" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}



{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Mark-Message-As-Read-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Mark-Message-As-Read-1.java" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}



{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Mark-Message-As-Read-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Mark-Message-As-Read-1.rb" >}}



{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Mark-Message-As-Read-1.ts" >}}



{{< /tab >}}

{{< tab tabNum="6" >}}



{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Mark-Message-As-Read-1.php" >}}

{{< /tab >}}

{{< /tabs >}}


### **Delete Message**
**Delete Message With Swagger UI**

In an attempt to manage your messages, you may need to delete some of them. Try to delete a message with Swagger UI:

- Open [link](https://apireference.aspose.cloud/email/#/EmailClient/https://apireference.aspose.cloud/email/#/EmailClient/DeleteEmailMessage) and click *"Try it out"* button
- Enter JSON to specify account, message to delete and click the *"Execute"* button

Use this JSON example in Swagger UI to do this operation:

{{< tabs tabTotal="1" tabID="11" tabName1="JSON" >}}

{{< tab tabNum="1" >}}

```javascript

{

  "firstAccount": "imap.account",

  "storageFolder": {

    "storage": "First storage",

    "folderPath": "folder/on/storage"

  },

  "messageId": "<message identifier>",

  "deletePermanently": true

}

```

{{< /tab >}}

{{< /tabs >}}


\
**Delete Message Using Aspose.Email Cloud SDKs**

To remove a message, you should know the Id of the email you want to delete.

To delete email use from [**DeleteEmailMessageAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#DeleteEmailMessageAsync) from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). This method requires **1 parameter** — [**DeleteEmailMessageRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/DeleteEmailMessageRequest.cs), which requests a model for this operation.

To initialize [**DeleteEmailMessageRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/DeleteEmailMessageRequest.cs) you should pass **1 parameter** — [**DeleteMessageBaseRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/DeleteMessageBaseRequest.cs), which is a delete message request.

[**DeleteMessageBaseRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/DeleteMessageBaseRequest.cs) requires the following parameters:

- *FirstAccount* — First account storage file name for receiving emails (or universal one).
- *SecondAccount* [**oprional**] — Second account storage file name for sending emails (ignored if first is universal).
- *StorageFolder* — Storage folder location of account files.
- *MessageId* — Message identifier.
- *DeletePermanently* — Specifies that message should be deleted permanently.



**Delete message**

{{< tabs tabTotal="6" tabID="13" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Delete-Message-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Delete-Message-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Delete-Message-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Delete-Message-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Delete-Message-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Delete-Message-1.php" >}}

{{< /tab >}}

{{< /tabs >}}


### **Append new message**
**Append New Message With Swagger UI**

Try to append a message to your email account with Swagger UI:

- Open [link](https://apireference.aspose.cloud/email/#/EmailClient/AppendEmailModelMessage) and click *"Try it out"* button
- Enter JSON with an email message, folder and account information, then click *"Execute"* button.

Use this JSON example in Swagger UI to do this operation:

{{< tabs tabTotal="1" tabID="14" tabName1="JSON" >}}

{{< tab tabNum="1" >}}

```javascript

{

  "firstAccount": "imap.account",

  "storageFolder": {

    "storage": "First storage",

    "folderPath": "folder/on/storage"

  },

  "folder": "INBOX",

  "markAsSent": true,

  "message":{

    "body":"Some body",

    "from":{

       "displayName":"From address",

       "address":"example@gmail.com"

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

{{< /tab >}}

{{< /tabs >}}


\
**Append New Message Using Aspose.Email Cloud SDKs**

To append a new message to your email account — use [**AppendEmailModelMessageAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#AppendEmailModelMessageAsync) from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#AppendEmailModelMessageAsync). This method requires **1 parameter** — [**AppendEmailModelMessageRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/AppendEmailModelMessageRequest.cs), which requests a model for this operation.

To initialize [](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/DeleteEmailMessageRequest.cs)[**AppendEmailModelMessageRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/AppendEmailModelMessageRequest.cs) you should pass **1 parameter** — [**AppendEmailModelRq**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/AppendEmailModelRq.cs), which is an append email request.

[**AppendEmailModelRq**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/AppendEmailModelRq.cs) requires the following parameters:

- *FirstAccount* — First account storage file name for receiving emails (or universal one).
- *SecondAccount* [**oprional**] — Second account storage file name for sending emails (ignored if first is universal).
- *StorageFolder* — Storage folder location of account files.
- *MarkAsSent* — Mark message as sent.
- *Message* — Email document.



**Append new message**

{{< tabs tabTotal="6" tabID="16" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Append-New-Message-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Append-New-Message-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Append-New-Message-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Append-New-Message-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Append-New-Message-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Append-New-Message-1.php" >}}

{{< /tab >}}

{{< /tabs >}}


### **Setup email account for sending messages**
**Setup Email Account For Sending Messages With Swagger UI**

Try to setup an account to send messages with Swagger UI:

- Open [link](https://apireference.aspose.cloud/email/#/EmailClient/SaveEmailClientAccount) and click *"Try it out"* button
- Enter JSON with email account information and click *"Execute"* button

Use this JSON example in Swagger UI to do this operation:

{{< tabs tabTotal="1" tabID="17" tabName1="JSON" >}}

{{< tab tabNum="1" >}}

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

      "FileName":"smtp.account",

      "Storage":"First Storage",

      "FolderPath":"folder/on/storage"

   }

}

```

{{< /tab >}}

{{< /tabs >}}


\
**Setup Email Account For Sending Messages Using Aspose.Email Cloud SDKs**

All you have to do to setup your email account for sending messages is to use [**SaveEmailClientAccountAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#SaveEmailClientAccountAsync) from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md). This method requires **1 parameter** — [**SaveEmailClientAccountRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/SaveEmailClientAccountRequest.cs), which requests a model for this operation.

To initialize [**SaveEmailClientAccountRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/SaveEmailClientAccountRequest.cs) you should pass **1 parameter** — [**StorageFileRqOfEmailClientAccount**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/StorageFileRqOfEmailClientAccount.cs).

[**StorageFileRqOfEmailClientAccount**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/StorageFileRqOfEmailClientAccount.cs) requires the following parameters:

- Value — [**EmailClientAccount**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/EmailClientAccount.cs) object.
- StorageFile — [**StorageFileLocation**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/StorageFileLocation.cs) object.



**setup account for sending email messages**

{{< tabs tabTotal="6" tabID="19" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Setup-Account-To-Send-Message-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Setup-Account-To-Send-Message-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Setup-Account-To-Send-Message-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Setup-Account-To-Send-Message-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Setup-Account-To-Send-Message-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Setup-Account-To-Send-Message-1.php" >}}

{{< /tab >}}

{{< /tabs >}}


### **Send Email**
**Send Email With Swagger UI**

Try to send an email with Swagger UI:


- Open (link)[https://apireference.aspose.cloud/email/#/EmailClient/SendEmailModel] and click *"Try it out"* button
- Enter JSON with an email message and account information, then click *"Execute"* button

Use this JSON example in Swagger UI to do this operation:

{{< tabs tabTotal="1" tabID="20" tabName1="JSON" >}}

{{< tab tabNum="1" >}}

```javascript

 {

   "Message":{

      "Body":"Some body",

      "From":{

         "DisplayName":"From address",

         "Address":"example@gmail.com"

      },

      "Subject":"Some subject",

      "To":[

         {

            "DisplayName":"To address",

            "Address":"to@aspose.com"

         }

      ]

   },

   "FirstAccount":"smtp.account",

   "StorageFolder":{

      "Storage":"First Storage",

      "FolderPath":"folder/on/storage"

   }

} 

```

{{< /tab >}}

{{< /tabs >}}


\
**Send Message Using Aspose.Email Cloud SDKs**

To append a new message to your email account — use [**SendEmailModelAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#SendEmailModelAsync) from [**EmailApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#AppendEmailModelMessageAsync). This method requires **1 parameter** — [**SendEmailModelRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/SendEmailModelRequest.cs), which requests a model for this operation.

To initialize [](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/DeleteEmailMessageRequest.cs)[**SendEmailModelRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/SendEmailModelRequest.cs) you should pass **1 parameter** — [**SendEmailModelRq**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/SendEmailModelRq.cs), which is an append email request.

[**SendEmailModelRq**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/Model/SendEmailModelRq.cs) requires the following parameters:

- *FirstAccount* — First account storage file name for receiving emails (or universal one).
- *SecondAccount* [**oprional**] — Second account storage file name for sending emails (ignored if first is universal).
- *StorageFolder* — Storage folder location of aup an email account for getticcount files.
- *Message* — Email document.



**And send a message**

{{< tabs tabTotal="6" tabID="22" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}



{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Send-Sample-Email-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}



{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Send-Sample-Email-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}



{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Send-Sample-Email-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}



{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Send-Sample-Email-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}



{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Send-Sample-Email-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}



{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Send-Sample-Email-1.php" >}}

{{< /tab >}}

{{< /tabs >}}


## **More Tutorials**
See more Aspose Email tutorials: 
