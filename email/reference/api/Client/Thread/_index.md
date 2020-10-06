---
title: "Thread"
type: docs
url: /reference-client-thread-api/
weight: 1
---

Email client thread operations.

## Delete

Delete thread by id. All messages from thread will also be deleted.             

{{< tabs tabTotal="6" tabID="client_thread_delete_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Client.Thread.DeleteAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.client().thread().delete(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.client.thread.delete(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.client.thread.delete(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.client.thread.delete(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->client()->thread()->delete($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: Delete email thread request.

Type: [**ClientThreadDeleteRequest**](/email/reference-client-thread-delete-request/).

{{< tabs tabTotal="6" tabID="client_thread_delete_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientThreadDeleteRequest
{
    Folder = "INBOX/SubFolder",
    ThreadId = "5",
    AccountLocation = new StorageFileLocation
    {
        FileName = "email.account",
        Storage = "First Storage",
        FolderPath = "file/location/folder/on/storage"
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientThreadDeleteRequest request = Models.clientThreadDeleteRequest()
    .folder("INBOX/SubFolder")
    .threadId("5")
    .accountLocation(Models.storageFileLocation()
        .fileName("email.account")
        .storage("First Storage")
        .folderPath("file/location/folder/on/storage")
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientThreadDeleteRequest(
    folder='INBOX/SubFolder',
    thread_id='5',
    account_location=models.StorageFileLocation(
        file_name='email.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientThreadDeleteRequest.new(
  folder: 'INBOX/SubFolder',
  thread_id: '5',
  account_location: StorageFileLocation.new(
    file_name: 'email.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.clientThreadDeleteRequest()
    .folder('INBOX/SubFolder')
    .threadId('5')
    .accountLocation(Models.storageFileLocation()
        .fileName('email.account')
        .storage('First Storage')
        .folderPath('file/location/folder/on/storage')
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::clientThreadDeleteRequest()
    ->folder('INBOX/SubFolder')
    ->threadId('5')
    ->accountLocation(Models::storageFileLocation()
        ->fileName('email.account')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## GetList

Get message threads from folder. All messages are partly fetched (without email body and some other fields).             

Returns [**EmailThreadList**](EmailThreadList.md) model.

{{< tabs tabTotal="6" tabID="client_thread_get_list_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Client.Thread.GetListAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailThreadList result = api.client().thread().getList(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.client.thread.get_list(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.client.thread.get_list(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.client.thread.getList(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->client()->thread()->getList($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: GetList method request.

Type: [**ClientThreadGetListRequest**](/email/reference-client-thread-get-list-request/).

{{< tabs tabTotal="6" tabID="client_thread_get_list_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientThreadGetListRequest
{ 
    Folder = "INBOX/SubFolder",
    Account = "email.account",
    Storage = "First Storage",
    AccountStorageFolder = "email/account/location/on/storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientThreadGetListRequest request = Models.clientThreadGetListRequest()
    .folder("INBOX/SubFolder")
    .account("email.account")
    .storage("First Storage")
    .accountStorageFolder("email/account/location/on/storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientThreadGetListRequest(
    folder='INBOX/SubFolder',
    account='email.account',
    storage='First Storage',
    account_storage_folder='email/account/location/on/storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientThreadGetListRequest.new(
    folder: 'INBOX/SubFolder',
    account: 'email.account',
    storage: 'First Storage',
    account_storage_folder: 'email/account/location/on/storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ClientThreadGetListRequest()
    .folder('INBOX/SubFolder')
    .account('email.account')
    .storage('First Storage')
    .accountStorageFolder('email/account/location/on/storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ClientThreadGetListRequest()
    ->folder('INBOX/SubFolder')
    ->account('email.account')
    ->storage('First Storage')
    ->account_storage_folder('email/account/location/on/storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## GetMessages

Get messages from thread by id. All messages are fully fetched. For accounts with CacheFile only cached messages will be returned.             

Returns [**EmailList**](EmailList.md) model.

{{< tabs tabTotal="6" tabID="client_thread_get_messages_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Client.Thread.GetMessagesAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailList result = api.client().thread().getMessages(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.client.thread.get_messages(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.client.thread.get_messages(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.client.thread.getMessages(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->client()->thread()->getMessages($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: GetMessages method request.

Type: [**ClientThreadGetMessagesRequest**](/email/reference-client-thread-get-messages-request/).

{{< tabs tabTotal="6" tabID="client_thread_get_messages_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientThreadGetMessagesRequest
{ 
    ThreadId = "5",
    Account = "email.account",
    Folder = "INBOX",
    Storage = "First Storage",
    AccountStorageFolder = "email/account/location/on/storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientThreadGetMessagesRequest request = Models.clientThreadGetMessagesRequest()
    .threadId("5")
    .account("email.account")
    .folder("INBOX")
    .storage("First Storage")
    .accountStorageFolder("email/account/location/on/storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientThreadGetMessagesRequest(
    thread_id='5',
    account='email.account',
    folder='INBOX',
    storage='First Storage',
    account_storage_folder='email/account/location/on/storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientThreadGetMessagesRequest.new(
    thread_id: '5',
    account: 'email.account',
    folder: 'INBOX',
    storage: 'First Storage',
    account_storage_folder: 'email/account/location/on/storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ClientThreadGetMessagesRequest()
    .threadId('5')
    .account('email.account')
    .folder('INBOX')
    .storage('First Storage')
    .accountStorageFolder('email/account/location/on/storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ClientThreadGetMessagesRequest()
    ->thread_id('5')
    ->account('email.account')
    ->folder('INBOX')
    ->storage('First Storage')
    ->account_storage_folder('email/account/location/on/storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## Move

Move thread to another folder.             

{{< tabs tabTotal="6" tabID="client_thread_move_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Client.Thread.MoveAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.client().thread().move(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.client.thread.move(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.client.thread.move(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.client.thread.move(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->client()->thread()->move($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: Move thread request.

Type: [**ClientThreadMoveRequest**](/email/reference-client-thread-move-request/).

{{< tabs tabTotal="6" tabID="client_thread_move_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientThreadMoveRequest
{
    DestinationFolder = "INBOX/SubFolder",
    ThreadId = "5",
    AccountLocation = new StorageFileLocation
    {
        FileName = "email.account",
        Storage = "First Storage",
        FolderPath = "file/location/folder/on/storage"
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientThreadMoveRequest request = Models.clientThreadMoveRequest()
    .destinationFolder("INBOX/SubFolder")
    .threadId("5")
    .accountLocation(Models.storageFileLocation()
        .fileName("email.account")
        .storage("First Storage")
        .folderPath("file/location/folder/on/storage")
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientThreadMoveRequest(
    destination_folder='INBOX/SubFolder',
    thread_id='5',
    account_location=models.StorageFileLocation(
        file_name='email.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientThreadMoveRequest.new(
  destination_folder: 'INBOX/SubFolder',
  thread_id: '5',
  account_location: StorageFileLocation.new(
    file_name: 'email.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.clientThreadMoveRequest()
    .destinationFolder('INBOX/SubFolder')
    .threadId('5')
    .accountLocation(Models.storageFileLocation()
        .fileName('email.account')
        .storage('First Storage')
        .folderPath('file/location/folder/on/storage')
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::clientThreadMoveRequest()
    ->destinationFolder('INBOX/SubFolder')
    ->threadId('5')
    ->accountLocation(Models::storageFileLocation()
        ->fileName('email.account')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## SetIsRead

Mark all messages in thread as read or unread.             

{{< tabs tabTotal="6" tabID="client_thread_set_is_read_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Client.Thread.SetIsReadAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.client().thread().setIsRead(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.client.thread.set_is_read(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.client.thread.set_is_read(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.client.thread.setIsRead(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->client()->thread()->setIsRead($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: Email account specifier and IsRead flag.

Type: [**ClientThreadSetIsReadRequest**](/email/reference-client-thread-set-is-read-request/).

{{< tabs tabTotal="6" tabID="client_thread_set_is_read_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientThreadSetIsReadRequest
{
    IsRead = true,
    Folder = "INBOX",
    ThreadId = "5",
    AccountLocation = new StorageFileLocation
    {
        FileName = "email.account",
        Storage = "First Storage",
        FolderPath = "file/location/folder/on/storage"
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientThreadSetIsReadRequest request = Models.clientThreadSetIsReadRequest()
    .isRead(true)
    .folder("INBOX")
    .threadId("5")
    .accountLocation(Models.storageFileLocation()
        .fileName("email.account")
        .storage("First Storage")
        .folderPath("file/location/folder/on/storage")
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientThreadSetIsReadRequest(
    is_read=True,
    folder='INBOX',
    thread_id='5',
    account_location=models.StorageFileLocation(
        file_name='email.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientThreadSetIsReadRequest.new(
  is_read: true,
  folder: 'INBOX',
  thread_id: '5',
  account_location: StorageFileLocation.new(
    file_name: 'email.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.clientThreadSetIsReadRequest()
    .isRead(true)
    .folder('INBOX')
    .threadId('5')
    .accountLocation(Models.storageFileLocation()
        .fileName('email.account')
        .storage('First Storage')
        .folderPath('file/location/folder/on/storage')
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::clientThreadSetIsReadRequest()
    ->isRead(true)
    ->folder('INBOX')
    ->threadId('5')
    ->accountLocation(Models::storageFileLocation()
        ->fileName('email.account')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

## More APIs
See more APIs:
{{< list-of-articles-in-this-section >}}
