---
title: "Business Cards Recognition API"
type: docs
url: /business-cards-recognition-api/
weight: 10
---

## **Introduction**
[VCF](https://wiki.fileformat.com/email/vcf/) (Virtual Card Format) or vCard is a digital file format for storing contact information and is a [file format](https://en.wikipedia.org/wiki/File_format) standard for electronic [business cards](https://en.wikipedia.org/wiki/Business_card). vCards are often attached to [e-mail](https://en.wikipedia.org/wiki/E-mail) messages but can be exchanged in other ways. The format is widely used for data interchange among popular information exchange applications. A vCard usually contains name and address information, telephone numbers, e-mail addresses, URLs, logos, photographs, and any audio clips. A vCard is used as a data interchange format in personal digital assistants (PDAs), personal information managers (PIMs) and customer relationship management (CRMs). 



{{% alert color="primary" %}} 

If you want to know more about working with **VCard files** — take a look at the Aspose Email Cloud tutorial: [**Quick Start With VCard API**](/email/quick-start-with-vcard-api/).

{{% /alert %}} 

Owing to the importance and emerging needs for this format, Aspose.Email Cloud has been enriched to support this format. The Business cards recognition API is a card scanner, which allows you to convert captured business cards and name card images, into a vCard format, for later to be stored as contacts. In simple words, it enables us to convert images into VCard format.

The following image depicts a conversion flow from a business card to vCard format.

![todo:image_alt_text](https://raw.githubusercontent.com/wiki/aspose-email-cloud/aspose-email-cloud-dotnet/images/bcr.jpg)


## **Image located on Storage**
Please try using AiBcrParseStorage method to recognize VCard from an image located on storage.
## **Parse business card from storage using Swagger UI**
1. Open [link](https://apireference.aspose.cloud/email/)
1. Click the *"Authorize"* button, enter your AppKey and AppSid, obtained from the [dashboard](https://dashboard.aspose.cloud/), click *"Authorize"* dialog button
1. Open [link](https://apireference.aspose.cloud/email/#/AiBcr/AiBcrParseStorage) and click *"Try it out"* button
1. Edit JSON to specify images and out folder (were parsed VCards should be placed) location information
1. Click *"Execute"* button
1. You can download produced VCard files using our Contact/Storage API or using dashboard.
## **Parse business card from storage using SDK**
**Parse business card images to VCard**

{{< tabs tabTotal="6" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Email-Business-Card-Image-to-vcard-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Email-Business-Card-Image-to-vcard-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-Email-PHP-Business-Card-Image-to-vcard-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Business-Card-Image-to-vcard-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Business-Card-Image-to-vcard-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Business-Card-Image-to-vcard-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}

## **Image not located on Storage**
If an image is not located on storage, it can be converted to Base64 and parsed using AiBcrParse method.
## **Parse business cards using Swagger UI**
1. Open [link](https://apireference.aspose.cloud/email/#/AiBcr/AiBcrParse) and click *"Try it out"* button
1. Convert business card image to Base64 string and add it to JSON
1. Click *"Execute"* button
## **Parse business cards using SDK**


**Parse business card images to VCard**

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Python" tabName5="Ruby" tabName6="Typescript" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "e50bc177cb788e499fd13c27b55d762e" "Examples-DotNET-CSharp-Email-Parse-Image-without-storage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "f057be7285ab86be13ff3fd45568d5c4" "Examples-Java-Email-Parse-Image-without-storage-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "ad60c1500a11fcf71b0e840ac5b3ffb6" "Examples-PHP-Email-Parse-Image-without-storage-1.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "6d17607766c7783b42db8f744d189579" "Examples-Python-Email-Parse-Image-without-storage-1.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "767aea704882493974d05202ff8a7961" "Examples-Ruby-Email-Parse-Image-without-storage-1.rb" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "6ec28658aa5c23997911e5c1c61a3493" "Examples-Node-Email-Parse-Image-without-storage-1.ts" >}}

{{< /tab >}}

{{< /tabs >}}


## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/email/sdk-setup/).

{{% /alert %}}
