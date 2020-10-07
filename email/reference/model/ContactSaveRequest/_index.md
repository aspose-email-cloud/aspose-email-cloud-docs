---
title: "ContactSaveRequest"
type: docs
url: /reference-model-contact-save-request/
weight: 1
---
Contact save to storage request             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Format** | **string** | Enumerates contact formats. Enum, available values: VCard, WebDav, Msg | 

Parent class: [StorageModelOfContactDto](/email/reference-model-storage-model-of-contact-dto/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="contact_save_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var contactSaveRequest = new ContactSaveRequest
{
    StorageFile = new StorageFileLocation
    {
        FileName = "contact.vcf",
        Storage = "First Storage",
        FolderPath = "file/location/folder/on/storage"
    },
    Value = new ContactDto
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
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactSaveRequest contactSaveRequest = Models.contactSaveRequest()
    .storageFile(Models.storageFileLocation()
        .fileName("contact.vcf")
        .storage("First Storage")
        .folderPath("file/location/folder/on/storage")
        .build())
    .value(Models.contactDto()
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
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
contact_save_request = models.ContactSaveRequest(
    storage_file=models.StorageFileLocation(
        file_name='contact.vcf',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'),
    value=models.ContactDto(
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
                href='www.aspose.com')]))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
contact_save_request = ContactSaveRequest.new(
  storage_file: StorageFileLocation.new(
    file_name: 'contact.vcf',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'),
  value: ContactDto.new(
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
        href: 'www.aspose.com')]))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let contactSaveRequest = Models.contactSaveRequest()
    .storageFile(Models.storageFileLocation()
        .fileName('contact.vcf')
        .storage('First Storage')
        .folderPath('file/location/folder/on/storage')
        .build())
    .value(Models.contactDto()
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
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$contactSaveRequest = Models::contactSaveRequest()
    ->storageFile(Models::storageFileLocation()
        ->fileName('contact.vcf')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
    ->value(Models::contactDto()
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
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

