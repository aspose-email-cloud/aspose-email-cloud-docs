---
title: "Aspose.Email Cloud 20.12 Release Notes"
type: docs
url: /aspose-email-cloud-20-12-release-notes/
weight: 90
---

## **SDK Changes**

EmailCloud constructor parameters renamed:
- `AppKey` is now `ClientSecret`.
- `AppSid` is now `ClientId`.

See examples below:

{{< tabs tabTotal="6" tabID="11" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var clientSecret = "Your Client secret";
var clientId = "Your Client id";
var api = new EmailCloud(clientSecret, clientId);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
String clientSecret = "Your Client secret";
String clientId = "Your Client id";
EmailCloud api = new EmailCloud(clientSecret, clientId);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api = EmailCloud(client_secret="Your Client secret", client_id="Your Client id")
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
@api = EmailCloud.new('client_secret', 'client_id')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
var api = new EmailCloud('clientId', 'clientSecret');
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$configuration = new Configuration();
$configuration
	->setClientSecret("clientSecret")
	->setClientId("clientId");
$api = new EmailCloud($configuration);
```

{{< /tab >}}

{{< /tabs >}}

## **Documentation improvements**

- SDK reference documentation improved:
  - More documentation provided for some API groups, APIs and methods.
  - Added extra links to end of documents to simplify navigation.

See [**updated documentation**](/email/reference-api/).