---
title: "EmailConfigDiscoverPasswordRequest"
type: docs
url: /reference-model-email-config-discover-password-request/
weight: 1
---

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Password** | **string** | Email account password.              | 

Parent class: [DiscoverEmailConfigRequest](/email/reference-model-discover-email-config-request/)

## Example

{{< tabs tabTotal="6" tabID="email_config_discover_password_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var emailConfigDiscoverPasswordRequest = new EmailConfigDiscoverPasswordRequest
{
    Password = "password",
    Address = "example@aspose.com",
    FastProcessing = true
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailConfigDiscoverPasswordRequest emailConfigDiscoverPasswordRequest = Models.emailConfigDiscoverPasswordRequest()
    .password("password")
    .address("example@aspose.com")
    .fastProcessing(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
email_config_discover_password_request = models.EmailConfigDiscoverPasswordRequest(
    password='password',
    address='example@aspose.com',
    fast_processing=True)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
email_config_discover_password_request = EmailConfigDiscoverPasswordRequest.new(
  password: 'password',
  address: 'example@aspose.com',
  fast_processing: true)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let emailConfigDiscoverPasswordRequest = Models.emailConfigDiscoverPasswordRequest()
    .password('password')
    .address('example@aspose.com')
    .fastProcessing(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$emailConfigDiscoverPasswordRequest = Models::emailConfigDiscoverPasswordRequest()
    ->password('password')
    ->address('example@aspose.com')
    ->fastProcessing(true)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

