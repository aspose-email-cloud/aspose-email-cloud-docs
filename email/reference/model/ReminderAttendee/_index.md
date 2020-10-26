---
title: "ReminderAttendee"
type: docs
url: /reference-model-reminder-attendee/
weight: 1
---
Defines an \"Attendee\" within a alarm.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Address** | **string** | Contains the email address. | 


## Example

{{< tabs tabTotal="6" tabID="reminder_attendee_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var reminderAttendee = new ReminderAttendee
{
    Address = "attendee@aspose.com"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ReminderAttendee reminderAttendee = Models.reminderAttendee()
    .address("attendee@aspose.com")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
reminder_attendee = models.ReminderAttendee(
    address='attendee@aspose.com')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
reminder_attendee = ReminderAttendee.new(
  address: 'attendee@aspose.com')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let reminderAttendee = Models.reminderAttendee()
    .address('attendee@aspose.com')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$reminderAttendee = Models::reminderAttendee()
    ->address('attendee@aspose.com')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

