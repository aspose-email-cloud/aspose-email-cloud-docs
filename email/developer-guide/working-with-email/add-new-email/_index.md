---
title: "Add New Email"
type: docs
url: /add-new-email/
weight: 20
---

## **Introduction**
This example allows you to Add new email using Aspose.Email for Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.



{{% alert color="primary" %}} 

If you want to know more about working with emails — take a look at the Aspose Email Cloud tutorial: [**Email Message Files**](/emailcloud/email-message-files/).

{{% /alert %}} 
## **Resource**
The following Aspose.Email for Cloud REST API resource has been used in the examples: [document](https://apireference.aspose.cloud/email/#!/Email/Email_PutCreateNewEmail).
## **REST Methods References**
We're referring some common methods in the REST examples to perform general operations. These methods can be found at the following page: [REST API Methods](https://apireference.aspose.cloud/email)
## **REST Examples**

{{< tabs tabTotal="4" tabID="5" tabName1="C#" tabName2="Java" tabName3="Android" tabName4="Objective C" >}}


{{< tab tabNum="1" >}}

```csharp

// Initialize variables being used

string appSid = "Get it from https://cloud.aspose.com";

string appKey = "Get it from https://cloud.aspose.com";

/// <summary>

/// Add new email.

/// </summary>

/// <param name="name">File name. e.g. myEmail.msg</param>

/// <param name="folder">Folder path.</param>

/// <param name="folder">EmailDocument object.</param>

/// <param name="storage">The document storage.</param>

string name; string folder; EmailDocumentPropertiesRequest emailDocumentPropertiesRequest; string storage = "";

// Build URI to perform request. ServiceController is located in Aspose.Cloud.Common in .NET SDK Source code available at http://goo.gl/BftpIi

string apiUrl = string.Format(@"email/{0}?storage={1}&folder={2}", name, storage, folder);

ServiceController.Put(apiUrl, appSid, appKey, JsonConvert.SerializeObject(emailDocumentPropertiesRequest));

```
{{< /tab >}}

{{< tab tabNum="2" >}}
```java

' Initialize variables being used

Dim appSid As String = "Get it from https://cloud.aspose.com"

Dim appKey As String = "Get it from https://cloud.aspose.com"

''' <summary>

''' Add new email.

''' </summary>

''' <param name="name">File name. e.g. myEmail.msg</param>

''' <param name="folder">Folder path.</param>

''' <param name="folder">EmailDocument object.</param>

''' <param name="storage">The document storage.</param>

Dim name As String

Dim folder As String

Dim emailDocumentPropertiesRequest As EmailDocumentPropertiesRequest

Dim storage As String = ""

' Build URI to perform request. ServiceController is located in Aspose.Cloud.Common in .NET SDK Source code available at http://goo.gl/BftpIi

Dim apiUrl As String = String.Format("email/{0}?storage={1}&folder={2}", name, storage, folder)

ServiceController.Put(apiUrl, appSid, appKey, JsonConvert.SerializeObject(emailDocumentPropertiesRequest))

```
{{< /tab >}}

{{< tab tabNum="3" >}}

```java

AsposeApp.setAppKeyAndAppSID("Get it from https://cloud.aspose.com", "Get it from https://cloud.aspose.com");

AsposeApp.setBaseProductURI("http://api.aspose.com/v1.1");

String EMAIL\_URI = AsposeApp.BASE\_PRODUCT\_URI + "/email/";

AddNewEmailResponse addNewEmailResponse = null;

String emailName = "newEmail.eml";

EmailDocument emailDocument = new EmailDocument();

emailDocument.links = new ArrayList<LinkModel>();

LinkModel mLink = new LinkModel();

mLink.href = "http://api.aspose.com/v1.1/email/newEmail.eml";

mLink.rel = "self";

mLink.type = null;

mLink.title = null;

emailDocument.links.add(mLink);

emailDocument.emailDocumentProperties = new EmailDocumentProperties();

emailDocument.emailDocumentProperties.link = new LinkModel();

emailDocument.emailDocumentProperties.link.href = "http://api.aspose.com/v1.1/email/newEmail.eml/documentproperties/";

emailDocument.emailDocumentProperties.link.rel = "self";

emailDocument.emailDocumentProperties.link.type = null;

emailDocument.emailDocumentProperties.link.title = null;

emailDocument.emailDocumentProperties.emailPropertiesList = new ArrayList<EmailProperty>();

EmailProperty mEmailProperty = new EmailProperty();

mEmailProperty.name = "From";

mEmailProperty.value = "ben@aspose.com";

emailDocument.emailDocumentProperties.emailPropertiesList.add(mEmailProperty);

mEmailProperty = new EmailProperty();

mEmailProperty.name = "To";

mEmailProperty.value = "marketplace@aspose.com";

emailDocument.emailDocumentProperties.emailPropertiesList.add(mEmailProperty);

mEmailProperty = new EmailProperty();

mEmailProperty.name = "Subject";

mEmailProperty.value = "Leaves Notification";

emailDocument.emailDocumentProperties.emailPropertiesList.add(mEmailProperty);

//build URL

String strURL = EMAIL\_URI + Uri.encode(emailName);

//sign URL

String signedURL = Utils.sign(strURL);

//Encoding to JSON

Gson gson = new Gson();

String jsonStr = gson.toJson(emailDocument);

InputStream responseStream = Utils.processCommand(signedURL, "PUT", jsonStr);

String responseStr = Utils.streamToString(responseStream);

//Parsing JSON

addNewEmailResponse = gson.fromJson(responseStr, AddNewEmailResponse.class);

if(addNewEmailResponse.getCode().equals("200") && addNewEmailResponse.getStatus().equals("OK")) {

    return addNewEmailResponse;

}


```
{{< /tab >}}

{{< tab tabNum="4" >}}
```java

[ASPOSEApp setAppKey:@"Get it from https://cloud.aspose.com" andAppSID:@"Get it from https://cloud.aspose.com"];

[ASPOSEProduct setBaseProductUri:@"http://api.aspose.com/v1.1"];

NSString \*EMAIL\_URI = [[ASPOSEProduct baseProductUri] stringByAppendingString:@"/email/"];

NSString \*fileName = @"Marketplace.eml";

ASPOSEEmailCommonInfo \*emailData = [[ASPOSEEmailCommonInfo alloc] init];

NSMutableArray<ASPOSEHrefToDocument> \*mLinks = (NSMutableArray<ASPOSEHrefToDocument> \*) [[NSMutableArray alloc] init];

ASPOSEHrefToDocument \*mLink = [[ASPOSEHrefToDocument alloc] init];

mLink.href = @"http://api.aspose.com/v1.1/email/newEmail.eml";

mLink.rel = @"self";

mLink.type = nil;

mLink.title = nil;

[mLinks addObject:mLink];

emailData.links = mLinks;

ASPOSEEDocumentProperties \*mDocumentProperties = [[ASPOSEEDocumentProperties alloc] init];

mLink = [[ASPOSEHrefToDocument alloc] init];

mLink.href = @"http://api.aspose.com/v1.1/email/newEmail.eml/documentproperties/";

mLink.rel = @"self";

mLink.type = nil;

mLink.title = nil;

mDocumentProperties.link = mLink;

NSMutableArray<ASPOSEEmailProperty> \*emailPropertiesList = (NSMutableArray<ASPOSEEmailProperty> \*) [[NSMutableArray alloc] init];

ASPOSEEmailProperty \*emailProperty = [[ASPOSEEmailProperty alloc] init];

emailProperty.name = @"From";

emailProperty.value = @"ben@aspose.com";

[emailPropertiesList addObject:emailProperty];

emailProperty = [[ASPOSEEmailProperty alloc] init];

emailProperty.name = @"To";

emailProperty.value = @"marketplace@aspose.com";

[emailPropertiesList addObject:emailProperty];

emailProperty = [[ASPOSEEmailProperty alloc] init];

emailProperty.name = @"Subject";

emailProperty.value = @"Progress Report";

[emailPropertiesList addObject:emailProperty];

mDocumentProperties.list = emailPropertiesList;

emailData.documentProperties = mDocumentProperties;

NSString \*requestJSONString = [emailData toJSONString];

//build URL

NSString \*strURL = [NSString stringWithFormat:@"%@%@", EMAIL\_URI,

                    [fileName stringByAddingPercentEscapesUsingEncoding:NSUTF8StringEncoding]];

//sign URL

NSString \*signedURL = [ASPOSEUtils sign:strURL];

NSData \*responseData = [ASPOSEUtils processCommand:signedURL httpMethod:@"PUT"

                                           content:requestJSONString contentType:CONTENT\_TYPE\_JSON];

if(responseData) {

    NSError \*error;

    ASPOSEAddNewDocumentResponse \*addNewEmailResponse = [[ASPOSEAddNewDocumentResponse alloc] initWithData:responseData error:&error];

    if(!error && [addNewEmailResponse.code isEqualToString:@"200"] && [addNewEmailResponse.status isEqualToString:@"OK"]) {

        return addNewEmailResponse;

    }

}


```

{{< /tab >}}
{{< /tabs >}}

## **Setup Aspose.Email Cloud SDK**


Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/emailcloud/sdk-setup/).

