---
title: "Create a New Document"
type: docs
url: /create-a-new-document/
description: " Create a new document using MAPI with Aspose.Email Cloud API. Easily create a new MAPI file in Aspose Cloud Storage"
weight: 20
---

# **Create a new document**
Aspose.Email Cloud API allows you to create a new MAPI file in your storage.
## **API Information**

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/email/Mapi/{name}|PUT|Create a new document|[**CreateMapi**](https://apireference.aspose.cloud/email/#/Mapi/CreateMapi)|
## **cURL Examples**
You can try this here: [**CreateMapi](https://apireference.aspose.cloud/email/#/Mapi/CreateMapi)**.** Click on "*Try it out*" button to use this function. 

**Create a MAPI contact document with Swagger UI**

{{< tabs tabTotal="1" tabID="1" tabName1="JSON" >}}

Use this JSON to create a MAPI contact document:



{{< tab tabNum="1" >}}

```javascript

{

   "HierarchicalObject":{

      "InternalProperties":[

         {

            "Value":"Contact surname",

            "Name":"Tag:'PidTagSurname':0x3A11:String",

            "Type":"PrimitiveObject"

         }

      ],

      "Name":"IPM.Contact",

      "Type":"HierarchicalObject"

   },

   "StorageFolder":{

      "Storage":"First Storage",

      "FolderPath":"document/folder/path/on/storage"

   }

}

```

{{< /tab >}}

{{< /tabs >}}


## **SDK Examples**
**Create a new document**

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

[**CreateMapi](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/docs/EmailApi.md#createmapi) **-** Create a new document.

[**HierarchicalObjectRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/docs/HierarchicalObjectRequest.md) - Create document request.

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-MAPI-Create-New-Document-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

[**createMapi](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/master/docs/EmailApi.md#createmapi) **-** Create a new document.

[**HierarchicalObjectRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/master/docs/HierarchicalObjectRequest.md) - Create document request.

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-MAPI-Create-New-Document-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

[**createMapi](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/3a5c2c35a31629493aa484b65870622165570db8/doc/EmailApi.md#createmapi) **-** Create a new document.

[**HierarchicalObjectRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/3a5c2c35a31629493aa484b65870622165570db8/doc/HierarchicalObjectRequest.md) - Create document request.

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-MAPI-Create-New-Document-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

[**create_mapi](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/master/sdk/docs/EmailApi.md#create_mapi) **-** Create a new document.

[**HierarchicalObjectRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/master/sdk/docs/HierarchicalObjectRequest.md) - Create document request.

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-MAPI-Create-New-Document-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

[**create_mapi](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/master/docs/EmailApi.md#create_mapi) **-** Create a new document.

[**HierarchicalObjectRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/master/docs/HierarchicalObjectRequest.md) - Create document request.

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-MAPI-Create-New-Document-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

[**createMapi](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/master/doc/EmailApi.md#createmapi) **-** Create a new document.

[**HierarchicalObjectRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/master/doc/HierarchicalObjectRequest.md) - Create document request.

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-MAPI-Create-New-Document-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}


## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/sdk-setup/).

{{% /alert %}}
