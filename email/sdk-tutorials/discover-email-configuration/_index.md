---
title: "Discover Email Configuration"
type: docs
url: /discover-email-configuration/
description: "Aspose Email tutorial shows how to work with automated email configuration discovery API with Aspose.Email Cloud API."
weight: 60
---

## **Work With Email Configuration**
This is an automated email configuration discovery API. It performs more than 5 different configuration discovery methods simultaneously to support the maximum count of email providers. You can find an email server's configuration with 3 different methods. 

{{% alert color="primary" %}} To see how to setup SDKs use the [SDK setup](/emailcloud/sdk-setup/) tutorial. {{% /alert %}} 


## **Discover Without Validation**
The simplest way to discover email configuration is calling [**DiscoverEmailConfig**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#DiscoverEmailConfig) method. This method requires **1 parameter** — [**DiscoverEmailConfigRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/DiscoverEmailConfigRequest.cs), which is a request model for this operation. 

 [**DiscoverEmailConfigRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/DiscoverEmailConfigRequest.cs) has 2 parameters:

- *Address* — Email address.
- *FastProcessing* [**optional**] — Turns on fast processing. All discover systems will run in parallel. First discovered result will be returned.

**How to discover email configuration without validation?**

{{< tabs tabTotal="6" tabID="1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-discover-email-configuration-without-validation-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-discover-email-configuration-without-validation-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-discover-email-configuration-without-validation-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-discover-email-configuration-without-validation-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-discover-email-configuration-without-validation-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-discover-email-configuration-without-validation-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
\
This method performs email configuration discovery using all methods that do not require validation. All methods invoked in parallel and the best result is returned to the user. **DiscoverEmailConfigRequest** contains one extra field - **fastProcessing**. This field determines that there is no need for the best possible result. If **fastProcessing** is set to true, service will also run all discover methods in parallel and return the first successful result without waiting for others.

**DiscoverEmailConfig** returns list of EmailAccountConfig objects. **ExtraInfo** field contains extra information like OWA or EWS URLs, enable protocol instructions, etc.

**See JSON Response Example For Gmail**

{{< tabs tabTotal="1" tabID="2" tabName1="JSON" >}}

{{< tab tabNum="1" >}}

```javascript

{

  "value": [

    {

      "displayName": "Google Mail",

      "protocolType": "IMAP",

      "host": "imap.gmail.com",

      "port": 993,

      "socketType": "SSLAuto",

      "authenticationTypes": [

        "PasswordCleartext",

        "OAuth2"

      ],

      "extraInfo": [

        {

          "name": "Enable: You need to enable IMAP access",

          "value": "https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop"

        }

      ],

      "isValidated": false

    },

    {

      "displayName": "Google Mail",

      "protocolType": "SMTP",

      "host": "smtp.gmail.com",

      "port": 465,

      "socketType": "SSLAuto",

      "authenticationTypes": [

        "PasswordCleartext",

        "OAuth2"

      ],

      "extraInfo": [

        {

          "name": "Enable: You need to enable IMAP access",

          "value": "https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop"

        }

      ],

      "isValidated": false

    },

    {

      "displayName": "Google Mail",

      "protocolType": "POP3",

      "host": "pop.gmail.com",

      "port": 995,

      "socketType": "SSLAuto",

      "authenticationTypes": [

        "PasswordCleartext",

        "OAuth2"

      ],

      "extraInfo": [

        {

          "name": "Enable: You need to enable IMAP access",

          "value": "https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop"

        }

      ],

      "isValidated": false

    }

  ]

}

```

{{< /tab >}}

{{< /tabs >}}


## **Discover With Validation**
To discover email configuration with validation, use methods **DiscoverEmailConfigOauth** and **DiscoverEmailConfigPassword**. These methods use all algorithms from **DiscoverEmailConfig** and some extra. Also, the discovered configuration will be validated, if it is possible. Service will try to connect to all discovered protocols using provided auth data.
### **Discover using password**
To discover email configuration using password authentication use [**DiscoverEmailConfigPassword**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#DiscoverEmailConfigPassword) method. This method requires **1 parameter** — [**DiscoverEmailConfigPasswordRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/DiscoverEmailConfigPasswordRequest.cs), which is a request model for this operation. 
To initialize this object you should define its 1 parameter — 
[**DiscoverEmailConfigPassword**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/e9dbe88b18e176d7570339372636a36edae848f5/Model/DiscoverEmailConfigPassword.cs).

[**DiscoverEmailConfigPassword**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/e9dbe88b18e176d7570339372636a36edae848f5/Model/DiscoverEmailConfigPassword.cs) has **4 parameters**:

- *Address* — Email address.
- *FastProcessing* [**optional**] — Turns on fast processing. All discover systems will run in parallel. First discovered result will be returned.
- *Login* — Email account login. If not specified, address used as a login.
- *Password* — Email account password. 

**How to discover email configuration using the password authentication?**

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-discover-email-configuration-using-the-password-authentication-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-discover-email-configuration-using-the-password-authentication-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-discover-email-configuration-using-the-password-authentication-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-discover-email-configuration-using-the-password-authentication-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-discover-email-configuration-using-the-password-authentication-1.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-discover-email-configuration-using-the-password-authentication-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
\
You can also provide **login** if it is not same as the **address**.
### **Discover using OAuth 2.0**
To discover email configuration using OAuth 2.0 use [**DiscoverEmailConfigOauth**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/docs/EmailApi.md#DiscoverEmailConfigOauth) method. This method requires **1 parameter** — [**DiscoverEmailConfigOauthRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/02941624e3e6e35c1c1d8fef37e3f201b6cc353c/Model/Requests/DiscoverEmailConfigOauthRequest.cs), which is a request model for this operation. 
To initialize this object you should define its 1 parameter — [**DiscoverEmailConfigOauth**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/e9dbe88b18e176d7570339372636a36edae848f5/Model/DiscoverEmailConfigOauth.cs). 

[**DiscoverEmailConfigOauth**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/e9dbe88b18e176d7570339372636a36edae848f5/Model/DiscoverEmailConfigOauth.cs) has 7 **parameters**:

- *Address* — Email address.
- *FastProcessing* [**optional**] — Turns on fast processing. All discover systems will run in parallel. First discovered result will be returned.
- *Login* [**optional**] — Email account login. If not specified, address used as a login.
- *ClientId* — OAuth client id.
- *ClientSecret* — OAuth client secret.
- *RefreshToken* — OAuth refresh token.
- *RequestUrl* — The URL to obtain an access token. If not specified, will be discovered from email configuration.



**How to discover email configuration using OAuth 2.0 authentication?**

{{< tabs tabTotal="6" tabID="5" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-discover-email-configuration-using-OAuth-2-0-authentication-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-discover-email-configuration-using-OAuth-2-0-authentication-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-discover-email-configuration-using-OAuth-2-0-authentication-1.py" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-discover-email-configuration-using-OAuth-2-0-authentication-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-discover-email-configuration-using-OAuth-2-0-authentication-1.ts" >}}





{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-discover-email-configuration-using-OAuth-2-0-authentication-1.php" >}}

{{< /tab >}}

{{< /tabs >}}
\
Provide **login** if it is not same as the address. You can also provide **requestUrl** (an URL to obtain an access token using refresh token). For some servers, **requestUrl** is discovered automatically.
## **More Tutorials**
See more Aspose Email tutorials: 


