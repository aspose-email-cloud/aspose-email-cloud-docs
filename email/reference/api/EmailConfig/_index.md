---
title: "EmailConfig"
type: docs
url: /reference-email-config-api/
weight: 1
---

Email server configuration discovery.

## Discover

Discover email accounts by email address. Does not validate discovered accounts. 
Returns [**EmailAccountConfigList**](/email/reference-model-email-account-config-list/) model. Requires:

{{< expand-list title="request" >}}

Discover method request. Type: [**EmailConfigDiscoverRequest**](/email/reference-model-email-config-discover-request/).

{{< tabs tabTotal="6" tabID="email_config_discover_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailConfigDiscoverRequest
{ 
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailConfigDiscoverRequest request = Models.emailConfigDiscoverRequest()
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.EmailConfigDiscoverRequest()
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = EmailConfigDiscoverRequest.new()
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.EmailConfigDiscoverRequest()
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::EmailConfigDiscoverRequest()
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="email_config_discover_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.EmailConfig.DiscoverAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailAccountConfigList result = api.emailConfig().discover(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.email_config.discover(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.email_config.discover(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.emailConfig.discover(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->emailConfig()->discover($request);
```

{{< /tab >}}

{{< /tabs >}}
## DiscoverOauth

Discover email accounts by email address. Validates discovered accounts using OAuth 2.0. 
Returns [**EmailAccountConfigList**](/email/reference-model-email-account-config-list/) model. Requires:

{{< expand-list title="request" >}}

Discover email configuration request. Type: [**EmailConfigDiscoverOauthRequest**](/email/reference-model-email-config-discover-oauth-request/).

{{< tabs tabTotal="6" tabID="email_config_discover_oauth_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailConfigDiscoverOauthRequest
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
EmailConfigDiscoverOauthRequest request = Models.emailConfigDiscoverOauthRequest()
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
request = models.EmailConfigDiscoverOauthRequest(
    client_id='ClientId',
    client_secret='ClientSecret',
    refresh_token='RefreshToken',
    address='example@aspose.com',
    fast_processing=True)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = EmailConfigDiscoverOauthRequest.new(
  client_id: 'ClientId',
  client_secret: 'ClientSecret',
  refresh_token: 'RefreshToken',
  address: 'example@aspose.com',
  fast_processing: true)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.emailConfigDiscoverOauthRequest()
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
$request = Models::emailConfigDiscoverOauthRequest()
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

{{< tabs tabTotal="6" tabID="email_config_discover_oauth_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.EmailConfig.DiscoverOauthAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailAccountConfigList result = api.emailConfig().discoverOauth(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.email_config.discover_oauth(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.email_config.discover_oauth(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.emailConfig.discoverOauth(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->emailConfig()->discoverOauth($request);
```

{{< /tab >}}

{{< /tabs >}}
## DiscoverPassword

Discover email accounts by email address. Validates discovered accounts using login and password. 
Returns [**EmailAccountConfigList**](/email/reference-model-email-account-config-list/) model. Requires:

{{< expand-list title="request" >}}

Discover email configuration request. Type: [**EmailConfigDiscoverPasswordRequest**](/email/reference-model-email-config-discover-password-request/).

{{< tabs tabTotal="6" tabID="email_config_discover_password_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailConfigDiscoverPasswordRequest
{
    Password = "password",
    Address = "example@aspose.com",
    FastProcessing = true
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailConfigDiscoverPasswordRequest request = Models.emailConfigDiscoverPasswordRequest()
    .password("password")
    .address("example@aspose.com")
    .fastProcessing(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.EmailConfigDiscoverPasswordRequest(
    password='password',
    address='example@aspose.com',
    fast_processing=True)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = EmailConfigDiscoverPasswordRequest.new(
  password: 'password',
  address: 'example@aspose.com',
  fast_processing: true)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.emailConfigDiscoverPasswordRequest()
    .password('password')
    .address('example@aspose.com')
    .fastProcessing(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::emailConfigDiscoverPasswordRequest()
    ->password('password')
    ->address('example@aspose.com')
    ->fastProcessing(true)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="email_config_discover_password_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.EmailConfig.DiscoverPasswordAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailAccountConfigList result = api.emailConfig().discoverPassword(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.email_config.discover_password(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.email_config.discover_password(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.emailConfig.discoverPassword(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->emailConfig()->discoverPassword($request);
```

{{< /tab >}}

{{< /tabs >}}

## More APIs

{{< list-of-articles-in-this-section >}}
