---
title: "ClientMessageMoveRequest"
type: docs
url: /reference-model-client-message-move-request/
weight: 1
---
Email client move message request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**SourceFolder** | **string** | Folder to move message from.              | [optional] 
**DestinationFolder** | **string** | Folder to move message to.              | 

Parent class: [ClientMessageBaseRequest](/email/reference-model-client-message-base-request/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="client_message_move_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var clientMessageMoveRequest = new ClientMessageMoveRequest
{
    SourceFolder = "INBOX",
    DestinationFolder = "INBOX/SubFolder",
    MessageId = "5",
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
ClientMessageMoveRequest clientMessageMoveRequest = Models.clientMessageMoveRequest()
    .sourceFolder("INBOX")
    .destinationFolder("INBOX/SubFolder")
    .messageId("5")
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
client_message_move_request = models.ClientMessageMoveRequest(
    source_folder='INBOX',
    destination_folder='INBOX/SubFolder',
    message_id='5',
    account_location=models.StorageFileLocation(
        file_name='email.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
client_message_move_request = ClientMessageMoveRequest.new(
  source_folder: 'INBOX',
  destination_folder: 'INBOX/SubFolder',
  message_id: '5',
  account_location: StorageFileLocation.new(
    file_name: 'email.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let clientMessageMoveRequest = Models.clientMessageMoveRequest()
    .sourceFolder('INBOX')
    .destinationFolder('INBOX/SubFolder')
    .messageId('5')
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
$clientMessageMoveRequest = Models::clientMessageMoveRequest()
    ->sourceFolder('INBOX')
    ->destinationFolder('INBOX/SubFolder')
    ->messageId('5')
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

