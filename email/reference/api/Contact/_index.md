---
title: "Contact"
type: docs
url: /reference-contact-api/
weight: 1
---

Contact document operations. Supported formats: VCard, MSG, WebDav

## AsFile

Converts contact model to specified format and returns as file. 
Returns a **File**. Requires:

{{< expand-list title="request" >}}

Contact model and format to convert. Type: [**ContactAsFileRequest**](/email/reference-model-contact-as-file-request/).

{{< tabs tabTotal="6" tabID="contact_as_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ContactAsFileRequest
{
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
ContactAsFileRequest request = Models.contactAsFileRequest()
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
request = models.ContactAsFileRequest(
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
request = ContactAsFileRequest.new(
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
let request = Models.contactAsFileRequest()
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
$request = Models::contactAsFileRequest()
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

{{< tabs tabTotal="6" tabID="contact_as_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Contact.AsFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.contact().asFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.contact.as_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.contact.as_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.contact.asFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->contact()->asFile($request);
```

{{< /tab >}}

{{< /tabs >}}
## AsMapi

Converts ContactDto to MapiContactDto. 
Returns [**MapiContactDto**](/email/reference-model-mapi-contact-dto/) model. Requires:

{{< expand-list title="contactDto" >}}

Contact model to convert. Type: [**ContactDto**](/email/reference-model-contact-dto/).

{{< tabs tabTotal="6" tabID="contact_as_mapi_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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
$contact_dto = Models::contactDto()
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

{{< tabs tabTotal="6" tabID="contact_as_mapi_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Contact.AsMapiAsync(contactDto);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiContactDto result = api.contact().asMapi(contactDto);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.contact.as_mapi(contact_dto)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.contact.as_mapi(contact_dto)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.contact.asMapi(contactDto);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->contact()->asMapi($contact_dto);
```

{{< /tab >}}

{{< /tabs >}}
## Convert

Converts contact document to specified format and returns as file. 
Returns a **File**. Requires:

{{< expand-list title="request" >}}

Convert method request. Type: [**ContactConvertRequest**](/email/reference-model-contact-convert-request/).

{{< tabs tabTotal="6" tabID="contact_convert_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ContactConvertRequest
{ 
    ToFormat = "VCard",
    FromFormat = "Msg",
    File = new MemoryStream(File.ReadAllBytes("/path/to/contact.msg"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactConvertRequest request = Models.contactConvertRequest()
    .toFormat("VCard")
    .fromFormat("Msg")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/contact.msg")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ContactConvertRequest(
    to_format='VCard',
    from_format='Msg',
    file='/path/to/contact.msg')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ContactConvertRequest.new(
    to_format: 'VCard',
    from_format: 'Msg',
    file: File.new('/path/to/contact.msg'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ContactConvertRequest()
    .toFormat('VCard')
    .fromFormat('Msg')
    .file(fs.readFileSync('/path/to/contact.msg'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ContactConvertRequest()
    ->to_format('VCard')
    ->from_format('Msg')
    ->file(new SplFileObject('/path/to/contact.msg'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="contact_convert_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Contact.ConvertAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.contact().convert(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.contact.convert(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.contact.convert(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.contact.convert(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->contact()->convert($request);
```

{{< /tab >}}

{{< /tabs >}}
## FromFile

Converts contact document to a model representation. 
Returns [**ContactDto**](/email/reference-model-contact-dto/) model. Requires:

{{< expand-list title="request" >}}

FromFile method request. Type: [**ContactFromFileRequest**](/email/reference-model-contact-from-file-request/).

{{< tabs tabTotal="6" tabID="contact_from_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ContactFromFileRequest
{ 
    Format = "Msg",
    File = new MemoryStream(File.ReadAllBytes("/path/to/contact.msg"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactFromFileRequest request = Models.contactFromFileRequest()
    .format("Msg")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/contact.msg")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ContactFromFileRequest(
    format='Msg',
    file='/path/to/contact.msg')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ContactFromFileRequest.new(
    format: 'Msg',
    file: File.new('/path/to/contact.msg'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ContactFromFileRequest()
    .format('Msg')
    .file(fs.readFileSync('/path/to/contact.msg'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ContactFromFileRequest()
    ->format('Msg')
    ->file(new SplFileObject('/path/to/contact.msg'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="contact_from_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Contact.FromFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactDto result = api.contact().fromFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.contact.from_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.contact.from_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.contact.fromFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->contact()->fromFile($request);
```

{{< /tab >}}

{{< /tabs >}}
## Get

Get contact document from storage. 
Returns [**ContactDto**](/email/reference-model-contact-dto/) model. Requires:

{{< expand-list title="request" >}}

Get method request. Type: [**ContactGetRequest**](/email/reference-model-contact-get-request/).

{{< tabs tabTotal="6" tabID="contact_get_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ContactGetRequest
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
ContactGetRequest request = Models.contactGetRequest()
    .format("VCard")
    .fileName("contact.vcf")
    .folder("folder/on/storage")
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ContactGetRequest(
    format='VCard',
    file_name='contact.vcf',
    folder='folder/on/storage',
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ContactGetRequest.new(
    format: 'VCard',
    file_name: 'contact.vcf',
    folder: 'folder/on/storage',
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ContactGetRequest()
    .format('VCard')
    .fileName('contact.vcf')
    .folder('folder/on/storage')
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ContactGetRequest()
    ->format('VCard')
    ->file_name('contact.vcf')
    ->folder('folder/on/storage')
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="contact_get_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Contact.GetAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactDto result = api.contact().get(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.contact.get(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.contact.get(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.contact.get(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->contact()->get($request);
```

{{< /tab >}}

{{< /tabs >}}
## GetAsFile

Converts contact document from storage to specified format and returns as file. 
Returns a **File**. Requires:

{{< expand-list title="request" >}}

GetAsFile method request. Type: [**ContactGetAsFileRequest**](/email/reference-model-contact-get-as-file-request/).

{{< tabs tabTotal="6" tabID="contact_get_as_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ContactGetAsFileRequest
{ 
    FileName = "contact.msg",
    ToFormat = "VCard",
    FromFormat = "Msg",
    Storage = "First Storage",
    Folder = "folder/on/storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactGetAsFileRequest request = Models.contactGetAsFileRequest()
    .fileName("contact.msg")
    .toFormat("VCard")
    .fromFormat("Msg")
    .storage("First Storage")
    .folder("folder/on/storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ContactGetAsFileRequest(
    file_name='contact.msg',
    to_format='VCard',
    from_format='Msg',
    storage='First Storage',
    folder='folder/on/storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ContactGetAsFileRequest.new(
    file_name: 'contact.msg',
    to_format: 'VCard',
    from_format: 'Msg',
    storage: 'First Storage',
    folder: 'folder/on/storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ContactGetAsFileRequest()
    .fileName('contact.msg')
    .toFormat('VCard')
    .fromFormat('Msg')
    .storage('First Storage')
    .folder('folder/on/storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ContactGetAsFileRequest()
    ->file_name('contact.msg')
    ->to_format('VCard')
    ->from_format('Msg')
    ->storage('First Storage')
    ->folder('folder/on/storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="contact_get_as_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Contact.GetAsFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.contact().getAsFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.contact.get_as_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.contact.get_as_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.contact.getAsFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->contact()->getAsFile($request);
```

{{< /tab >}}

{{< /tabs >}}
## GetList

Get contact list from storage folder. 
Returns [**ContactStorageList**](/email/reference-model-contact-storage-list/) model. Requires:

{{< expand-list title="request" >}}

GetList method request. Type: [**ContactGetListRequest**](/email/reference-model-contact-get-list-request/).

{{< tabs tabTotal="6" tabID="contact_get_list_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ContactGetListRequest
{ 
    Format = "VCard",
    Folder = "folder/on/storage",
    Storage = "First Storage",
    ItemsPerPage = 10,
    PageNumber = 0
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactGetListRequest request = Models.contactGetListRequest()
    .format("VCard")
    .folder("folder/on/storage")
    .storage("First Storage")
    .itemsPerPage(10)
    .pageNumber(0)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ContactGetListRequest(
    format='VCard',
    folder='folder/on/storage',
    storage='First Storage',
    items_per_page=10,
    page_number=0)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ContactGetListRequest.new(
    format: 'VCard',
    folder: 'folder/on/storage',
    storage: 'First Storage',
    items_per_page: 10,
    page_number: 0)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ContactGetListRequest()
    .format('VCard')
    .folder('folder/on/storage')
    .storage('First Storage')
    .itemsPerPage(10)
    .pageNumber(0)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ContactGetListRequest()
    ->format('VCard')
    ->folder('folder/on/storage')
    ->storage('First Storage')
    ->items_per_page(10)
    ->page_number(0)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="contact_get_list_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Contact.GetListAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactStorageList result = api.contact().getList(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.contact.get_list(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.contact.get_list(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.contact.getList(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->contact()->getList($request);
```

{{< /tab >}}

{{< /tabs >}}
## Save

Save contact to storage. Requires:

{{< expand-list title="request" >}}

Create/Update contact request. Type: [**ContactSaveRequest**](/email/reference-model-contact-save-request/).

{{< tabs tabTotal="6" tabID="contact_save_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ContactSaveRequest
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
ContactSaveRequest request = Models.contactSaveRequest()
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
request = models.ContactSaveRequest(
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
request = ContactSaveRequest.new(
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
let request = Models.contactSaveRequest()
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
$request = Models::contactSaveRequest()
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

{{< tabs tabTotal="6" tabID="contact_save_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Contact.SaveAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.contact().save(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.contact.save(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.contact.save(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.contact.save(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->contact()->save($request);
```

{{< /tab >}}

{{< /tabs >}}

## More APIs

{{< list-of-articles-in-this-section >}}
