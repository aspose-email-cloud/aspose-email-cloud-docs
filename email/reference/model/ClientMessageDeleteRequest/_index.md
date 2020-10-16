---
title: "ClientMessageDeleteRequest"
type: docs
url: /reference-model-client-message-delete-request/
weight: 1
---
Email client delete message request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Folder** | **string** | Folder to delete message from.              | [optional] 

Parent class: [ClientMessageBaseRequest](/email/reference-model-client-message-base-request/)

## Example

{{< tabs tabTotal="6" tabID="client_message_delete_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var clientMessageDeleteRequest = new ClientMessageDeleteRequest
{
    Folder = "INBOX",
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
ClientMessageDeleteRequest clientMessageDeleteRequest = Models.clientMessageDeleteRequest()
    .folder("INBOX")
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
client_message_delete_request = models.ClientMessageDeleteRequest(
    folder='INBOX',
    message_id='5',
    account_location=models.StorageFileLocation(
        file_name='email.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
client_message_delete_request = ClientMessageDeleteRequest.new(
  folder: 'INBOX',
  message_id: '5',
  account_location: StorageFileLocation.new(
    file_name: 'email.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let clientMessageDeleteRequest = Models.clientMessageDeleteRequest()
    .folder('INBOX')
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
$clientMessageDeleteRequest = Models::clientMessageDeleteRequest()
    ->folder('INBOX')
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

