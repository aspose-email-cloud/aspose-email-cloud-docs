---
title: "PostalAddress"
type: docs
url: /reference-model-postal-address/
weight: 1
---
A postal address             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Address** | **string** | Address.              | [optional] 
**Category** | [**EnumWithCustomOfPostalAddressCategory**](/email/reference-model-enum-with-custom-of-postal-address-category/) | Address category.              | [optional] 
**City** | **string** | Address&#39;s city.              | [optional] 
**Country** | **string** | Address&#39;s country.              | [optional] 
**CountryCode** | **string** | Country code.              | [optional] 
**IsMailingAddress** | **bool?** | Defines whether address may be used for mailing.              | 
**PostalCode** | **string** | Postal code.              | [optional] 
**PostOfficeBox** | **string** | Post Office box.              | [optional] 
**Preferred** | **bool?** | Defines whether postal address is preferred.              | 
**StateOrProvince** | **string** | Address&#39;s region.              | [optional] 
**Street** | **string** | Address&#39;s street.              | [optional] 


{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="postal_address_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var postalAddress = new PostalAddress
{
    Address = "221b",
    Category = new EnumWithCustomOfPostalAddressCategory
    {
        
    },
    City = "London",
    Country = "United Kingdom",
    IsMailingAddress = true,
    PostalCode = "NW1 6XE",
    Preferred = true,
    Street = "Baker St"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
PostalAddress postalAddress = Models.postalAddress()
    .address("221b")
    .category(Models.enumWithCustomOfPostalAddressCategory()
        
        .build())
    .city("London")
    .country("United Kingdom")
    .isMailingAddress(true)
    .postalCode("NW1 6XE")
    .preferred(true)
    .street("Baker St")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
postal_address = models.PostalAddress(
    address='221b',
    category=models.EnumWithCustomOfPostalAddressCategory(
        ),
    city='London',
    country='United Kingdom',
    is_mailing_address=True,
    postal_code='NW1 6XE',
    preferred=True,
    street='Baker St')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
postal_address = PostalAddress.new(
  address: '221b',
  category: EnumWithCustomOfPostalAddressCategory.new(
    ),
  city: 'London',
  country: 'United Kingdom',
  is_mailing_address: true,
  postal_code: 'NW1 6XE',
  preferred: true,
  street: 'Baker St')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let postalAddress = Models.postalAddress()
    .address('221b')
    .category(Models.enumWithCustomOfPostalAddressCategory()
        
        .build())
    .city('London')
    .country('United Kingdom')
    .isMailingAddress(true)
    .postalCode('NW1 6XE')
    .preferred(true)
    .street('Baker St')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$postalAddress = Models::postalAddress()
    ->address('221b')
    ->category(Models::enumWithCustomOfPostalAddressCategory()
        
        ->build())
    ->city('London')
    ->country('United Kingdom')
    ->isMailingAddress(true)
    ->postalCode('NW1 6XE')
    ->preferred(true)
    ->street('Baker St')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

