---
title: "Business Cards Recognition"
type: docs
url: /business-cards-recognition/
weight: 15
---

## **Introduction**
[VCF](https://wiki.fileformat.com/email/vcf/) (Virtual Card Format) or vCard is a digital file format for storing contact information and is a [file format](https://en.wikipedia.org/wiki/File_format) standard for electronic [business cards](https://en.wikipedia.org/wiki/Business_card). vCards are often attached to [e-mail](https://en.wikipedia.org/wiki/E-mail) messages but can be exchanged in other ways. The format is widely used for data interchange among popular information exchange applications. A vCard usually contains name and address information, telephone numbers, e-mail addresses, URLs, logos, photographs, and any audio clips. A vCard is used as a data interchange format in personal digital assistants (PDAs), personal information managers (PIMs) and customer relationship management (CRMs). 



{{% alert color="primary" %}} 

If you want to know more about working with **VCard files** — take a look at the Aspose Email Cloud tutorial: [**Quick Start With VCard API**](/email/quick-start-with-vcard-api/).

{{% /alert %}} 

Owing to the importance and emerging needs for this format, Aspose.Email Cloud has been enriched to support this format. The Business cards recognition API is a card scanner, which allows you to convert captured business cards and name card images, into a vCard format, for later to be stored as contacts. In simple words, it enables us to convert images into VCard format.

The following image depicts a conversion flow from a business card to vCard format.

![todo:image\_alt\_text](https://raw.githubusercontent.com/wiki/aspose-email-cloud/aspose-email-cloud-dotnet/images/bcr.jpg)

{{% alert color="primary" %}}

To see how to setup SDKs use the [SDK setup tutorial](/email/sdk-setup/).

{{% /alert %}} 

## **Parse Business Card Image to VCard**

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
using (var file = File.OpenRead("path/to/file.png"))
{
    var result = await api.Ai.Bcr.ParseAsync(
        new AiBcrParseRequest(file, isSingle: true));
    Console.WriteLine(result.Value.First().DisplayName)
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] fileBytes = IOUtils.toByteArray(
    new FileInputStream(
        "some/business/card/image/on/disk.png"));
ContactList result = api.ai().bcr().parse(
    new AiBcrParseRequest(fileBytes, null, null, true));
ContactDto firstVCard = result.getValue().get(0);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
image_file = 'path/to/business/card/image.png'
result = api.ai.bcr.parse(
    models.AiBcrParseRequest(image_file))
contact = result.value[0]
display_name = contact.display_name
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
image = File.new('path/to/business/card/image.png')
result = api.ai.bcr.parse(
  AiBcrParseRequest.new(file: image, is_single: true))
contact = result.value[0]
display_name = contact.display_name
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const imageData = fs.readFileSync(
    'path/to/business/card/image.png');
const result = await api.ai.bcr.parse(
    new AiBcrParseRequest(
        imageData, undefined, undefined, true));
const contact = result.value[0];
const displayName = contact.displayName;
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$path = 'path/to/business/card/image.png';
$result = $api->ai()->bcr()->parse(
    new AiBcrParseRequest(
        new SplFileObject($path),
        null,
        null,
        true));
$contact = $result->getValue()[0];
$displayName = $contact->getDisplayName();
```

{{< /tab >}}

{{< /tabs >}}


## **Image Located on Storage**
Please try using [**ParseStorage**](/email/reference-ai-bcr-api/#parsestorage) method from [**AiBcrApi**](/email/reference-ai-bcr-api/) to recognize VCard from an image located on storage.

{{< tabs tabTotal="6" tabID="1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var storageName = "First Storage";
var outFolderPath = "path/to/out/folder/on/storage";
StorageFileLocationList result = await api.Ai.Bcr.ParseStorageAsync(
    new AiBcrParseStorageRequest(
        new StorageFolderLocation(storageName, outFolderPath),
        new List<AiBcrImageStorageFile>
        {
            new AiBcrImageStorageFile(true,
                new StorageFileLocation(
                    storageName,
                    "image/location/on/storage",
                    "image.png"))
        }, null));
// Get file location from recognition result
StorageFileLocation contactFile = result.Value.First();

// Download VCard file, produced by recognition method
using (var contactFileStream = await api.CloudStorage.File.DownloadFileAsync(
    new DownloadFileRequest(
        $"{contactFile.FolderPath}/{contactFile.FileName}",
        contactFile.Storage)))
using (var memoryStream = new MemoryStream())
{
    await contactFileStream.CopyToAsync(memoryStream);
    var contactFileContent = Encoding.UTF8.GetString(memoryStream.ToArray());
    //Print vcf file content to console:
    Constole.WriteLine(contactFileContent);
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
String storage = "First Storage";
String folder = "image/location/on/storage";
String fileName = "image.png";
String outFolderPath = "path/to/out/folder/on/storage";
ListResponseOfStorageFileLocation result =
    api.ai().bcr().parseStorage(
        new AiBcrParseStorageRequest(
            new StorageFolderLocation(storage, outFolderPath),
            Collections.singletonList(
                new AiBcrImageStorageFile(
                    true,
                    new StorageFileLocation(
                        storage,
                        folder,
                        fileName))),
                    null));
// Get file location from recognition result
StorageFileLocation contactFile = result.getValue().get(0);
// Download VCard file, produced by recognition method
byte[] contactBytes = api.cloudStorage().file().downloadFile(
    new DownloadFileRequest(
        contactFile.getFolderPath() + "/" + contactFile.getFileName(),
        contactFile.getStorage(),
        null));
String contactFileContent = new String(contactBytes, "UTF-8");
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
storage = 'First Storage'
folder = 'image/location/on/storage'
file_name = 'image.png'
out_folder_path = 'path/to/out/folder/on/storage'
result = api.ai.bcr.parse_storage(
    models.AiBcrParseStorageRequest(
        images=[models.AiBcrImageStorageFile(
            True,
            models.StorageFileLocation(
                storage,
                folder,
                file_name))],
        out_folder=models.StorageFolderLocation(
            storage, out_folder_path)))
# Get file location from recognition result
contact_file = result.value[0]
# Download VCard file, produced by recognition method
downloaded = api.cloud_storage.file.download_file(
    models.DownloadFileRequest(
        contact_file.folder_path + "/" + contact_file.file_name,
        storage))
with open(downloaded, 'r') as f:
    file_data = f.read()
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
storage = 'First Storage'
folder = 'image/location/on/storage'
file_name = 'image.png'
out_folder = 'path/to/out/folder/on/storage'
result = api.ai.bcr.parse_storage(
  AiBcrParseStorageRequest.new(
    out_folder: StorageFolderLocation.new(
        storage: storage,
        folder_path: out_folder),
    images: [AiBcrImageStorageFile.new(
      is_single: true,
      file: StorageFileLocation.new(
        storage: storage,
        folder_path: folder,
        file_name: file_name))]))
# Get file location from recognition result
contact_file = result.value[0]
# Download VCard file, produced by recognition method
downloaded = api.cloud_storage.file.download_file(
  DownloadFileRequest.new(
    path: "#{contact_file.folder_path}/#{contact_file.file_name}",
    storage_name: contact_file.storage))
content = IO.read(downloaded)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const storage = "First Storage";
const folder = "image/location/on/storage";
const fileName = "image.png";
const outFolderPath = "path/to/out/folder/on/storage";

const result = await api.ai.bcr.parseStorage(
    new AiBcrParseStorageRequest(
        new StorageFolderLocation(storage, outFolderPath),
        [new AiBcrImageStorageFile(true,
            new StorageFileLocation(storage, folder, fileName))]));
// Get file location from recognition result
const contactFile = result.value[0];
// Download VCard file, produced by recognition method
const contactBinary = await api.cloudStorage.file.downloadFile(
    new DownloadFileRequest(
        contactFile.folderPath + '/' + contactFile.fileName,
        storage));
const contactString = contactBinary.toString();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$storage = "First Storage";
$folder = "image/location/on/storage";
$fileName = "image.png";
$outFolderPath = "path/to/out/folder/on/storage";
$result = $api->ai()->bcr()->parseStorage(
    new AiBcrParseStorageRequest(
        new StorageFolderLocation($storage, $outFolderPath),
        array(new AiBcrImageStorageFile(
            true,
            new StorageFileLocation(
                $storage,
                $folder,
                $fileName)))));
// Get file location from recognition result
$contactFile = $result->getValue()[0];
// Download VCard file, produced by recognition method
$contactTempFile = $api->cloudStorage()->file()->downloadFile(
    new DownloadFileRequest(
        $contactFile->getFolderPath() . "/" . $contactFile->getFileName(),
        $storage));
$fileContent = $contactTempFile->fread($contactTempFile->getSize());
```

{{< /tab >}}

{{< /tabs >}}

## **More Tutorials**
See more Aspose Email Tutorials: 
{{< list-of-articles-in-this-section >}}