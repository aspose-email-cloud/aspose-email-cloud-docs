---
title: "Retrieve Message Properties"
type: docs
url: /retrieve-message-properties/
weight: 10
---

## **Introduction**
This example allows you to retrieve an email's property using Aspose.Email for Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **Resource**
The following Aspose.Email for Cloud REST API resource has been used in the examples:[properties](https://apireference.aspose.cloud/email/#/Email/GetEmailProperty)
## **REST Methods References**
We're referring some common methods in the REST examples to perform general operations. These methods can be found at the following page: [REST API Methods](https://apireference.aspose.cloud/email)
## **REST Examples**

{{< tabs tabTotal="11" tabID="1" tabName1="C#" tabName2="VB.NET" tabName3="Java" tabName4="PHP" 
tabName5="Ruby" tabName6="Python" tabName7="Perl" tabName8="Node.js" tabName9="C++" 
tabName10="Android" tabName11="Objective C" >}}

{{< tab tabNum="1" >}}
```java

// Initialize variables being used

string appSid = "Get it from https://cloud.aspose.com";

string appKey = "Get it from https://cloud.aspose.com";

string name = "email-sample.msg";

string folder = "Email";

string storage = string.Empty;

// Build URI to perform request

string apiUrl = string.Format(@"email/{0}?storage={1}&folder={2}", name, storage, folder);

// Parse the json string to JObject. ServiceController is located in Aspose.Cloud.Common in .NET SDK Source code available at http://goo.gl/BftpIi

JObject jObject = JObject.Parse(ServiceController.Get(apiUrl, appSid, appKey));

EmailDocumentPropertiesResponse emailDocumentPropertiesResponse = jObject.ToObject<EmailDocumentPropertiesResponse>();

```
{{< /tab >}}

{{< tab tabNum="2" >}}
```java

' Initialize variables being used

Dim appSid As String = "Get it from https://cloud.aspose.com"

Dim appKey As String = "Get it from https://cloud.aspose.com"

Dim name As String = "email-sample.msg"

Dim folder As String = "Email"

Dim storage As String = String.Empty

' Build URI to perform request

Dim apiUrl As String = String.Format("email/{0}?storage={1}&folder={2}", name, storage, folder)

' Parse the json string to JObject. ServiceController is located in Aspose.Cloud.Common in .NET SDK Source code available at http://goo.gl/BftpIi

Dim jObject As JObject = JObject.Parse(ServiceController.Get(apiUrl, appSid, appKey))

Dim emailDocumentPropertiesResponse As EmailDocumentPropertiesResponse = jObject.ToObject(Of EmailDocumentPropertiesResponse)()

```
{{< /tab >}}

{{< tab tabNum="3" >}}
```java

import java.io.\*;

import com.aspose.cloud.common.\*;

String appSID = "...";

String appKey = "...";

String method = "GET";

String requestUrl = "http://api.aspose.com/v1.1/email/Sample1.eml/properties/MessageId";

String signedUrl = Utils.Sign(requestUrl, appKey, appSID);

InputStream stream = Utils.ProcessCommand(signedUrl, method);

String response = Utils.StreamToString(stream);

stream.close();


```
{{< /tab >}}

{{< tab tabNum="4" >}}
```java

use Aspose\Cloud\Common\AsposeApp;

use Aspose\Cloud\Common\Utils;

AsposeApp::$appSID = "...";

AsposeApp::$appKey = "...";

$method = "GET";

$base_url = "http://api.aspose.com/v1.1";

$request_url = "$base_url/email/Sample1.eml/properties/MessageId";

$signed_url = Utils::sign($request_url);

$response = Utils::processCommand($signed_url, $method, "", "");

$response = json_decode($response);

var_dump($response);


```
{{< /tab >}}

{{< tab tabNum="5" >}}
```java

app_sid = "..."

app_key = "..."

request_url = "http://api.aspose.com/v1.1/email/Sample1.eml/properties/MessageId"

Aspose::Cloud::Common::AsposeApp.new(app_sid, app_key)

signed_url = Aspose::Cloud::Common::Utils.sign(request_url)

response = RestClient.get(signed_url, :accept=>:json)

response = JSON.parse(response)

p response


```
{{< /tab >}}

{{< tab tabNum="6" >}}
```java

import json

from aspose.cloud.common import \*

AsposeApp.app_sid = "..."

AsposeApp.app_key = "..."

method = "GET"

request_url = "http://api.aspose.com/v1.1/email/Sample1.eml/properties/MessageId"

signed_url = Utils.sign(Utils(), request_url)

response = Utils.process_command(Utils(), signed_url, method, "", "")

response_json = json.loads(response)

print response_json


```
{{< /tab >}}

{{< tab tabNum="7" >}}
```perl

use Data::Dumper;

my $app_sid = "...";

my $app_key = "...";

my $base_url = "http://api.aspose.com/v1.1";

my $request_method = "GET";

my $request_url = "$base_url/email/Sample1.eml/properties/MessageId";

my $signed_url = Sign($request_url, $app_sid, $app_key);

my $result = ProcessCommand($request_method, $signed_url);

print Dumper($result);


```
{{< /tab >}}

{{< tab tabNum="8" >}}
```javascript

var appSID = "...";

var appKey = "...";

var base_url = "http://api.aspose.com/v1.1/";

var method = "GET";

var request_url = base_url + "email/Sample1.eml/properties/MessageId";

var signed_url = Sign(request_url, appSID, appKey);

ProcessCommand(

  method,

  signed_url,

  null,

  function(response) {

    console.log(JSON.stringify(response, null, 2));

  }

);


```
{{< /tab >}}

{{< tab tabNum="9" >}}
```cpp

std::string app_sid = "...";

std::string app_key = "...";

std::string base_url = "http://api.aspose.com/v1.1/";

std::string method = "GET";

std::string request_url = base_url + "email/Sample1.eml/properties/MessageId";

std::string signed_url = sign(request_url, app_sid, app_key);

rapidjson::Document response = process_command(method, signed_url);

std::cout << "Status: " << response["Status"].GetString() << std::endl;

```
{{< /tab >}}

{{< tab tabNum="10" >}}
```java

AsposeApp.setAppKeyAndAppSID("Get it from https://cloud.aspose.com", "Get it from https://cloud.aspose.com")

AsposeApp.setBaseProductURI("http://api.aspose.com/v1.1");

String EMAIL_URI = AsposeApp.BASE_PRODUCT_URI + "/email/";

String propertyValue = null;

//build URL

String strURL = EMAIL_URI + Uri.encode("Message.msg") + "/properties/" + Uri.encode("Body");

//sign URL

String signedURL = Utils.sign(strURL);

InputStream responseStream = Utils.processCommand(signedURL, "GET");

String jsonStr = Utils.streamToString(responseStream);

//Parsing JSON

Gson gson = new Gson();

EmailPropertyResponse emailPropertyResponse = gson.fromJson(jsonStr, EmailPropertyResponse.class);

if(emailPropertyResponse.getCode().equals("200") && emailPropertyResponse.getStatus().equals("OK")) {

    propertyValue = emailPropertyResponse.emailProperty.value;

}


```
{{< /tab >}}

{{< tab tabNum="11" >}}
```java

[ASPOSEApp setAppKey:@"Get it from https://cloud.aspose.com" andAppSID:@"Get it from https://cloud.aspose.com"];

[ASPOSEProduct setBaseProductUri:@"http://api.aspose.com/v1.1"];

NSString \*EMAIL_URI = [[ASPOSEProduct baseProductUri] stringByAppendingString:@"/email/"];

NSObject \*propertyValue = nil;

NSString \*fileName = @"Self Assessment.eml";

//build URL

NSString \*strURL = [NSString stringWithFormat:@"%@%@/properties/%@", EMAIL_URI,

                    [fileName stringByAddingPercentEscapesUsingEncoding:NSUTF8StringEncoding], @"Body"];

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

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/email/sdk-setup/). 

{{% /alert %}}


## **cURL Example**
{{< tabs tabTotal="2" tabID="16" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -v "http://api.aspose.cloud/v1.1/email/email_test.eml?appSID=XXXX&signature=XXXX" \
     -X GET \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

Retrieved File

```

{{< /tab >}}

{{< /tabs >}}
## **SDK Examples**
**Retrieve message property**

{{< tabs tabTotal="9" tabID="19" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Objective C" tabName9="Perl" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-email" "838d7478e3720f941514d3d04417e82e" "Examples-DotNET-CSharp-Email-Properties-RetrieveMessageProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-email" "10428737982c525bf33b54ad9c27b707" "Examples-JAVA-SDK-src-main-java-com-aspose-email-cloud-properties-RetrieveMessagePropertiesExample-RetrieveMessagePropertiesExample.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-email" "3f41448648db89803193189f274722fa" "Examples-Ruby-EmailProperties-get_mail_common_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-email" "13478a90f198800bfcdafa983dbd0fcd" "RetrieveMessageProperties.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-email" "838d7478e3720f941514d3d04417e82e" "Examples-Node.js-Email-Properties-RetrieveMessageProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-email" "95a576636fc5c03e126e2617c83ce117" "Examples-Android-app-src-main-java-com-aspose-email-cloud-examples-working-properties-RetrieveMessagePropertiesExample-RetrieveMessagePropertiesExample.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-email" "838d7478e3720f941514d3d04417e82e" "Examples-Perl-Email-Properties-RetrieveMessageProperties-1.pl" >}}

{{< /tab >}}

{{< /tabs >}}
