---
title: "Contact"
type: docs
url: /reference-mapi-contact-api/
weight: 1
---

MAPI contact operations



## AsContactDto

Converts MAPI contact model to ContactDto model. 
Returns [**ContactDto**](/email/reference-model-contact-dto/) model. Requires:

{{< expand-list title="mapiContactDto" >}}

MAPI contact model to convert. Type: [**MapiContactDto**](/email/reference-model-mapi-contact-dto/).

{{< tabs tabTotal="6" tabID="mapi_contact_as_contact_dto_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var mapiContactDto = new MapiContactDto
{
    ElectronicAddresses = new MapiContactElectronicAddressPropertySetDto
    {
        DefaultEmailAddress = new MapiContactElectronicAddressDto
        {
            EmailAddress = "email@aspose.com"
        }
    },
    NameInfo = new MapiContactNamePropertySetDto
    {
        GivenName = "Alex",
        Surname = "Thomas"
    },
    PersonalInfo = new MapiContactPersonalInfoPropertySetDto
    {
        BusinessHomePage = "www.aspose.com"
    },
    ProfessionalInfo = new MapiContactProfessionalPropertySetDto
    {
        Profession = "GENERAL DIRECTOR"
    },
    Telephones = new MapiContactTelephonePropertySetDto
    {
        PrimaryTelephoneNumber = "+49 211 4247 21"
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiContactDto mapiContactDto = Models.mapiContactDto()
    .electronicAddresses(Models.mapiContactElectronicAddressPropertySetDto()
        .defaultEmailAddress(Models.mapiContactElectronicAddressDto()
            .emailAddress("email@aspose.com")
            .build())
        .build())
    .nameInfo(Models.mapiContactNamePropertySetDto()
        .givenName("Alex")
        .surname("Thomas")
        .build())
    .personalInfo(Models.mapiContactPersonalInfoPropertySetDto()
        .businessHomePage("www.aspose.com")
        .build())
    .professionalInfo(Models.mapiContactProfessionalPropertySetDto()
        .profession("GENERAL DIRECTOR")
        .build())
    .telephones(Models.mapiContactTelephonePropertySetDto()
        .primaryTelephoneNumber("+49 211 4247 21")
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
mapi_contact_dto = models.MapiContactDto(
    electronic_addresses=models.MapiContactElectronicAddressPropertySetDto(
        default_email_address=models.MapiContactElectronicAddressDto(
            email_address='email@aspose.com')),
    name_info=models.MapiContactNamePropertySetDto(
        given_name='Alex',
        surname='Thomas'),
    personal_info=models.MapiContactPersonalInfoPropertySetDto(
        business_home_page='www.aspose.com'),
    professional_info=models.MapiContactProfessionalPropertySetDto(
        profession='GENERAL DIRECTOR'),
    telephones=models.MapiContactTelephonePropertySetDto(
        primary_telephone_number='+49 211 4247 21'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
mapi_contact_dto = MapiContactDto.new(
  electronic_addresses: MapiContactElectronicAddressPropertySetDto.new(
    default_email_address: MapiContactElectronicAddressDto.new(
      email_address: 'email@aspose.com')),
  name_info: MapiContactNamePropertySetDto.new(
    given_name: 'Alex',
    surname: 'Thomas'),
  personal_info: MapiContactPersonalInfoPropertySetDto.new(
    business_home_page: 'www.aspose.com'),
  professional_info: MapiContactProfessionalPropertySetDto.new(
    profession: 'GENERAL DIRECTOR'),
  telephones: MapiContactTelephonePropertySetDto.new(
    primary_telephone_number: '+49 211 4247 21'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let mapiContactDto = Models.mapiContactDto()
    .electronicAddresses(Models.mapiContactElectronicAddressPropertySetDto()
        .defaultEmailAddress(Models.mapiContactElectronicAddressDto()
            .emailAddress('email@aspose.com')
            .build())
        .build())
    .nameInfo(Models.mapiContactNamePropertySetDto()
        .givenName('Alex')
        .surname('Thomas')
        .build())
    .personalInfo(Models.mapiContactPersonalInfoPropertySetDto()
        .businessHomePage('www.aspose.com')
        .build())
    .professionalInfo(Models.mapiContactProfessionalPropertySetDto()
        .profession('GENERAL DIRECTOR')
        .build())
    .telephones(Models.mapiContactTelephonePropertySetDto()
        .primaryTelephoneNumber('+49 211 4247 21')
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mapi_contact_dto = Models::mapiContactDto()
    ->electronicAddresses(Models::mapiContactElectronicAddressPropertySetDto()
        ->defaultEmailAddress(Models::mapiContactElectronicAddressDto()
            ->emailAddress('email@aspose.com')
            ->build())
        ->build())
    ->nameInfo(Models::mapiContactNamePropertySetDto()
        ->givenName('Alex')
        ->surname('Thomas')
        ->build())
    ->personalInfo(Models::mapiContactPersonalInfoPropertySetDto()
        ->businessHomePage('www.aspose.com')
        ->build())
    ->professionalInfo(Models::mapiContactProfessionalPropertySetDto()
        ->profession('GENERAL DIRECTOR')
        ->build())
    ->telephones(Models::mapiContactTelephonePropertySetDto()
        ->primaryTelephoneNumber('+49 211 4247 21')
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="mapi_contact_as_contact_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Mapi.Contact.AsContactDtoAsync(mapiContactDto);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactDto result = api.mapi().contact().asContactDto(mapiContactDto);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.mapi.contact.as_contact_dto(mapi_contact_dto)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.mapi.contact.as_contact_dto(mapi_contact_dto)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.mapi.contact.asContactDto(mapiContactDto);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->mapi()->contact()->asContactDto($mapi_contact_dto);
```

{{< /tab >}}

{{< /tabs >}}
## AsFile

Converts MAPI contact model to specified format and returns as file. 
Returns a **File**. Requires:

{{< expand-list title="request" >}}

MAPI contact model to convert. Type: [**MapiContactAsFileRequest**](/email/reference-model-mapi-contact-as-file-request/).

{{< tabs tabTotal="6" tabID="mapi_contact_as_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiContactAsFileRequest
{
    Format = "Msg",
    Value = new MapiContactDto
    {
        ElectronicAddresses = new MapiContactElectronicAddressPropertySetDto
        {
            DefaultEmailAddress = new MapiContactElectronicAddressDto
            {
                EmailAddress = "email@aspose.com"
            }
        },
        NameInfo = new MapiContactNamePropertySetDto
        {
            GivenName = "Alex",
            Surname = "Thomas"
        },
        PersonalInfo = new MapiContactPersonalInfoPropertySetDto
        {
            BusinessHomePage = "www.aspose.com"
        },
        ProfessionalInfo = new MapiContactProfessionalPropertySetDto
        {
            Profession = "GENERAL DIRECTOR"
        },
        Telephones = new MapiContactTelephonePropertySetDto
        {
            PrimaryTelephoneNumber = "+49 211 4247 21"
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiContactAsFileRequest request = Models.mapiContactAsFileRequest()
    .format("Msg")
    .value(Models.mapiContactDto()
        .electronicAddresses(Models.mapiContactElectronicAddressPropertySetDto()
            .defaultEmailAddress(Models.mapiContactElectronicAddressDto()
                .emailAddress("email@aspose.com")
                .build())
            .build())
        .nameInfo(Models.mapiContactNamePropertySetDto()
            .givenName("Alex")
            .surname("Thomas")
            .build())
        .personalInfo(Models.mapiContactPersonalInfoPropertySetDto()
            .businessHomePage("www.aspose.com")
            .build())
        .professionalInfo(Models.mapiContactProfessionalPropertySetDto()
            .profession("GENERAL DIRECTOR")
            .build())
        .telephones(Models.mapiContactTelephonePropertySetDto()
            .primaryTelephoneNumber("+49 211 4247 21")
            .build())
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.MapiContactAsFileRequest(
    format='Msg',
    value=models.MapiContactDto(
        electronic_addresses=models.MapiContactElectronicAddressPropertySetDto(
            default_email_address=models.MapiContactElectronicAddressDto(
                email_address='email@aspose.com')),
        name_info=models.MapiContactNamePropertySetDto(
            given_name='Alex',
            surname='Thomas'),
        personal_info=models.MapiContactPersonalInfoPropertySetDto(
            business_home_page='www.aspose.com'),
        professional_info=models.MapiContactProfessionalPropertySetDto(
            profession='GENERAL DIRECTOR'),
        telephones=models.MapiContactTelephonePropertySetDto(
            primary_telephone_number='+49 211 4247 21')))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = MapiContactAsFileRequest.new(
  format: 'Msg',
  value: MapiContactDto.new(
    electronic_addresses: MapiContactElectronicAddressPropertySetDto.new(
      default_email_address: MapiContactElectronicAddressDto.new(
        email_address: 'email@aspose.com')),
    name_info: MapiContactNamePropertySetDto.new(
      given_name: 'Alex',
      surname: 'Thomas'),
    personal_info: MapiContactPersonalInfoPropertySetDto.new(
      business_home_page: 'www.aspose.com'),
    professional_info: MapiContactProfessionalPropertySetDto.new(
      profession: 'GENERAL DIRECTOR'),
    telephones: MapiContactTelephonePropertySetDto.new(
      primary_telephone_number: '+49 211 4247 21')))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.mapiContactAsFileRequest()
    .format('Msg')
    .value(Models.mapiContactDto()
        .electronicAddresses(Models.mapiContactElectronicAddressPropertySetDto()
            .defaultEmailAddress(Models.mapiContactElectronicAddressDto()
                .emailAddress('email@aspose.com')
                .build())
            .build())
        .nameInfo(Models.mapiContactNamePropertySetDto()
            .givenName('Alex')
            .surname('Thomas')
            .build())
        .personalInfo(Models.mapiContactPersonalInfoPropertySetDto()
            .businessHomePage('www.aspose.com')
            .build())
        .professionalInfo(Models.mapiContactProfessionalPropertySetDto()
            .profession('GENERAL DIRECTOR')
            .build())
        .telephones(Models.mapiContactTelephonePropertySetDto()
            .primaryTelephoneNumber('+49 211 4247 21')
            .build())
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::mapiContactAsFileRequest()
    ->format('Msg')
    ->value(Models::mapiContactDto()
        ->electronicAddresses(Models::mapiContactElectronicAddressPropertySetDto()
            ->defaultEmailAddress(Models::mapiContactElectronicAddressDto()
                ->emailAddress('email@aspose.com')
                ->build())
            ->build())
        ->nameInfo(Models::mapiContactNamePropertySetDto()
            ->givenName('Alex')
            ->surname('Thomas')
            ->build())
        ->personalInfo(Models::mapiContactPersonalInfoPropertySetDto()
            ->businessHomePage('www.aspose.com')
            ->build())
        ->professionalInfo(Models::mapiContactProfessionalPropertySetDto()
            ->profession('GENERAL DIRECTOR')
            ->build())
        ->telephones(Models::mapiContactTelephonePropertySetDto()
            ->primaryTelephoneNumber('+49 211 4247 21')
            ->build())
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="mapi_contact_as_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Mapi.Contact.AsFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.mapi().contact().asFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.mapi.contact.as_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.mapi.contact.as_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.mapi.contact.asFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->mapi()->contact()->asFile($request);
```

{{< /tab >}}

{{< /tabs >}}
## FromFile

Converts contact file to a MAPI model representation. 
Returns [**MapiContactDto**](/email/reference-model-mapi-contact-dto/) model. Requires:

{{< expand-list title="request" >}}

FromFile method request. Type: [**MapiContactFromFileRequest**](/email/reference-model-mapi-contact-from-file-request/).

{{< tabs tabTotal="6" tabID="mapi_contact_from_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiContactFromFileRequest
{ 
    Format = "Msg",
    File = new MemoryStream(File.ReadAllBytes("/path/to/contact.msg"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiContactFromFileRequest request = Models.mapiContactFromFileRequest()
    .format("Msg")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/contact.msg")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.MapiContactFromFileRequest(
    format='Msg',
    file='/path/to/contact.msg')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = MapiContactFromFileRequest.new(
    format: 'Msg',
    file: File.new('/path/to/contact.msg'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.MapiContactFromFileRequest()
    .format('Msg')
    .file(fs.readFileSync('/path/to/contact.msg'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::MapiContactFromFileRequest()
    ->format('Msg')
    ->file(new SplFileObject('/path/to/contact.msg'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="mapi_contact_from_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Mapi.Contact.FromFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiContactDto result = api.mapi().contact().fromFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.mapi.contact.from_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.mapi.contact.from_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.mapi.contact.fromFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->mapi()->contact()->fromFile($request);
```

{{< /tab >}}

{{< /tabs >}}
## Get

Get MAPI contact document. 
Returns [**MapiContactDto**](/email/reference-model-mapi-contact-dto/) model. Requires:

{{< expand-list title="request" >}}

Get method request. Type: [**MapiContactGetRequest**](/email/reference-model-mapi-contact-get-request/).

{{< tabs tabTotal="6" tabID="mapi_contact_get_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiContactGetRequest
{ 
    Format = "VCard",
    FileName = "contact.vcf",
    Folder = "folder/on/storage",
    Storage = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiContactGetRequest request = Models.mapiContactGetRequest()
    .format("VCard")
    .fileName("contact.vcf")
    .folder("folder/on/storage")
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.MapiContactGetRequest(
    format='VCard',
    file_name='contact.vcf',
    folder='folder/on/storage',
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = MapiContactGetRequest.new(
    format: 'VCard',
    file_name: 'contact.vcf',
    folder: 'folder/on/storage',
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.MapiContactGetRequest()
    .format('VCard')
    .fileName('contact.vcf')
    .folder('folder/on/storage')
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::MapiContactGetRequest()
    ->format('VCard')
    ->file_name('contact.vcf')
    ->folder('folder/on/storage')
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="mapi_contact_get_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Mapi.Contact.GetAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiContactDto result = api.mapi().contact().get(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.mapi.contact.get(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.mapi.contact.get(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.mapi.contact.get(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->mapi()->contact()->get($request);
```

{{< /tab >}}

{{< /tabs >}}
## Save

Save MAPI Contact to storage. Requires:

{{< expand-list title="request" >}}

Create/Update contact request. Type: [**MapiContactSaveRequest**](/email/reference-model-mapi-contact-save-request/).

{{< tabs tabTotal="6" tabID="mapi_contact_save_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiContactSaveRequest
{
    Format = "Msg",
    StorageFile = new StorageFileLocation
    {
        FileName = "contact.msg",
        Storage = "First Storage",
        FolderPath = "file/location/folder/on/storage"
    },
    Value = new MapiContactDto
    {
        ElectronicAddresses = new MapiContactElectronicAddressPropertySetDto
        {
            DefaultEmailAddress = new MapiContactElectronicAddressDto
            {
                EmailAddress = "email@aspose.com"
            }
        },
        NameInfo = new MapiContactNamePropertySetDto
        {
            GivenName = "Alex",
            Surname = "Thomas"
        },
        PersonalInfo = new MapiContactPersonalInfoPropertySetDto
        {
            BusinessHomePage = "www.aspose.com"
        },
        ProfessionalInfo = new MapiContactProfessionalPropertySetDto
        {
            Profession = "GENERAL DIRECTOR"
        },
        Telephones = new MapiContactTelephonePropertySetDto
        {
            PrimaryTelephoneNumber = "+49 211 4247 21"
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiContactSaveRequest request = Models.mapiContactSaveRequest()
    .format("Msg")
    .storageFile(Models.storageFileLocation()
        .fileName("contact.msg")
        .storage("First Storage")
        .folderPath("file/location/folder/on/storage")
        .build())
    .value(Models.mapiContactDto()
        .electronicAddresses(Models.mapiContactElectronicAddressPropertySetDto()
            .defaultEmailAddress(Models.mapiContactElectronicAddressDto()
                .emailAddress("email@aspose.com")
                .build())
            .build())
        .nameInfo(Models.mapiContactNamePropertySetDto()
            .givenName("Alex")
            .surname("Thomas")
            .build())
        .personalInfo(Models.mapiContactPersonalInfoPropertySetDto()
            .businessHomePage("www.aspose.com")
            .build())
        .professionalInfo(Models.mapiContactProfessionalPropertySetDto()
            .profession("GENERAL DIRECTOR")
            .build())
        .telephones(Models.mapiContactTelephonePropertySetDto()
            .primaryTelephoneNumber("+49 211 4247 21")
            .build())
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.MapiContactSaveRequest(
    format='Msg',
    storage_file=models.StorageFileLocation(
        file_name='contact.msg',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'),
    value=models.MapiContactDto(
        electronic_addresses=models.MapiContactElectronicAddressPropertySetDto(
            default_email_address=models.MapiContactElectronicAddressDto(
                email_address='email@aspose.com')),
        name_info=models.MapiContactNamePropertySetDto(
            given_name='Alex',
            surname='Thomas'),
        personal_info=models.MapiContactPersonalInfoPropertySetDto(
            business_home_page='www.aspose.com'),
        professional_info=models.MapiContactProfessionalPropertySetDto(
            profession='GENERAL DIRECTOR'),
        telephones=models.MapiContactTelephonePropertySetDto(
            primary_telephone_number='+49 211 4247 21')))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = MapiContactSaveRequest.new(
  format: 'Msg',
  storage_file: StorageFileLocation.new(
    file_name: 'contact.msg',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'),
  value: MapiContactDto.new(
    electronic_addresses: MapiContactElectronicAddressPropertySetDto.new(
      default_email_address: MapiContactElectronicAddressDto.new(
        email_address: 'email@aspose.com')),
    name_info: MapiContactNamePropertySetDto.new(
      given_name: 'Alex',
      surname: 'Thomas'),
    personal_info: MapiContactPersonalInfoPropertySetDto.new(
      business_home_page: 'www.aspose.com'),
    professional_info: MapiContactProfessionalPropertySetDto.new(
      profession: 'GENERAL DIRECTOR'),
    telephones: MapiContactTelephonePropertySetDto.new(
      primary_telephone_number: '+49 211 4247 21')))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.mapiContactSaveRequest()
    .format('Msg')
    .storageFile(Models.storageFileLocation()
        .fileName('contact.msg')
        .storage('First Storage')
        .folderPath('file/location/folder/on/storage')
        .build())
    .value(Models.mapiContactDto()
        .electronicAddresses(Models.mapiContactElectronicAddressPropertySetDto()
            .defaultEmailAddress(Models.mapiContactElectronicAddressDto()
                .emailAddress('email@aspose.com')
                .build())
            .build())
        .nameInfo(Models.mapiContactNamePropertySetDto()
            .givenName('Alex')
            .surname('Thomas')
            .build())
        .personalInfo(Models.mapiContactPersonalInfoPropertySetDto()
            .businessHomePage('www.aspose.com')
            .build())
        .professionalInfo(Models.mapiContactProfessionalPropertySetDto()
            .profession('GENERAL DIRECTOR')
            .build())
        .telephones(Models.mapiContactTelephonePropertySetDto()
            .primaryTelephoneNumber('+49 211 4247 21')
            .build())
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::mapiContactSaveRequest()
    ->format('Msg')
    ->storageFile(Models::storageFileLocation()
        ->fileName('contact.msg')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
    ->value(Models::mapiContactDto()
        ->electronicAddresses(Models::mapiContactElectronicAddressPropertySetDto()
            ->defaultEmailAddress(Models::mapiContactElectronicAddressDto()
                ->emailAddress('email@aspose.com')
                ->build())
            ->build())
        ->nameInfo(Models::mapiContactNamePropertySetDto()
            ->givenName('Alex')
            ->surname('Thomas')
            ->build())
        ->personalInfo(Models::mapiContactPersonalInfoPropertySetDto()
            ->businessHomePage('www.aspose.com')
            ->build())
        ->professionalInfo(Models::mapiContactProfessionalPropertySetDto()
            ->profession('GENERAL DIRECTOR')
            ->build())
        ->telephones(Models::mapiContactTelephonePropertySetDto()
            ->primaryTelephoneNumber('+49 211 4247 21')
            ->build())
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="mapi_contact_save_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Mapi.Contact.SaveAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.mapi().contact().save(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.mapi.contact.save(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.mapi.contact.save(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.mapi.contact.save(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->mapi()->contact()->save($request);
```

{{< /tab >}}

{{< /tabs >}}

## More APIs

{{< list-of-articles-in-this-section >}}
