---
title: "Calendar"
type: docs
url: /reference-calendar-api/
weight: 1
---

iCalendar document operations.

## AsAlternate

Convert iCalendar to AlternateView             

Returns [**AlternateView**](AlternateView.md) model.

{{< tabs tabTotal="6" tabID="calendar_as_alternate_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Calendar.AsAlternateAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AlternateView result = api.calendar().asAlternate(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.calendar.as_alternate(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.calendar.as_alternate(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.calendar.asAlternate(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->calendar()->asAlternate($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: iCalendar to AlternateView request

Type: [**CalendarAsAlternateRequest**](/email/reference-calendar-as-alternate-request/).

{{< tabs tabTotal="6" tabID="calendar_as_alternate_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CalendarAsAlternateRequest
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
CalendarAsAlternateRequest request = Models.calendarAsAlternateRequest()
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
request = models.CalendarAsAlternateRequest(
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
request = CalendarAsAlternateRequest.new(
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
let request = Models.calendarAsAlternateRequest()
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
$request = Models::calendarAsAlternateRequest()
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

{{< /expand-list >}}
## AsFile

Converts calendar model to specified format and returns as file.             

Returns a file.

{{< tabs tabTotal="6" tabID="calendar_as_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Calendar.AsFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.calendar().asFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.calendar.as_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.calendar.as_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.calendar.asFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->calendar()->asFile($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: Calendar model and format to convert.

Type: [**CalendarAsFileRequest**](/email/reference-calendar-as-file-request/).

{{< tabs tabTotal="6" tabID="calendar_as_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CalendarAsFileRequest
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
CalendarAsFileRequest request = Models.calendarAsFileRequest()
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
request = models.CalendarAsFileRequest(
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
request = CalendarAsFileRequest.new(
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
let request = Models.calendarAsFileRequest()
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
$request = Models::calendarAsFileRequest()
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

{{< /expand-list >}}
## AsMapi

Converts CalendarDto to MapiCalendarDto.             

Returns [**MapiCalendarDto**](MapiCalendarDto.md) model.

{{< tabs tabTotal="6" tabID="calendar_as_mapi_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Calendar.AsMapiAsync(calendarDto);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiCalendarDto result = api.calendar().asMapi(calendarDto);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.calendar.as_mapi(calendar_dto)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.calendar.as_mapi(calendar_dto)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.calendar.asMapi(calendarDto);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->calendar()->asMapi($calendar_dto);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="calendarDto" >}}

Description: iCalendar model calendar representation.

Type: [**CalendarDto**](/email/reference-calendar-dto/).

{{< tabs tabTotal="6" tabID="calendar_as_mapi_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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
$calendar_dto = Models::calendarDto()
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

{{< /expand-list >}}
## Convert

Converts calendar document to specified format and returns as file.             

Returns a file.

{{< tabs tabTotal="6" tabID="calendar_convert_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Calendar.ConvertAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.calendar().convert(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.calendar.convert(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.calendar.convert(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.calendar.convert(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->calendar()->convert($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: Convert method request.

Type: [**CalendarConvertRequest**](/email/reference-calendar-convert-request/).

{{< tabs tabTotal="6" tabID="calendar_convert_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CalendarConvertRequest
{ 
    Format = "Ics",
    File = new MemoryStream(File.ReadAllBytes("/path/to/calendar.msg"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarConvertRequest request = Models.calendarConvertRequest()
    .format("Ics")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/calendar.msg")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CalendarConvertRequest(
    format='Ics',
    file='/path/to/calendar.msg')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CalendarConvertRequest.new(
    format: 'Ics',
    file: File.new('/path/to/calendar.msg'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CalendarConvertRequest()
    .format('Ics')
    .file(fs.readFileSync('/path/to/calendar.msg'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CalendarConvertRequest()
    ->format('Ics')
    ->file(new SplFileObject('/path/to/calendar.msg'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## FromFile

Converts calendar document to a model representation.             

Returns [**CalendarDto**](CalendarDto.md) model.

{{< tabs tabTotal="6" tabID="calendar_from_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Calendar.FromFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarDto result = api.calendar().fromFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.calendar.from_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.calendar.from_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.calendar.fromFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->calendar()->fromFile($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: FromFile method request.

Type: [**CalendarFromFileRequest**](/email/reference-calendar-from-file-request/).

{{< tabs tabTotal="6" tabID="calendar_from_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CalendarFromFileRequest
{ 
    File = new MemoryStream(File.ReadAllBytes("/path/to/calendar.ics"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarFromFileRequest request = Models.calendarFromFileRequest()
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/calendar.ics")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CalendarFromFileRequest(
    file='/path/to/calendar.ics')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CalendarFromFileRequest.new(
    file: File.new('/path/to/calendar.ics'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CalendarFromFileRequest()
    .file(fs.readFileSync('/path/to/calendar.ics'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CalendarFromFileRequest()
    ->file(new SplFileObject('/path/to/calendar.ics'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## Get

Get calendar file from storage.             

Returns [**CalendarDto**](CalendarDto.md) model.

{{< tabs tabTotal="6" tabID="calendar_get_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Calendar.GetAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarDto result = api.calendar().get(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.calendar.get(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.calendar.get(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.calendar.get(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->calendar()->get($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: Get method request.

Type: [**CalendarGetRequest**](/email/reference-calendar-get-request/).

{{< tabs tabTotal="6" tabID="calendar_get_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CalendarGetRequest
{ 
    FileName = "calendar.ics",
    Folder = "calendar/location/on/storage",
    Storage = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarGetRequest request = Models.calendarGetRequest()
    .fileName("calendar.ics")
    .folder("calendar/location/on/storage")
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CalendarGetRequest(
    file_name='calendar.ics',
    folder='calendar/location/on/storage',
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CalendarGetRequest.new(
    file_name: 'calendar.ics',
    folder: 'calendar/location/on/storage',
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CalendarGetRequest()
    .fileName('calendar.ics')
    .folder('calendar/location/on/storage')
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CalendarGetRequest()
    ->file_name('calendar.ics')
    ->folder('calendar/location/on/storage')
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## GetAsAlternate

Get iCalendar from storage as AlternateView             

Returns [**AlternateView**](AlternateView.md) model.

{{< tabs tabTotal="6" tabID="calendar_get_as_alternate_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Calendar.GetAsAlternateAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AlternateView result = api.calendar().getAsAlternate(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.calendar.get_as_alternate(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.calendar.get_as_alternate(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.calendar.getAsAlternate(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->calendar()->getAsAlternate($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: GetAsAlternate method request.

Type: [**CalendarGetAsAlternateRequest**](/email/reference-calendar-get-as-alternate-request/).

{{< tabs tabTotal="6" tabID="calendar_get_as_alternate_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CalendarGetAsAlternateRequest
{ 
    FileName = "calendar.ics",
    CalendarAction = "Create",
    Folder = "calendar/location/on/storage",
    Storage = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarGetAsAlternateRequest request = Models.calendarGetAsAlternateRequest()
    .fileName("calendar.ics")
    .calendarAction("Create")
    .folder("calendar/location/on/storage")
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CalendarGetAsAlternateRequest(
    file_name='calendar.ics',
    calendar_action='Create',
    folder='calendar/location/on/storage',
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CalendarGetAsAlternateRequest.new(
    file_name: 'calendar.ics',
    calendar_action: 'Create',
    folder: 'calendar/location/on/storage',
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CalendarGetAsAlternateRequest()
    .fileName('calendar.ics')
    .calendarAction('Create')
    .folder('calendar/location/on/storage')
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CalendarGetAsAlternateRequest()
    ->file_name('calendar.ics')
    ->calendar_action('Create')
    ->folder('calendar/location/on/storage')
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## GetAsFile

Converts calendar document from storage to specified format and returns as file.             

Returns a file.

{{< tabs tabTotal="6" tabID="calendar_get_as_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Calendar.GetAsFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.calendar().getAsFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.calendar.get_as_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.calendar.get_as_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.calendar.getAsFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->calendar()->getAsFile($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: GetAsFile method request.

Type: [**CalendarGetAsFileRequest**](/email/reference-calendar-get-as-file-request/).

{{< tabs tabTotal="6" tabID="calendar_get_as_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CalendarGetAsFileRequest
{ 
    FileName = "calendar.msg",
    Format = "Ics",
    Storage = "First Storage",
    Folder = "calendar/file/location/on/storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarGetAsFileRequest request = Models.calendarGetAsFileRequest()
    .fileName("calendar.msg")
    .format("Ics")
    .storage("First Storage")
    .folder("calendar/file/location/on/storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CalendarGetAsFileRequest(
    file_name='calendar.msg',
    format='Ics',
    storage='First Storage',
    folder='calendar/file/location/on/storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CalendarGetAsFileRequest.new(
    file_name: 'calendar.msg',
    format: 'Ics',
    storage: 'First Storage',
    folder: 'calendar/file/location/on/storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CalendarGetAsFileRequest()
    .fileName('calendar.msg')
    .format('Ics')
    .storage('First Storage')
    .folder('calendar/file/location/on/storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CalendarGetAsFileRequest()
    ->file_name('calendar.msg')
    ->format('Ics')
    ->storage('First Storage')
    ->folder('calendar/file/location/on/storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## GetList

Get iCalendar list from storage folder.             

Returns [**CalendarStorageList**](CalendarStorageList.md) model.

{{< tabs tabTotal="6" tabID="calendar_get_list_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Calendar.GetListAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarStorageList result = api.calendar().getList(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.calendar.get_list(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.calendar.get_list(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.calendar.getList(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->calendar()->getList($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: GetList method request.

Type: [**CalendarGetListRequest**](/email/reference-calendar-get-list-request/).

{{< tabs tabTotal="6" tabID="calendar_get_list_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CalendarGetListRequest
{ 
    Folder = "some/folder/on/storage",
    ItemsPerPage = 10,
    PageNumber = 0,
    Storage = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarGetListRequest request = Models.calendarGetListRequest()
    .folder("some/folder/on/storage")
    .itemsPerPage(10)
    .pageNumber(0)
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CalendarGetListRequest(
    folder='some/folder/on/storage',
    items_per_page=10,
    page_number=0,
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CalendarGetListRequest.new(
    folder: 'some/folder/on/storage',
    items_per_page: 10,
    page_number: 0,
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CalendarGetListRequest()
    .folder('some/folder/on/storage')
    .itemsPerPage(10)
    .pageNumber(0)
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CalendarGetListRequest()
    ->folder('some/folder/on/storage')
    ->items_per_page(10)
    ->page_number(0)
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## Save

Save iCalendar             

{{< tabs tabTotal="6" tabID="calendar_save_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Calendar.SaveAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.calendar().save(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.calendar.save(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.calendar.save(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.calendar.save(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->calendar()->save($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: iCalendar create/update request

Type: [**CalendarSaveRequest**](/email/reference-calendar-save-request/).

{{< tabs tabTotal="6" tabID="calendar_save_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CalendarSaveRequest
{
    StorageFile = new StorageFileLocation
    {
        FileName = "calendar.ics",
        Storage = "First Storage",
        FolderPath = "file/location/folder/on/storage"
    },
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
CalendarSaveRequest request = Models.calendarSaveRequest()
    .storageFile(Models.storageFileLocation()
        .fileName("calendar.ics")
        .storage("First Storage")
        .folderPath("file/location/folder/on/storage")
        .build())
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
request = models.CalendarSaveRequest(
    storage_file=models.StorageFileLocation(
        file_name='calendar.ics',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'),
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
request = CalendarSaveRequest.new(
  storage_file: StorageFileLocation.new(
    file_name: 'calendar.ics',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'),
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
let request = Models.calendarSaveRequest()
    .storageFile(Models.storageFileLocation()
        .fileName('calendar.ics')
        .storage('First Storage')
        .folderPath('file/location/folder/on/storage')
        .build())
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
$request = Models::calendarSaveRequest()
    ->storageFile(Models::storageFileLocation()
        ->fileName('calendar.ics')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
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

{{< /expand-list >}}

## More APIs
See more APIs:
{{< list-of-articles-in-this-section >}}
