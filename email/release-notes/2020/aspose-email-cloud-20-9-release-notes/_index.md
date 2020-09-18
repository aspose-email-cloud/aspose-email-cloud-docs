---
title: "Aspose.Email Cloud 20.9 Release Notes"
type: docs
url: /aspose-email-cloud-20-9-release-notes/
weight: 110
---

## **API Changes**
Aspose.Email Cloud 20.9 comes with a new v4.0 API which includes:

- BaseObject, HierarchicalObject, PrimitiveObject models, and corresponding APIs removed.
- New unified file API was implemented.
- Business card recognition API was improved.
- OFT file format support added.
- Email message converting API improved.


## **SDK Changes**

All SDKs were completely redesigned:

- EmailApi class replaced by EmailCloud.
- All methods were split into groups and renamed. Now it is much easier to find the function you need. For example:
    ```cs
    var emailMessage = new EmailDto();
    ...
    //Previous versions:
    var mapiStream = api.ConvertEmailModelToFile(
        new ConvertEmailModelToFileRequest(
            "Msg", emailMessage));
    
    //v4.0 based SDK:
    var mapiStream = cloud.Email.AsFile(
        new EmailAsFileRequest("Msg", emailMessage));
    ```
- Request models now stored in the same folder as all other models. So you don't have to guess which namespace should be used. Also, there is no unnecessary double wrapping of models anymore:
    ```cs
    //Previous versions:
    await api.SaveEmailClientAccountAsync(new SaveEmailClientAccountRequest(
        //StorageFileRqOfEmailClientAccount model is an unnecessary second wrapping here:
        new StorageFileRqOfEmailClientAccount(
            emailClientAccount,
            new StorageFileLocation(StorageName, Folder, fileName))));
    //v4.0 based SDK:
    await cloud.Client.Account.SaveAsync(new ClientAccountSaveRequest(
    new StorageFileLocation(StorageName, Folder, fileName), emailClientAccount));
    ```
- Model inheritance discriminators using improved.
- Ruby model constructors now use named arguments instead of positional.
- Typescript functions now return the result without any extra HTTP data.
- Typescript SDK package imports corrected.
- All PHP model files now have the correct CamelCase naming.
- All Java SDK models now have Fluent property setters.
