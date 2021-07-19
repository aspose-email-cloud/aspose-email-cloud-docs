---
title: "Aspose.Email Cloud 19.11 Release Notes"
type: docs
url: /aspose-email-cloud-19-11-release-notes/
weight: 20
---

## **API changes**
Aspose.Email Cloud 19.11 comes with new v3.0 API, which includes:

- SaaSposeResponse model was removed.
- All POST, PUT, DELETE actions parameters were moved from query to the request`s body 
## **New features**
Introducing new APIs for VCard, iCalendar ﬁles and MAPI messages

- **VCard**, also known as VCF (Virtual Contact File), is a ﬁle format standard for electronic business cards, which is popular.  VCards are often attached to e-mail messages. They can contain name and address information, telephone numbers, e-mail addresses, URLs, logos, photographs, and audio clips. 
- **Messaging Application Programming Interface** (MAPI) is an API for Microsoft Windows which allows programs to become email-aware. While MAPI is designed to be independent of the protocol, it is usually used to communicate with Microsoft Exchange Server.
- **iCalendar** allows users to store and exchange calendaring and scheduling information such as events, to-dos, journal entries, and free/busy information.  For example, you need to get iCalendar properties using .NET SDK. You can use the following code to achieve this. 

```csharp
using System;
using System.Collections.Generic;
using System.Threading.Tasks;
using Aspose.Email.Cloud.Sdk.Api;
using Aspose.Email.Cloud.Sdk.Client;
using Aspose.Email.Cloud.Sdk.Model;
using Aspose.Email.Cloud.Sdk.Model.Requests;

namespace Example
{
    internal static class Program
    {
        public static async Task Main(string[] args)
        {
            var conﬁguration = new Conﬁguration
            {
                AppKey = "app key",
                AppSid = "app secret",
                ApiVersion = "v3.0",
                ApiBaseUrl = "https://api.aspose.cloud"
            };
            var api = new EmailApi(conﬁguration);
            var response = await api.GetCalendarAsync(new GetCalendarRequest("sample.ics", "1", "First Storage"));
            Console.WriteLine(response.Name); /\* Prints "CALENDAR" \*/
            foreach(var property in response.InternalProperties)
            {
                Console.WriteLine(property.Name); /\* Prints iCalendar property names \*/
            }
        }
    }
}
```

- **GetCalendarAsync** This method gets iCalendar ﬁles list in the folder on the storage.  To use this method you need to pass three requirement parameters: **folder path in the storage**, **items count on the page** and **page number**. 
- **GetCalendarRequest** This method is intended to get calendar ﬁle properties. To use this method you should pass only one parameter – **calendar ﬁle name in the storage**.
## **Storage APIs are included in Email**
To provide a better user experience and uniﬁcation, we added storage APIs into Email. For example, to upload a ﬁle with .NET SDK, you just need to use EmailApi class. This approach makes developing easier.

```csharp
using(var stream = File.OpenRead("someFile.ext")) {
    var uploadRequest = new UploadFileRequest("folder/on/storage/ﬁleName.ext", stream, "Storage Name");
    await api.UploadFileAsync(uploadRequest);
}
```
## **SDK changes**
- PHP SDK package renamed to "aspose/aspose-email-cloud" 
- Java SDK package renamed to "aspose-email-cloud"
- Python SDK package renamed to "aspose-email-cloud" (old package is removed from PYPI)
- NodeJs SDK package renamed to "@asposecloud/aspose-email-cloud" 
- NET SDK now supports multiple target frameworks, such as: net20, net452, netstandard2.0, Xamarin.iOS10, Xamarin.Mac20, MonoAndroid60
- .NET SDK contains async methods for frameworks net452 and netstandard2.0
- **All SDKs include Storage APIs**
- .NET, Ruby, Python, Java SDKs now **have full-reference documentation** in markdown ﬁles. See GitHub repositories:
  - [.Net  ](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet)
  - [Ruby](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby)
  - [Python ](https://github.com/aspose-email-cloud/aspose-email-cloud-python)
  - [Java ](https://github.com/aspose-email-cloud/aspose-email-cloud-java)
- All SDKs provide all API methods in the one **EmailApi** class, including storage methods.
