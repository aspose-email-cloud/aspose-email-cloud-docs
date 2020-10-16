---
title: "MapiContactAsFileRequest"
type: docs
url: /reference-model-mapi-contact-as-file-request/
weight: 1
---
Convert MapiContact to file request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Format** | **string** | Enumerates contact formats. Enum, available values: VCard, WebDav, Msg | 
**Value** | [**MapiContactDto**](/email/reference-model-mapi-contact-dto/) | MAPI contact model.              | 


## Example

{{< tabs tabTotal="6" tabID="mapi_contact_as_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var mapiContactAsFileRequest = new MapiContactAsFileRequest
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
MapiContactAsFileRequest mapiContactAsFileRequest = Models.mapiContactAsFileRequest()
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
mapi_contact_as_file_request = models.MapiContactAsFileRequest(
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
mapi_contact_as_file_request = MapiContactAsFileRequest.new(
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
let mapiContactAsFileRequest = Models.mapiContactAsFileRequest()
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
$mapiContactAsFileRequest = Models::mapiContactAsFileRequest()
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

