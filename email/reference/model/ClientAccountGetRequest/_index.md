---
title: "ClientAccountGetRequest"
type: docs
url: /reference-model-client-account-get-request/
weight: 2
---

Request model for [EmailCloud.Client.Account.Get](/email/reference-client-account-api/#get) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**fileName** |**string**|File name on storage. |
**folder** |**string**|Folder on storage. |[optional] 
**storage** |**string**|Storage name. |[optional] 

## Example

{{< tabs tabTotal="6" tabID="client_account_get_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientAccountGetRequest
{ 
    FileName = "email.account",
    Folder = "email/account/location/on/storage",
    Storage = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientAccountGetRequest request = Models.clientAccountGetRequest()
    .fileName("email.account")
    .folder("email/account/location/on/storage")
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientAccountGetRequest(
    file_name='email.account',
    folder='email/account/location/on/storage',
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientAccountGetRequest.new(
    file_name: 'email.account',
    folder: 'email/account/location/on/storage',
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ClientAccountGetRequest()
    .fileName('email.account')
    .folder('email/account/location/on/storage')
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ClientAccountGetRequest()
    ->file_name('email.account')
    ->folder('email/account/location/on/storage')
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

