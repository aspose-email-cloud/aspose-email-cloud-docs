---
title: "Save VCard File"
type: docs
url: /save-vcard-file/
weight: 50
---

## **Save VCard file**
Aspose.Email Cloud API allows you to save VCard file using [**ContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactDto.md).



{{% alert color="primary" %}} 

If you want to know more about working with **VCard files** — take a look at the Aspose Email Cloud tutorial: [**Quick Start With VCard API**](/emailcloud/quick-start-with-vcard-api/).

{{% /alert %}} 


## **API Information**

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/email/ContactModel/{format}/{name}|PUT|Save contact.|[**SaveContactModelAsync**](https://apireference.aspose.cloud/email/#/ContactModel/SaveContactModel)|
## **cURL Examples**
You can try this here: [**SaveContactModelAsync**](https://apireference.aspose.cloud/email/#/ContactModel/SaveContactModel). Click on "*Try it out*" button to use this function. 

**Create contact with Swagger UI**

Use this JSON to create a contact:
JSON has 2 fields:

- **Value** represents **ContactDto**
- **StorageFolder** represents file location on Storage

{{< tabs tabTotal="1" tabID="1" tabName1="JSON" >}}





{{< tab tabNum="1" >}}



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

{{< /tab >}}

{{< /tabs >}}
## **SDK Examples**
**Save VCard file**

[**SaveContactModelAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/docs/EmailApi.md#SaveContactModelAsync) - Save contact. Performs operation asynchronously. Not available on .NETFramework v2.0.

**SaveContactModelRequest** - Request model for [SaveContactModel](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/docs/EmailApi.md#SaveContactModelAsync) operation.

[**StorageModelRqOfContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/docs/StorageModelRqOfContactDto.md) - Create contact request.


{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Save-VCard-To-Storage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

[**saveContactModel](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/37ee732853b3f483c1af14402662fe790ad5aaf9/docs/EmailApi.md#SaveContactModel) **-** Save contact.

**SaveContactModelRequest** - Request model for [SaveContactModel](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/37ee732853b3f483c1af14402662fe790ad5aaf9/docs/EmailApi.md#SaveContactModel) operation.

[**StorageModelRqOfContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/37ee732853b3f483c1af14402662fe790ad5aaf9/docs/StorageModelRqOfContactDto.md) - Create contact request.

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Save-VCard-To-Storage-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

 [**saveContactModel](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/3a5c2c35a31629493aa484b65870622165570db8/doc/EmailApi.md#saveContactModel) **-** Save contact.

**SaveContactModelRequest** - Request model for [SaveContactModel](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/3a5c2c35a31629493aa484b65870622165570db8/doc/EmailApi.md#saveContactModel) operation.

[**StorageModelRqOfContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/3a5c2c35a31629493aa484b65870622165570db8/doc/StorageModelRqOfContactDto.md) - Create contact request.

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Save-VCard-To-Storage-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

[**save_contact_model](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/22a14eb5f9ca38fcf2e79193a2890d3018fbaf84/sdk/docs/EmailApi.md#save_contact_model) **-** Save contact.

**SaveContactModelRequest** - Request model for [save_contact_model](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/22a14eb5f9ca38fcf2e79193a2890d3018fbaf84/sdk/docs/EmailApi.md#save_contact_model) operation.

[**StorageModelRqOfContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/22a14eb5f9ca38fcf2e79193a2890d3018fbaf84/sdk/docs/StorageModelRqOfContactDto.md) - Create contact request.

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Save-VCard-To-Storage-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

[**save_contact_model](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/f3225bb43730f601716d5aa26c0f5e1734a64833/docs/EmailApi.md#save_contact_model) **-** Save contact.

**SaveContactModelRequest** - Request model for [save_contact_model](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/f3225bb43730f601716d5aa26c0f5e1734a64833/docs/EmailApi.md#save_contact_model) operation.

[**StorageModelRqOfContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/f3225bb43730f601716d5aa26c0f5e1734a64833/docs/StorageModelRqOfContactDto.md) - Create contact request.

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Save-VCard-To-Storage-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

[**saveContactModel](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/0d0ec4f4a9ca1beb87e3c194f1ac69630d5205fe/doc/EmailApi.md#saveContactModel) **-** Save contact.

**SaveContactModelRequest** - Request model for [saveContactModel](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/0d0ec4f4a9ca1beb87e3c194f1ac69630d5205fe/doc/EmailApi.md#saveContactModel) operation.

[**StorageModelRqOfContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/0d0ec4f4a9ca1beb87e3c194f1ac69630d5205fe/doc/StorageModelRqOfContactDto.md) - Create contact request.

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Save-VCard-To-Storage-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}


## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/emailcloud/sdk-setup/).

{{% /alert %}}
