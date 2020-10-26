---
title: "RecurrencePatternDto"
type: docs
url: /reference-model-recurrence-pattern-dto/
weight: 1
---
iCalendar recurrence pattern.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Interval** | **int?** | Number of recurrence units.              | 
**Occurs** | **int?** | Number of occurrences of the recurrence pattern.              | 
**EndDate** | **DateTime?** | End date.              | 
**WeekStart** | **string** | Represents the day of the week. Enum, available values: None, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday, Day, WeekDay, WeekendDay | 
**Discriminator** | **string** |  | 


## Example

{{< tabs tabTotal="6" tabID="recurrence_pattern_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var recurrencePatternDto = new RecurrencePatternDto
{
    Interval = -1,
    WeekStart = "Monday"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
RecurrencePatternDto recurrencePatternDto = Models.recurrencePatternDto()
    .interval(-1)
    .weekStart("Monday")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
recurrence_pattern_dto = models.RecurrencePatternDto(
    interval=-1,
    week_start='Monday')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
recurrence_pattern_dto = RecurrencePatternDto.new(
  interval: -1,
  week_start: 'Monday')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let recurrencePatternDto = Models.recurrencePatternDto()
    .interval(-1)
    .weekStart('Monday')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$recurrencePatternDto = Models::recurrencePatternDto()
    ->interval(-1)
    ->weekStart('Monday')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

