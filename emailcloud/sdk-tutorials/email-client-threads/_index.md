---
title: "Email Client Threads"
type: docs
url: /email-client-threads/
description: "Aspose.Email Cloud SDK allows to manipulate message threads using our built-in email client. Threads support EWS, POP3, IMAP, WebDav, virtual Multi-account."
weight: 70
---

Message Threads

This tutorial is about **manipulating message threads using [Aspose.](https://products.aspose.cloud/email/net)[Email](https://products.aspose.cloud/email/net) build-in client.**

{{% alert color="primary" %}} 

You may ask '*Is there any difference between messages and threads?*'. At first glance, the difference is not obvious, but there is.

- **Messages**. The most important entity when you create an email application. The message contains email’s body, attachments, sender, recipients, metadata and other useful pieces of information.
- **Threads**. Messages, collected together with a variety of parameters are called threads. Using threads, you can get more structured emails in the mailbox.

{{% /alert %}} 

Using threads, you can easily structure emails in the mailbox. Instead of working with an unstructured list of messages, it is better to work and analyze only certain threads of emails. In the picture below you can see how the messages are arranged in threads:

![todo:image\_alt\_text](email-client-threads_1.png)
## **Built-In Email Client**
[**Aspose.Email Cloud API**](https://products.aspose.cloud/email/family) provides a [built-in email client](/email-client/) with a unified API, which supports different account types like **SMTP**, **POP3**, **IMAP**, **EWS**.



{{% alert color="primary" %}} 

- Setup SDK, using tutorial: [**SDK setup**](/sdk-setup-html/).
- Setup your email client accounts, using tutorial: **[Quick Start With Email Client**](/quick-start-with-email-client-html/)**.

{{% /alert %}} 

Threads support by protocols:

- **Exchange Web Services (EWS)** **Accounts**: native support, no extra configuration needed. Exchange Web Services is an alternative to the MAPI protocol. EWS is used by the latest version of Microsoft Outlook for Mac and Microsoft Entourage for Mac.
- **POP3**: thread support is implemented using message cache. Message cache location on storage should be specified. The Post Office Protocol allows manipulating the user's client application with a mailbox supported on a mail server.
- **IMAP**: thread support is implemented using message cache, at the moment. Native threads support will be implemented in a future version. The Internet Message Access Protocol is the Internet protocol that allows an email client to access emails on a remote mail server.
- **WebDav**: threads are not supported.
- **Virtual Multi-account**: gets threads from underlying accounts and provides them as is.
## **Thread Support using Message Cache**
Aspose.Email [built-in email client](/email-client/) supports native threads for **EWS** accounts. For **POP3** and **IMAP** accounts we provide this functionality using our own threads implementation. This implementation uses messages’ cache, located on [Aspose Storage](https://apireference.aspose.cloud/storage/) and our own threads algorithm, which generates threads based on message subject and participants.

Native threads for **IMAP** will be added in future versions. Message cache will still be used for **IMAP** accounts if the **IMAP** server does not provide native threads.

To support threads using cache, you should provide cache location during email account setup:

**Setup account with cache file**

{{< tabs tabTotal="6" tabID="1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Setup-Account-With-Cache-File-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Setup-Account-With-Cache-File-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Setup-Account-With-Cache-File-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Setup-Account-With-Cache-File-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Setup-Account-With-Cache-File-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Setup-Account-With-Cache-File-1.php" >}}

{{< /tab >}}

{{< /tabs >}}



The **account.cache** file contains basic information about messages and threads (*folder, subject, message identifiers, dates* and *participants*).

{{% alert color="primary" %}} 

Using **account.cache** file has some restrictions:

- The file will be created automatically during **ListEmailThreads** call if updateFolderCache is set to true.
- **ListEmailThreads** caches only messages for folders that were requested. So, to initialize cache for several folders, you should call **ListEmailThreads** for every single folder. Folder cache initialization takes more time than updating cache in the future.
- **ListEmailThreads** is the only way to sync messages with the account. It finds all messages that were not cached before, and adds them to the existing threads or creates new ones. **ListEmailThreads** also removes messages from the cache if they were removed from the account.
- **ListEmailThreads**, **DeleteEmailThread**, **MoveEmailThread** methods lock **account.cache** file while processing. So, these methods will never run in parallel.
- **DeleteEmailThread** and **MoveEmailThread** methods delete/move messages in the email account and also update information about affected messages in **account.cache** file.
- **FetchEmailThreadMessages** method does not update and lock **account.cache** file, this method returns only messages that exist in the cache.

{{% /alert %}} 
## **Get List of Threads**
To get the list of threads for a given folder (folder parameter is ignored for **POP3** accounts), use **ListEmailThreads** method:

**Get list of threads**

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Get-List-Of-Threads-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Get-List-Of-Threads-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Get-List-Of-Threads-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Get-List-Of-Threads-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Get-List-Of-Threads-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Get-List-Of-Threads-1.php" >}}

{{< /tab >}}

{{< /tabs >}}

Set parameter **updateFolderCache** to **false** if you don't need to sync threads cache with your email account.
## **Fetch Thread Messages**
**ListEmailThreads** method returns all email threads from the folder. All threads contain a lists of messages. However, these messages contain only basic information: *MessageId, Date, Subject, Participants* (*From, To, CC*). Use **FetchEmailThreadMessages** method if you need to fetch full messages for a thread, including message bodies, attachments, alternate views, etc.

Some native thread implementations (such as **EWS** conversations) require **folder** argument. However, you can set this parameter to null if cached threads used (the thread's folder is already stored in the cache).

**Fetch thread messages**

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Fetch-Thread-Messages-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Fetch-Thread-Messages-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Fetch-Thread-Messages-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Fetch-Thread-Messages-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Fetch-Thread-Messages-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Fetch-Thread-Messages-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
## **Mark All Thread Messages as Read or Unread**
The **SetEmailThreadReadFlag** method should be used to mark all thread messages as (un)read.

Some native thread implementations (such as **EWS** conversations) require **folder** argument. However, you can set this parameter to null if cached threads used (the thread's folder is already stored in the cache).

**Mark thread as read**

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Mark-Thread-as-Read-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Mark-Thread-as-Read-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Mark-Thread-as-Read-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Mark-Thread-as-Read-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Mark-Thread-as-Read-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Mark-Thread-as-Read-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
## **Delete Thread**
You can delete the thread and all corresponding messages using **DeleteEmailThread** method.

Some native thread implementations (such as **EWS** conversations) require **folder** argument. However, you can set this parameter to null if cached threads used (the thread's folder is already stored in the cache).

**Delete thread**

{{< tabs tabTotal="6" tabID="5" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Delete-Thread-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Delete-Thread-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Delete-Thread-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Delete-Thread-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Delete-Thread-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Delete-Thread-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
## **Move Thread to Another Folder**
All thread messages can be moved from one folder to another using one single request of **MoveEmailThread** method (**POP3 is not supported**):

**Move thread**

{{< tabs tabTotal="6" tabID="6" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Move-Thread-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Move-Thread-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Move-Thread-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Move-Thread-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Move-Thread-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Move-Thread-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
## **More Tutorials**
See more Aspose Email tutorials: 


