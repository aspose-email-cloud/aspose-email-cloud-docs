---
title: "Convert Email, Calendar and Contact Files"
type: docs
url: /convert-email-calendar-and-contact-files/
description: "Aspose.Email Cloud allows to convert email, convert iCalendar and convert contact files (convert VCard). Convert from Outlook &amp;amp; Thunderbird."
weight: 80
---

## **Convert Calendar (iCalendar) Files**
{{% alert color="primary" %}}

This tutorial describes only the file conversion API. To get more information about **iCalendar** API usage see [**iCalendar API Tutorial**](/emailcloud/quick-start-with-icalendar-api/).

{{% /alert %}} 

**iCalendar** file can be reproduced as a [**CalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarDto.md) object. This object can be converted to **iCalendar** or Microsoft Outlook **MSG** file.
### **Create CalendarDto Object**
Let's create a **CalendarDto** object:

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
```

{{< /tab >}}

{{< /tabs >}}
### **Convert CalendarDto to MAPI File**
We can convert created **CalendarDto** to **MAPI** or **ICS** file:

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var mapi = await api.Calendar.AsFileAsync(
    new CalendarAsFileRequest("Msg", calendar));

//mapi can be saved as a calendar.msg file:
using (var file = File.OpenWrite("calendar.msg"))
{
    await mapi.CopyToAsync(file);
}
mapi.Seek(0, SeekOrigin.Begin);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] mapi = api.calendar().asFile(
    new CalendarAsFileRequest("Msg", calendar));

// mapi can be saved as a calendar.msg file:
try (FileOutputStream stream = new FileOutputStream("calendar.msg")){
    stream.write(mapi);
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
mapi = api.calendar.as_file(
    models.CalendarAsFileRequest('Msg', calendar))
# mapi variable contains temp MSG file location
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
mapi = api.calendar.as_file(
  CalendarAsFileRequest.new(format: 'Msg', value: calendar))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const mapi = await api.calendar.asFile(
  new CalendarAsFileRequest('Msg', calendar));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mapi = $api->calendar()->asFile(
  new CalendarAsFileRequest('Msg', $calendar));
```

{{< /tab >}}

{{< /tabs >}}
### **Convert CalendarDto to ICS**
That's it, you can open a file created in the Microsoft Outlook or any other application with MSG files support. You can also convert MSG file to an iCalendar file:

**Convert Calendar File to ICS**

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var ics = await api.Calendar.ConvertAsync(
    new CalendarConvertRequest(
        "Ics", mapi));
//ics can be saved as a calendar.ics file:
using (var file = File.OpenWrite("calendar.ics"))
{
    await ics.CopyToAsync(file);
}
ics.Seek(0, SeekOrigin.Begin);

//ICS is a text format. We can convert the stream to a string and check that it
//contains specified location as a substring:
using (var memoryStream = new MemoryStream())
{
    await ics.CopyToAsync(memoryStream);
    var icsString = Encoding.UTF8.GetString(memoryStream.ToArray());
    Assert.IsTrue(icsString.Contains(calendar.Location));
}

ics.Seek(0, SeekOrigin.Begin);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] ics = api.calendar().convert(
    new CalendarConvertRequest(
        "Ics", mapi));

//ics can be saved as a calendar.ics file:
try (FileOutputStream stream = new FileOutputStream("calendar.ics")){
    stream.write(ics);
}

//ICS is a text format. We can convert icsBytes to a string and check that it
//contains specified location as a substring:
String calendarContent = new String(ics, "UTF-8");
assert calendarContent.contains(calendar.getLocation());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
ics = api.calendar.convert(models.CalendarConvertRequest('Ics', mapi))
# ICS is a text format. We can read the file to a string and check that it
# contains specified location as a substring:
with open(ics, 'r') as f:
    file_data = f.read()
    assert calendar.location in file_data
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
ics = api.calendar.convert(
  CalendarConvertRequest.new(
    format: 'Ics',
    file: mapi))
# ICS is a text format. We can read file content to a string and check that it
# contains specified location as a substring:
ics_content = IO.read(ics)
expect(ics_content).to include calendar.location
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const ics = await api.calendar.convert(new CalendarConvertRequest(
    'Ics', mapi));
