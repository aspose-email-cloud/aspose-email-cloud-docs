---
title: "ClientThreadDeleteRequest"
type: docs
url: /reference-model-client-thread-delete-request/
weight: 1
---
Delete email client thread request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Folder** | **string** | Folder on email server, where thread is stored.              | [optional] 

Parent class: [ClientThreadBaseRequest](/email/reference-model-client-thread-base-request/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="client_thread_delete_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var clientThreadDeleteRequest = new ClientThreadDeleteRequest
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
ClientThreadDeleteRequest clientThreadDeleteRequest = Models.clientThreadDeleteRequest()
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
client_thread_delete_request = models.ClientThreadDeleteRequest(
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
client_thread_delete_request = ClientThreadDeleteRequest.new(
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
let clientThreadDeleteRequest = Models.clientThreadDeleteRequest()
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
$clientThreadDeleteRequest = Models::clientThreadDeleteRequest()
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

