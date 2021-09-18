---
title: "CalendarAsFileRequest"
type: docs
url: /reference-model-calendar-as-file-request/
weight: 1
---
iCalendar model to file request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Format** | **string** | Calendar file format. Enum, available values: Ics, Msg | 
**Value** | [**CalendarDto**](/email/reference-model-calendar-dto/) | iCalendar model              | 


## Example

{{< tabs tabTotal="6" tabID="calendar_as_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var calendarAsFileRequest = new CalendarAsFileRequest
{
    Value = new CalendarDto
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
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarAsFileRequest calendarAsFileRequest = Models.calendarAsFileRequest()
    .value(Models.calendarDto()
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
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
calendar_as_file_request = models.CalendarAsFileRequest(
    value=models.CalendarDto(
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
        summary='Some summary'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
calendar_as_file_request = CalendarAsFileRequest.new(
  value: CalendarDto.new(
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
    summary: 'Some summary'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let calendarAsFileRequest = Models.calendarAsFileRequest()
    .value(Models.calendarDto()
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
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$calendarAsFileRequest = Models::calendarAsFileRequest()
    ->value(Models::calendarDto()
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
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

