---
title: "ContactDto"
type: docs
url: /reference-model-contact-dto/
weight: 1
---
VCard document representation.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**AssociatedPersons** | [**List&lt;AssociatedPerson&gt;**](/email/reference-model-associated-person/) | Associated persons.              | [optional] 
**Attachments** | [**List&lt;Attachment&gt;**](/email/reference-model-attachment/) | Document attachments.              | [optional] 
**CompanyName** | **string** | Company name.              | [optional] 
**ComputerNetworkName** | **string** | Computer network.              | [optional] 
**CustomerId** | **string** | Customer id.              | [optional] 
**DepartmentName** | **string** | Department name.              | [optional] 
**DisplayName** | **string** | Display name.              | [optional] 
**EmailAddresses** | [**List&lt;EmailAddress&gt;**](/email/reference-model-email-address/) | Person&#39;s email addresses.              | [optional] 
**Events** | [**List&lt;CustomerEvent&gt;**](/email/reference-model-customer-event/) | Person&#39;s events.              | [optional] 
**FileAs** | **string** | A name used for sorting.              | [optional] 
**FileAsMapping** | **string** | Specifies how to generate and recompute the value of the dispidFileAs property when other contact name properties change. Coincides MS-OXPROPS revision 16.2 from 7/31/2014. Enum, available values: Empty, DisplayName, FirstName, LastName, Organization, LastFirstMiddle, OrgLastFirstMiddle, LastFirstMiddleOrg, LastFirstMiddle2, LastFirstMiddle3, OrgLastFirstMiddle2, OrgLastFirstMiddle3, LastFirstMiddleOrg2, LastFirstMiddleOrg3, LastFirstMiddleGen, FirstMiddleLastGen, LastFirstMiddleGen2, BestMatch, AccordingToLocale, None | 
**FreeBusyLocation** | **string** | URL path from which a client can retrieve free/busy information for the contact as an iCal file.              | [optional] 
**Gender** | **string** | Enum defines gender of a person. Enum, available values: Unspecified, Female, Male | 
**GivenName** | **string** | Person&#39;s given name.              | [optional] 
**GovernmentIdNumber** | **string** | Government id number.              | [optional] 
**Hobbies** | **string** | Person&#39;s hobbies.              | [optional] 
**Initials** | **string** | Person&#39;s initials.              | [optional] 
**InstantMessengers** | [**List&lt;InstantMessengerAddress&gt;**](/email/reference-model-instant-messenger-address/) | Person&#39;s instant messenger addresses.              | [optional] 
**JobTitle** | **string** | Person&#39;s job title.              | [optional] 
**Language** | **string** | Language.              | [optional] 
**Location** | **string** | Person&#39;s location.              | [optional] 
**MiddleName** | **string** | Person&#39;s middle name.              | [optional] 
**Nickname** | **string** | Person&#39;s nickname.              | [optional] 
**Notes** | **string** | Notes.              | [optional] 
**NotesFormat** | **string** | Defines format of a text. Enum, available values: Text, Html | 
**OfficeLocation** | **string** | Office location.              | [optional] 
**OrganizationalIdNumber** | **string** | Contains an identifier for the mail user used within the mail user&#39;s organization.              | [optional] 
**PhoneNumbers** | [**List&lt;PhoneNumber&gt;**](/email/reference-model-phone-number/) | Person&#39;s phone numbers.              | [optional] 
**Photo** | [**ContactPhoto**](/email/reference-model-contact-photo/) | Person&#39;s photo.              | [optional] 
**PhysicalAddresses** | [**List&lt;PostalAddress&gt;**](/email/reference-model-postal-address/) | Person&#39;s physical addresses.              | [optional] 
**PreferredTextEncoding** | **string** | Encoding for all text properties.              | [optional] 
**Prefix** | **string** | A prefix of a full name such like Mr.(mister), Dr.(doctor) and so on.              | [optional] 
**Profession** | **string** | A job position of a person in a company.              | [optional] 
**Suffix** | **string** | A suffix of a full name such like Jr.(junior), Sr.(senior) and so on.              | [optional] 
**Surname** | **string** | Person&#39;s surname.              | [optional] 
**Urls** | [**List&lt;Url&gt;**](/email/reference-model-url/) | Person&#39;s urls.              | [optional] 


