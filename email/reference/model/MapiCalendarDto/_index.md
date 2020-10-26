---
title: "MapiCalendarDto"
type: docs
url: /reference-model-mapi-calendar-dto/
weight: 1
---
Represents the mapi calendar object             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**AppointmentCounterProposal** | **bool?** | Value indicating whether a Meeting Response object is a counter proposal.              | 
**Attendees** | [**MapiCalendarAttendeesDto**](/email/reference-model-mapi-calendar-attendees-dto/) | Attendees              | [optional] 
**BusyStatus** | **string** | Enumerates the mapi calendar possible busy status Enum, available values: Free, Tentative, Busy, OutOfOffice | 
**ClientIntent** | **List&lt;string&gt;** | Actions the user has taken on this Meeting object.              Items: Enumerates the actions the user can taken on the Meeting object Enum, available values: Manager, Delegate, DeletedWithNoResponse, DeletedExceptionWithNoResponse, RespondedTentative, RespondedAccept, RespondedDecline, ModifiedStartTime, ModifiedEndTime, ModifiedLocation, RespondedExceptionDecline, Canceled, ExceptionCanceled | [optional] 
**EndDate** | **DateTime?** | End date and time of the event. If the date is not set, default value for DateTime is returned.              | 
**EndDateTimeZone** | [**MapiCalendarTimeZoneDto**](/email/reference-model-mapi-calendar-time-zone-dto/) | Time zone information that indicates the time zone of the EndDate property.              | [optional] 
**IsAllDay** | **bool?** | Value indicating whether the event is an all-day event.              | 
**KeyWords** | **string** | Categories of the calendar object.              | [optional] 
**Location** | **string** | Location of the event.              | [optional] 
**Recurrence** | [**MapiCalendarEventRecurrenceDto**](/email/reference-model-mapi-calendar-event-recurrence-dto/) | Recurrence properties.              | [optional] 
**ReminderDelta** | **int?** | Interval, in minutes, between the time at which the reminder first becomes overdue and the start time of the Calendar object.              | 
**ReminderFileParameter** | **string** | Full path of the sound that a client SHOULD play when the reminder becomes overdue.              | [optional] 
**ReminderSet** | **bool?** | Value indicating whether a reminder is set on the object.              | 
**Sequence** | **int?** | Sequence number.              | 
**StartDate** | **DateTime?** | Start date and time of the event. If the date is not set, default value for DateTime is returned.              | 
**StartDateTimeZone** | [**MapiCalendarTimeZoneDto**](/email/reference-model-mapi-calendar-time-zone-dto/) | Time zone information that indicates the time zone of the StartDate property.              | [optional] 
**Uid** | **string** | Unique identifier.              | [optional] 
**Organizer** | [**MapiElectronicAddressDto**](/email/reference-model-mapi-electronic-address-dto/) | Organizer              | [optional] 

Parent class: [MapiMessageItemBaseDto](/email/reference-model-mapi-message-item-base-dto/)

## Example

{{< tabs tabTotal="6" tabID="mapi_calendar_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var mapiCalendarDto = new MapiCalendarDto
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
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiCalendarDto mapiCalendarDto = Models.mapiCalendarDto()
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
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
mapi_calendar_dto = models.MapiCalendarDto(
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
    subject='Some summary')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
mapi_calendar_dto = MapiCalendarDto.new(
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
  subject: 'Some summary')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let mapiCalendarDto = Models.mapiCalendarDto()
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
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mapiCalendarDto = Models::mapiCalendarDto()
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
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

