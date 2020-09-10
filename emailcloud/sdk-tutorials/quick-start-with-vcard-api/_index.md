---
title: "Quick Start With VCard API"
type: docs
url: /quick-start-with-vcard-api/
description: "Aspose Email tutorial — how to work with contact card files using Aspose.Email Cloud. Create, edit, process VCard, scan business card images to VCard."
weight: 50
---

## **VCard API**
[Aspose.Email Cloud API](https://products.aspose.cloud/email/family) supports working with VCard files. You can use our API to read, edit and save VCard files. Also, you can use our Business card recognition API to parse VCard file from image.

The SDKs support two different ways of operating with VCard files using MapiContactDto and ContactDto. This tutorial shows how to use ContactDto.

{{% alert color="primary" %}} To see how to setup SDKs use the [SDK setup](/sdk-setup/) tutorial. {{% /alert %}} 
## **How to Create Contact File Object and Save It to Storage**
**ContactDto** object contains all contact’s information such as gender, surname, email addresses, phone numbers, etc.

Let’s create a **ContactDto** object and save it to the Storage as **.vcf** file.

To save **ContactDto** use [**SaveAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactApi.md#SaveAsync) from [**ContactApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactApi.md). This method requires **1 parameter** — [**ContactSaveRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactSaveRequest.md), which is a request for this operation.

[**ContactSaveRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactSaveRequest.md) has **3 parameters**:

- *Format* — Contact document format. Enum, available values: VCard, WebDav, Msg.
- *StorageFile* — Contact document location on storage. This parameter accepts [**StorageFileLocation**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/StorageFileLocation.md) object.
- *Value* — [**ContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactDto.md) object.

**How to create ContactDto object and save it to the Storage?**

{{< tabs tabTotal="6" tabID="1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var contact = new ContactDto
{
    Gender = "Male", Surname = "Thomas", GivenName = "Alex",
    EmailAddresses = new List<EmailAddress>
    {
        new EmailAddress
        {
            Category = new EnumWithCustomOfEmailAddressCategory("Work", null),
            Address = "alex.thomas@work.com", Preferred = true,
            DisplayName = "Alex Thomas"
        }
    },
    PhoneNumbers = new List<PhoneNumber>
    {
        new PhoneNumber
        {
            Category = new EnumWithCustomOfPhoneNumberCategory("Work", null),
            Number = "+49211424721", Preferred = true
        }
    }
};

var storage = "First storage";
var folder = "path/to/folder/on/storage";
var contactFile = $"contact.vcf";
await api.Contact.SaveAsync(
    new ContactSaveRequest(
        new StorageFileLocation(storage, folder, contactFile),
        contact, "VCard"));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactDto contact = new ContactDto()
    .gender("Male")
    .surname("Thomas")
    .givenName("Alex")
    .addEmailAddressesItem(new EmailAddress(
        new EnumWithCustomOfEmailAddressCategory("Work", null),
        "Alex Thomas", true, null, "alex.thomas@work.com"))
    .addPhoneNumbersItem(new PhoneNumber(
        new EnumWithCustomOfPhoneNumberCategory("Work", null),
        "+49211424721", true));

String storage = "First storage";
String folder = "path/to/folder/on/storage";
String contactFile = "contact.vcf";

api.contact().save(
    new ContactSaveRequest(
        new StorageFileLocation(storage, folder, contactFile),
        contact, "VCard"));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
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

storage = 'First storage'
folder = 'path/to/folder/on/storage'
contact_file = 'contact.vcf'
api.contact.save(
    models.ContactSaveRequest(
        models.StorageFileLocation(storage, folder, contact_file),
        contact, 'VCard'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
contact = ContactDto.new(
  surname: 'Cane',
  given_name: 'John',
  gender: 'Male',
  email_addresses: [EmailAddress.new(address: 'address@aspose.com')],
  phone_numbers: [PhoneNumber.new(number: '+4734534643')])

storage = 'First storage'
folder = 'path/to/folder/on/storage'
contact_file = 'contact.vcf'
api.contact.save(
  ContactSaveRequest.new(
    storage_file: StorageFileLocation.new(
      storage: storage,
      folder_path: folder,
      file_name: contact_file),
    value: contact,
    format: 'VCard'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
var contact = new ContactDto();
contact.gender = 'Male';
contact.surname = 'Thomas';
contact.givenName = 'Alex';
contact.emailAddresses = [new EmailAddress(
    new EnumWithCustomOfEmailAddressCategory('Work'),
    'Alex Thomas', true, undefined, 'alex.thomas@work.com')];
contact.phoneNumbers = [new PhoneNumber(
    new EnumWithCustomOfPhoneNumberCategory('Work'),
    '+49211424721', true)];

var storage = 'First storage';
var folder = 'path/to/folder/on/storage';
var contactFile = 'contact.vcf';
await api.contact.save(
    new ContactSaveRequest(
        new StorageFileLocation(storage, folder, contactFile),
        contact, 'VCard'));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$contact = (new ContactDto())
    ->setGender("Male")
    ->setSurname("Thomas")
    ->setGivenName("Alex")
    ->setEmailAddresses(array(new EmailAddress(
        new EnumWithCustomOfEmailAddressCategory("Work"),
        "Alex Thomas", true, null, "alex.thomas@work.com")))
    ->setPhoneNumbers(array(new PhoneNumber(
        new EnumWithCustomOfPhoneNumberCategory("Work"),
        "+49211424721", true)));

$storage = "First storage";
$folder = "path/to/folder/on/storage";
$contactFile = "contact.vcf";

api->contact()->save(new ContactSaveRequest(
    new StorageFileLocation($storage, $folder, $contactFile),
    $contact,
    "VCard"
));
```

{{< /tab >}}

{{< /tabs >}}
## **How to Download VCard File From Storage**
You can find the saved file on [Aspose.Cloud Dashboard](https://dashboard.aspose.cloud/#/files), or download it using SDK.

To find the contact card file on Storage use [**DownloadFileAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/FileApi.md#downloadfileasync) from [**FileApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/FileApi.md). This method requires **1 parameter** — [**DownloadFileRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/Model/DownloadFileRequest.cs), which is a request for this operation.

[**DownloadFileRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/Model/DownloadFileRequest.cs) has **3 parameters**:

- *Path* — File path e.g. "/folder/contact.vcf".
- *StorageName* — Storage name.
- *VersionId* [**optional**] — File version ID to download

**How to download VCard file from the Storage?**

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var resultStream = await api.CloudStorage.File.DownloadFileAsync(
    new DownloadFileRequest($"{folder}/{contactFile}", storage));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.cloudStorage().file().downloadFile(
    new DownloadFileRequest(folder + "/" + contactFile, storage, null));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
downloaded_file_location = api.cloud_storage.file.download_file(
    models.DownloadFileRequest(folder + '/' + contact_file, storage))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
downloaded_file_location = api.cloud_storage.file.download_file(
    DownloadFileRequest.new(folder + '/' + contact_file, storage))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
var downloaded = await api.cloudStorage.file.downloadFile(
    new DownloadFileRequest(folder + '/' + contactFile, storage));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$downloaded = $api->cloudStorage()->file()->downloadFile(
    new DownloadFileRequest($folder.'/'.$contactFile, $storage));
$fileContent = $downloaded->fread($downloaded->getSize());
```

{{< /tab >}}

{{< /tabs >}}
## **How to Get VCard File From Storage as ContactDto Object**
Let's get this file from storage as a ContactDto object.

To get a contact card file from Storage as **ContactDto** use [**GetAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactApi.md#GetAsync) from [**ContactApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactApi.md). This method requires **1 parameter** — **ContactGetRequest**, which is a request for this operation.

**ContactGetRequest** has **4 parameters**:

- *Format —* Contact document format. Enum, available values: VCard, WebDav, Msg.
- *FileName* — VCard file name in storage.
- *Folder* — Path to the folder in storage.
- *Storage* — Storage name.

**How to get VCard file from the Storage as a ContactDto object?**

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var contactDto = await api.Contact.GetAsync(new ContactGetRequest(
    "VCard", contactFile, folder, storage));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactDto contactDto = api.contact().get(new ContactGetRequest(
    "VCard", contactFile, folder, storage));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
contact_dto = api.contact.get(models.ContactGetRequest(
    'VCard', contact_file, folder, storage))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
contact_dto = api.contact.get(
  ContactGetRequest.new(
    format: 'VCard',
    file_name: contact_file,
    folder: folder,
    storage: storage))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
var contactDto = await api.contact.get(new ContactGetRequest(
    'VCard', contactFile, folder, storage));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$contactDto = api->contact()->get(new ContactGetRequest(
    'VCard', $contactFile, $folder, $storage));
```

{{< /tab >}}

{{< /tabs >}}

You can change model fields and save it again. The file will be rewritten if you don't change file name and location.
## **How to Use Business Card Recognition API**

{{% alert color="primary" %}} To get more information take a look at the [Business Cards Recognition API](/developer-guide/working-with-contact-cards/business-cards-recognition-api/). {{% /alert %}} 

Now, let's use our **Business Card Recognition API**.

First, we need an image of a business card. Something like this:

![alex.png](quick-start-with-vcard-api_1.png)

This file should be placed somewhere on the disk, for example at "*/tmp/alex.png*".

To parse an image of a contact card use [**ParseAsync**]https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/AiBcrApi.md#ParseAsync) from [**AiBcrApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/AiBcrApi.md). This method requires **1 parameter** — **AiBcrParseRequest**, which is a request for this operation.

**AiBcrParseRequest** has **4 parameters**:

- *Languages* — Comma-separated ISO-639 codes of languages (either 639-1 or 639-3; i.e. "it" or "ita" for Italian); it's "" by default.
- *Countries* — Comma-separated codes of countries.
- *File* — Vcard file.
- *IsSingle* — Determines that image contains single VCard or more. Ignored in the current version.

**How to parse an image of business card to VCard?**

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
using (var file = File.OpenRead("alex.png"))
{
    ContactList result = await api.Ai.Bcr.ParseAsync(
        new AiBcrParseRequest(file, isSingle: true));
    //...
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] file = IOUtils.toByteArray(
    new FileInputStream("alex.png"));
ContactList result = api.ai().bcr().parse(
  new AiBcrParseRequest(fileBytes, null, null, true));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.ai.bcr.parse(
  models.AiBcrParseRequest('alex.png'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
file = File.new('alex.png')
result = api.ai.bcr.parse(AiBcrParseRequest.new(
  file: file, is_single: true))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
const imageData = fs.readFileSync('alex.png');
const result = await api.ai.bcr.parse(
  new AiBcrParseRequest(imageData));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = self::api()->ai()->bcr()->parse(
    new AiBcrParseRequest(new SplFileObject("alex.png"))
);
```

{{< /tab >}}

{{< /tabs >}}
## **How to Get a List of VCard Files From One Folder**
You can get a list of VCard files stored in one folder on storage using a single API request. Files will be filtered by an extension (**.msg** for Msg format and **.vcf** for VCard) and read to list of ContactDto object. The method supports pagination.

To get a list of VCard files use [**GetListAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactApi.md#GetListAsync) from [**ContactApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactApi.md). This method requires **1 parameter** — **ContactGetListRequest**, which is a request for this operation.

**ContactGetListRequest** has **5 parameters**:

- *Format* — Contact document format. Enum, available values: VCard, WebDav, Msg.
- *Folder* — Path to the folder in storage.
- *Storage* — Storage name.
- *ItemsPerPage* — Count of items on page.
- *PageNumber* — Page number.

**How to get a list of VCard files stored in one folder?**

{{< tabs tabTotal="6" tabID="5" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
ContactStorageList contacts = await api.Contact.GetListAsync(
    new ContactGetListRequest(
        "VCard", folder, storage, 10, 0));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactStorageList contacts = api.contact().getList(
  new ContactGetListRequest(
    "VCard", folder, storage, 10, 0));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
contacts = api.contact.get_list(models.ContactGetListRequest(
    'VCard', folder, storage, 10, 0))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
contacts = api.contact.get_list(ContactGetListRequest.new(
  format: 'VCard',
  folder: folder,
  storage: storage,
  items_per_page: 10,
  page_number: 0))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
var contacts = api.contact.getList(new ContactGetListRequest(
    'VCard', folder, storage, 10, 0))
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$contacts = $api->contact()->getList(new ContactGetListRequest(
    'VCard', $folder, $storage, 10, 0));
```

{{< /tab >}}

{{< /tabs >}}


## **More Tutorials**
See more Aspose Email tutorials: 


