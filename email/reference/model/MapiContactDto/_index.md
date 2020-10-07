---
title: "MapiContactDto"
type: docs
url: /reference-model-mapi-contact-dto/
weight: 1
---
Represents outlook contact information.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**ElectronicAddresses** | [**MapiContactElectronicAddressPropertySetDto**](/email/reference-model-mapi-contact-electronic-address-property-set-dto/) | Specify properties for up to three different e-mail addresses and three different fax addresses.              | [optional] 
**Events** | [**MapiContactEventPropertySetDto**](/email/reference-model-mapi-contact-event-property-set-dto/) | Specify events associated with a contact.              | [optional] 
**NameInfo** | [**MapiContactNamePropertySetDto**](/email/reference-model-mapi-contact-name-property-set-dto/) | The properties are used to specify the name of the person represented by the contact.              | [optional] 
**OtherFields** | [**MapiContactOtherPropertySetDto**](/email/reference-model-mapi-contact-other-property-set-dto/) | Specify other fields of contact.              | [optional] 
**PersonalInfo** | [**MapiContactPersonalInfoPropertySetDto**](/email/reference-model-mapi-contact-personal-info-property-set-dto/) | Specify other additional contact information.              | [optional] 
**Photo** | [**MapiContactPhotoDto**](/email/reference-model-mapi-contact-photo-dto/) | Contact photo.              | [optional] 
**PhysicalAddresses** | [**MapiContactPhysicalAddressPropertySetDto**](/email/reference-model-mapi-contact-physical-address-property-set-dto/) | Specify three physical addresses: Home Address, Work Address, and Other Address. One of the addresses can be marked as the Mailing Address.              | [optional] 
**ProfessionalInfo** | [**MapiContactProfessionalPropertySetDto**](/email/reference-model-mapi-contact-professional-property-set-dto/) | Properties are used to store professional details for the person represented by the contact.              | [optional] 
**Telephones** | [**MapiContactTelephonePropertySetDto**](/email/reference-model-mapi-contact-telephone-property-set-dto/) | Specify telephone numbers for the contact.              | [optional] 

Parent class: [MapiMessageItemBaseDto](/email/reference-model-mapi-message-item-base-dto/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="mapi_contact_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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
$mapiContactDto = Models::mapiContactDto()
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

