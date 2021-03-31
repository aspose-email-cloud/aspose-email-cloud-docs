---
title: "Aspose.Email Cloud 21.4 Release Notes"
type: docs
url: /aspose-email-cloud-21-4-release-notes/
weight: 170
---

## **New features**
## **1. Email client native conversation threads support for IMAP protocol**
The email conversation threads support has been improved for IMAP protocol:
- RFC 5256 THREAD extensions support added.
- Gmail IMAP threads support added.

Message cache-based thread support can still be used for all IMAP servers that do not support any native thread implementations.

More details are available in the [**Tutorial**](/email/email-client-threads/).
```csharp
const string inbox = "INBOX";
EmailThreadList threads = await api.Client.Thread.GetListAsync(
    new ClientThreadGetListRequest
    {
        Folder = inbox,
        Account = accountFile,
        Storage = storage,
        AccountStorageFolder = folder
    });
```

## **SDK Changes**
The new field `SourceFolder` was added to `ClientThreadMoveRequest`. In some protocols, the source folder should be specified to properly find all the messages related to the conversation that should be moved.
