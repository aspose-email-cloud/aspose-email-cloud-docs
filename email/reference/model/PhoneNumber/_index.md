---
title: "PhoneNumber"
type: docs
url: /reference-model-phone-number/
weight: 1
---
A phone number.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Category** | [**EnumWithCustomOfPhoneNumberCategory**](/email/reference-model-enum-with-custom-of-phone-number-category/) | Phone number category.              | [optional] 
**Number** | **string** | Phone number.              | [optional] 
**Preferred** | **bool?** | Defines whether phone number is preferred.              | 


## Example

{{< tabs tabTotal="6" tabID="phone_number_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var phoneNumber = new PhoneNumber
{
    Category = new EnumWithCustomOfPhoneNumberCategory
    {
        Value = "Company"
    },
    Number = "+44 141 628 8900",
    Preferred = true
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
PhoneNumber phoneNumber = Models.phoneNumber()
    .category(Models.enumWithCustomOfPhoneNumberCategory()
        .value("Company")
        .build())
    .number("+44 141 628 8900")
    .preferred(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
phone_number = models.PhoneNumber(
    category=models.EnumWithCustomOfPhoneNumberCategory(
        value='Company'),
    number='+44 141 628 8900',
    preferred=True)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
phone_number = PhoneNumber.new(
  category: EnumWithCustomOfPhoneNumberCategory.new(
    value: 'Company'),
  number: '+44 141 628 8900',
  preferred: true)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let phoneNumber = Models.phoneNumber()
    .category(Models.enumWithCustomOfPhoneNumberCategory()
        .value('Company')
        .build())
    .number('+44 141 628 8900')
    .preferred(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$phoneNumber = Models::phoneNumber()
    ->category(Models::enumWithCustomOfPhoneNumberCategory()
        ->value('Company')
        ->build())
    ->number('+44 141 628 8900')
    ->preferred(true)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

