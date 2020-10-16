---
title: "ClientMessageSetIsReadRequest"
type: docs
url: /reference-model-client-message-set-is-read-request/
weight: 1
---
Email client mark message is read/unread request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**IsRead** | **bool?** | Message is read flag.              | 

Parent class: [ClientMessageBaseRequest](/email/reference-model-client-message-base-request/)

## Example

{{< tabs tabTotal="6" tabID="client_message_set_is_read_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var clientMessageSetIsReadRequest = new ClientMessageSetIsReadRequest
{
    IsRead = true,
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
ClientMessageSetIsReadRequest clientMessageSetIsReadRequest = Models.clientMessageSetIsReadRequest()
    .isRead(true)
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
client_message_set_is_read_request = models.ClientMessageSetIsReadRequest(
    is_read=True,
    message_id='5',
    account_location=models.StorageFileLocation(
        file_name='email.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
client_message_set_is_read_request = ClientMessageSetIsReadRequest.new(
  is_read: true,
  message_id: '5',
  account_location: StorageFileLocation.new(
    file_name: 'email.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let clientMessageSetIsReadRequest = Models.clientMessageSetIsReadRequest()
    .isRead(true)
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
$clientMessageSetIsReadRequest = Models::clientMessageSetIsReadRequest()
    ->isRead(true)
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

