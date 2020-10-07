---
title: "ClientAccountSaveMultiRequest"
type: docs
url: /reference-model-client-account-save-multi-request/
weight: 1
---
Email client multi account save request.             

Properties:

Class has no properties

Parent class: [StorageModelOfEmailClientMultiAccount](/email/reference-model-storage-model-of-email-client-multi-account/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="client_account_save_multi_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var clientAccountSaveMultiRequest = new ClientAccountSaveMultiRequest
{
    StorageFile = new StorageFileLocation
    {
        FileName = "email.multi.account",
        Storage = "First Storage",
        FolderPath = "file/location/folder/on/storage"
    },
    Value = new EmailClientMultiAccount
    {
        ReceiveAccounts = new List<EmailClientAccount>
        {
            new EmailClientAccount
            {
                Host = "imap.gmail.com",
                Port = 993,
                SecurityOptions = "SSLAuto",
                Credentials = new EmailClientAccountPasswordCredentials
                {
                    Password = "password",
                    Login = "example@gmail.com"
                }
            },
            new EmailClientAccount
            {
                Host = "exchange@outlook.com",
                Port = 443,
                ProtocolType = "EWS",
                Credentials = new EmailClientAccountOauthCredentials
                {
                    ClientId = "clientId",
                    ClientSecret = "clientSecret",
                    RefreshToken = "refreshToken",
                    Login = "example@outlook.com"
                }
            }
        },
        SendAccount = new EmailClientAccount
        {
            Host = "smtp.gmail.com",
            Port = 465,
            SecurityOptions = "SSLAuto",
            ProtocolType = "SMTP",
            Credentials = new EmailClientAccountPasswordCredentials
            {
                Password = "password",
                Login = "example@gmail.com"
            }
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientAccountSaveMultiRequest clientAccountSaveMultiRequest = Models.clientAccountSaveMultiRequest()
    .storageFile(Models.storageFileLocation()
        .fileName("email.multi.account")
        .storage("First Storage")
        .folderPath("file/location/folder/on/storage")
        .build())
    .value(Models.emailClientMultiAccount()
        .receiveAccounts(Arrays.<EmailClientAccount>asList(
            Models.emailClientAccount()
                .host("imap.gmail.com")
                .port(993)
                .securityOptions("SSLAuto")
                .credentials(Models.emailClientAccountPasswordCredentials()
                    .password("password")
                    .login("example@gmail.com")
                    .build())
                .build(),
            Models.emailClientAccount()
                .host("exchange@outlook.com")
                .port(443)
                .protocolType("EWS")
                .credentials(Models.emailClientAccountOauthCredentials()
                    .clientId("clientId")
                    .clientSecret("clientSecret")
                    .refreshToken("refreshToken")
                    .login("example@outlook.com")
                    .build())
                .build()))
        .sendAccount(Models.emailClientAccount()
            .host("smtp.gmail.com")
            .port(465)
            .securityOptions("SSLAuto")
            .protocolType("SMTP")
            .credentials(Models.emailClientAccountPasswordCredentials()
                .password("password")
                .login("example@gmail.com")
                .build())
            .build())
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
client_account_save_multi_request = models.ClientAccountSaveMultiRequest(
    storage_file=models.StorageFileLocation(
        file_name='email.multi.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'),
    value=models.EmailClientMultiAccount(
        receive_accounts=[
            models.EmailClientAccount(
                host='imap.gmail.com',
                port=993,
                security_options='SSLAuto',
                credentials=models.EmailClientAccountPasswordCredentials(
                    password='password',
                    login='example@gmail.com')),
            models.EmailClientAccount(
                host='exchange@outlook.com',
                port=443,
                protocol_type='EWS',
                credentials=models.EmailClientAccountOauthCredentials(
                    client_id='clientId',
                    client_secret='clientSecret',
                    refresh_token='refreshToken',
                    login='example@outlook.com'))],
        send_account=models.EmailClientAccount(
            host='smtp.gmail.com',
            port=465,
            security_options='SSLAuto',
            protocol_type='SMTP',
            credentials=models.EmailClientAccountPasswordCredentials(
                password='password',
                login='example@gmail.com'))))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
client_account_save_multi_request = ClientAccountSaveMultiRequest.new(
  storage_file: StorageFileLocation.new(
    file_name: 'email.multi.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'),
  value: EmailClientMultiAccount.new(
    receive_accounts: [
      EmailClientAccount.new(
        host: 'imap.gmail.com',
        port: 993,
        security_options: 'SSLAuto',
        credentials: EmailClientAccountPasswordCredentials.new(
          password: 'password',
          login: 'example@gmail.com')),
      EmailClientAccount.new(
        host: 'exchange@outlook.com',
        port: 443,
        protocol_type: 'EWS',
        credentials: EmailClientAccountOauthCredentials.new(
          client_id: 'clientId',
          client_secret: 'clientSecret',
          refresh_token: 'refreshToken',
          login: 'example@outlook.com'))],
    send_account: EmailClientAccount.new(
      host: 'smtp.gmail.com',
      port: 465,
      security_options: 'SSLAuto',
      protocol_type: 'SMTP',
      credentials: EmailClientAccountPasswordCredentials.new(
        password: 'password',
        login: 'example@gmail.com'))))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let clientAccountSaveMultiRequest = Models.clientAccountSaveMultiRequest()
    .storageFile(Models.storageFileLocation()
        .fileName('email.multi.account')
        .storage('First Storage')
        .folderPath('file/location/folder/on/storage')
        .build())
    .value(Models.emailClientMultiAccount()
        .receiveAccounts([
            Models.emailClientAccount()
                .host('imap.gmail.com')
                .port(993)
                .securityOptions('SSLAuto')
                .credentials(Models.emailClientAccountPasswordCredentials()
                    .password('password')
                    .login('example@gmail.com')
                    .build())
                .build(),
            Models.emailClientAccount()
                .host('exchange@outlook.com')
                .port(443)
                .protocolType('EWS')
                .credentials(Models.emailClientAccountOauthCredentials()
                    .clientId('clientId')
                    .clientSecret('clientSecret')
                    .refreshToken('refreshToken')
                    .login('example@outlook.com')
                    .build())
                .build()])
        .sendAccount(Models.emailClientAccount()
            .host('smtp.gmail.com')
            .port(465)
            .securityOptions('SSLAuto')
            .protocolType('SMTP')
            .credentials(Models.emailClientAccountPasswordCredentials()
                .password('password')
                .login('example@gmail.com')
                .build())
            .build())
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$clientAccountSaveMultiRequest = Models::clientAccountSaveMultiRequest()
    ->storageFile(Models::storageFileLocation()
        ->fileName('email.multi.account')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
    ->value(Models::emailClientMultiAccount()
        ->receiveAccounts(array(
            Models::emailClientAccount()
                ->host('imap.gmail.com')
                ->port(993)
                ->securityOptions('SSLAuto')
                ->credentials(Models::emailClientAccountPasswordCredentials()
                    ->password('password')
                    ->login('example@gmail.com')
                    ->build())
                ->build(),
            Models::emailClientAccount()
                ->host('exchange@outlook.com')
                ->port(443)
                ->protocolType('EWS')
                ->credentials(Models::emailClientAccountOauthCredentials()
                    ->clientId('clientId')
                    ->clientSecret('clientSecret')
                    ->refreshToken('refreshToken')
                    ->login('example@outlook.com')
                    ->build())
                ->build()))
        ->sendAccount(Models::emailClientAccount()
            ->host('smtp.gmail.com')
            ->port(465)
            ->securityOptions('SSLAuto')
            ->protocolType('SMTP')
            ->credentials(Models::emailClientAccountPasswordCredentials()
                ->password('password')
                ->login('example@gmail.com')
                ->build())
            ->build())
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

