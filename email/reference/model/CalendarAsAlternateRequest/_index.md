---
title: "CalendarAsAlternateRequest"
type: docs
url: /reference-model-calendar-as-alternate-request/
weight: 1
---
Convert iCalendar to AlternateView request             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Value** | [**CalendarDto**](/email/reference-model-calendar-dto/) | iCalendar document model              | 
**Action** | **string** | iCalendar actions. Enum, available values: Create, Update, Cancel | 
**SequenceId** | **string** | iCalendar sequence id              | [optional] 


## Example

{{< tabs tabTotal="6" tabID="calendar_as_alternate_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var calendarAsAlternateRequest = new CalendarAsAlternateRequest
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
    },
    SequenceId = "cf4ffb6c-895d-4e58-bdb4-0a3918e96a43"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarAsAlternateRequest calendarAsAlternateRequest = Models.calendarAsAlternateRequest()
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
    .sequenceId("cf4ffb6c-895d-4e58-bdb4-0a3918e96a43")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
calendar_as_alternate_request = models.CalendarAsAlternateRequest(
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
        summary='Some summary'),
    sequence_id='cf4ffb6c-895d-4e58-bdb4-0a3918e96a43')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
calendar_as_alternate_request = CalendarAsAlternateRequest.new(
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
    summary: 'Some summary'),
  sequence_id: 'cf4ffb6c-895d-4e58-bdb4-0a3918e96a43')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let calendarAsAlternateRequest = Models.calendarAsAlternateRequest()
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
    .sequenceId('cf4ffb6c-895d-4e58-bdb4-0a3918e96a43')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$calendarAsAlternateRequest = Models::calendarAsAlternateRequest()
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
    ->sequenceId('cf4ffb6c-895d-4e58-bdb4-0a3918e96a43')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

