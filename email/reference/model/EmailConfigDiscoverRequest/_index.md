---
title: "EmailConfigDiscoverRequest"
type: docs
url: /reference-model-email-config-discover-request/
weight: 2
---

Request model for [EmailCloud.EmailConfig.Discover](/email/reference-email-config-api/#discover) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**address** |**string**|Email address. |
**fastProcessing** |**bool?**|Turns on fast processing. All discover systems will run in parallel. First discovered result will be returned.              |[optional] [default to false]

## Example

{{< tabs tabTotal="6" tabID="email_config_discover_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailConfigDiscoverRequest
{ 
    Address = "address@gmail.com"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailConfigDiscoverRequest request = Models.emailConfigDiscoverRequest()
    .address("address@gmail.com")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.EmailConfigDiscoverRequest(
    address='address@gmail.com')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = EmailConfigDiscoverRequest.new(
    address: 'address@gmail.com')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.EmailConfigDiscoverRequest()
    .address('address@gmail.com')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::EmailConfigDiscoverRequest()
    ->address('address@gmail.com')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

