---
title: "Create VCard File"
type: docs
url: /create-vcard-file/
weight: 20
---



## **What is VCard?**
**VCard** is a text format for exchanging electronic business cards. A vCard file consists of records of type VCard, each contains information from one business card. A VCard record can contain a name, address, phone numbers, URL, logo, video and audio fragments, etc.


Aspose.Email Cloud API allows you to create a VCard file using [**ContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactDto.md).



{{% alert color="primary" %}} 

If you want to know more about working with **VCard files** — take a look at the Aspose Email Cloud tutorial: [**Quick Start With VCard API**](/email/quick-start-with-vcard-api/).

{{% /alert %}} 
## **API Information**

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/email/ContactModel/{format}/{name}|PUT|Save contact.|[**SaveContactModel**](https://apireference.aspose.cloud/email/#/ContactModel/SaveContactModel)|
## **cURL Examples**
You can try this here: [**SaveContactModel**](https://apireference.aspose.cloud/email/#/ContactModel/SaveContactModel). Click on "*Try it out*" button to use this function. 



Use this JSON to create a contact

JSON has 2 fields:

- **Value** represents ContactDto
- **StorageFolder** represents file location on Storage

```javascript

{

   "Value":{

      "EmailAddresses":[

         {

            "Category":{

               "Value":"Work"

            },

            "DisplayName":"Alex Thomas",

            "Preferred":true,

            "Address":"alex.thomas@work.com"

         }

      ],

      "Gender":"Male",

      "GivenName":"Alex",

      "PhoneNumbers":[

         {

            "Category":{

               "Value":"Work"

            },

            "Number":"+49211424721",

            "Preferred":true

         }

      ],

      "Surname":"Thomas"

   },

   "StorageFolder":{

      "Storage":"First Storage",

      "FolderPath":"folder/on/storage"

   }

}

```


## **SDK Examples**
**Create VCard file**
[**ContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactDto.md) - The model contains contact’s properties.

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Create-VCard-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

[**ContactDto](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/37ee732853b3f483c1af14402662fe790ad5aaf9/docs/ContactDto.md) **-** The model contains contact’s properties.

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Create-VCard-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}



[**ContactDto](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/3a5c2c35a31629493aa484b65870622165570db8/doc/ContactDto.md) **-** The model contains contact’s properties.

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Create-VCard-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

[**ContactDto](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/22a14eb5f9ca38fcf2e79193a2890d3018fbaf84/sdk/docs/ContactDto.md) **-** The model contains contact’s properties.

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Create-VCard-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}



[**ContactDto](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/f3225bb43730f601716d5aa26c0f5e1734a64833/docs/ContactDto.md) **-** The model contains contact’s properties.

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Create-VCard-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

[**ContactDto](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/0d0ec4f4a9ca1beb87e3c194f1ac69630d5205fe/doc/ContactDto.md) **-** The model contains contact’s properties.

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Create-VCard-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}

\
Here EnumWithCustom is an enumeration with the custom value support. It has 2 fields: Valueand Description. Description field is used only if Value is "Custom". For example, if you want to create a phone number with the category "For friends":

```csharp

number.Category = new EnumWithCustomOfPhoneNumberCategory("Custom", "For friends")

```


## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/email/sdk-setup/).

{{% /alert %}}
