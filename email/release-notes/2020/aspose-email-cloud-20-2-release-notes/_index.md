---
title: "Aspose.Email Cloud 20.2 Release Notes"
type: docs
url: /aspose-email-cloud-20-2-release-notes/
weight: 180
---

## **New features**
### **Introducing Email configuration auto-discover API**
If you want to read or send emails using email clients (e.g. Microsoft Outlook, Gmail, Thunderbird, etc.) you need to know their settings. 

Email client configuration consists of:

- Name;
- Protocol type;
- Host;
- Port;
- Socket type;
- etc.

Now you can easily get email client settings. We added a new API to discover email client configuration from an email address:

```csharp
var configs = await emailApi.DiscoverEmailConfigAsync(
    new DiscoverEmailConfigRequest("example@gmail.com"));
var imap = configs.Value
    .First(config => config.ProtocolType == "IMAP");

System.Console.WriteLine(imap.ToString());
/* This code will print:
class EmailAccountConfig {
  DisplayName: Google Mail
  ProtocolType: IMAP
  Host: imap.gmail.com
  Port: 993
  SocketType: SSLAuto
  ...
}*/
```

The email configuration auto discover API also supports emails with custom domains:

```csharp
var configs = await emailApi.DiscoverEmailConfigAsync(
    new DiscoverEmailConfigRequest("example@kickstarter.com"));
System.Console.WriteLine(configs.Value.First().DisplayName); //Prints "Google Mail"
```

You can use credentials to validate discovered configurations (login/password, oauth refresh token). Some extra discover algorithms used if credentials provided:

```csharp
var configs = await emailApi.DiscoverEmailConfigPasswordAsync(
    new DiscoverEmailConfigPasswordRequest(
        new DiscoverEmailConfigPassword
        {
            Address = "example.login@gmail.com",
            Password = "example.password"
        }));
```

See more examples on tutorial [Discover Email Configuration](/email/discover-email-configuration/).
## **SDK changes**
- Fixed bug with file support in Java SDK (getMapiAttachment, getCalendarAttachment, etc.)
- Ruby \*RequestData classes now have attribute accessors
- Java, Typescript, Python docstrings improved
- Java SDK methods now throw own ApiException instead of Exception
- Fixed bug in Typescript EmailApi constructor (appKey and appSid were mixed up)
