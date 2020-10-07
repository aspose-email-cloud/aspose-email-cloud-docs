---
title: "AiBcrParseRequest"
type: docs
url: /reference-model-ai-bcr-parse-request/
weight: 2
---

Request model for [EmailCloud.Ai.Bcr.Parse](/email/reference-ai-bcr-api/#parse) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**file** |**System.IO.Stream**|File to parse |
**countries** |**string**|Comma-separated codes of countries. |[optional] 
**languages** |**string**|Comma-separated ISO-639 codes of languages (either 639-1 or 639-3; i.e. \"it\" or \"ita\" for Italian); it's \"\" by default.              |[optional] 
**isSingle** |**bool?**|Determines that image contains single VCard or more. |[optional] [default to true]

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="ai_bcr_parse_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiBcrParseRequest
{ 
    File = new MemoryStream(File.ReadAllBytes("/path/to/image.png")),
    Countries = "us",
    Languages = "en",
    IsSingle = true
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiBcrParseRequest request = Models.aiBcrParseRequest()
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/image.png")))
    .countries("us")
    .languages("en")
    .isSingle(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.AiBcrParseRequest(
    file='/path/to/image.png',
    countries='us',
    languages='en',
    is_single=True)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = AiBcrParseRequest.new(
    file: File.new('/path/to/image.png'),
    countries: 'us',
    languages: 'en',
    is_single: true)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.AiBcrParseRequest()
    .file(fs.readFileSync('/path/to/image.png'))
    .countries('us')
    .languages('en')
    .isSingle(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::AiBcrParseRequest()
    ->file(new SplFileObject('/path/to/image.png'))
    ->countries('us')
    ->languages('en')
    ->is_single(true)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

