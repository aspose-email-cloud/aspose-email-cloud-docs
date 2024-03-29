---
title: "CalendarDto"
type: docs
url: /reference-model-calendar-dto/
weight: 1
---
iCalendar document representation.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Attachments** | [**List&lt;Attachment&gt;**](/email/reference-model-attachment/) | Document attachments. | [optional] 
**Attendees** | [**List&lt;MailAddress&gt;**](/email/reference-model-mail-address/) | Event attendees. | 
**Description** | **string** | Description. | [optional] 
**EndDate** | **DateTime?** | End date. | 
**EndTimeZone** | **string** | End time zone. | [optional] 
**Flags** | **List&lt;string&gt;** | Appointment flags. Items: Enumerates iCalendar flags. Enum, available values: None, AllDayEvent | [optional] 
**IsDescriptionHtml** | **bool?** | Indicates if description is in HTML format. | 
**Location** | **string** | Location. | 
**Method** | **string** | Defines the iCalendar object method type associated with the calendar document. Enum, available values: None, Publish, Request, Reply, Add, Cancel, Refresh, Counter, DeclineCounter | 
**MicrosoftBusyStatus** | **string** | Specifies the BUSY status. Enum, available values: NotDefined, Free, Tentative, Busy, Oof | 
**MicrosoftIntendedStatus** | **string** | Specifies the INTENDED status. Enum, available values: NotDefined, Free, Tentative, Busy, Oof | 
**OptionalAttendees** | [**List&lt;MailAddress&gt;**](/email/reference-model-mail-address/) | Optional attendees.              | [optional] 
**Organizer** | [**MailAddress**](/email/reference-model-mail-address/) | Event organizer.              | 
**RecurrenceString** | **string** | Deprecated, use &#39;Recurrence&#39; property. String representation of recurrence pattern (See iCalendar RFC, \&quot;Recurrence rule\&quot; section). For example:               For daily recurrence:         \&quot;FREQ&#x3D;DAILY;COUNT&#x3D;10;WKST&#x3D;MO\&quot;                   For monthly recurrence:         \&quot;BYSETPOS&#x3D;1;BYDAY&#x3D;MO,TU,WE,TH,FR;FREQ&#x3D;MONTHLY;INTERVAL&#x3D;10;WKST&#x3D;MO\&quot;                   For yearly recurrence:         \&quot;BYMONTHDAY&#x3D;30;BYMONTH&#x3D;1;FREQ&#x3D;YEARLY;WKST&#x3D;MO\&quot;                    | [optional] 
**Recurrence** | [**RecurrencePatternDto**](/email/reference-model-recurrence-pattern-dto/) | Recurrence pattern              | [optional] 
**Reminders** | [**List&lt;CalendarReminder&gt;**](/email/reference-model-calendar-reminder/) | Reminders. | [optional] 
**SequenceId** | **string** | The sequence id. Read only. | [optional] 
**StartDate** | **DateTime?** | Start date. | 
**StartTimeZone** | **string** | Start time zone. | [optional] 
**Status** | **string** | Defines the overall status or confirmation for the calendar document. Enum, available values: NotDefined, Cancelled, Tentative, Confirmed | 
**Summary** | **string** | Summary. | [optional] 
**Transparency** | **string** | Specifies whether or not this appointment is intended to be visible in availability searches. Enum, available values: NotDefined, Transparent, Opaque | 
**Class** | **string** | Defines the access classification for the calendar. Enum, available values: Public, Private, Confidential, NotDefined | 
**MicrosoftImportance** | **string** | Specifies the importance of a calendar object. Enum, available values: Low, Normal, High, NotDefined | 


## Example

{{< tabs tabTotal="6" tabID="calendar_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var calendarDto = new CalendarDto
{
    Attendees = new List<MailAddress>
    {
        new MailAddress
        {
            DisplayName = "Attendee Name",
            Address = "attendee@aspose.com",
            ParticipationStatus = "Accepted"
        }
    },
    Description = "Some description",
    EndDate = DateTime.Today,
    Location = "Some location",
    Organizer = new MailAddress
    {
        DisplayName = "Organizer Name",
        Address = "organizer@aspose.com"
    },
    Recurrence = new DailyRecurrencePatternDto
    {
        Interval = -1,
        Occurs = 10,
        WeekStart = "Monday"
    },
    StartDate = DateTime.Today,
    Summary = "Some summary"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarDto calendarDto = Models.calendarDto()
    .attendees(Arrays.<MailAddress>asList(
        Models.mailAddress()
            .displayName("Attendee Name")
            .address("attendee@aspose.com")
            .participationStatus("Accepted")
            .build()))
    .description("Some description")
    .endDate(Calendar.getInstance().getTime())
    .location("Some location")
    .organizer(Models.mailAddress()
        .displayName("Organizer Name")
        .address("organizer@aspose.com")
        .build())
    .recurrence(Models.dailyRecurrencePatternDto()
        .interval(-1)
        .occurs(10)
        .weekStart("Monday")
        .build())
    .startDate(Calendar.getInstance().getTime())
    .summary("Some summary")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
calendar_dto = models.CalendarDto(
    attendees=[
        models.MailAddress(
            display_name='Attendee Name',
            address='attendee@aspose.com',
            participation_status='Accepted')],
    description='Some description',
    end_date=datetime.today(),
    location='Some location',
    organizer=models.MailAddress(
        display_name='Organizer Name',
        address='organizer@aspose.com'),
    recurrence=models.DailyRecurrencePatternDto(
        interval=-1,
        occurs=10,
        week_start='Monday'),
    start_date=datetime.today(),
    summary='Some summary')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
calendar_dto = CalendarDto.new(
  attendees: [
    MailAddress.new(
      display_name: 'Attendee Name',
      address: 'attendee@aspose.com',
      participation_status: 'Accepted')],
  description: 'Some description',
  end_date: DateTime.now,
  location: 'Some location',
  organizer: MailAddress.new(
    display_name: 'Organizer Name',
    address: 'organizer@aspose.com'),
  recurrence: DailyRecurrencePatternDto.new(
    interval: -1,
    occurs: 10,
    week_start: 'Monday'),
  start_date: DateTime.now,
  summary: 'Some summary')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let calendarDto = Models.calendarDto()
    .attendees([
        Models.mailAddress()
            .displayName('Attendee Name')
            .address('attendee@aspose.com')
            .participationStatus('Accepted')
            .build()])
    .description('Some description')
    .endDate(new Date())
    .location('Some location')
    .organizer(Models.mailAddress()
        .displayName('Organizer Name')
        .address('organizer@aspose.com')
        .build())
    .recurrence(Models.dailyRecurrencePatternDto()
        .interval(-1)
        .occurs(10)
        .weekStart('Monday')
        .build())
    .startDate(new Date())
    .summary('Some summary')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$calendarDto = Models::calendarDto()
    ->attendees(array(
        Models::mailAddress()
            ->displayName('Attendee Name')
            ->address('attendee@aspose.com')
            ->participationStatus('Accepted')
            ->build()))
    ->description('Some description')
    ->endDate(new DateTime())
    ->location('Some location')
    ->organizer(Models::mailAddress()
        ->displayName('Organizer Name')
        ->address('organizer@aspose.com')
        ->build())
    ->recurrence(Models::dailyRecurrencePatternDto()
        ->interval(-1)
        ->occurs(10)
        ->weekStart('Monday')
        ->build())
    ->startDate(new DateTime())
    ->summary('Some summary')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

