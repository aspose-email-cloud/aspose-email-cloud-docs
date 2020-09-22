---
title: "Discover Email Configuration"
type: docs
url: /discover-email-configuration/
description: "Aspose Email tutorial shows how to work with automated email configuration discovery API with Aspose.Email Cloud API."
weight: 60
---

## **Work With Email Configuration**
This is an automated email configuration discovery API. It performs more than 5 different configuration discovery methods simultaneously to support the maximum count of email providers. You can find an email server's configuration with 3 different methods.

{{% alert color="primary" %}} To see how to setup SDKs use the [SDK setup](/email/sdk-setup/) tutorial. {{% /alert %}} 


## **Discover Without Validation**
The simplest way to discover email configuration is calling [**Discover**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailConfigApi.md#Discover) method from [**EmailConfigApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailConfigApi.md) class. This method requires **1 parameter** — **EmailConfigDiscoverRequest**, which is a request model for this operation. 

 **EmailConfigDiscoverRequest** has 2 parameters:

- *Address* — Email address.
- *FastProcessing* [**optional**] — Turns on fast processing. All discover systems will run in parallel. First discovered result will be returned.

**How to discover email configuration without validation?**

{{< tabs tabTotal="6" tabID="1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
EmailAccountConfigList configs = await api.EmailConfig.DiscoverAsync(
    new EmailConfigDiscoverRequest("example@gmail.com"));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailAccountConfigList configList = api.emailConfig().discover(
    new EmailConfigDiscoverRequest("example@gmail.com", false));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
configs = api.email_config.discover(
    models.EmailConfigDiscoverRequest('example@gmail.com'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
configs = api.email_config.discover(
  EmailConfigDiscoverRequest.new(
    address: 'example@gmail.com'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
var configs = await api.emailConfig.discover(
    new EmailConfigDiscoverRequest(
        'example@gmail.com'));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$configs = $api->emailConfig()->discover(
    new EmailConfigDiscoverRequest(
        "example@gmail.com"));
```

{{< /tab >}}

{{< /tabs >}}

This method performs email configuration discovery using all methods that do not require validation. All methods invoked in parallel and the best result is returned to the user. **EmailConfigDiscoverRequest** contains one extra field - **fastProcessing**. This field determines that there is no need for the best possible result. If **fastProcessing** is set to true, service will also run all discover methods in parallel and return the first successful result without waiting for others.

**Discover** returns list of EmailAccountConfig objects. **ExtraInfo** field contains extra information like OWA or EWS URLs, enable protocol instructions, etc.

<details>
  <summary>See JSON Response Example For Gmail</summary>

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

</details>


## **Discover With Validation**
To discover email configuration with validation, use methods **DiscoverOauth** and **DiscoverPassword**. These methods use all algorithms from **Discover** and some extra. Also, the discovered configuration will be validated, if it is possible. Service will try to connect to all discovered protocols using provided auth data.
### **Discover using password**
To discover email configuration using password authentication use [**DiscoverPassword**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailConfigApi.md#discoverpassword) method. This method requires **1 parameter** — [**EmailConfigDiscoverPasswordRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailConfigDiscoverPasswordRequest.md), which is a request model for this operation. 

[**EmailConfigDiscoverPasswordRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailConfigDiscoverPasswordRequest.md) has **4 parameters**:

- *Address* — Email address.
- *FastProcessing* [**optional**] — Turns on fast processing. All discover systems will run in parallel. First discovered result will be returned.
- *Login* — Email account login. If not specified, address used as a login.
- *Password* — Email account password. 

**How to discover email configuration using the password authentication?**

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
EmailAccountConfigList configs =
    await api.EmailConfig.DiscoverPasswordAsync(
        new EmailConfigDiscoverPasswordRequest
        {
            Address = "example.login@gmail.com",
            Password = "example.password",
            FastProcessing = true
        });
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailAccountConfigList configList = api.emailConfig().discoverPassword(
    (EmailConfigDiscoverPasswordRequest) new EmailConfigDiscoverPasswordRequest()
        .password("example.password")
        .address("example@gmail.com")
        .fastProcessing(true));
```
{{< /tab >}}

{{< tab tabNum="3" >}}

```py
configs = api.email_config.discover_password(
    models.EmailConfigDiscoverPasswordRequest(
        'example@gmail.com', True, password='example.password'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
configs = api.email_config.discover_password(
  EmailConfigDiscoverPasswordRequest.new(
    address: 'example@gmail.com',
    fast_processing: true,
    password: 'example.password'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
var configs = await api.emailConfig.discoverPassword(
    new EmailConfigDiscoverPasswordRequest(
        'example@gmail.com', true, undefined,
        'example.password'));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$configs = $api->emailConfig()->discoverPassword(
    new EmailConfigDiscoverPasswordRequest(
        "example@gmail.com", true, null, "example.password"));
```

{{< /tab >}}

{{< /tabs >}}

You can also provide **login** if it is not same as the **address**.
### **Discover using OAuth 2.0**
To discover email configuration using OAuth 2.0 use [**DiscoverOauth**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailConfigApi.md#discoveroauth) method. This method requires **1 parameter** — [**EmailConfigDiscoverOauthRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailConfigDiscoverOauthRequest.md), which is a request model for this operation. 

[**EmailConfigDiscoverOauthRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailConfigDiscoverOauthRequest.md) has 7 **parameters**:

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

```cs
var configs = await api.EmailConfig.DiscoverOauthAsync(
    new EmailConfigDiscoverOauthRequest(
        {
            Address = "example.login@gmail.com",
            ClientId = "Your client id",
            ClientSecret = "Your client secret",
            RefreshToken = "Your refresh token",
            FastProcessing = true
        });
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailAccountConfigList configList = api.emailConfig().discoverOauth(
    (EmailConfigDiscoverOauthRequest) new EmailConfigDiscoverOauthRequest()
        .clientId("your client id")
        .clientSecret("your client secret")
        .refreshToken("your refresh token")
        .address("example@gmail.com")
        .fastProcessing(true));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
configs = api.email_config.discover_oauth(
    models.EmailConfigDiscoverOauthRequest(
        'example@gmail.com', True, None, 'client id',
        'client secret', 'refresh token'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
configs = @api.email_config.discover_oauth(
  EmailConfigDiscoverOauthRequest.new(
    address: 'example@gmail.com',
    fast_processing: true,
    client_id: 'client id',
    client_secret: 'client secret',
    refresh_token: 'refresh token'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
var configs = await td.api().emailConfig.discoverOauth(
    new EmailConfigDiscoverOauthRequest(
        'example@gmail.com', true, undefined,
        'client-id', 'client-secret', 'refresh-token'));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$configs = $api->emailConfig()->discoverOauth(
    new EmailConfigDiscoverOauthRequest("example@gmail.com", true, null,
        "your client id", "your client secret", "your refresh token"));
```

{{< /tab >}}

{{< /tabs >}}
\
Provide **login** if it is not same as the address. You can also provide **requestUrl** (an URL to obtain an access token using refresh token). For some servers, **requestUrl** is discovered automatically.
## **More Tutorials**
See more Aspose Email tutorials: 
{{< list-of-articles-in-this-section >}}
