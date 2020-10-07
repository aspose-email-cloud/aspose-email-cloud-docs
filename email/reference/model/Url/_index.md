---
title: "Url"
type: docs
url: /reference-model-url/
weight: 1
---
Url and its category.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Category** | [**EnumWithCustomOfUrlCategory**](/email/reference-model-enum-with-custom-of-url-category/) | Url category.              | [optional] 
**Preferred** | **bool?** | Defines whether url is preferred.              | 
**Href** | **string** | URL.              | [optional] 


{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="url_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var url = new Url
{
    Category = new EnumWithCustomOfUrlCategory
    {
        Value = "Work"
    },
    Preferred = true,
    Href = "https://products.aspose.cloud/email"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
Url url = Models.url()
    .category(Models.enumWithCustomOfUrlCategory()
        .value("Work")
        .build())
    .preferred(true)
    .href("https://products.aspose.cloud/email")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
url = models.Url(
    category=models.EnumWithCustomOfUrlCategory(
        value='Work'),
    preferred=True,
    href='https://products.aspose.cloud/email')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
url = Url.new(
  category: EnumWithCustomOfUrlCategory.new(
    value: 'Work'),
  preferred: true,
  href: 'https://products.aspose.cloud/email')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let url = Models.url()
    .category(Models.enumWithCustomOfUrlCategory()
        .value('Work')
        .build())
    .preferred(true)
    .href('https://products.aspose.cloud/email')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$url = Models::url()
    ->category(Models::enumWithCustomOfUrlCategory()
        ->value('Work')
        ->build())
    ->preferred(true)
    ->href('https://products.aspose.cloud/email')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

