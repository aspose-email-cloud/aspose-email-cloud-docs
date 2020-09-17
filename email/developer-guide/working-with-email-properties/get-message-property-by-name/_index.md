---
title: "Get Message Property By Name"
type: docs
url: /get-message-property-by-name/
weight: 30
---

## **Introduction**
This example allows you to get an email's property by name using Aspose.Email for Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **Resource**
The following Aspose.Email for Cloud REST API resource has been used in the examples: [properties](https://apireference.aspose.cloud/email/#/Email/GetEmailProperty).
## **REST Methods References**
We're referring some common methods in the REST examples to perform general operations. These methods can be found at the following page: [REST API Methods](https://apireference.aspose.cloud/email)
## **REST Examples**

{{< tabs tabTotal="4" tabID="1" tabName1="C#" tabName2="VB.NET"  
tabName3="Android" tabName4="Objective C" >}}
{{< tab tabNum="1" >}}
```java

// Initialize variables being used

string appSid = "Get it from https://cloud.aspose.com";

string appKey = "Get it from https://cloud.aspose.com";

/// <summary>

/// Read document property by name.

/// </summary>

/// <param name="name">File name. e.g. myEmail.msg</param>

/// <param name="propertyName">Property Name</param>

/// <param name="folder">Folder path.</param>

/// <param name="storage">The document storage.</param>

string name; string propertyName; string folder; string storage = "";

// Build URI to perform request. ServiceController is located in Aspose.Cloud.Common in .NET SDK Source code available at http://goo.gl/BftpIi

string apiUrl = string.Format(@"email/{0}/properties/{1}?storage={2}&folder={3}", name, propertyName, storage, folder);

JObject jObject = JObject.Parse(ServiceController.Get(apiUrl, appSid, appKey));

EmailPropertyResponse emailPropertyResponse = jObject.ToObject<EmailPropertyResponse>();

```
{{< /tab >}}

{{< tab tabNum="2" >}}
```java

' Initialize variables being used

Dim appSid As String = "Get it from https://cloud.aspose.com"

Dim appKey As String = "Get it from https://cloud.aspose.com"

''' <summary>

''' Read document property by name.

''' </summary>

''' <param name="name">File name. e.g. myEmail.msg</param>

''' <param name="propertyName">Property Name</param>

''' <param name="folder">Folder path.</param>

''' <param name="storage">The document storage.</param>

Dim name As String

Dim propertyName As String

Dim folder As String

Dim storage As String = ""

' Build URI to perform request. ServiceController is located in Aspose.Cloud.Common in .NET SDK Source code available at http://goo.gl/BftpIi

Dim apiUrl As String = String.Format("email/{0}/properties/{1}?storage={2}&folder={3}", name, propertyName, storage, folder)

Dim jObject\_\_1 As JObject = JObject.Parse(ServiceController.[Get](apiUrl, appSid, appKey))

Dim emailPropertyResponse As EmailPropertyResponse = jObject\_\_1.ToObject(Of EmailPropertyResponse)()

```

{{< /tab >}}

{{< tab tabNum="3" >}}
```java

AsposeApp.setAppKeyAndAppSID("Get it from https://cloud.aspose.com", "Get it from https://cloud.aspose.com");

AsposeApp.setBaseProductURI("http://api.aspose.com/v1.1");

String EMAIL\_URI = AsposeApp.BASE\_PRODUCT\_URI + "/email/";

String propertyValue = null;

String fileName = "Message.msg";

String propertyName = "Body";

//build URL

String strURL = EMAIL\_URI + Uri.encode(fileName) + "/properties/" + Uri.encode(propertyName);

//sign URL

String signedURL = Utils.sign(strURL);

InputStream responseStream = Utils.processCommand(signedURL, "GET");

String jsonStr = Utils.streamToString(responseStream);

//Parsing JSON

Gson gson = new Gson();

EmailPropertyResponse emailPropertyResponse = gson.fromJson(jsonStr, EmailPropertyResponse.class);

if(emailPropertyResponse.getCode().equals("200") && emailPropertyResponse.getStatus().equals("OK")) {

    propertyValue = (String)emailPropertyResponse.emailProperty.value;

}



```
{{< /tab >}}

{{< tab tabNum="4" >}}
```java

[ASPOSEApp setAppKey:@"Get it from https://cloud.aspose.com" andAppSID:@"Get it from https://cloud.aspose.com"];

[ASPOSEProduct setBaseProductUri:@"http://api.aspose.com/v1.1"];

NSString \*EMAIL\_URI = [[ASPOSEProduct baseProductUri] stringByAppendingString:@"/email/"];

NSObject \*propertyValue = nil;

NSString \*fileName = @"Self Assessment.eml";

NSString \*propertyName = @"Body";

//build URL

NSString \*strURL = [NSString stringWithFormat:@"%@%@/properties/%@", EMAIL\_URI,

                    [fileName stringByAddingPercentEscapesUsingEncoding:NSUTF8StringEncoding], propertyName];

//sign URL

NSString \*signedURL = [ASPOSEUtils sign:strURL];

NSData \*responseData = [ASPOSEUtils processCommand:signedURL httpMethod:@"GET"];

//Parsing JSON

if(responseData) {

    NSError \*error;

    ASPOSEEmailPropertyResponse \*emailPropertyResponse = [[ASPOSEEmailPropertyResponse alloc] initWithData:responseData error:&error];

    if(!error && [emailPropertyResponse.code isEqualToString:@"200"] && [emailPropertyResponse.status isEqualToString:@"OK"]) {

        propertyValue = emailPropertyResponse.emailProperty.value;

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

curl -v "http://api.aspose.cloud/v1.1/email/email\_test.eml/properties/Subject?appSID=XXXX&signature=XXXX" \
     -X GET \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "EmailProperty": {

    "Link": {

      "Href": "http://api.aspose.cloud/v1.1/email/email\_test.eml/documentproperties/Subject",

      "Rel": "self",

      "Type": null,

      "Title": null

    },

    "Name": "Subject",

    "Value": "This is a new subject"

  },

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}
## **SDK Examples**
**Get message property**

{{< tabs tabTotal="9" tabID="19" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Objective C" tabName9="Perl" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-email" "838d7478e3720f941514d3d04417e82e" "Examples-DotNET-CSharp-Email-Properties-GetMessageProperty-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-email" "10428737982c525bf33b54ad9c27b707" "Examples-JAVA-SDK-src-main-java-com-aspose-email-cloud-properties-GetMessagePropertyByNameExample-GetMessagePropertyByNameExample.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-email" "3f41448648db89803193189f274722fa" "Examples-Ruby-EmailProperties-read\_document\_property\_by\_name-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-email" "13478a90f198800bfcdafa983dbd0fcd" "GetMessagePropertyByName.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-email" "838d7478e3720f941514d3d04417e82e" "Examples-Node.js-Email-Properties-GetMessageProperty-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-email" "95a576636fc5c03e126e2617c83ce117" "Examples-Android-app-src-main-java-com-aspose-email-cloud-examples-working-properties-GetMessagePropertyByNameExample-GetMessagePropertyByNameExample.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-email" "838d7478e3720f941514d3d04417e82e" "Examples-Perl-Email-Properties-GetMessageProperty-1.pl" >}}

{{< /tab >}}

{{< /tabs >}}
