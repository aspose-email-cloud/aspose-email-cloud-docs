---
title: "MapiContactElectronicAddressPropertySetDto"
type: docs
url: /reference-model-mapi-contact-electronic-address-property-set-dto/
weight: 1
---
Specify properties for up to three different e-mail addresses (Email1, Email2, and Email3) and three different fax addresses (Primary Fax, Business Fax, and Home Fax)             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**BusinessFax** | [**MapiContactElectronicAddressDto**](/email/reference-model-mapi-contact-electronic-address-dto/) | Refers to the group of properties that define the business fax address for a contact. | [optional] 
**DefaultEmailAddress** | [**MapiContactElectronicAddressDto**](/email/reference-model-mapi-contact-electronic-address-dto/) | Default value of electronic address Uses when user does not set any electronic address if UseAutocomplete property is set &#39;true&#39;              | [optional] 
**Email1** | [**MapiContactElectronicAddressDto**](/email/reference-model-mapi-contact-electronic-address-dto/) | Refers to the group of properties that define the first e-mail address for a contact.              | [optional] 
**Email2** | [**MapiContactElectronicAddressDto**](/email/reference-model-mapi-contact-electronic-address-dto/) | Refers to the group of properties that define the second e-mail address for a contact.              | [optional] 
**Email3** | [**MapiContactElectronicAddressDto**](/email/reference-model-mapi-contact-electronic-address-dto/) | Refers to the group of properties that define the third e-mail address for a contact.              | [optional] 
**HomeFax** | [**MapiContactElectronicAddressDto**](/email/reference-model-mapi-contact-electronic-address-dto/) | Refers to the group of properties that define the home fax address for a contact.              | [optional] 
**IsEmpty** | **bool?** | Shows if MapiContactElectronicAddressPropertySetDto is empty | 
**PrimaryFax** | [**MapiContactElectronicAddressDto**](/email/reference-model-mapi-contact-electronic-address-dto/) | Refers to the group of properties that define the primary fax address for a contact.              | [optional] 
**UseAutocomplete** | **bool?** | Indicates that one electronic address is completed automatically in case if user does not set any electronic address              | 


