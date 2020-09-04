---
title: "Read Contact Document Properties"
type: docs
url: /read-contact-document-properties/
weight: 40
---

## **Introduction**
Aspose.Email Cloud allows you to read properties from a Context Document uploaded to the Cloud.

{{% alert color="primary" %}} 

If you want to know more about working with **VCard files** — take a look at the Aspose Email Cloud tutorial: [**Quick Start With VCard API**](/quick-start-with-vcard-api/).

{{% /alert %}} 


## **API Information**
Aspose.Email Cloud provides the following API:

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/email/Contact/{format}/{name}/properties|GET|Read Contact Card Properties|[GetContactProperties](https://apireference.aspose.cloud/email/#/Contact/GetContactProperties)|

## **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X GET "https://api.aspose.cloud/v3.0/email/Contact/VCard/sample.vcf/properties?folder=ical" -H "accept: application/json" -H "authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYmYiOjE1NzU5MjI1OTksImV4cCI6MTU3NjAwODk5OSwiaXNzIjoiaHR0cHM6Ly9hcGkuYXNwb3NlLmNsb3VkIiwiYXVkIjpbImh0dHBzOi8vYXBpLmFzcG9zZS5jbG91ZC9yZXNvdXJjZXMiLCJhcGkucGxhdGZvcm0iLCJhcGkucHJvZHVjdHMiXSwiY2xpZW50X2lkIjoiNzg5NDZmYjQtM2JkNC00ZDNlLWIzMDktZjllMmZmOWFjNmY5IiwiY2xpZW50X2lkU3J2SWQiOiI2NTk5ODQiLCJzY29wZSI6WyJhcGkucGxhdGZvcm0iLCJhcGkucHJvZHVjdHMiXX0.uvziiSW3zGjTbKit2jGyRQv2YqsOXVMMg70PtPGfzUf5V4hW5Gj5tY-tGQI1zY0jqBi2X5usXORO4CZzLO903Zgu9QekMkMO\_aaj4LWDLUGZ1mIYANzsS9Ntavz5S4FrHdXnFw2JJLCnwHce5ouES1ZcNURrzvdolr-KTo2OKkw9c9IJQD5CfvtMR\_yzqY1CJYuPRgohqAwyitXLvTC6oAXhNUecuRalBkcU5JQOosMNMifbpgqOxBbsc-BKpdMnkLl4uFODX5e7ZQQjz3qN5VwjDT\_DDwAGhN98AQt2Wx4E4GbAaY-ZzP8jeYq3yCy37y4XrzN8JWyLTw7zPTzp3w"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

   "internalProperties":[

      {

         "value":"Bjorn Jensen",

         "name":"DISPLAYNAME",

         "type":"PrimitiveObject"

      },

      {

         "internalProperties":[

            {

               "index":0,

               "internalProperties":[

                  {

                     "value":"Custom",

                     "name":"CATEGORY",

                     "type":"PrimitiveObject"

                  },

                  {

                     "value":"bjorn@umich.edu",

                     "name":"ADDRESS",

                     "type":"PrimitiveObject"

                  },

                  {

                     "value":"False",

                     "name":"PREFERED",

                     "type":"PrimitiveObject"

                  }

               ],

               "name":"EMAILADDRESS",

               "type":"IndexedHierarchicalObject"

            }

         ],

         "name":"EMAILADDRESSES",

         "type":"HierarchicalObject"

      },

      {

         "value":"None",

         "name":"FILEASMAPPING",

         "type":"PrimitiveObject"

      },

      {

         "value":"Bjorn",

         "name":"GIVENNAME",

         "type":"PrimitiveObject"

      },

      {

         "value":"Text",

         "name":"NOTESFORMAT",

         "type":"PrimitiveObject"

      },

      {

         "internalProperties":[

            {

               "index":0,

               "internalProperties":[

                  {

                     "value":"Custom",

                     "name":"CATEGORY",

                     "type":"PrimitiveObject"

                  },

                  {

                     "value":"+1 313 747-4454",

                     "name":"NUMBER",

                     "type":"PrimitiveObject"

                  },

                  {

                     "value":"False",

                     "name":"PREFERED",

                     "type":"PrimitiveObject"

                  }

               ],

               "name":"PHONENUMBER",

               "type":"IndexedHierarchicalObject"

            }

         ],

         "name":"PHONENUMBERS",

         "type":"HierarchicalObject"

      },

      {

         "value":"utf-8",

         "name":"PREFERREDTEXTENCODING",

         "type":"PrimitiveObject"

      },

      {

         "value":"Jensen",

         "name":"SURNAME",

         "type":"PrimitiveObject"

      }

   ],

   "name":"CONTACT",

   "type":"HierarchicalObject"

}

```

{{< /tab >}}

{{< /tabs >}}


## **Setup Aspose.Email Cloud SDK**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-email-cloud) for a complete list of Aspose.Email SDKs along with working examples.

{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/sdk-setup/).

{{% /alert %}} 




