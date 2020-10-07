---
title: "CalendarStorageList"
type: docs
url: /reference-model-calendar-storage-list/
weight: 1
---
iCalendar models list with corresponding storage locations.             

Properties:

Class has no properties

Parent class: [ListResponseOfStorageModelOfCalendarDto](/email/reference-model-list-response-of-storage-model-of-calendar-dto/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="calendar_storage_list_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var calendarStorageList = new CalendarStorageList
{
    Value = new List<StorageModelOfCalendarDto>
    {
        new StorageModelOfCalendarDto
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
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarStorageList calendarStorageList = Models.calendarStorageList()
    .value(Arrays.<StorageModelOfCalendarDto>asList(
        Models.storageModelOfCalendarDto()
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
            .build()))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
calendar_storage_list = models.CalendarStorageList(
    value=[
        models.StorageModelOfCalendarDto(
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
                summary='Some summary'))])
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
calendar_storage_list = CalendarStorageList.new(
  value: [
    StorageModelOfCalendarDto.new(
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
        summary: 'Some summary'))])
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let calendarStorageList = Models.calendarStorageList()
    .value([
        Models.storageModelOfCalendarDto()
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
            .build()])
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$calendarStorageList = Models::calendarStorageList()
    ->value(array(
        Models::storageModelOfCalendarDto()
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
            ->build()))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

