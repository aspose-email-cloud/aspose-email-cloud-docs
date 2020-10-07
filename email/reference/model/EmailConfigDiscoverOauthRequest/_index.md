---
title: "EmailConfigDiscoverOauthRequest"
type: docs
url: /reference-model-email-config-discover-oauth-request/
weight: 1
---

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**ClientId** | **string** | OAuth client id.              | 
**ClientSecret** | **string** | OAuth client secret.              | 
**RefreshToken** | **string** | OAuth refresh token.              | 
**RequestUrl** | **string** | The url to obtain access token. If not specified, will be discovered from email configuration.              | [optional] 

Parent class: [DiscoverEmailConfigRequest](/email/reference-model-discover-email-config-request/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="email_config_discover_oauth_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var emailConfigDiscoverOauthRequest = new EmailConfigDiscoverOauthRequest
{
    ClientId = "ClientId",
    ClientSecret = "ClientSecret",
    RefreshToken = "RefreshToken",
    Address = "example@aspose.com",
    FastProcessing = true
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailConfigDiscoverOauthRequest emailConfigDiscoverOauthRequest = Models.emailConfigDiscoverOauthRequest()
    .clientId("ClientId")
    .clientSecret("ClientSecret")
    .refreshToken("RefreshToken")
    .address("example@aspose.com")
    .fastProcessing(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
email_config_discover_oauth_request = models.EmailConfigDiscoverOauthRequest(
    client_id='ClientId',
    client_secret='ClientSecret',
    refresh_token='RefreshToken',
    address='example@aspose.com',
    fast_processing=True)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
email_config_discover_oauth_request = EmailConfigDiscoverOauthRequest.new(
  client_id: 'ClientId',
  client_secret: 'ClientSecret',
  refresh_token: 'RefreshToken',
  address: 'example@aspose.com',
  fast_processing: true)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let emailConfigDiscoverOauthRequest = Models.emailConfigDiscoverOauthRequest()
    .clientId('ClientId')
    .clientSecret('ClientSecret')
    .refreshToken('RefreshToken')
    .address('example@aspose.com')
    .fastProcessing(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$emailConfigDiscoverOauthRequest = Models::emailConfigDiscoverOauthRequest()
    ->clientId('ClientId')
    ->clientSecret('ClientSecret')
    ->refreshToken('RefreshToken')
    ->address('example@aspose.com')
    ->fastProcessing(true)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

