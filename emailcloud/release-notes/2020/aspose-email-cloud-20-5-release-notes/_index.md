---
title: "Aspose.Email Cloud 20.5 Release Notes"
type: docs
url: /aspose-email-cloud-20-5-release-notes/
weight: 20
---

## **New Features**
## **1. Email client conversation threads**
An email [**conversation threads**](https://en.wikipedia.org/wiki/Conversation_threading) support has been added to Aspose.Email Cloud build-in client. Using conversation threads, you can get more structured emails in the mailbox. With the new API for conversation threads you can visually group your messages with their replies.

```csharp

var threads = await emailApi.ListEmailThreadsAsync(new ListEmailThreadsRequest(

    "INBOX", "email.account", null, storage, folder, true, 200));

```

Conversation threads are supported for POP3, IMAP, EWS, and virtual multi accounts.

Using API for conversation threads you can:

- get the list of threads in a folder
- fetch thread messages
- mark all thread messages as read or unread
- move thread to another folder
- delete thread

More details are available in the [**Tutorial**](/emailcloud/email-client-threads/).
## **2. Extended file converting API**
The most popular method in Aspose.Email Cloud API is ConvertEmail. This method converts email documents from one format to another. We have extended the file converting API and added new methods:

- ConvertContact and ConvertCalendar - converts VCard and iCalendar files from one supported format to another (for example, from iCalendar ICS file to MapiCalendar MSG format)
- ConvertEmailModelToFile - converts an EmailDto to a file in any supported format (EML, MSG, MHTML, HTML)
- GetEmailFileAsModel - converts an email file to an EmailDto object
- ConvertContactModelToFile, ConvertCalendarModelToFile, GetContactFileAsModel, GetCalendarFileAsModel - convert files to corresponding DTO objects (ContactDto and CalendarDto) and back

We hope you will like these new methods as much as you like ConvertEmail.

More details are available in the [**Tutorial**](/emailcloud/convert-email-calendar-and-contact-files/).
## **Documentation Improvements**
We have prepared new tutorials to help you get started with Aspose.Email Cloud SDK. All tutorials are available here: [**SDK Tutorials**](/emailcloud/sdk-tutorials/).
