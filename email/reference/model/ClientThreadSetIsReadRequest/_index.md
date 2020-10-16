---
title: "ClientThreadSetIsReadRequest"
type: docs
url: /reference-model-client-thread-set-is-read-request/
weight: 1
---
Mark thread messages as read or unread request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**IsRead** | **bool?** | Message is read flag.              | 
**Folder** | **string** | Folder on email server, where thread is stored.              | [optional] 

Parent class: [ClientThreadBaseRequest](/email/reference-model-client-thread-base-request/)

## Example

{{< tabs tabTotal="6" tabID="client_thread_set_is_read_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var clientThreadSetIsReadRequest = new ClientThreadSetIsReadRequest
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
ClientThreadSetIsReadRequest clientThreadSetIsReadRequest = Models.clientThreadSetIsReadRequest()
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
client_thread_set_is_read_request = models.ClientThreadSetIsReadRequest(
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
client_thread_set_is_read_request = ClientThreadSetIsReadRequest.new(
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
let clientThreadSetIsReadRequest = Models.clientThreadSetIsReadRequest()
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
$clientThreadSetIsReadRequest = Models::clientThreadSetIsReadRequest()
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

