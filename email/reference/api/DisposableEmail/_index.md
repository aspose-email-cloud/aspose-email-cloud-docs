---
title: "DisposableEmail"
type: docs
url: /reference-disposable-email-api/
weight: 1
---

Check email address is disposable operations

## IsDisposable

Check email address is disposable             

Returns [**ValueTOfBoolean**](/email/reference-model-value-t-of-boolean/) model.

{{< tabs tabTotal="6" tabID="disposable_email_is_disposable_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.DisposableEmail.IsDisposableAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ValueTOfBoolean result = api.disposableEmail().isDisposable(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.disposable_email.is_disposable(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.disposable_email.is_disposable(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.disposableEmail.isDisposable(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->disposableEmail()->isDisposable($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: IsDisposable method request.

Type: [**DisposableEmailIsDisposableRequest**](/email/reference-model-disposable-email-is-disposable-request/).

{{< tabs tabTotal="6" tabID="disposable_email_is_disposable_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

{{< /expand-list >}}

## More APIs
See more APIs:
{{< list-of-articles-in-this-section >}}
