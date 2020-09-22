---
title: "Download Attachment from Email"
type: docs
url: /download-attachment-from-email/
weight: 10
---

## **Introduction**
This example allows you to download attachment from a message by attachment name using Aspose.Email for Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.



{{% alert color="primary" %}} 

If you want to know more about working with emails’ attachments — take a look at the Aspose Email Cloud tutorial: [**Email Message Files**](/email/email-message-files/).

{{% /alert %}} 
## **Resource**
The following Aspose.Email for Cloud REST API resource has been used in the examples: [attachment](https://apireference.aspose.cloud/email/#/Email/GetEmailAttachment)
## **REST Methods References**
We're referring some common methods in the REST examples to perform general operations. These methods can be found at the following page: [REST API Methods](https://apireference.aspose.cloud/email)
## **REST Examples**

{{< tabs tabTotal="6" tabID="1" tabName1="C#" tabName2="VB.NET" tabName3="Java" tabName4="PHP" tabName5="Ruby" tabName6="Python" tabName7="Node.js" tabName8="C++"  tabName9="Android" tabName10="Objective C" >}}

{{< tab tabNum="1" >}}

```java

// Initialize variables being used string appSid = "Get it from https://cloud.aspose.com"; string appKey = "Get it from https://cloud.aspose.com"; string name = "email-sample.eml"; string attachName = "barcode-sample.png"; string folder = "Email"; string outPath = "c:\\email-attach-out.png"; string storage = string.Empty; // Build URI to perform request string apiUrl = string.Format(@"email/{0}/attachments/{1}?storage={2}&folder={3}", name, attachName, storage, folder); // Get response stream and write it to local disk path using (Stream responseStream = ServiceController.GetStream(apiUrl, appSid, appKey)) using (Stream file = File.OpenWrite(outPath)) { ServiceController.CopyStream(responseStream, file); }

```
{{< /tab >}}

{{< tab tabNum="2" >}}
```java

' Initialize variables being used Dim appSid As String = "Get it from https://cloud.aspose.com" Dim appKey As String = "Get it from https://cloud.aspose.com" Dim name As String = "email-sample.eml" Dim attachName As String = "barcode-sample.png" Dim folder As String = "Email" Dim outPath As String = "c:\email-attach-out.png" Dim storage As String = String.Empty ' Build URI to perform request Dim apiUrl As String = String.Format("email/{0}/attachments/{1}?storage={2}&folder={3}", name, attachName, storage, folder) ' Get response stream and write it to local disk path Using responseStream As Stream = ServiceController.GetStream(apiUrl, appSid, appKey) Using file As Stream = File.OpenWrite(outPath) ServiceController.CopyStream(responseStream, file) End Using End Using

```
{{< /tab >}}

{{< tab tabNum="3" >}}
```java

import java.io.\*; import com.aspose.cloud.common.Utils; import com.aspose.cloud.storage.Folder; String appSID = "..."; String appKey = "..."; String method = "GET"; String requestUrl = "http://api.aspose.com/v1.1/email/Sample1.eml/attachments/attachment.txt"; String outputFile = "attachment.txt"; String outputFilePath = new File(System.getProperty("user.dir"), outputFile).getPath(); String signedUrl = Utils.Sign(requestUrl, appKey, appSID); InputStream responseStream = Utils.ProcessCommand(signedUrl, method); Folder.SaveStreamToFile(outputFilePath, responseStream); responseStream.close(); System.out.println("File saved: " + outputFilePath);

```
{{< /tab >}}

{{< tab tabNum="4" >}}
```java

use Aspose\Cloud\Common\AsposeApp; use Aspose\Cloud\Common\Utils; AsposeApp::$appSID = "..."; AsposeApp::$appKey = "..."; $method = "GET"; $base_url = "http://api.aspose.com/v1.1"; $request_url = "$base_url/email/Sample1.eml/attachments/attachment.txt"; $output_file = getcwd() . "/attachment.txt"; $signed_url = Utils::sign($request_url); $response = Utils::processCommand($signed_url, $method, "", ""); file_put_contents($output_file, $response); echo "File saved: $output_file\n";

```
{{< /tab >}}

{{< tab tabNum="5" >}}
```java

app_sid = "..." app_key = "..." request_url = "http://api.aspose.com/v1.1/email/Sample1.eml/attachments/attachment.txt" output_file = File.join(Dir.pwd, "attachment.txt") Aspose::Cloud::Common::AsposeApp.new(app_sid, app_key) signed_url = Aspose::Cloud::Common::Utils.sign(request_url) response = RestClient.get(signed_url) File.open(output_file, "wb") { |file| file.write(response) } puts "File saved: #{output_file}"

```
{{< /tab >}}

{{< tab tabNum="6" >}}
```java

import os.path from aspose.cloud.common import \* AsposeApp.app_sid = "..." AsposeApp.app_key = "..." method = "GET" request_url = "http://api.aspose.com/v1.1/email/Sample1.eml/attachments/attachment.txt" output_file = "attachment.txt" output_file_path = os.path.join(os.getcwd(), output_file) signed_url = Utils.sign(Utils(), request_url) response = Utils.process_command(Utils(), signed_url, method, "", "") Utils.save_file(Utils(), response, output_file_path) print "File saved:", output_file_path

```
{{< /tab >}}

{{< tab tabNum="7" >}}

```javascript

var appSID = '...'; var appKey = '...'; var base_url = 'http://api.aspose.com/v1.1/'; var fs = require('fs'); var method = 'GET'; var request_url = base_url + 'email/Sample1.eml/attachments/attachment.txt'; var output_file = 'attachment.txt'; ProcessCommandContent( method, Sign(request_url, appSID, appKey), null, function(buffer) { fs.writeFileSync(output_file, buffer); } );

```
{{< /tab >}}

{{< tab tabNum="8" >}}
```cpp

std::string app_sid("..."); std::string app_key("..."); std::string base_url("http://api.aspose.com/v1.1/"); std::string method = "GET"; std::string request_url = base_url + "email/Sample1.eml/attachments/attachment.txt"; std::string signed_url = sign(request_url, app_sid, app_key); std::string output_file = "attachment.txt"; std::ofstream output_fstream; output_fstream.open(output_file, std::ofstream::binary); process_command(method, signed_url, output_fstream); output_fstream.close(); std::cout << "File saved: " << output_file << std::endl;

```
{{< /tab >}}

{{< tab tabNum="9" >}}
```java

AsposeApp.setAppKeyAndAppSID("Get it from https://cloud.aspose.com", "Get it from https://cloud.aspose.com") AsposeApp.setBaseProductURI("http://api.aspose.com/v1.1"); String EMAIL_URI = AsposeApp.BASE_PRODUCT_URI + "/email/"; //build URL String strURL = EMAIL_URI + Uri.encode("Message.msg") + "/attachments/" + Uri.encode("License.txt"); //sign URL String signedURL = Utils.sign(strURL); InputStream responseStream = Utils.processCommand(signedURL, "GET"); //Save attachment on Disk String localAttachmentPath = Utils.saveStreamToFile(responseStream, "License.txt");

```
{{< /tab >}}

{{< tab tabNum="10" >}}
```java

[ASPOSEApp setAppKey:@"Get it from https://cloud.aspose.com" andAppSID:@"Get it from https://cloud.aspose.com"]; [ASPOSEProduct setBaseProductUri:@"http://api.aspose.com/v1.1"]; NSString \*EMAIL_URI = [[ASPOSEProduct baseProductUri] stringByAppendingString:@"/email/"]; NSString \*fileName = @"Self Assessment.eml"; NSString \*attachmentName = @"License.txt"; //build URL NSString \*strURL = [NSString stringWithFormat:@"%@%@/attachments/%@", EMAIL_URI, [fileName stringByAddingPercentEscapesUsingEncoding:NSUTF8StringEncoding], [attachmentName stringByAddingPercentEscapesUsingEncoding:NSUTF8StringEncoding]]; //sign URL NSString \*signedURL = [ASPOSEUtils sign:strURL]; NSData \*responseData = [ASPOSEUtils processCommand:signedURL httpMethod:@"GET"]; //Parsing JSON if(responseData) { NSError \*error; emailAttachmentResponse = [[ASPOSEEmailAttachmentResponse alloc] initWithData:responseData error:&error]; if(emailAttachmentResponse == nil) { //Save file on Disk emailAttachmentResponse = [[ASPOSEEmailAttachmentResponse alloc] init]; emailAttachmentResponse.localFilePath = [ASPOSEFolder saveFile:responseData withName:@"License.txt"]; } }

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

curl -v "http://api.aspose.cloud/v1.1/email/email_test2.eml/attachments/README.TXT?appSID=XXXX&signature=XXXX" \
     -X GET \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

Attachment

```

{{< /tab >}}

{{< /tabs >}}
## **SDK Examples**
**Download attachment from email**

{{< tabs tabTotal="9" tabID="19" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Objective C" tabName9="Perl" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-email" "838d7478e3720f941514d3d04417e82e" "Examples-DotNET-CSharp-Attachments-DownloadAttachment-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-email" "10428737982c525bf33b54ad9c27b707" "Examples-JAVA-SDK-src-main-java-com-aspose-email-cloud-attachments-DownloadAttacmentFromEmail-DownloadAttacmentFromEmail.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "" "a052f420f51722082cbb70d5e8d0f339" "Examples-PHP-Attachments-GetEmailAttachment-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-email" "3f41448648db89803193189f274722fa" "Examples-Ruby-Attachments-get_email_attachment_by_name-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-email" "13478a90f198800bfcdafa983dbd0fcd" "DownloadAttachmentWithEmail.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-email" "838d7478e3720f941514d3d04417e82e" "Examples-Node.js-Attachments-DownloadAttachment-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-email" "95a576636fc5c03e126e2617c83ce117" "Examples-Android-app-src-main-java-com-aspose-email-cloud-examples-working-attachments-DownloadAttacmentFromEmail-DownloadAttacmentFromEmail.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-email" "838d7478e3720f941514d3d04417e82e" "Examples-Perl-Attachments-DownloadAttachment-1.pl" >}}

{{< /tab >}}

{{< /tabs >}}
