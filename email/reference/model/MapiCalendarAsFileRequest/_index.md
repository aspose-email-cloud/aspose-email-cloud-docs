---
title: "MapiCalendarAsFileRequest"
type: docs
url: /reference-model-mapi-calendar-as-file-request/
weight: 1
---
Convert MapiCalendar to file request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Format** | **string** | Calendar file format./nEnum, available values: Ics, Msg | 
**Value** | [**MapiCalendarDto**](/email/reference-model-mapi-calendar-dto/) | MAPI calendar model.              | 


## Example

{{< tabs tabTotal="6" tabID="mapi_calendar_as_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var mapiCalendarAsFileRequest = new MapiCalendarAsFileRequest
{
    Format = "Msg",
    Value = new MapiCalendarDto
    {
        Attendees = new MapiCalendarAttendeesDto
        {
            AppointmentRecipients = new List<MapiRecipientDto>
            {
                new MapiRecipientDto
                {
                    EmailAddress = "organizer@aspose.com",
                    AddressType = "SMTP",
                    DisplayName = "Organizer Name",
                    RecipientType = "MapiTo"
                },
                new MapiRecipientDto
                {
                    EmailAddress = "attendee@aspose.com",
                    AddressType = "SMTP",
                    DisplayName = "Attendee Name",
                    RecipientType = "MapiTo"
                }
            }
        },
        BusyStatus = "Tentative",
        ClientIntent = new List<MapiCalendarClientIntent>
        {
            "Manager"
        },
        EndDate = DateTime.Today,
        Location = "Some location",
        Recurrence = new MapiCalendarEventRecurrenceDto
        {
            RecurrencePattern = new MapiCalendarDailyRecurrencePatternDto
            {
                Frequency = "Daily",
                OccurrenceCount = 10,
                WeekStartDay = "Monday"
            }
        },
        StartDate = DateTime.Today,
        Organizer = new MapiElectronicAddressDto
        {
            EmailAddress = "organizer@aspose.com"
        },
        Body = "Some description",
        Subject = "Some summary"
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiCalendarAsFileRequest mapiCalendarAsFileRequest = Models.mapiCalendarAsFileRequest()
    .format("Msg")
    .value(Models.mapiCalendarDto()
        .attendees(Models.mapiCalendarAttendeesDto()
            .appointmentRecipients(Arrays.<MapiRecipientDto>asList(
                Models.mapiRecipientDto()
                    .emailAddress("organizer@aspose.com")
                    .addressType("SMTP")
                    .displayName("Organizer Name")
                    .recipientType("MapiTo")
                    .build(),
                Models.mapiRecipientDto()
                    .emailAddress("attendee@aspose.com")
                    .addressType("SMTP")
                    .displayName("Attendee Name")
                    .recipientType("MapiTo")
                    .build()))
            .build())
        .busyStatus("Tentative")
        .clientIntent(Arrays.<MapiCalendarClientIntent>asList(
            "Manager"))
        .endDate(Calendar.getInstance().getTime())
        .location("Some location")
        .recurrence(Models.mapiCalendarEventRecurrenceDto()
            .recurrencePattern(Models.mapiCalendarDailyRecurrencePatternDto()
                .frequency("Daily")
                .occurrenceCount(10)
                .weekStartDay("Monday")
                .build())
            .build())
        .startDate(Calendar.getInstance().getTime())
        .organizer(Models.mapiElectronicAddressDto()
            .emailAddress("organizer@aspose.com")
            .build())
        .body("Some description")
        .subject("Some summary")
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
mapi_calendar_as_file_request = models.MapiCalendarAsFileRequest(
    format='Msg',
    value=models.MapiCalendarDto(
        attendees=models.MapiCalendarAttendeesDto(
            appointment_recipients=[
                models.MapiRecipientDto(
                    email_address='organizer@aspose.com',
                    address_type='SMTP',
                    display_name='Organizer Name',
                    recipient_type='MapiTo'),
                models.MapiRecipientDto(
                    email_address='attendee@aspose.com',
                    address_type='SMTP',
                    display_name='Attendee Name',
                    recipient_type='MapiTo')]),
        busy_status='Tentative',
        client_intent=[
            'Manager'],
        end_date=datetime.today(),
        location='Some location',
        recurrence=models.MapiCalendarEventRecurrenceDto(
            recurrence_pattern=models.MapiCalendarDailyRecurrencePatternDto(
                frequency='Daily',
                occurrence_count=10,
                week_start_day='Monday')),
        start_date=datetime.today(),
        organizer=models.MapiElectronicAddressDto(
            email_address='organizer@aspose.com'),
        body='Some description',
        subject='Some summary'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
mapi_calendar_as_file_request = MapiCalendarAsFileRequest.new(
  format: 'Msg',
  value: MapiCalendarDto.new(
    attendees: MapiCalendarAttendeesDto.new(
      appointment_recipients: [
        MapiRecipientDto.new(
          email_address: 'organizer@aspose.com',
          address_type: 'SMTP',
          display_name: 'Organizer Name',
          recipient_type: 'MapiTo'),
        MapiRecipientDto.new(
          email_address: 'attendee@aspose.com',
          address_type: 'SMTP',
          display_name: 'Attendee Name',
          recipient_type: 'MapiTo')]),
    busy_status: 'Tentative',
    client_intent: [
      'Manager'],
    end_date: DateTime.now,
    location: 'Some location',
    recurrence: MapiCalendarEventRecurrenceDto.new(
      recurrence_pattern: MapiCalendarDailyRecurrencePatternDto.new(
        frequency: 'Daily',
        occurrence_count: 10,
        week_start_day: 'Monday')),
    start_date: DateTime.now,
    organizer: MapiElectronicAddressDto.new(
      email_address: 'organizer@aspose.com'),
    body: 'Some description',
    subject: 'Some summary'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let mapiCalendarAsFileRequest = Models.mapiCalendarAsFileRequest()
    .format('Msg')
    .value(Models.mapiCalendarDto()
        .attendees(Models.mapiCalendarAttendeesDto()
            .appointmentRecipients([
                Models.mapiRecipientDto()
                    .emailAddress('organizer@aspose.com')
                    .addressType('SMTP')
                    .displayName('Organizer Name')
                    .recipientType('MapiTo')
                    .build(),
                Models.mapiRecipientDto()
                    .emailAddress('attendee@aspose.com')
                    .addressType('SMTP')
                    .displayName('Attendee Name')
                    .recipientType('MapiTo')
                    .build()])
            .build())
        .busyStatus('Tentative')
        .clientIntent([
            'Manager'])
        .endDate(new Date())
        .location('Some location')
        .recurrence(Models.mapiCalendarEventRecurrenceDto()
            .recurrencePattern(Models.mapiCalendarDailyRecurrencePatternDto()
                .frequency('Daily')
                .occurrenceCount(10)
                .weekStartDay('Monday')
                .build())
            .build())
        .startDate(new Date())
        .organizer(Models.mapiElectronicAddressDto()
            .emailAddress('organizer@aspose.com')
            .build())
        .body('Some description')
        .subject('Some summary')
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mapiCalendarAsFileRequest = Models::mapiCalendarAsFileRequest()
    ->format('Msg')
    ->value(Models::mapiCalendarDto()
        ->attendees(Models::mapiCalendarAttendeesDto()
            ->appointmentRecipients(array(
                Models::mapiRecipientDto()
                    ->emailAddress('organizer@aspose.com')
                    ->addressType('SMTP')
                    ->displayName('Organizer Name')
                    ->recipientType('MapiTo')
                    ->build(),
                Models::mapiRecipientDto()
                    ->emailAddress('attendee@aspose.com')
                    ->addressType('SMTP')
                    ->displayName('Attendee Name')
                    ->recipientType('MapiTo')
                    ->build()))
            ->build())
        ->busyStatus('Tentative')
        ->clientIntent(array(
            'Manager'))
        ->endDate(new DateTime())
        ->location('Some location')
        ->recurrence(Models::mapiCalendarEventRecurrenceDto()
            ->recurrencePattern(Models::mapiCalendarDailyRecurrencePatternDto()
                ->frequency('Daily')
                ->occurrenceCount(10)
                ->weekStartDay('Monday')
                ->build())
            ->build())
        ->startDate(new DateTime())
        ->organizer(Models::mapiElectronicAddressDto()
            ->emailAddress('organizer@aspose.com')
            ->build())
        ->body('Some description')
        ->subject('Some summary')
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

