---
title: "ClientAccountGetMultiRequest"
type: docs
url: /reference-model-client-account-get-multi-request/
weight: 2
---

Request model for [EmailCloud.Client.Account.GetMulti](/email/reference-client-account-api/#getmulti) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**fileName** |**string**|File name on storage |
**folder** |**string**|Folder on storage |[optional] 
**storage** |**string**|Storage name |[optional] 

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="client_account_get_multi_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

