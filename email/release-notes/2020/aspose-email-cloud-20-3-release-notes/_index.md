---
title: "Aspose.Email Cloud 20.3 Release Notes"
type: docs
url: /aspose-email-cloud-20-3-release-notes/
weight: 170
---

## **New features**
## **1. Disposable email address detection**
Disposable email hurts statistics collecting and clients analysis. To avoid this you can use [Aspose.Email Cloud API](https://products.aspose.cloud/email/family) to determine whether an email address is disposable or not:

```csharp

var isDisposable = await emailApi.IsEmailAddressDisposableAsync(

    new IsEmailAddressDisposableRequest("example@mailcatch.com"));

Console.WriteLine(isDisposable.Value); //prints true

```

More languages and examples available in the [Developer Guide](/email/disposable-emails-detection-api/).
## **2. Virtual multi email account client**
We extended the functionality of the built-in email client. Now you can create virtual multi-account to search, fetch and delete messages from several accounts at the same time:

```csharp

//New multi account model

var multiAccount = new EmailClientMultiAccount

{

    ReceiveAccounts = new List<EmailClientAccount>

    {

        new EmailClientAccount("imap.gmail.com", 993, "SSLAuto", "IMAP",

            new EmailClientAccountPasswordCredentials("example@gmail.com", null, "password")),

        new EmailClientAccount("exchange.outlook.com", 443, "SSLAuto", "EWS",

            new EmailClientAccountPasswordCredentials("example@outlook.com", null,"password"))

    }

};

//Save it to file with extension ".multi.account"

await emailApi.SaveEmailClientMultiAccountAsync(

    new SaveEmailClientMultiAccountRequest(

        new StorageFileRqOfEmailClientMultiAccount(

            multiAccount,

            new StorageFileLocation(

                "First storage", "folder/on/storage", "fileName.multi.account"))));

//Find all messages from example@aspose.com, received to both example@gmail.com and example@outlook.com

var messages = await emailApi.ListEmailModelsAsync(new ListEmailModelsRequest(

    "INBOX", "('From' Contains 'example@aspose.com')", 

    "fileName.multi.account", null,

	"First Storage", "folder/on/storage",

	true));

```

More languages and examples available in the [Developer Guide](/email/email-client/).
## **Other improvements**
We improved our [apireference](https://apireference.aspose.cloud/email/). For some endpoints, you can see prefilled example values, when you press *"Try it out"* button. We are going to add more examples in future. Now examples available for:

- <https://apireference.aspose.cloud/email/#/EmailClient/SendEmailModel>
- <https://apireference.aspose.cloud/email/#/EmailClient/AppendEmailModelMessage>
- <https://apireference.aspose.cloud/email/#/EmailClient/DeleteEmailFolder>
- <https://apireference.aspose.cloud/email/#/EmailClient/DeleteEmailMessage>
- <https://apireference.aspose.cloud/email/#/EmailClient/SetEmailReadFlag>
