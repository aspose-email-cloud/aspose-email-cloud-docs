---
title: "MapiContactSaveRequest"
type: docs
url: /reference-model-mapi-contact-save-request/
weight: 1
---
MapiContact save to storage request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Format** | **string** | Enumerates contact formats./nEnum, available values: VCard, WebDav, Msg | 

Parent class: [StorageModelOfMapiContactDto](/email/reference-model-storage-model-of-mapi-contact-dto/)

## Example

{{< tabs tabTotal="6" tabID="mapi_contact_save_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var mapiContactSaveRequest = new MapiContactSaveRequest
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
MapiContactSaveRequest mapiContactSaveRequest = Models.mapiContactSaveRequest()
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
mapi_contact_save_request = models.MapiContactSaveRequest(
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
mapi_contact_save_request = MapiContactSaveRequest.new(
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
let mapiContactSaveRequest = Models.mapiContactSaveRequest()
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
$mapiContactSaveRequest = Models::mapiContactSaveRequest()
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

