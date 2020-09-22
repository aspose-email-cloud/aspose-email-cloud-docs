---
title: "How To Operate VCard Using Model API"
type: docs
url: /how-to-operate-vcard-using-model-api/
description: "Aspose.Email Cloud API allows you to work with VCard files. See how to operate a contact card or VCard files using Model API."
weight: 40
---

## **Introduction**
{{% alert color="primary" %}} [VCF](https://wiki.fileformat.com/email/vcf/) (Virtual Card Format) or vCard is a digital file format for storing contact information. The format is widely used for data interchange among popular information exchange applications. {{% /alert %}} 
## **Model API**
When using Model API, the files are represented using models.

VCard Model API supports:

- Get VCard file from storage as [ContactDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactDto.md) ([GetContactModel](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#GetContactModel))
- Save [ContactDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactDto.md) to Storage ([SaveContactModel](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#SaveContactModel))
- Get a list of VCard files from Storage folder ([GetContactModelList](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#GetContactModelList))
- Recognize VCard from image to [ContactDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactDto.md) ([AiBcrParseModel](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#AiBcrParseModel))
### **Create Contact Card — ContactDto Object**
The first step is to create [ContactDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactDto.md) object:

{{% alert color="primary" %}} If you want to know more about how to **create contact card files using different Aspose.Email Cloud SDKs**, please take a look at the article: [**Create VCard File**](/email/create-vcard-file/). {{% /alert %}} 



**Create ContactDto object**

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Email-Create-ContactDTO-1.cs" >}}

Here **EnumWithCustom** is an enumeration with the custom value support. It has 2 fields: Value and Description. Description field is used only if Value is "Custom". For example, if you want to create a phone number with the category "For friends":



```java

number.Category = new EnumWithCustomOfPhoneNumberCategory("Custom", "For friends");

```

### **Save Contact Card to Storage**
Next step is to save the [ContactDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactDto.md) to the storage: 

{{% alert color="primary" %}} If you want to know more about how to **save contact card files using different Aspose.Email Cloud SDKs**, take a look at the article: [**Save VCard File**](/email/save-vcard-file/). {{% /alert %}} 



**Save ContactDto to Storage**

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Email-Save-ContactDTO-to-Storage-1.cs" >}}

### **Parse an Image of Business Card to Contact Card File**
In case you need to parse an image to [ContactDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactDto.md), please try using the following code snippet.

{{% alert color="primary" %}} If you want to know more about how to **parse an image of a business card to the contact card file using different Aspose.Email Cloud SDKs**, take a look at the article: [**Parse Image To VCard File**](/email/parse-image-to-vcard-file/). {{% /alert %}} 



**Parse Image to ContactDto**

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Email-Parse-Image-to-ContactDTO-1.cs" >}}


## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/email/sdk-setup/).

{{% /alert %}}
