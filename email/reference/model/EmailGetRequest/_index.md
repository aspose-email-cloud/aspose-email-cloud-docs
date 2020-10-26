---
title: "EmailGetRequest"
type: docs
url: /reference-model-email-get-request/
weight: 2
---

Request model for [EmailCloud.Email.Get](/email/reference-email-api/#get) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**format** |**string**|Email document format. Enum, available values: Eml, Msg, MsgUnicode, Mhtml, Html, Tnef, Oft |
**fileName** |**string**|Email document file name. |
**folder** |**string**|Path to folder in storage. |[optional] 
**storage** |**string**|Storage name. |[optional] 

## Example

{{< tabs tabTotal="6" tabID="email_get_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailGetRequest
{ 
    Format = "Eml",
    FileName = "email.eml",
    Folder = "folder/on/storage",
    Storage = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailGetRequest request = Models.emailGetRequest()
    .format("Eml")
    .fileName("email.eml")
    .folder("folder/on/storage")
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.EmailGetRequest(
    format='Eml',
    file_name='email.eml',
    folder='folder/on/storage',
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = EmailGetRequest.new(
    format: 'Eml',
    file_name: 'email.eml',
    folder: 'folder/on/storage',
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.EmailGetRequest()
    .format('Eml')
    .fileName('email.eml')
    .folder('folder/on/storage')
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::EmailGetRequest()
    ->format('Eml')
    ->file_name('email.eml')
    ->folder('folder/on/storage')
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

