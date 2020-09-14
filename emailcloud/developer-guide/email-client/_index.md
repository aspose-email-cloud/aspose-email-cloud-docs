---
title: "Email Client"
type: docs
url: /email-client/
description: "Aspose.Email Cloud API provides email client which supports: POP3, IMAP, SMTP; OAuth &amp;amp; Basic authentication; Multi-account; process emails."
weight: 110
---

## **Email Client API**
[**Aspose.Email Cloud API**](https://products.aspose.cloud/email/family) provides an email client API which supports:

- POP3, IMAP, SMTP, Exchange, WebDav protocols.
- OAuth and Basic authentication.
- Virtual Multi-account (provides API to handle several email accounts as one).
- The email client allows to:
  - Send emails.
  - Append email messages to folders.
  - Mark emails as read.
  - Get email lists, search emails.
  - Fetch emails by id.
  - Delete messages by id.
  - Folder operations (Get list/Create/Delete folder).

**You should set up email accounts before using email client API.**

Email account information should be stored on Storage as **.account** or **.multi.account** file. 

File with **.account** extension is used to store one email account. It contains information about email server configuration (*host, port, protocol, security options*) and authentication data (*login/password or OAuth credentials*). You can find out more in [working with single email account ](/emailcloud/single-email-account-setup/)article.  

File with **.multi.account** extension is used to store Virtual Multi-account. ou can find out more in [working with multi email account ](/emailcloud/multi-email-account-setup/)article.  

All email client methods use one account or an account pair (firstAccount + secondAccount). For example, you can call an API method with a combination of IMAP and SMTP accounts. So the client will use the SMTP account to send and the IMAP account to receive messages.

