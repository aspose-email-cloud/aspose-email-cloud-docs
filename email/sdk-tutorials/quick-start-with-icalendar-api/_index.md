---
title: "Quick Start With iCalendar API"
type: docs
url: /quick-start-with-icalendar-api/
description: "Aspose Email tutorial shows how to work with iCalendar files using Aspose.Email Cloud. Create calendars, edit calendars, process appointments, etc."
weight: 40
---

## **iCalendar API**
[Aspose.Email Cloud API](https://products.aspose.cloud/email/family) supports working with iCalendar files. You can use our API to read, edit and save iCalendar (.ics) files. Also, you can convert them to [**AlternateView**](/email/icalendar-to-alternateview-converter/) and add them to email messages.

Our SDKs support two different ways of operating with iCalendar files using **MapiCalendarDto** and **CalendarDto**. This tutorial shows how to use **CalendarDto**.

{{% alert color="primary" %}} To see how to setup SDKs use the [SDK setup](/email/sdk-setup/) tutorial. {{% /alert %}} 


## **Create Calendar File Object and Save It to Storage**
[**CalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarDto.md) object contains all information about an appointment including attendees, start date, end date, description and etc.

First, let’s create a **CalendarDto** object and save it to Storage.

To save a **CalendarDto** to Storage use [**SaveAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarApi.md#saveasync) 
from [**CalendarApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarApi.md). 
This method requires **1 parameter** — 
[**CalendarSaveRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarSaveRequest.md), which is a request model for this operation. 

[**CalendarSaveRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarSaveRequest.md) requires **3 parameters**: 
- *Format* — Calendar file format (Ics or Msg).
- *StorageFile* — [**StorageFileLocation**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/StorageFileLocation.md) object that determines iCalendar file location on storage.
- *Value* — [**CalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarDto.md) object to save.

**How to create a CalendarDto object and save it to the Storage?**

{{< tabs tabTotal="6" tabID="1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var calendar = new CalendarDto
{
    Attendees = new List<MailAddress>
    {
        new MailAddress("Attendee Name", "attendee@aspose.com", "Accepted")
    },
    Description = "Some description",
    Summary = "Some summary",
    Organizer = new MailAddress("Organizer Name", "organizer@aspose.com", null),
    StartDate = DateTime.UtcNow.AddDays(1).AddHours(12),
    EndDate = DateTime.UtcNow.AddDays(1).AddHours(13),
    Location = "Some location"
};
 
var storageName = "First storage";
var folder = "folder/on/storage";
var calendarFileName = "calendar.ics";

await api.Calendar.SaveAsync(new CalendarSaveRequest(
    new StorageFileLocation(storageName, folder, calendarFileName),
    calendar, "Ics"));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
Calendar startDate = Calendar.getInstance();
Calendar endDate = (Calendar) startDate.clone();
endDate.set(Calendar.HOUR_OF_DAY, endDate.get(Calendar.HOUR_OF_DAY) + 1);
CalendarDto calendar = new CalendarDto()
    .addAttendeesItem(new MailAddress("Attendee Name", "attendee@aspose.com", "Accepted"))
    .description("Some description")
    .summary("Some summary")
    .organizer(new MailAddress("Organizer Name", "organizer@aspose.com", "Accepted"))
    .startDate(startDate.getTime())
    .endDate(endDate.getTime())
    .location("Some location");
String storage = "First storage";
String folder = "folder/on/storage";
String calendarFile = "calendar.ics";

api.calendar().save(new CalendarSaveRequest(
    new StorageFileLocation(storage, folder, calendarFile),
    calendar, "Ics"));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
calendar = models.CalendarDto()
calendar.attendees = [models.MailAddress('Attendee Name', 'attendee@aspose.com', 'Accepted')]
calendar.description = 'Some description'
calendar.summary = 'Some summary'
calendar.organizer = models.MailAddress('Organizer Name', 'organizer@aspose.com', 'Accepted')
calendar.start_date = datetime.today() + timedelta(days=1)
calendar.end_date = calendar.start_date + timedelta(hours=1)
calendar.location = 'Some location'
 
storage = 'First storage'
folder = 'folder/on/storage'
calendar_file = 'calendar.ics'

api.calendar.save(models.CalendarSaveRequest(
    models.StorageFileLocation(storage, folder, calendar_file),
    calendar, "Ics"))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
calendar = CalendarDto.new(
  location: 'Some location',
  summary: 'Some summary',
  description: 'Some description',
  start_date: DateTime.now,
  end_date: DateTime.now,
  organizer: MailAddress.new(address: 'organizer@aspose.com'),
  attendees: [MailAddress.new(address: 'attendee@aspose.com')],
  recurrence: DailyRecurrencePatternDto.new(occurs: 10, week_start: 'Monday'))
 
storage = 'First storage'
folder = 'folder/on/storage'
calendar_file = 'calendar.ics'

api.calendar.save(
  CalendarSaveRequest.new(
    storage_file: StorageFileLocation.new(
      storage: storage,
      folder_path: folder,
      file_name: calendar_file),
    value: calendar,
    format: 'Ics'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
var calendar = new models.CalendarDto();
calendar.attendees = [
    new models.MailAddress('Attendee Name', 'attendee@aspose.com', 'Accepted')
];
calendar.description = 'Some description';
calendar.summary = 'Some summary';
calendar.organizer = new models.MailAddress('Organizer Name', 'organizer@aspose.com');
calendar.startDate = getDate(undefined, 1);
calendar.endDate = getDate(calendar.startDate, 1);
calendar.location = 'Some location';
 
var storage = 'First storage';
var folder = 'folder/on/storage';
var calendarFile = 'calendar.ics';

api.calendar.save(new CalendarSaveRequest(
    new StorageFileLocation(storage, folder, calendarFile),
    calendar, 'Ics'));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$calendar = (new CalendarDto())
    ->setAttendees(array(new MailAddress("Attendee Name", "attendee@aspose.com", "Accepted")))
    ->setDescription("Some description")
    ->setSummary("Some summary")
    ->setOrganizer(new MailAddress("Organizer Name", "organizer@aspose.com", "Accepted"))
    ->setStartDate(new DateTime())
    ->setEndDate((new DateTime())->add(new DateInterval("PT1H")))
    ->setLocation("Some location");
 
$storage = "First storage";
$folder = "folder/on/storage";
$calendarFile = "calendar.ics";

$api->calendar()->save(new CalendarSaveRequest(
    new StorageFileLocation($storage, $folder, $calendarFile),
    $calendar,
    "Ics"
));
```

{{< /tab >}}

{{< /tabs >}}
## **Download iCalendar File From Storage**
You can find the saved file on [Aspose.Cloud Dashboard](https://dashboard.aspose.cloud/#/files), or download it using SDK.

To download a file from the storage use [**DownloadFileAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/FileApi.md#downloadfileasync) from [**FileApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/FileApi.md). This method requires 1 parameter — **DownloadFileRequest**, which is a request for this operation.

**DownloadFileRequest** has **3 parameters**:

- *Path* — File path e.g. "/folder/file.ext".
- *StorageName* — Storage name.
- *VersionId* [**optional**] — File version ID to download.

**How to download iCalendar file from the Storage?**

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var fileStream = await api.CloudStorage.File.DownloadFileAsync(
    new DownloadFileRequest($"{folder}/{calendarFile}", storage));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] fileBytes = api.cloudStorage().file().downloadFile(
    new DownloadFileRequest(folder + "/" + calendarFile, storage, null));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
downloaded_file_location = api.cloud_storage.file.download_file(
    models.DownloadFileRequest(folder + '/' + calendar_file, storage))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
downloaded_file_location = api.cloud_storage.file.download_file(
  DownloadFileRequest.new(
    path: folder + '/' + calendar_file, storage_name: storage))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
var downloaded = await api.cloudStorage.file.downloadFile(
    new DownloadFileRequest(folder + '/' + calendarFile, storage));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$calendarTempFile = $api->cloudStorage()->file()->downloadFile(
    new DownloadFileRequest($folder.'/'.$calendarFile, $storage));
$fileContent = $calendarTempFile->fread($calendarTempFile->getSize());
```

{{< /tab >}}

{{< /tabs >}}

## **Get Calendar File From Storage as CalendarDto Object**
Let's get this file from storage as a **CalendarDto** object.

To get a calendar file from Storage use [**GetAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarApi.md#getasync) 
from [**CalendarApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarApi.md). 
This method requires **1 parameter** — 
**CalendarGetRequest**, which is a request for this operation.

**CalendarGetRequest** has **3 parameters**:

- *FileName* — iCalendar file name in storage.
- *Folder* — Path to the folder in storage.
- *Storage* — Storage name.

**How to get a file from the Storage as a CalendarDto object?**

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
CalendarDto calendarDto = await api.Calendar.GetAsync(
    new CalendarGetRequest(calendarFile, folder, storage));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarDto calendarDto = api.calendar().get(
    new CalendarGetRequest(calendarFile, folder, storage));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
calendar_dto = api.calendar.get(
    models.CalendarGetRequest(
        calendar_file, folder, storage))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
calendar_dto = api.calendar.get(CalendarGetRequest.new(
  file_name: calendar_file, folder: folder, storage: storage))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
var calendarDto = await api.calendar.get(
    new CalendarGetRequest(calendarFile, folder, storage));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$calendarDto = $api->calendar()->get(
    new CalendarGetRequest($calendarFile, $folder, $storage));
```

{{< /tab >}}

{{< /tabs >}}

You can change model fields and save it again. The file will be rewritten if you don't change file name and location.
## **Convert Calendar Object to AlternateView**
We also provide API methods for converting **CalendarDto** to an **AlternateView**. **AlternateView** can be added to **EmailDto**, which can be saved as **EML** file or sent using a built-in email client.

{{% alert color="primary" %}} 

To get more information about built-in email client — take a look at the [Email Client tutorial](/email/quick-start-with-email-client/).

{{% /alert %}} 



To convert a **CalendarDto** object to **AlternateView** use [**AsAlternateAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarApi.md#asalternateasync) from [**CalendarApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarApi.md). This method has **3 parameters**:
- *Value* — iCalendar document model.
- *Action* — iCalendar actions. Enum, available values: Create, Update, Cancel.
- *SequenceId* — iCalendar sequence id.

**How to convert CalendarDto to an AlternateView?**

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
//Convert CalendarDto to AlternateView
var alternate = await api.Calendar.AsAlternateAsync(
    new CalendarAsAlternateRequest(calendar, "Create", null));

//Create EmailDto with AlternateView
var emailDto = new EmailDto
{
    AlternateViews = new List<AlternateView>
    {
        alternate
    },
    From = new MailAddress("From address", "organizer@aspose.com", "Accepted", null),
    To = new List<MailAddress> {new MailAddress("To address", "attendee@aspose.com", null, null)},
    Subject = "Some subject",
    Body = "Some body"
};

//Save EmailDto as EML file
var emailFile = "email.eml";

await api.Email.SaveAsync(new EmailSaveRequest(
    new StorageFileLocation(StorageName, Folder, emailFile), email, "Eml"));

//Or Setup SMTP account to send emailDto
var credentials = new EmailClientAccountPasswordCredentials
{
    Login = "example@gmail.com",
    Password = "password"
};
var sendAccountDto = new EmailClientAccount
{
    Host = "smtp.gmail.com",
    Port = 465,
    ProtocolType = "SMTP",
    SecurityOptions = "SSLAuto",
    Credentials = credentials
};
var smtpAccount = "smtp.account";
var smtpLocation = new StorageFileLocation(storage, folder, smtpAccount);
await api.Client.Account.SaveAsync(new ClientAccountSaveRequest(
    smtpLocation, sendAccountDto));
//And send it
await api.Client.Message.SendAsync(new ClientMessageSendRequest(
    smtpLocation, new MailMessageDto(emailDto)));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
//Convert CalendarDto to AlternateView
AlternateView alternate = api.calendar().asAlternate(
    new CalendarAsAlternateRequest(calendar, "Create", null));

//Create EmailDto with AlternateView
EmailDto email = new EmailDto()
    .addAlternateViewsItem(alternate)
    .from(new MailAddress("From Name", "organizer@aspose.com", null, null))
    .addToItem(new MailAddress("To Name", "attendee@aspose.com", null, null))
    .subject("Some subject")
    .body("Some body");

//Save EmailDto as EML file
String emailFile = "email.eml";
api.email().save(new EmailSaveRequest(
    new StorageFileLocation(storage, folder, emailFile),
    email, "Eml"));

//Or Setup SMTP account to send email
EmailClientAccountPasswordCredentials credentials =
    new EmailClientAccountPasswordCredentials("example@gmail.com", "password");
EmailClientAccount sendAccountDto = new EmailClientAccount(
    "smtp.gmail.com", 465, "SSLAuto", "SMTP", credentials, null);
String smtpAccount = "smtp.account";
StorageFileLocation smtpLocation = new StorageFileLocation(storage, folder, smtpAccount);
api.client().account().save(new ClientAccountSaveRequest(
    smtpLocation, sendAccountDto));

//And send it
api.client().message().send(new ClientMessageSendRequest(
    smtpLocation, new MailMessageDto(email)));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
# Convert CalendarDto to AlternateView
alternate = api.calendar.as_alternate(models.CalendarAsAlternateRequest(
    calendar, 'Create'))

# Create EmailDto with AlternateView
email = models.EmailDto(
    alternate_views=[alternate],
    # 'from' is reserved, so from field is named '_from':
    _from=models.MailAddress('From Name', 'organizer@aspose.com'),
    to=[models.MailAddress('To Name', 'attendee@aspose.com')],
    subject='Some subject',
    body='Some body')

# Save EmailDto as EML file
email_file = 'email.eml'
api.email.save(models.EmailSaveRequest(
    models.StorageFileLocation(storage, folder, email_file),
    email, 'Eml'))

# Or Setup SMTP account to send email
credentials = models.EmailClientAccountPasswordCredentials(
    'example@gmail.com', 'password')
send_account_dto = models.EmailClientAccount(
    'smtp.gmail.com', 465, 'SSLAuto', 'SMTP', credentials)
smtp_account = 'smtp.account'
smtp_location = models.StorageFileLocation(storage, folder, smtp_account)
api.client.account.save(models.ClientAccountSaveRequest(
    smtp_location, send_account_dto))
# And send it
api.client.message.send(models.ClientMessageSendRequest(
    smtp_location, models.MailMessageDto(email)))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Convert CalendarDto to AlternateView
alternate = api.calendar.as_alternate(
  CalendarAsAlternateRequest.new(
    value: calendar, action: 'Create'))

# Create EmailDto with AlternateView
email = EmailDto.new(
  alternate_views: [alternate],
  from: MailAddress.new(display_name: 'From Name', address: 'cloud.em@yandex.ru'),
  to: [MailAddress.new(display_name: 'To Name', address: 'cloud.em@yandex.ru')],
  subject: 'Some subject',
  body: 'Some body')

# Save EmailDto as EML file
email_file = 'email.eml'
api.email.save(
  EmailSaveRequest.new(
    storage_file: StorageFileLocation.new(
      storage: storage,
      folder_path: folder,
      file_name: email_file),
    value: email,
    format: 'Eml'))

# Or Setup SMTP account to send email
credentials = EmailClientAccountPasswordCredentials.new(
  login: 'example@gmail.com', password: 'password')
send_account_dto = EmailClientAccount.new(
  host: 'smtp.gmail.com',
  port: 465,
  security_options: 'SSLAuto',
  protocol_type: 'SMTP',
  credentials: credentials)
smtp_account = 'smtp.account'
smtp_location = StorageFileLocation.new(
  storage: storage,
  folder_path: folder,
  file_name: smtp_account)
api.client.account.save(
  ClientAccountSaveRequest.new(
    storage_file: smtp_location, value: send_account_dto))
# And send it
api.client.message.send(ClientMessageSendRequest.new(
  account_location: smtp_location, message: MailMessageDto.new(value: email)))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
//Convert CalendarDto to AlternateView
const alternate = await api.calendar.asAlternate(
    new CalendarAsAlternateRequest(calendar, 'Create'));

//Create EmailDto with AlternateView
const email = new EmailDto();
email.alternateViews = [alternate];
email.from = new MailAddress('From address', 'organizer@aspose.com');
email.to = [new MailAddress('To address', 'attendee@aspose.com')];
email.subject = 'Some subject';
email.body = 'Some body';

//Save EmailDto as EML file
const emailFile = 'email.eml';
await api.email.save(new EmailSaveRequest(
    new StorageFileLocation(storage, folder, emailFile), email,'Eml'));

//Or Setup SMTP account to send email
const credentials = new EmailClientAccountPasswordCredentials(
    'example@gmail.com', 'password');
const sendAccountDto = new EmailClientAccount(
    'smtp.gmail.com', 465, 'SSLAuto', 'SMTP', credentials);
const smtpAccount = 'smtp.account';
const smtpLocation = new StorageFileLocation(storage, folder, smtpAccount);
await api.client.account.save(new ClientAccountSaveRequest(
    smtpLocation, sendAccountDto));
//And send it
await api.client.message.send(new ClientMessageSendRequest(
    smtpLocation, new MailMessageDto(email)));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
//Convert CalendarDto to AlternateView
$alternate = $api->calendar()->asAlternate(
    new CalendarAsAlternateRequest($calendar, "Create"));

//Create EmailDto with AlternateView
$email = (new EmailDto())
    ->setAlternateViews(array($alternate))
    ->setFrom(new MailAddress("Organizer Name", "organizer@aspose.com"))
    ->setTo(array(new MailAddress("Attendee Name", "attendee@aspose.com")))
    ->setSubject("Some subject")
    ->setBody("Some body");

//Save EmailDto as EML file
$emailFile = "email.eml";
$api->email()->save(new EmailSaveRequest(
    new StorageFileLocation($storage, $folder, $emailFile),
    $email, "Eml"));

//Or Setup SMTP account to send email
$credentials = new EmailClientAccountPasswordCredentials(
    "example@gmail.com", "password");
$sendAccountDto = new EmailClientAccount(
    "smtp.gmail.com", 465, "SSLAuto", "SMTP", $credentials);
$smtpAccount = "smtp.account";
$smtpLocation = new StorageFileLocation($storage, $folder, $smtpAccount);
$api->client()->account()->save(
    new ClientAccountSaveRequest($smtpLocation, $sendAccountDto));
//And send it
$api->client()->message()->send(new ClientMessageSendRequest(
    $smtpLocation, new MailMessageDto($email)
));
```

{{< /tab >}}

{{< /tabs >}}
## **Get a List of iCalendar Files From One Folder**
You can get a list of iCalendar files stored in one folder on storage using a single API request. Files will be filtered by ".ics" extension and read to list of CalendarDto object. The method supports pagination.

To get a list of iCalendar files use [**GetListAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarApi.md#GetListAsync) from [**CalendarApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarApi.md). This method requires **1 parameter** — **CalendarGetListRequest**, which is a request for this operation.

**CalendarGetListRequest** has **4 parameters**:

- *Folder* — Path to the folder in storage.
- *ItemsPerPage* — Count of items on page.
- *PageNumber* — Page number.
- *Storage* — Storage name.

**How to get a list of iCalendar files stored in one folder?**

{{< tabs tabTotal="6" tabID="5" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
CalendarStorageList calendarList = await api.Calendar.GetListAsync(
    new CalendarGetListRequest(folder, 10, 0, storage));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarStorageList calendarList = api.calendar().getList(
    new CalendarGetListRequest(folder, 10, 0, storage));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
calendar_list = api.calendar.get_list(
    models.CalendarGetListRequest(folder, 10, 0, storage))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
calendar_list = api.calendar.get_list(CalendarGetListRequest.new(
  folder: folder, items_per_page: 10, page_number: 0, storage: storage))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
const calendarList = api.calendar.getList(
    new CalendarGetListRequest(folder, 10, 0, storage));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$calendarList = $api->calendar()->getList(
    new CalendarGetListRequest($folder, 10, 0, $storage));
```

{{< /tab >}}

{{< /tabs >}}


## **More Tutorials**
See more Aspose Email tutorials: 
{{< list-of-articles-in-this-section >}}
