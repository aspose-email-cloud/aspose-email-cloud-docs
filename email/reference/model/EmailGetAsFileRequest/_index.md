---
title: "EmailGetAsFileRequest"
type: docs
url: /reference-model-email-get-as-file-request/
weight: 2
---

Request model for [EmailCloud.Email.GetAsFile](/email/reference-email-api/#getasfile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**fileName** |**string**|Email document file name |
**format** |**string**|File format Enum, available values: Eml, Msg, MsgUnicode, Mhtml, Html, Tnef, Oft |
**storage** |**string**|Storage name |[optional] 
**folder** |**string**|Path to folder in storage |[optional] 

## Example

{{< tabs tabTotal="6" tabID="email_get_as_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailGetAsFileRequest
{ 
    FileName = "email.eml",
    Format = "Mhtml",
    Storage = "First Storage",
    Folder = "folder/on/storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailGetAsFileRequest request = Models.emailGetAsFileRequest()
    .fileName("email.eml")
    .format("Mhtml")
    .storage("First Storage")
    .folder("folder/on/storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.EmailGetAsFileRequest(
    file_name='email.eml',
    format='Mhtml',
    storage='First Storage',
    folder='folder/on/storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = EmailGetAsFileRequest.new(
    file_name: 'email.eml',
    format: 'Mhtml',
    storage: 'First Storage',
    folder: 'folder/on/storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.EmailGetAsFileRequest()
    .fileName('email.eml')
    .format('Mhtml')
    .storage('First Storage')
    .folder('folder/on/storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::EmailGetAsFileRequest()
    ->file_name('email.eml')
    ->format('Mhtml')
    ->storage('First Storage')
    ->folder('folder/on/storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

