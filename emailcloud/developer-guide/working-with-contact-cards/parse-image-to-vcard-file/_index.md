---
title: "Parse Image To VCard File"
type: docs
url: /parse-image-to-vcard-file/
weight: 30
---

## **Parse an image to VCard file**
Aspose.Email Cloud API allows you to parse an image to VCard file using [**ContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactDto.md) and [**The Business Card Recognition**](/business-cards-recognition-api/).

{{% alert color="primary" %}} 

If you want to know more about working with **VCard files** — take a look at the Aspose Email Cloud tutorial: [**Quick Start With VCard API**](/quick-start-with-vcard-api/).

{{% /alert %}} 
## **API Information**

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/email/AiBcr/parse-model|POST|Parse images to vCard document models|[**AiBcrParseModel**](https://apireference.aspose.cloud/email/#/AiBcr/AiBcrParseModel)|
## **cURL Examples**
You can try this here: [**AiBcrParseModel**](https://apireference.aspose.cloud/email/#/AiBcr/AiBcrParseModel). Click on "*Try it out*" button to use this function. 

**Parse an image with Swagger UI**

{{< tabs tabTotal="1" tabID="1" tabName1="JSON" >}}

Use this JSON to parse an image: 

{{< tab tabNum="1" >}}

```javascript

{

   "Images":[

      {

         "Base64Data":"Insert your image's base64 representation here",

         "IsSingle":true

      }

   ]

}

```

{{< /tab >}}

{{< /tabs >}}


## **SDK Examples**
**Parse an image to VCard file**

[**AiBcrParseModel**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/9511b81d6c62dda413dc23f6f6f8a0973a144343/docs/EmailApi.md#AiBcrParseModel) - Parse images to vCard document models.

**AiBcrParseModelRequest** - Request model for aiBcrParseModel operation.

[**AiBcrBase64Rq**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/docs/AiBcrBase64Rq.md) - Request with base64 images data.

[**AiBcrBase64Image**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/dff3d963b6d39312189f14dafafe2aa2ab774b4b/docs/AiBcrBase64Image.md) - Base64 images data.


{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Parse-Image-To-VCard-File-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

[**aiBcrParseModel](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/37ee732853b3f483c1af14402662fe790ad5aaf9/docs/EmailApi.md#aibcrparsemodel) **-** Parse images to vCard document models.

**AiBcrParseModelRequest -** Request model for aiBcrParseModel operation.

[**AiBcrBase64Rq**](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/73f48e63538ba6e46ff77a473c839c1e7170c462/docs/AiBcrBase64Rq.md) - Request with base64 images data.

[**AiBcrBase64Image**](https://github.com/aspose-email-cloud/aspose-email-cloud-java/blob/73f48e63538ba6e46ff77a473c839c1e7170c462/docs/AiBcrBase64Image.md) - Base64 images data.

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Parse-Image-To-VCard-File-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

[**aiBcrParseModel](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/3a5c2c35a31629493aa484b65870622165570db8/doc/EmailApi.md#aibcrparsemodel) **-** Parse images to vCard document models.

**AiBcrParseModelRequest -** Request model for aiBcrParseModel operation.

[**AiBcrBase64Rq**](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/f507a0aa93ffedfc5845bdcf07534e3d05c4b9ce/doc/AiBcrBase64Rq.md) - Request with base64 images data.

[**AiBcrBase64Image**](https://github.com/aspose-email-cloud/aspose-email-cloud-php/blob/f507a0aa93ffedfc5845bdcf07534e3d05c4b9ce/doc/AiBcrBase64Image.md) - Base64 images data.

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Parse-Image-To-VCard-File-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

[**ai_bcr_parse_model](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/22a14eb5f9ca38fcf2e79193a2890d3018fbaf84/sdk/docs/EmailApi.md#ai_bcr_parse_model) **-** Parse images to vCard document models.

**AiBcrParseModelRequest -** Request model for aiBcrParseModel operation.

[**AiBcrBase64Rq**](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/8e364e51130302fc3574f9c5e9188c1793fb238c/sdk/docs/AiBcrBase64Rq.md) - Request with base64 images data.

[**AiBcrBase64Image**](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/8e364e51130302fc3574f9c5e9188c1793fb238c/sdk/docs/AiBcrBase64Image.md) - Base64 images data.

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Parse-Image-To-VCard-File-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

[**ai_bcr_parse_model](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/f3225bb43730f601716d5aa26c0f5e1734a64833/docs/EmailApi.md#ai_bcr_parse_model) **-** Parse images to vCard document models.

**AiBcrParseModelRequest -** Request model for aiBcrParseModel operation.

[**AiBcrBase64Rq**](https://github.com/aspose-email-cloud/aspose-email-cloud-python/blob/8e364e51130302fc3574f9c5e9188c1793fb238c/sdk/docs/AiBcrBase64Rq.md) - Request with base64 images data.

[**AiBcrBase64Image**](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/blob/57a6dbc44033c6fd33bca8d1c441c4df0cb9e236/docs/AiBcrBase64Image.md) - Base64 images data.

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Parse-Image-To-VCard-File-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}



[**aiBcrParseModel](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/0d0ec4f4a9ca1beb87e3c194f1ac69630d5205fe/doc/EmailApi.md#aiBcrParseModel) **-** Parse images to vCard document models.

**AiBcrParseModelRequest -** Request model for aiBcrParseModel operation.

[**AiBcrBase64Rq**](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/3eb34ee080e3747b1109f7b66c80918a6cf0df68/doc/AiBcrBase64Rq.md) - Request with base64 images data.

[**AiBcrBase64Image**](https://github.com/aspose-email-cloud/aspose-email-cloud-node/blob/3eb34ee080e3747b1109f7b66c80918a6cf0df68/doc/AiBcrBase64Image.md) - Base64 images data.

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Parse-Image-To-VCard-File-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}
## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/sdk-setup/).

{{% /alert %}}
