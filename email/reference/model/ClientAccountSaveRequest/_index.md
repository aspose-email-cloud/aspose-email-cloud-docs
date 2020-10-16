---
title: "ClientAccountSaveRequest"
type: docs
url: /reference-model-client-account-save-request/
weight: 1
---
Email client account save request             

Properties:

Class has no properties

Parent class: [StorageModelOfEmailClientAccount](/email/reference-model-storage-model-of-email-client-account/)

## Example

{{< tabs tabTotal="6" tabID="client_account_save_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var clientAccountSaveRequest = new ClientAccountSaveRequest
{
    StorageFile = new StorageFileLocation
    {
        FileName = "email.account",
        Storage = "First Storage",
        FolderPath = "file/location/folder/on/storage"
    },
    Value = new EmailClientAccount
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
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientAccountSaveRequest clientAccountSaveRequest = Models.clientAccountSaveRequest()
    .storageFile(Models.storageFileLocation()
        .fileName("email.account")
        .storage("First Storage")
        .folderPath("file/location/folder/on/storage")
        .build())
    .value(Models.emailClientAccount()
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
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
client_account_save_request = models.ClientAccountSaveRequest(
    storage_file=models.StorageFileLocation(
        file_name='email.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'),
    value=models.EmailClientAccount(
        host='smtp.example.com',
        port=465,
        security_options='SSLAuto',
        protocol_type='SMTP',
        credentials=models.EmailClientAccountOauthCredentials(
            client_id='clientId',
            client_secret='clientSecret',
            refresh_token='refreshToken',
            login='example@example.com')))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
client_account_save_request = ClientAccountSaveRequest.new(
  storage_file: StorageFileLocation.new(
    file_name: 'email.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'),
  value: EmailClientAccount.new(
    host: 'smtp.example.com',
    port: 465,
    security_options: 'SSLAuto',
    protocol_type: 'SMTP',
    credentials: EmailClientAccountOauthCredentials.new(
      client_id: 'clientId',
      client_secret: 'clientSecret',
      refresh_token: 'refreshToken',
      login: 'example@example.com')))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let clientAccountSaveRequest = Models.clientAccountSaveRequest()
    .storageFile(Models.storageFileLocation()
        .fileName('email.account')
        .storage('First Storage')
        .folderPath('file/location/folder/on/storage')
        .build())
    .value(Models.emailClientAccount()
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
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$clientAccountSaveRequest = Models::clientAccountSaveRequest()
    ->storageFile(Models::storageFileLocation()
        ->fileName('email.account')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
    ->value(Models::emailClientAccount()
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
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

