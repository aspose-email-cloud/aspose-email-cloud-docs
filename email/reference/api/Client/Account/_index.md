---
title: "Account"
type: docs
url: /reference-client-account-api/
weight: 1
---

Email server account for built-in client operations.

## Get

Get email client account from storage.             

Returns [**EmailClientAccount**](/email/reference-model-email-client-account/) model.

{{< tabs tabTotal="6" tabID="client_account_get_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Client.Account.GetAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailClientAccount result = api.client().account().get(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.client.account.get(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.client.account.get(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.client.account.get(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->client()->account()->get($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: Get method request.

Type: [**ClientAccountGetRequest**](/email/reference-model-client-account-get-request/).

{{< tabs tabTotal="6" tabID="client_account_get_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientAccountGetRequest
{ 
    FileName = "email.account",
    Folder = "email/account/location/on/storage",
    Storage = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientAccountGetRequest request = Models.clientAccountGetRequest()
    .fileName("email.account")
    .folder("email/account/location/on/storage")
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientAccountGetRequest(
    file_name='email.account',
    folder='email/account/location/on/storage',
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientAccountGetRequest.new(
    file_name: 'email.account',
    folder: 'email/account/location/on/storage',
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ClientAccountGetRequest()
    .fileName('email.account')
    .folder('email/account/location/on/storage')
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ClientAccountGetRequest()
    ->file_name('email.account')
    ->folder('email/account/location/on/storage')
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## GetMulti

Get email client multi account file (*.multi.account). Will respond error if file extension is not \".multi.account\".             

Returns [**EmailClientMultiAccount**](/email/reference-model-email-client-multi-account/) model.

{{< tabs tabTotal="6" tabID="client_account_get_multi_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Client.Account.GetMultiAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailClientMultiAccount result = api.client().account().getMulti(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.client.account.get_multi(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.client.account.get_multi(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.client.account.getMulti(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->client()->account()->getMulti($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: GetMulti method request.

Type: [**ClientAccountGetMultiRequest**](/email/reference-model-client-account-get-multi-request/).

{{< tabs tabTotal="6" tabID="client_account_get_multi_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientAccountGetMultiRequest
{ 
    FileName = "email.multi.account",
    Folder = "email/account/location/on/storage",
    Storage = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientAccountGetMultiRequest request = Models.clientAccountGetMultiRequest()
    .fileName("email.multi.account")
    .folder("email/account/location/on/storage")
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientAccountGetMultiRequest(
    file_name='email.multi.account',
    folder='email/account/location/on/storage',
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientAccountGetMultiRequest.new(
    file_name: 'email.multi.account',
    folder: 'email/account/location/on/storage',
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ClientAccountGetMultiRequest()
    .fileName('email.multi.account')
    .folder('email/account/location/on/storage')
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ClientAccountGetMultiRequest()
    ->file_name('email.multi.account')
    ->folder('email/account/location/on/storage')
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## Save

Create/update email client account file (*.account) with credentials             

{{< tabs tabTotal="6" tabID="client_account_save_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Client.Account.SaveAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.client().account().save(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.client.account.save(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.client.account.save(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.client.account.save(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->client()->account()->save($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: Email account information

Type: [**ClientAccountSaveRequest**](/email/reference-model-client-account-save-request/).

{{< tabs tabTotal="6" tabID="client_account_save_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientAccountSaveRequest
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
ClientAccountSaveRequest request = Models.clientAccountSaveRequest()
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
request = models.ClientAccountSaveRequest(
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
request = ClientAccountSaveRequest.new(
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
let request = Models.clientAccountSaveRequest()
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
$request = Models::clientAccountSaveRequest()
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

{{< /expand-list >}}
## SaveMulti

Create email client multi account file (*.multi.account). Will respond error if file extension is not \".multi.account\".             

{{< tabs tabTotal="6" tabID="client_account_save_multi_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Client.Account.SaveMultiAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.client().account().saveMulti(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.client.account.save_multi(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.client.account.save_multi(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.client.account.saveMulti(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->client()->account()->saveMulti($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: Email accounts information.

Type: [**ClientAccountSaveMultiRequest**](/email/reference-model-client-account-save-multi-request/).

{{< tabs tabTotal="6" tabID="client_account_save_multi_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientAccountSaveMultiRequest
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
ClientAccountSaveMultiRequest request = Models.clientAccountSaveMultiRequest()
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
request = models.ClientAccountSaveMultiRequest(
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
request = ClientAccountSaveMultiRequest.new(
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
let request = Models.clientAccountSaveMultiRequest()
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
$request = Models::clientAccountSaveMultiRequest()
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

## More APIs
See more APIs:
{{< list-of-articles-in-this-section >}}
