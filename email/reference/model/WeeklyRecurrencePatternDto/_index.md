---
title: "WeeklyRecurrencePatternDto"
type: docs
url: /reference-model-weekly-recurrence-pattern-dto/
weight: 1
---
Weekly recurrence pattern.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**StartDays** | **List&lt;string&gt;** | Start days              Items: Represents the day of the week. Enum, available values: None, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday, Day, WeekDay, WeekendDay | [optional] 

Parent class: [RecurrencePatternDto](/email/reference-model-recurrence-pattern-dto/)

## Example

{{< tabs tabTotal="6" tabID="weekly_recurrence_pattern_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var weeklyRecurrencePatternDto = new WeeklyRecurrencePatternDto
{
    StartDays = new List<CalendarDay>
    {
        "Tuesday",
        "Thursday"
    },
    Interval = -1,
    Occurs = 10,
    WeekStart = "Sunday"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
WeeklyRecurrencePatternDto weeklyRecurrencePatternDto = Models.weeklyRecurrencePatternDto()
    .startDays(Arrays.<CalendarDay>asList(
        "Tuesday",
        "Thursday"))
    .interval(-1)
    .occurs(10)
    .weekStart("Sunday")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
weekly_recurrence_pattern_dto = models.WeeklyRecurrencePatternDto(
    start_days=[
        'Tuesday',
        'Thursday'],
    interval=-1,
    occurs=10,
    week_start='Sunday')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
weekly_recurrence_pattern_dto = WeeklyRecurrencePatternDto.new(
  start_days: [
    'Tuesday',
    'Thursday'],
  interval: -1,
  occurs: 10,
  week_start: 'Sunday')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let weeklyRecurrencePatternDto = Models.weeklyRecurrencePatternDto()
    .startDays([
        'Tuesday',
        'Thursday'])
    .interval(-1)
    .occurs(10)
    .weekStart('Sunday')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$weeklyRecurrencePatternDto = Models::weeklyRecurrencePatternDto()
    ->startDays(array(
        'Tuesday',
        'Thursday'))
    ->interval(-1)
    ->occurs(10)
    ->weekStart('Sunday')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

