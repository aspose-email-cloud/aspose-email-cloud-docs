---
title: "ClientThreadMoveRequest"
type: docs
url: /reference-model-client-thread-move-request/
weight: 1
---
Email client move thread request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**DestinationFolder** | **string** | Email account folder to move thread to.              | 

Parent class: [ClientThreadBaseRequest](/email/reference-model-client-thread-base-request/)

## Example

{{< tabs tabTotal="6" tabID="client_thread_move_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var clientThreadMoveRequest = new ClientThreadMoveRequest
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
ClientThreadMoveRequest clientThreadMoveRequest = Models.clientThreadMoveRequest()
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
client_thread_move_request = models.ClientThreadMoveRequest(
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
client_thread_move_request = ClientThreadMoveRequest.new(
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
let clientThreadMoveRequest = Models.clientThreadMoveRequest()
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
$clientThreadMoveRequest = Models::clientThreadMoveRequest()
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