{{% /alert %}}
## **cURL Example**
{{< tabs tabTotal="2" tabID="16" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -v "http://api.aspose.cloud/v1.1/email/email\_test2.eml?appSID=XXXX&signature=XXXX" \
     -X PUT \
    -d '{"DocumentProperties": {"List": [{"Name": "Body", "Value": "This is body"}, {"Name": "To", "Value": "developer@aspose.com"}, {"Name": "From", "Value": "sales@aspose.com"}]}, "Format": "eml"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Document": {

    "Links": [

      {

        "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml",

        "Rel": "self",

        "Type": null,

        "Title": null

      },

      {

        "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml?format=eml",

        "Rel": "alternate",

        "Type": "application/eml",

        "Title": "Download as EML"

      },

      {

        "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml?format=msg",

        "Rel": "alternate",

        "Type": "application/msg",

        "Title": "Download as MSG"

      },

      {

        "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml?format=mht",

        "Rel": "alternate",

        "Type": "application/mht",

        "Title": "Download as MHT"

      }

    ],

    "DocumentProperties": {

      "Link": {

        "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml/documentproperties/",

        "Rel": "self",

        "Type": null,

        "Title": null

      },

      "List": [

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml/documentproperties/Bcc",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "Bcc",

          "Value": ""

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml/documentproperties/Body",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "Body",

          "Value": "This is body"

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml/documentproperties/CC",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "CC",

          "Value": ""

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml/documentproperties/Date",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "Date",

          "Value": "\/Date(1491769809496+0000)\/"

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml/documentproperties/DeliveryNotificationOptions",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "DeliveryNotificationOptions",

          "Value": 0

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml/documentproperties/From",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "From",

          "Value": "sales@aspose.com"

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml/documentproperties/To",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "To",

          "Value": "developer@aspose.com"

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml/documentproperties/HtmlBody",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "HtmlBody",

          "Value": ""

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml/documentproperties/IsBodyHtml",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "IsBodyHtml",

          "Value": false

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml/documentproperties/MessageId",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "MessageId",

          "Value": ""

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml/documentproperties/Priority",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "Priority",

          "Value": "Normal"

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml/documentproperties/Subject",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "Subject",

          "Value": ""

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml/documentproperties/TextBody",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "TextBody",

          "Value": "This is body"

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test2.eml/documentproperties/Attachments",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "Attachments",

          "Value": [



          ]

        }

      ]

    }

  },

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}
## **SDK Examples**
**Add new email**

{{< tabs tabTotal="9" tabID="19" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Objective C" tabName9="Perl" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-email" "838d7478e3720f941514d3d04417e82e" "Examples-DotNET-CSharp-Email-AddNewEmail-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-email" "10428737982c525bf33b54ad9c27b707" "Examples-JAVA-SDK-src-main-java-com-aspose-email-cloud-examples-working-AddNewEmailExample-AddNewEmailExample.java" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "" "a052f420f51722082cbb70d5e8d0f339" "Examples-PHP-Email-PutCreateNewEmail-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-email" "3f41448648db89803193189f274722fa" "Examples-Ruby-Email-add\_new\_email-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-email" "13478a90f198800bfcdafa983dbd0fcd" "AddNewEmail.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-email" "838d7478e3720f941514d3d04417e82e" "Examples-Node.js-Email-AddNewEmail-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-email" "95a576636fc5c03e126e2617c83ce117" "Examples-Android-app-src-main-java-com-aspose-email-cloud-examples-working-AddNewEmailExample-AddNewEmailExample.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-email" "838d7478e3720f941514d3d04417e82e" "Examples-Perl-Email-AddNewEmail-1.pl" >}}

{{< /tab >}}

{{< /tabs >}}