//ICS is a text format. We can convert the buffer to a string and check that it
//contains specified location as a substring:
let icsString = ics.toString();
expect(icsString).to.include(calendar.location);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$ics = $api->calendar()->convert(new CalendarConvertRequest('Ics', $mapi));
//ICS is a text format. We can read it to a string and check that it
//contains specified location as a substring:
$fileContent = $ics->fread($ics->getSize());
$this->assertRegExp("/" . $calendar->getLocation() . "/", $fileContent);
```

{{< /tab >}}

{{< /tabs >}}
### **Convert iCalendar File to CalendarDto**
All iCalendar files can be converted back to CalendarDto objects:

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var dto = await api.Calendar.FromFileAsync(
    new CalendarFromFileRequest(ics));
Assert.AreEqual(calendar.Location, dto.Location);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarDto dto = api.calendar().fromFile(
    new CalendarFromFileRequest(ics));
assert calendar.getLocation().equals(dto.getLocation());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
dto = api.calendar.from_file(
    models.CalendarFromFileRequest(ics))
assert calendar.location == dto.location
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
dto = api.calendar.from_file(
  CalendarFromFileRequest.new(file: ics))
expect(dto.location). to eq calendar.location
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const dto = await api.calendar.fromFile(
    new CalendarFromFileRequest(ics));
expect(dto.location).to.be.equal(calendar.location);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$dto = $api->calendar()->fromFile(
    new CalendarFromFileRequest($ics));
$this->assertEquals($calendar->getLocation(), $dto->getLocation());
```

{{< /tab >}}

{{< /tabs >}}
## **Convert Contact Card (VCard) Files**

{{% alert color="primary" %}}

This tutorial describes only the file conversion API. To get more information about VCard API usage see [**VCard API Tutorial**](/emailcloud/quick-start-with-vcard-api/).

{{% /alert %}} 

VCard files conversion API looks the same as iCalendar API. VCard file can be represented using a [**ContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactDto.md) object. This object can be converted to a VCard or MAPI contact file. Both contact formats can be converted to each other and back to the [**ContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactDto.md) object. You can see all the available methods in the examples below:

**Convert VCard Files**

