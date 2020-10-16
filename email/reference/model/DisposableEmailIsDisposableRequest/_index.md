---
title: "DisposableEmailIsDisposableRequest"
type: docs
url: /reference-model-disposable-email-is-disposable-request/
weight: 2
---

Request model for [EmailCloud.DisposableEmail.IsDisposable](/email/reference-disposable-email-api/#isdisposable) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**address** |**string**|An email address to check |

## Example

{{< tabs tabTotal="6" tabID="disposable_email_is_disposable_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new DisposableEmailIsDisposableRequest
{ 
    Address = "example@mailcatch.com"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
DisposableEmailIsDisposableRequest request = Models.disposableEmailIsDisposableRequest()
    .address("example@mailcatch.com")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.DisposableEmailIsDisposableRequest(
    address='example@mailcatch.com')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = DisposableEmailIsDisposableRequest.new(
    address: 'example@mailcatch.com')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.DisposableEmailIsDisposableRequest()
    .address('example@mailcatch.com')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::DisposableEmailIsDisposableRequest()
    ->address('example@mailcatch.com')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

