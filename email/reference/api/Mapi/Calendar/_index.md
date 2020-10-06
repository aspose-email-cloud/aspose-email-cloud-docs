---
title: "Calendar"
type: docs
url: /reference-mapi-calendar-api/
weight: 1
---

MAPI calendar operations.

## AsCalendarDto

Converts MAPI calendar model to CalendarDto model.             

Returns [**CalendarDto**](CalendarDto.md) model.

{{< tabs tabTotal="6" tabID="mapi_calendar_as_calendar_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Mapi.Calendar.AsCalendarDtoAsync(mapiCalendarDto);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarDto result = api.mapi().calendar().asCalendarDto(mapiCalendarDto);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.mapi.calendar.as_calendar_dto(mapi_calendar_dto)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.mapi.calendar.as_calendar_dto(mapi_calendar_dto)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.mapi.calendar.asCalendarDto(mapiCalendarDto);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->mapi()->calendar()->asCalendarDto($mapi_calendar_dto);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="mapiCalendarDto" >}}

Description: MAPI calendar model to convert.

Type: [**MapiCalendarDto**](/email/reference-mapi-calendar-dto/).

{{< tabs tabTotal="6" tabID="mapi_calendar_as_calendar_dto_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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
$mapi_calendar_dto = Models::mapiCalendarDto()
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

{{< /expand-list >}}
## AsFile

Converts MAPI calendar model to specified format and returns as file.             

Returns a file.

{{< tabs tabTotal="6" tabID="mapi_calendar_as_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Mapi.Calendar.AsFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.mapi().calendar().asFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.mapi.calendar.as_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.mapi.calendar.as_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.mapi.calendar.asFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->mapi()->calendar()->asFile($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: MAPI calendar model to convert.

Type: [**MapiCalendarAsFileRequest**](/email/reference-mapi-calendar-as-file-request/).

{{< tabs tabTotal="6" tabID="mapi_calendar_as_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiCalendarAsFileRequest
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
MapiCalendarAsFileRequest request = Models.mapiCalendarAsFileRequest()
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
request = models.MapiCalendarAsFileRequest(
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
request = MapiCalendarAsFileRequest.new(
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
let request = Models.mapiCalendarAsFileRequest()
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
$request = Models::mapiCalendarAsFileRequest()
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

{{< /expand-list >}}
## FromFile

Converts calendar file to a MAPI model representation.             

Returns [**MapiCalendarDto**](MapiCalendarDto.md) model.

{{< tabs tabTotal="6" tabID="mapi_calendar_from_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Mapi.Calendar.FromFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiCalendarDto result = api.mapi().calendar().fromFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.mapi.calendar.from_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.mapi.calendar.from_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.mapi.calendar.fromFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->mapi()->calendar()->fromFile($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: FromFile method request.

Type: [**MapiCalendarFromFileRequest**](/email/reference-mapi-calendar-from-file-request/).

{{< tabs tabTotal="6" tabID="mapi_calendar_from_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiCalendarFromFileRequest
{ 
    File = new MemoryStream(File.ReadAllBytes("/path/to/calendar.msg"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiCalendarFromFileRequest request = Models.mapiCalendarFromFileRequest()
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/calendar.msg")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.MapiCalendarFromFileRequest(
    file='/path/to/calendar.msg')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = MapiCalendarFromFileRequest.new(
    file: File.new('/path/to/calendar.msg'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.MapiCalendarFromFileRequest()
    .file(fs.readFileSync('/path/to/calendar.msg'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::MapiCalendarFromFileRequest()
    ->file(new SplFileObject('/path/to/calendar.msg'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## Get

Get MAPI calendar document.             

Returns [**MapiCalendarDto**](MapiCalendarDto.md) model.

{{< tabs tabTotal="6" tabID="mapi_calendar_get_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Mapi.Calendar.GetAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiCalendarDto result = api.mapi().calendar().get(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.mapi.calendar.get(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.mapi.calendar.get(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.mapi.calendar.get(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->mapi()->calendar()->get($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: Get method request.

Type: [**MapiCalendarGetRequest**](/email/reference-mapi-calendar-get-request/).

{{< tabs tabTotal="6" tabID="mapi_calendar_get_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiCalendarGetRequest
{ 
    FileName = "calendar.msg",
    Folder = "calendar/location/on/storage",
    Storage = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiCalendarGetRequest request = Models.mapiCalendarGetRequest()
    .fileName("calendar.msg")
    .folder("calendar/location/on/storage")
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.MapiCalendarGetRequest(
    file_name='calendar.msg',
    folder='calendar/location/on/storage',
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = MapiCalendarGetRequest.new(
    file_name: 'calendar.msg',
    folder: 'calendar/location/on/storage',
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.MapiCalendarGetRequest()
    .fileName('calendar.msg')
    .folder('calendar/location/on/storage')
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::MapiCalendarGetRequest()
    ->file_name('calendar.msg')
    ->folder('calendar/location/on/storage')
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## Save

Save MAPI Calendar to storage.             

{{< tabs tabTotal="6" tabID="mapi_calendar_save_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Mapi.Calendar.SaveAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.mapi().calendar().save(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.mapi.calendar.save(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.mapi.calendar.save(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.mapi.calendar.save(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->mapi()->calendar()->save($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: Calendar create/update request.

Type: [**MapiCalendarSaveRequest**](/email/reference-mapi-calendar-save-request/).

{{< tabs tabTotal="6" tabID="mapi_calendar_save_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiCalendarSaveRequest
{
    Format = "Msg",
    StorageFile = new StorageFileLocation
    {
        FileName = "calendar.msg",
        Storage = "First Storage",
        FolderPath = "file/location/folder/on/storage"
    },
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
MapiCalendarSaveRequest request = Models.mapiCalendarSaveRequest()
    .format("Msg")
    .storageFile(Models.storageFileLocation()
        .fileName("calendar.msg")
        .storage("First Storage")
        .folderPath("file/location/folder/on/storage")
        .build())
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
request = models.MapiCalendarSaveRequest(
    format='Msg',
    storage_file=models.StorageFileLocation(
        file_name='calendar.msg',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'),
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
request = MapiCalendarSaveRequest.new(
  format: 'Msg',
  storage_file: StorageFileLocation.new(
    file_name: 'calendar.msg',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'),
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
let request = Models.mapiCalendarSaveRequest()
    .format('Msg')
    .storageFile(Models.storageFileLocation()
        .fileName('calendar.msg')
        .storage('First Storage')
        .folderPath('file/location/folder/on/storage')
        .build())
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
$request = Models::mapiCalendarSaveRequest()
    ->format('Msg')
    ->storageFile(Models::storageFileLocation()
        ->fileName('calendar.msg')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
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

{{< /expand-list >}}

## More APIs
See more APIs:
{{< list-of-articles-in-this-section >}}