{{< tabs tabTotal="6" tabID="5" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
const string surname = "Thomas";
ContactDto contact => new ContactDto
{
    Gender = "Male",
    Surname = surname,
    GivenName = "Alex",
    EmailAddresses = new List<EmailAddress>
    {
        new EmailAddress
        {
            Category = new EnumWithCustomOfEmailAddressCategory("Work", null),
            Address = "alex.thomas@work.com",
            Preferred = true,
            DisplayName = "Alex Thomas"
        }
    },
    PhoneNumbers = new List<PhoneNumber>
    {
        new PhoneNumber
        {
            Category = new EnumWithCustomOfPhoneNumberCategory("Work", null),
            Number = "+49211424721",
            Preferred = true
        }
    }
};

var mapiStream = await api.Contact.AsFileAsync(
    new ContactAsFileRequest("Msg", contact));
var vcardStream = await api.Contact.ConvertAsync(
    new ContactConvertRequest("VCard", "Msg", mapiStream));
using (var memoryStream = new MemoryStream())
{
    await vcardStream.CopyToAsync(memoryStream);
    var vcardString = Encoding.UTF8.GetString(memoryStream.ToArray());
    Assert.IsTrue(vcardString.Contains(surname));
}

vcardStream.Seek(0, SeekOrigin.Begin);
var dto = await api.Contact.FromFileAsync(
    new ContactFromFileRequest("VCard", vcardStream));
Assert.AreEqual(surname, dto.Surname);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
String surname = "Thomas";
ContactDto contactDto = new ContactDto()
    .gender("Male")
    .surname(surname)
    .givenName("Alex")
    .addEmailAddressesItem(new EmailAddress(
        new EnumWithCustomOfEmailAddressCategory("Work", null),
        "Alex Thomas", true, null, "alex.thomas@work.com", null))
    .addPhoneNumbersItem(new PhoneNumber(
        new EnumWithCustomOfPhoneNumberCategory("Work", null),
        "+49211424721", true));
byte[] mapiBytes = api.contact().asFile(
    new ContactAsFileRequest("Msg", contactDto));
byte[] vcardBytes = api.contact().convert(
    new ContactConvertRequest("VCard", "Msg", mapiBytes));
String contactContent = new String(vcardBytes, "UTF-8");
assert contactContent.contains(surname);
ContactDto dto = api.contact().fromFile(
    new ContactFromFileRequest("VCard", vcardBytes));
assert surname.equals(dto.getSurname());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
contact = models.ContactDto(
    gender='Male',
    surname='Thomas',
    given_name='Alex',
    email_addresses=[
        models.EmailAddress(
            models.EnumWithCustomOfEmailAddressCategory('Work'),
            'Alex Thomas', True, address='alex.thomas@work.com')],
    phone_numbers=[
        models.PhoneNumber(
            models.EnumWithCustomOfPhoneNumberCategory('Work'),
            '+49211424721', True)])
mapi = api.contact.as_file(
    models.ContactAsFileRequest('Msg', contact))
vcard = api.contact.convert(
    models.ContactConvertRequest('VCard', 'Msg', mapi))
with open(vcard, 'r') as f:
    file_data = f.read()
    assert contact.surname in file_data
dto = api.contact.from_file(
    models.ContactFromFileRequest('VCard', vcard))
assert contact.surname == dto.surname
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
contact = ContactDto.new(
  surname: 'Cane',
  given_name: 'John',
  gender: 'Male',
  email_addresses: [
    EmailAddress.new(address: 'address@aspose.com')],
  phone_numbers: [
    PhoneNumber.new(number: '+4734534643')])
mapi_file = api.contact.as_file(
  ContactAsFileRequest.new(
    format: 'Msg',
    value: contact))
vcard_file = api.contact.convert(
  ContactConvertRequest.new(
    to_format: 'VCard',
    from_format: 'Msg',
    file: mapi_file))
vcard_content = IO.read(vcard_file)
expect(vcard_content).to include contact.surname
dto = api.contact.from_file(
  ContactFromFileRequest.new(
    format: 'VCard',
    file: vcard_file))
expect(dto.surname).to eq contact.surname
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const surname = 'Cane';
const contactDto = new ContactDto();
contactDto.surname = surname;
contactDto.givenName = 'John';
contactDto.gender = 'Male';
const emailAddress = new EmailAddress();
emailAddress.address = 'address@aspose.com'
contactDto.emailAddresses = [emailAddress];
contactDto.phoneNumbers = [
    new PhoneNumber(undefined, '+47234325344')];
const mapi = await api.contact.asFile(
    new ContactAsFileRequest('Msg', contactDto));
const vcard = await api.contact.convert(
    new ContactConvertRequest(
        'VCard', 'Msg', mapi));
const vcardString = vcard.toString();
expect(vcardString).to.include(surname);
const dto = await api.contact.fromFile(
    new ContactFromFileRequest('VCard', vcard));
expect(dto.surname).to.be.equal(surname);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$contactDto = (new ContactDto())
    ->setSurname('Cane')
    ->setGivenName('John')
    ->setGender('Male')
    ->setEmailAddresses(array(
        (new EmailAddress())->setAddress(
            'address@aspose.com')))
    ->setPhoneNumbers(array(
        (new PhoneNumber())->setNumber(
            '+47235456456')));
$mapi = $api->contact()->asFile(new ContactAsFileRequest('Msg', $contactDto));
$vcard = $api->contact()->convert(new ContactConvertRequest('VCard', 'Msg', $mapi));
$fileContent = $vcard->fread($vcard->getSize());
$this->assertRegExp("/" . $contactDto->getSurname() . "/", $fileContent);
$dto = $api->contact()->fromFile(new ContactFromFileRequest('VCard', $vcard));
$this->assertEquals($contactDto->getSurname(), $dto->getSurname());
```

{{< /tab >}}

{{< /tabs >}}

## **Convert Email Messages**

{{% alert color="primary" %}}

This tutorial describes only the file conversion API. To get more information about Email messages API usage see [**Email Message Files API Tutorial**](/emailcloud/email-message-files/).

{{% /alert %}} 

The email message can be represented as an [**EmailDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailDto.md) object. This object can be converted into an EML, MSG, MHTM, HTML file. Files can be converted to each other and back to the [**EmailDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailDto.md) object. The code below demonstrates all email message conversion methods:

{{< tabs tabTotal="6" tabID="6" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
EmailDto email => new EmailDto
{
    Subject = "Re: Some subject",
    Body = "Some body",
    IsBodyHtml = true,
    HtmlBody = "<b>Some body</b>",
    BodyType = "Html",
    IsDraft = true,
    Attachments = new List<Attachment>
    {
        new Attachment
        {
            Base64Data =
                Convert.ToBase64String(Encoding.UTF8.GetBytes("Some file content")),
            Name = "some-file.txt"
        }
    },
    DeliveryNotificationOptions = new List<string> {"OnSuccess", "Delay"},
    From = new MailAddress {Address = FromAddress, DisplayName = "From Address"},
    To = new List<MailAddress>
        {new MailAddress {Address = "to@aspose.com", DisplayName = "To Address"}}
};

var mapiStream = await api.Email.AsFileAsync(
    new EmailAsFileRequest("Msg", email));
var emlStream = await api.Email.ConvertAsync(
    new EmailConvertRequest("Msg", "Eml", mapiStream));
using (var memoryStream = new MemoryStream())
{
    await emlStream.CopyToAsync(memoryStream);
    var emlString = Encoding.UTF8.GetString(memoryStream.ToArray());
    Assert.IsTrue(emlString.Contains(FromAddress));
}

emlStream.Seek(0, SeekOrigin.Begin);
var dto = await api.Email.FromFileAsync(
    new EmailFromFileRequest("Eml", emlStream));
Assert.AreEqual(FromAddress, dto.From.Address);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
String from = "from@aspose.com";
EmailDto emailDto = new EmailDto()
    .from(new MailAddress().address(from))
    .addToItem(new MailAddress().address("to@aspose.com"))
    .subject("Some subject")
    .body("Some body")
    .date(new Date());

byte[] mapiBytes = api.email().asFile(
    new EmailAsFileRequest("Msg", emailDto));
byte[] emlBytes = api.email().convert(
    new EmailConvertRequest("Msg", "Eml", mapiBytes));
String emlContent = new String(emlBytes, "UTF-8");
assert emlContent.contains(from);
EmailDto dto = api.email().fromFile(
    new EmailFromFileRequest("Eml", emlBytes));
assert from.equals(dto.getFrom().getAddress());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
email_document = models.EmailDto(
    _from=models.MailAddress(address='from@aspose.com'),
    to=[models.MailAddress(address='to@aspose.com')],
    subject='Some subject',
    body='Some body',
    _date=datetime.today())

mapi = api.email.as_file(
    models.EmailAsFileRequest('Msg', email_document))
eml = api.email.convert(
    models.EmailConvertRequest('Msg', 'Eml', mapi))
with open(eml, 'r') as f:
    file_data = f.read()
    assert email_document._from.address in file_data
dto = api.email.from_file(
    models.EmailFromFileRequest('Eml', eml))
assert email_document._from.address == dto._from.address
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
email = EmailDto.new(
  from: MailAddress.new(address: 'from@aspose.com'),
  to: [MailAddress.new(address: 'to@aspose.com')],
  subject: 'Some subject',
  body: 'Some body',
  date: DateTime.now)
mapi_file = api.email.as_file(
  EmailAsFileRequest.new(format: 'Msg', value: email))
eml_file = api.email.convert(
  EmailConvertRequest.new(
    from_format: 'Msg',
    to_format: 'Eml',
    file: mapi_file))
eml_content = IO.read(eml_file)
expect(eml_content).to include email.from.address
dto = api.email.from_file(
  EmailFromFileRequest.new(
    format: 'Eml', file: eml_file))
expect(dto.from.address).to eq email.from.address
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const emailDto = new EmailDto();
emailDto.from = new MailAddress(undefined, from);
emailDto.to = [new MailAddress(undefined, 'to@aspose.com')];
emailDto.subject = 'Some subject';
emailDto.body = 'Some body';
emailDto.date = new Date();

const mapi = await api.email.asFile(
    new EmailAsFileRequest('Msg', emailDto));
const eml = await api.email.convert(
    new EmailConvertRequest('Msg', 'Eml', mapi));
const emlString = eml.toString();
expect(emlString).to.include(from);
const dto = await api.email.fromFile(
    new EmailFromFileRequest('Eml', eml));
expect(dto.from.address).to.be.equal(from);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$emailDto = (new EmailDto())
    ->setFrom(new MailAddress(null, 'from@aspose.com'))
    ->setTo(array(new MailAddress(null, 'to@aspose.com')))
    ->setSubject('Some subject')
    ->setBody('Some body')
    ->setDate(new DateTime());

$mapi = $api->email()->asFile(
    new EmailAsFileRequest('Msg', $emailDto));
$eml = $api->email()->convert(
    new EmailConvertRequest('Msg', 'Eml', $mapi));
$fileContent = $eml->fread($eml->getSize());
$this->assertRegExp(
    "/" . $emailDto->getFrom()->getAddress() . "/",
    $fileContent);
$dto = $api->email()->fromFile(
    new EmailFromFileRequest('Eml', $eml));
$this->assertEquals(
    $emailDto->getFrom()->getAddress(),
    $dto->getFrom()->getAddress());
```

{{< /tab >}}

{{< /tabs >}}


## **More Tutorials**
See more Aspose Email Tutorials: 