{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="contact_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var contactDto = new ContactDto
{
    Attachments = new List<Attachment>
    {
        new Attachment
        {
            Name = "attachment.txt",
            Base64Data = "U29tZSBmaWxlIGNvbnRlbnQ="
        }
    },
    DisplayName = "Alex Thomas",
    EmailAddresses = new List<EmailAddress>
    {
        new EmailAddress
        {
            Category = new EnumWithCustomOfEmailAddressCategory
            {
                Value = "Custom",
                Description = "Partners"
            },
            DisplayName = "Alex Thomas Partners",
            Preferred = true,
            Address = "email@aspose.com"
        }
    },
    Gender = "Male",
    GivenName = "Alex",
    PhoneNumbers = new List<PhoneNumber>
    {
        new PhoneNumber
        {
            Category = new EnumWithCustomOfPhoneNumberCategory
            {
                Value = "Office"
            },
            Number = "+49 211 4247 21",
            Preferred = true
        }
    },
    Profession = "GENERAL DIRECTOR",
    Surname = "Thomas",
    Urls = new List<Url>
    {
        new Url
        {
            Category = new EnumWithCustomOfUrlCategory
            {
                Value = "Work"
            },
            Preferred = true,
            Href = "www.aspose.com"
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactDto contactDto = Models.contactDto()
    .attachments(Arrays.<Attachment>asList(
        Models.attachment()
            .name("attachment.txt")
            .base64Data("U29tZSBmaWxlIGNvbnRlbnQ=")
            .build()))
    .displayName("Alex Thomas")
    .emailAddresses(Arrays.<EmailAddress>asList(
        Models.emailAddress()
            .category(Models.enumWithCustomOfEmailAddressCategory()
                .value("Custom")
                .description("Partners")
                .build())
            .displayName("Alex Thomas Partners")
            .preferred(true)
            .address("email@aspose.com")
            .build()))
    .gender("Male")
    .givenName("Alex")
    .phoneNumbers(Arrays.<PhoneNumber>asList(
        Models.phoneNumber()
            .category(Models.enumWithCustomOfPhoneNumberCategory()
                .value("Office")
                .build())
            .number("+49 211 4247 21")
            .preferred(true)
            .build()))
    .profession("GENERAL DIRECTOR")
    .surname("Thomas")
    .urls(Arrays.<Url>asList(
        Models.url()
            .category(Models.enumWithCustomOfUrlCategory()
                .value("Work")
                .build())
            .preferred(true)
            .href("www.aspose.com")
            .build()))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
contact_dto = models.ContactDto(
    attachments=[
        models.Attachment(
            name='attachment.txt',
            base64_data='U29tZSBmaWxlIGNvbnRlbnQ=')],
    display_name='Alex Thomas',
    email_addresses=[
        models.EmailAddress(
            category=models.EnumWithCustomOfEmailAddressCategory(
                value='Custom',
                description='Partners'),
            display_name='Alex Thomas Partners',
            preferred=True,
            address='email@aspose.com')],
    gender='Male',
    given_name='Alex',
    phone_numbers=[
        models.PhoneNumber(
            category=models.EnumWithCustomOfPhoneNumberCategory(
                value='Office'),
            number='+49 211 4247 21',
            preferred=True)],
    profession='GENERAL DIRECTOR',
    surname='Thomas',
    urls=[
        models.Url(
            category=models.EnumWithCustomOfUrlCategory(
                value='Work'),
            preferred=True,
            href='www.aspose.com')])
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
contact_dto = ContactDto.new(
  attachments: [
    Attachment.new(
      name: 'attachment.txt',
      base64_data: 'U29tZSBmaWxlIGNvbnRlbnQ=')],
  display_name: 'Alex Thomas',
  email_addresses: [
    EmailAddress.new(
      category: EnumWithCustomOfEmailAddressCategory.new(
        value: 'Custom',
        description: 'Partners'),
      display_name: 'Alex Thomas Partners',
      preferred: true,
      address: 'email@aspose.com')],
  gender: 'Male',
  given_name: 'Alex',
  phone_numbers: [
    PhoneNumber.new(
      category: EnumWithCustomOfPhoneNumberCategory.new(
        value: 'Office'),
      number: '+49 211 4247 21',
      preferred: true)],
  profession: 'GENERAL DIRECTOR',
  surname: 'Thomas',
  urls: [
    Url.new(
      category: EnumWithCustomOfUrlCategory.new(
        value: 'Work'),
      preferred: true,
      href: 'www.aspose.com')])
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let contactDto = Models.contactDto()
    .attachments([
        Models.attachment()
            .name('attachment.txt')
            .base64Data('U29tZSBmaWxlIGNvbnRlbnQ=')
            .build()])
    .displayName('Alex Thomas')
    .emailAddresses([
        Models.emailAddress()
            .category(Models.enumWithCustomOfEmailAddressCategory()
                .value('Custom')
                .description('Partners')
                .build())
            .displayName('Alex Thomas Partners')
            .preferred(true)
            .address('email@aspose.com')
            .build()])
    .gender('Male')
    .givenName('Alex')
    .phoneNumbers([
        Models.phoneNumber()
            .category(Models.enumWithCustomOfPhoneNumberCategory()
                .value('Office')
                .build())
            .number('+49 211 4247 21')
            .preferred(true)
            .build()])
    .profession('GENERAL DIRECTOR')
    .surname('Thomas')
    .urls([
        Models.url()
            .category(Models.enumWithCustomOfUrlCategory()
                .value('Work')
                .build())
            .preferred(true)
            .href('www.aspose.com')
            .build()])
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$contactDto = Models::contactDto()
    ->attachments(array(
        Models::attachment()
            ->name('attachment.txt')
            ->base64Data('U29tZSBmaWxlIGNvbnRlbnQ=')
            ->build()))
    ->displayName('Alex Thomas')
    ->emailAddresses(array(
        Models::emailAddress()
            ->category(Models::enumWithCustomOfEmailAddressCategory()
                ->value('Custom')
                ->description('Partners')
                ->build())
            ->displayName('Alex Thomas Partners')
            ->preferred(true)
            ->address('email@aspose.com')
            ->build()))
    ->gender('Male')
    ->givenName('Alex')
    ->phoneNumbers(array(
        Models::phoneNumber()
            ->category(Models::enumWithCustomOfPhoneNumberCategory()
                ->value('Office')
                ->build())
            ->number('+49 211 4247 21')
            ->preferred(true)
            ->build()))
    ->profession('GENERAL DIRECTOR')
    ->surname('Thomas')
    ->urls(array(
        Models::url()
            ->category(Models::enumWithCustomOfUrlCategory()
                ->value('Work')
                ->build())
            ->preferred(true)
            ->href('www.aspose.com')
            ->build()))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

