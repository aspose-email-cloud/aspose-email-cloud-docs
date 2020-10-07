---
title: "MonthlyRecurrencePatternDto"
type: docs
url: /reference-model-monthly-recurrence-pattern-dto/
weight: 1
---
Monthly recurrence pattern.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**StartDay** | **string** | Represents the day of the week. Enum, available values: None, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday, Day, WeekDay, WeekendDay | 
**StartOffset** | **int?** | Start offset.              | 
**StartPosition** | **string** | Day positions, typically found in a month. Enum, available values: None, First, Second, Third, Fourth, Last | 

Parent class: [RecurrencePatternDto](/email/reference-model-recurrence-pattern-dto/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="monthly_recurrence_pattern_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var monthlyRecurrencePatternDto = new MonthlyRecurrencePatternDto
{
    StartDay = "Monday",
    StartPosition = "First",
    Interval = -1,
    WeekStart = "Monday"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MonthlyRecurrencePatternDto monthlyRecurrencePatternDto = Models.monthlyRecurrencePatternDto()
    .startDay("Monday")
    .startPosition("First")
    .interval(-1)
    .weekStart("Monday")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
monthly_recurrence_pattern_dto = models.MonthlyRecurrencePatternDto(
    start_day='Monday',
    start_position='First',
    interval=-1,
    week_start='Monday')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
monthly_recurrence_pattern_dto = MonthlyRecurrencePatternDto.new(
  start_day: 'Monday',
  start_position: 'First',
  interval: -1,
  week_start: 'Monday')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let monthlyRecurrencePatternDto = Models.monthlyRecurrencePatternDto()
    .startDay('Monday')
    .startPosition('First')
    .interval(-1)
    .weekStart('Monday')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$monthlyRecurrencePatternDto = Models::monthlyRecurrencePatternDto()
    ->startDay('Monday')
    ->startPosition('First')
    ->interval(-1)
    ->weekStart('Monday')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

