---
title: "EmailClientAccount"
type: docs
url: /reference-model-email-client-account/
weight: 1
---
A universal email client account             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Host** | **string** | Mail server host name or IP address              | 
**Port** | **int?** | Mail server port              | 
**SecurityOptions** | **string** | Email account security mode Enum, available values: None, SSLExplicit, SSLImplicit, SSLAuto, Auto | 
**ProtocolType** | **string** | Type of connection protocol. Enum, available values: IMAP, POP3, SMTP, EWS, WebDav | 
**Credentials** | [**EmailClientAccountCredentials**](/email/reference-model-email-client-account-credentials/) | Email client account credentials              | 
**CacheFile** | [**StorageFileLocation**](/email/reference-model-storage-file-location/) | File with messages cache. Used to provide extra functions, which are not supported by account              | [optional] 


## Example

{{< tabs tabTotal="6" tabID="email_client_account_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var emailClientAccount = new EmailClientAccount
{
    Host = "smtp.example.com",
    Port = 465,
    SecurityOptions = "SSLAuto",
    ProtocolType = "SMTP",
    Credentials = new EmailClientAccountOauthCredentials
    {
        ClientId = "clientId",
        ClientSecret = "clientSecret",
        RefreshToken = "refreshToken",
        Login = "example@example.com"
    },
    CacheFile = new StorageFileLocation
    {
        FileName = "account.cache",
        Storage = "First Storage",
        FolderPath = "file/location/folder/on/storage"
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailClientAccount emailClientAccount = Models.emailClientAccount()
    .host("smtp.example.com")
    .port(465)
    .securityOptions("SSLAuto")
    .protocolType("SMTP")
    .credentials(Models.emailClientAccountOauthCredentials()
        .clientId("clientId")
        .clientSecret("clientSecret")
        .refreshToken("refreshToken")
        .login("example@example.com")
        .build())
    .cacheFile(Models.storageFileLocation()
        .fileName("account.cache")
        .storage("First Storage")
        .folderPath("file/location/folder/on/storage")
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
email_client_account = models.EmailClientAccount(
    host='smtp.example.com',
    port=465,
    security_options='SSLAuto',
    protocol_type='SMTP',
    credentials=models.EmailClientAccountOauthCredentials(
        client_id='clientId',
        client_secret='clientSecret',
        refresh_token='refreshToken',
        login='example@example.com'),
    cache_file=models.StorageFileLocation(
        file_name='account.cache',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
email_client_account = EmailClientAccount.new(
  host: 'smtp.example.com',
  port: 465,
  security_options: 'SSLAuto',
  protocol_type: 'SMTP',
  credentials: EmailClientAccountOauthCredentials.new(
    client_id: 'clientId',
    client_secret: 'clientSecret',
    refresh_token: 'refreshToken',
    login: 'example@example.com'),
  cache_file: StorageFileLocation.new(
    file_name: 'account.cache',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let emailClientAccount = Models.emailClientAccount()
    .host('smtp.example.com')
    .port(465)
    .securityOptions('SSLAuto')
    .protocolType('SMTP')
    .credentials(Models.emailClientAccountOauthCredentials()
        .clientId('clientId')
        .clientSecret('clientSecret')
        .refreshToken('refreshToken')
        .login('example@example.com')
        .build())
    .cacheFile(Models.storageFileLocation()
        .fileName('account.cache')
        .storage('First Storage')
        .folderPath('file/location/folder/on/storage')
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$emailClientAccount = Models::emailClientAccount()
    ->host('smtp.example.com')
    ->port(465)
    ->securityOptions('SSLAuto')
    ->protocolType('SMTP')
    ->credentials(Models::emailClientAccountOauthCredentials()
        ->clientId('clientId')
        ->clientSecret('clientSecret')
        ->refreshToken('refreshToken')
        ->login('example@example.com')
        ->build())
    ->cacheFile(Models::storageFileLocation()
        ->fileName('account.cache')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

