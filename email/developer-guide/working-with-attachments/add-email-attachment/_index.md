---
title: "Add Email Attachment"
type: docs
url: /add-email-attachment/
weight: 20
---

## **Introduction**
This example allows you to add attachment to a message by attachment name using Aspose.Email for Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.



{{% alert color="primary" %}} 

If you want to know more about working with emails’ attachments — take a look at the Aspose Email Cloud tutorial: [**Email Message Files**](/emailcloud/email-message-files/).

{{% /alert %}} 
## **Resource**
The following Aspose.Email for Cloud REST API resource has been used in the examples:[attachment](https://apireference.aspose.cloud/email/#/Email/AddEmailAttachment)
## **REST Methods References**
We're referring some common methods in the REST examples to perform general operations. These methods can be found at the following page: [REST API Methods](https://apireference.aspose.cloud/email)
## **REST Examples**

{{< tabs tabTotal="4" tabID="1" tabName1="C#" tabName2="VB.NET" tabName3="Android" tabName4="Objective C" >}}

{{< tab tabNum="1" >}}
```java

// Initialize variables being used

string appSid = "Get it from https://cloud.aspose.com";

string appKey = "Get it from https://cloud.aspose.com";

string name = "email-sample.mht";

string attachName = "sample.png";

string folder = "Email";

string storage = string.Empty;

// Build URI to perform request

string apiUrl = string.Format(@"email/{0}/attachments/{1}?storage={2}&folder={3}", name, attachName, storage, folder);

ServiceController.Post(apiUrl, appSid, appKey);

```
{{< /tab >}}

{{< tab tabNum="2" >}}
```java

' Initialize variables being used

Dim appSid As String = "Get it from https://cloud.aspose.com"

Dim appKey As String = "Get it from https://cloud.aspose.com"

Dim name As String = "email-sample.mht"

Dim attachName As String = "sample.png"

Dim folder As String = "Email"

Dim storage As String = String.Empty

' Build URI to perform request

Dim apiUrl As String = String.Format("email/{0}/attachments/{1}?storage={2}&folder={3}", name, attachName, storage, folder)

ServiceController.Post(apiUrl, appSid, appKey)

```

{{< /tab >}}

{{< tab tabNum="3" >}}
```java

AsposeApp.setAppKeyAndAppSID("Get it from https://cloud.aspose.com", "Get it from https://cloud.aspose.com");

AsposeApp.setBaseProductURI("http://api.aspose.com/v1.1");

String EMAIL\_URI = AsposeApp.BASE\_PRODUCT\_URI + "/email/";

AddEmailAttachmentResponse addEmailAttachmentResponse = null;

String fileName = "Leaves.eml";

String attachmentName = "certificate.png"

//build URL

String strURL = EMAIL\_URI + Uri.encode(fileName) + "/attachments/" + Uri.encode(attachmentName);

//sign URL

String signedURL = Utils.sign(strURL);

InputStream responseStream = Utils.processCommand(signedURL, "POST");

String jsonStr = Utils.streamToString(responseStream);

//Parsing JSON

Gson gson = new Gson();

addEmailAttachmentResponse = gson.fromJson(jsonStr, AddEmailAttachmentResponse.class);

if(addEmailAttachmentResponse.getCode().equals("200") && addEmailAttachmentResponse.getStatus().equals("OK")) {

    return addEmailAttachmentResponse;

}


```
{{< /tab >}}

{{< tab tabNum="4" >}}
```java

[ASPOSEApp setAppKey:@"Get it from https://cloud.aspose.com" andAppSID:@"Get it from https://cloud.aspose.com"];

[ASPOSEProduct setBaseProductUri:@"http://api.aspose.com/v1.1"];

NSString \*EMAIL\_URI = [[ASPOSEProduct baseProductUri] stringByAppendingString:@"/email/"];

ASPOSEAddNewDocumentResponse \*addEmailAttachmentResponse = nil;

NSString \*fileName = @"Monthly Report.eml";

NSString \*attachmentName = @"sample.jpg";

//build URL

NSString \*strURL = [NSString stringWithFormat:@"%@%@/attachments/%@", EMAIL\_URI,

                    [fileName stringByAddingPercentEscapesUsingEncoding:NSUTF8StringEncoding],

                    [attachmentName stringByAddingPercentEscapesUsingEncoding:NSUTF8StringEncoding]];

//sign URL

NSString \*signedURL = [ASPOSEUtils sign:strURL];

NSData \*responseData = [ASPOSEUtils processCommand:signedURL httpMethod:@"POST"];

if(responseData) {

    NSError \*error;

    ASPOSEAddNewDocumentResponse \*addEmailAttachmentResponse = [[ASPOSEAddNewDocumentResponse alloc] initWithData:responseData error:&error];

    if(!error && [addEmailAttachmentResponse.code isEqualToString:@"200"] && [addEmailAttachmentResponse.status isEqualToString:@"OK"]) {

        return addEmailAttachmentResponse;

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

curl -v "http://api.aspose.cloud/v1.1/email/email\_test.eml/attachments/README.TXT?appSID=XXXX&signature=XXXX" \
     -X POST \
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

        "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml",

        "Rel": "self",

        "Type": null,

        "Title": null

      },

      {

        "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml?format=eml",

        "Rel": "alternate",

        "Type": "application/eml",

        "Title": "Download as EML"

      },

      {

        "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml?format=msg",

        "Rel": "alternate",

        "Type": "application/msg",

        "Title": "Download as MSG"

      },

      {

        "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml?format=mht",

        "Rel": "alternate",

        "Type": "application/mht",

        "Title": "Download as MHT"

      }

    ],

    "DocumentProperties": {

      "Link": {

        "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/",

        "Rel": "self",

        "Type": null,

        "Title": null

      },

      "List": [

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/Bcc",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "Bcc",

          "Value": ""

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/Body",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "Body",

          "Value": "test message"

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/CC",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "CC",

          "Value": ""

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/Date",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "Date",

          "Value": "\/Date(1400060620000)\/"

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/DeliveryNotificationOptions",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "DeliveryNotificationOptions",

          "Value": 0

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/From",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "From",

          "Value": "masood@kpisol.com"

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/To",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "To",

          "Value": "masood@kpisol.com"

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/HtmlBody",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "HtmlBody",

          "Value": ""

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/IsBodyHtml",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "IsBodyHtml",

          "Value": false

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/MessageId",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "MessageId",

          "Value": "<53733ACC.7050206@kpisol.com>"

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/Priority",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "Priority",

          "Value": "Normal"

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/Subject",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "Subject",

          "Value": "test"

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/TextBody",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "TextBody",

          "Value": "test message"

        },

        {

          "Link": {

            "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/Attachments",

            "Rel": "self",

            "Type": null,

            "Title": null

          },

          "Name": "Attachments",

          "Value": [

            {

              "Name": "README.TXT"

            },

            {

              "Name": "README.TXT"

            }

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
**Add email attachment**

{{< tabs tabTotal="9" tabID="19" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Objective C" tabName9="Perl" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-email" "838d7478e3720f941514d3d04417e82e" "Examples-DotNET-CSharp-Email-AddNewEmail-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-email" "10428737982c525bf33b54ad9c27b707" "Examples-JAVA-SDK-src-main-java-com-aspose-email-cloud-examples-working-AddNewAttachment-AddNewAttachment.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "" "a052f420f51722082cbb70d5e8d0f339" "Examples-PHP-Attachments-PostAddEmailAttachment-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-email" "3f41448648db89803193189f274722fa" "Examples-Ruby-Attachments-add\_email\_attachment-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-email" "13478a90f198800bfcdafa983dbd0fcd" "AddNewAttachment.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-email" "838d7478e3720f941514d3d04417e82e" "Examples-Node.js-Email-AddNewEmail-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-email" "95a576636fc5c03e126e2617c83ce117" "Examples-Android-app-src-main-java-com-aspose-email-cloud-examples-working-attachments-AddNewAttachment-AddNewAttachment.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-email" "838d7478e3720f941514d3d04417e82e" "Examples-Perl-Email-AddNewEmail-1.pl" >}}

{{< /tab >}}

{{< /tabs >}}
