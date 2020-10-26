---
title: "AiNameParseEmailAddressRequest"
type: docs
url: /reference-model-ai-name-parse-email-address-request/
weight: 2
---

Request model for [EmailCloud.Ai.Name.ParseEmailAddress](/email/reference-ai-name-api/#parseemailaddress) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**emailAddress** |**string**|Email address to parse. |
**language** |**string**|An ISO-639 code of the language; either 639-1 or 639-3 (e.g. \"it\" or \"ita\" for Italian).              |[optional] 
**location** |**string**|A geographic code such as an ISO-3166 two letter country code, for example \"FR\" for France.              |[optional] 
**encoding** |**string**|A character encoding name. |[optional] 
**script** |**string**|A writing system code; starts with the ISO-15924 script name. |[optional] 
**style** |**string**|Name writing style. Enum, available values: Formal, Informal, Legal, Academic |[optional] [default to 0]

## Example

{{< tabs tabTotal="6" tabID="ai_name_parse_email_address_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiNameParseEmailAddressRequest
{ 
    EmailAddress = "john-cane@gmail.com"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameParseEmailAddressRequest request = Models.aiNameParseEmailAddressRequest()
    .emailAddress("john-cane@gmail.com")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.AiNameParseEmailAddressRequest(
    email_address='john-cane@gmail.com')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = AiNameParseEmailAddressRequest.new(
    email_address: 'john-cane@gmail.com')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.AiNameParseEmailAddressRequest()
    .emailAddress('john-cane@gmail.com')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::AiNameParseEmailAddressRequest()
    ->email_address('john-cane@gmail.com')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

