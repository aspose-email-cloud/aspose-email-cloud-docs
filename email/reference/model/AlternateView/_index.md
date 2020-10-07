---
title: "AlternateView"
type: docs
url: /reference-model-alternate-view/
weight: 1
---
Represents the format to view a message.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**BaseUri** | **string** | Base URI.              | [optional] 
**LinkedResources** | [**List&lt;LinkedResource&gt;**](/email/reference-model-linked-resource/) | Embedded resources referred to by this alternate view.              | [optional] 

Parent class: [AttachmentBase](/email/reference-model-attachment-base/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="alternate_view_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var alternateView = new AlternateView
{
    Base64Data = "<File content represented as Base64 string>",
    ContentId = "fa7a8948-4af1-432a-b4d9-ee0c28542e75",
    ContentType = new ContentType
    {
        CharSet = "utf-8",
        MediaType = "text/calendar",
        Name = "meeting.ics",
        Parameters = new List<ContentTypeParameter>
        {
            new ContentTypeParameter
            {
                Name = "Method",
                Value = "REQUEST"
            },
            new ContentTypeParameter
            {
                Name = "Name",
                Value = "meeting.ics"
            },
            new ContentTypeParameter
            {
                Name = "charset",
                Value = "utf-8"
            }
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AlternateView alternateView = Models.alternateView()
    .base64Data("<File content represented as Base64 string>")
    .contentId("fa7a8948-4af1-432a-b4d9-ee0c28542e75")
    .contentType(Models.contentType()
        .charSet("utf-8")
        .mediaType("text/calendar")
        .name("meeting.ics")
        .parameters(Arrays.<ContentTypeParameter>asList(
            Models.contentTypeParameter()
                .name("Method")
                .value("REQUEST")
                .build(),
            Models.contentTypeParameter()
                .name("Name")
                .value("meeting.ics")
                .build(),
            Models.contentTypeParameter()
                .name("charset")
                .value("utf-8")
                .build()))
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
alternate_view = models.AlternateView(
    base64_data='<File content represented as Base64 string>',
    content_id='fa7a8948-4af1-432a-b4d9-ee0c28542e75',
    content_type=models.ContentType(
        char_set='utf-8',
        media_type='text/calendar',
        name='meeting.ics',
        parameters=[
            models.ContentTypeParameter(
                name='Method',
                value='REQUEST'),
            models.ContentTypeParameter(
                name='Name',
                value='meeting.ics'),
            models.ContentTypeParameter(
                name='charset',
                value='utf-8')]))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
alternate_view = AlternateView.new(
  base64_data: '<File content represented as Base64 string>',
  content_id: 'fa7a8948-4af1-432a-b4d9-ee0c28542e75',
  content_type: ContentType.new(
    char_set: 'utf-8',
    media_type: 'text/calendar',
    name: 'meeting.ics',
    parameters: [
      ContentTypeParameter.new(
        name: 'Method',
        value: 'REQUEST'),
      ContentTypeParameter.new(
        name: 'Name',
        value: 'meeting.ics'),
      ContentTypeParameter.new(
        name: 'charset',
        value: 'utf-8')]))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let alternateView = Models.alternateView()
    .base64Data('<File content represented as Base64 string>')
    .contentId('fa7a8948-4af1-432a-b4d9-ee0c28542e75')
    .contentType(Models.contentType()
        .charSet('utf-8')
        .mediaType('text/calendar')
        .name('meeting.ics')
        .parameters([
            Models.contentTypeParameter()
                .name('Method')
                .value('REQUEST')
                .build(),
            Models.contentTypeParameter()
                .name('Name')
                .value('meeting.ics')
                .build(),
            Models.contentTypeParameter()
                .name('charset')
                .value('utf-8')
                .build()])
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$alternateView = Models::alternateView()
    ->base64Data('<File content represented as Base64 string>')
    ->contentId('fa7a8948-4af1-432a-b4d9-ee0c28542e75')
    ->contentType(Models::contentType()
        ->charSet('utf-8')
        ->mediaType('text/calendar')
        ->name('meeting.ics')
        ->parameters(array(
            Models::contentTypeParameter()
                ->name('Method')
                ->value('REQUEST')
                ->build(),
            Models::contentTypeParameter()
                ->name('Name')
                ->value('meeting.ics')
                ->build(),
            Models::contentTypeParameter()
                ->name('charset')
                ->value('utf-8')
                ->build()))
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

