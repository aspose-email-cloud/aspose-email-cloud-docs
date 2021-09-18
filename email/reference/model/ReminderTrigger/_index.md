---
title: "ReminderTrigger"
type: docs
url: /reference-model-reminder-trigger/
weight: 1
---
Specifies when an alarm will trigger.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**DateTime** | **DateTime?** | A trigger set to an absolute date/time. | 
**Duration** | **long?** | Specifies a relative time in ticks for the trigger of the alarm.              | [optional] 
**Related** | **string** | Specify the relationship of the alarm trigger with respect to the start or end of the event./nEnum, available values: Start, End | 


## Example

{{< tabs tabTotal="6" tabID="reminder_trigger_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var reminderTrigger = new ReminderTrigger
{
    DateTime = DateTime.Today,
    Duration = 600000000
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ReminderTrigger reminderTrigger = Models.reminderTrigger()
    .dateTime(Calendar.getInstance().getTime())
    .duration(600000000)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
reminder_trigger = models.ReminderTrigger(
    date_time=datetime.today(),
    duration=600000000)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
reminder_trigger = ReminderTrigger.new(
  date_time: DateTime.now,
  duration: 600000000)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let reminderTrigger = Models.reminderTrigger()
    .dateTime(new Date())
    .duration(600000000)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$reminderTrigger = Models::reminderTrigger()
    ->dateTime(new DateTime())
    ->duration(600000000)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

