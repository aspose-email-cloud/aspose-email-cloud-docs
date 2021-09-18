---
title: "YearlyRecurrencePatternDto"
type: docs
url: /reference-model-yearly-recurrence-pattern-dto/
weight: 1
---
Yearly recurrence pattern.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**StartDay** | **string** | Represents the day of the week./nEnum, available values: None, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday, Day, WeekDay, WeekendDay | 
**StartMonth** | **string** | Represents a calendar month./nEnum, available values: None, January, February, March, April, May, June, July, August, September, October, November, December | 
**StartOffset** | **int?** | Start offset.              | 
**StartPosition** | **string** | Day positions, typically found in a month./nEnum, available values: None, First, Second, Third, Fourth, Last | 

Parent class: [RecurrencePatternDto](/email/reference-model-recurrence-pattern-dto/)

## Example

{{< tabs tabTotal="6" tabID="yearly_recurrence_pattern_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var yearlyRecurrencePatternDto = new YearlyRecurrencePatternDto
{
    StartMonth = "January",
    StartOffset = 30,
    Interval = -1,
    WeekStart = "Monday"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
YearlyRecurrencePatternDto yearlyRecurrencePatternDto = Models.yearlyRecurrencePatternDto()
    .startMonth("January")
    .startOffset(30)
    .interval(-1)
    .weekStart("Monday")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
yearly_recurrence_pattern_dto = models.YearlyRecurrencePatternDto(
    start_month='January',
    start_offset=30,
    interval=-1,
    week_start='Monday')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
yearly_recurrence_pattern_dto = YearlyRecurrencePatternDto.new(
  start_month: 'January',
  start_offset: 30,
  interval: -1,
  week_start: 'Monday')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let yearlyRecurrencePatternDto = Models.yearlyRecurrencePatternDto()
    .startMonth('January')
    .startOffset(30)
    .interval(-1)
    .weekStart('Monday')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$yearlyRecurrencePatternDto = Models::yearlyRecurrencePatternDto()
    ->startMonth('January')
    ->startOffset(30)
    ->interval(-1)
    ->weekStart('Monday')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

