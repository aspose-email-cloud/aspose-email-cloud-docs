---
title: "TaskRegeneratingPatternDto"
type: docs
url: /reference-model-task-regenerating-pattern-dto/
weight: 1
---
Represents the regenerating recurrence pattern that specifies how many days, weeks, months or years after the completion of the current task the next occurrence will be due.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**RegeneratingType** | **string** | Enumerates the types of regenerating pattern./nEnum, available values: Daily, Weekly, Monthly, Yearly | 

Parent class: [RecurrencePatternDto](/email/reference-model-recurrence-pattern-dto/)

## Example

{{< tabs tabTotal="6" tabID="task_regenerating_pattern_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var taskRegeneratingPatternDto = new TaskRegeneratingPatternDto
{
    Interval = 1,
    Occurs = 2,
    EndDate = DateTime.Today,
    WeekStart = "Sunday"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
TaskRegeneratingPatternDto taskRegeneratingPatternDto = Models.taskRegeneratingPatternDto()
    .interval(1)
    .occurs(2)
    .endDate(Calendar.getInstance().getTime())
    .weekStart("Sunday")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
task_regenerating_pattern_dto = models.TaskRegeneratingPatternDto(
    interval=1,
    occurs=2,
    end_date=datetime.today(),
    week_start='Sunday')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
task_regenerating_pattern_dto = TaskRegeneratingPatternDto.new(
  interval: 1,
  occurs: 2,
  end_date: DateTime.now,
  week_start: 'Sunday')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let taskRegeneratingPatternDto = Models.taskRegeneratingPatternDto()
    .interval(1)
    .occurs(2)
    .endDate(new Date())
    .weekStart('Sunday')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$taskRegeneratingPatternDto = Models::taskRegeneratingPatternDto()
    ->interval(1)
    ->occurs(2)
    ->endDate(new DateTime())
    ->weekStart('Sunday')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

