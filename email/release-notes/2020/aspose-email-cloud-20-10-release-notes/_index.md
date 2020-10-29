---
title: "Aspose.Email Cloud 20.10 Release Notes"
type: docs
url: /aspose-email-cloud-20-10-release-notes/
weight: 100
---

## **SDK Changes**

Model builders have been added for Typescript, PHP, Java SDKs to simplify the initialization.

{{< expand-list title="Model builder example" >}}

{{< tabs tabTotal="3" tabID="builders" tabName1="Typescript" tabName2="PHP" tabName3="Java" >}}

{{< tab tabNum="1" >}}

```ts
let emailDto = Models.emailDto()
    .body('Some body')
    .from(Models.mailAddress()
        .displayName('From Address')
        .address('from@aspose.com')
        .build())
    .subject('Re: Some subject')
    .to([
        Models.mailAddress()
            .displayName('To Address')
            .address('to@aspose.com')
            .build()])
    .build();
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```php
$emailDto = Models::emailDto()
    ->body('Some body')
    ->from(Models::mailAddress()
        ->displayName('From Address')
        ->address('from@aspose.com')
        ->build())
    ->subject('Re: Some subject')
    ->to(array(
        Models::mailAddress()
            ->displayName('To Address')
            ->address('to@aspose.com')
            ->build()))
    ->build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```Java
EmailDto emailDto = Models.emailDto()
    .body("Some body")
    .from(Models.mailAddress()
        .displayName("From Address")
        .address("from@aspose.com")
        .build())
    .subject("Re: Some subject")
    .to(Arrays.<MailAddress>asList(
        Models.mailAddress()
            .displayName("To Address")
            .address("to@aspose.com")
            .build()))
    .build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

## **Documentation improvements**

- SDK reference documentation is now available at [docs.aspose.cloud/email/reference-api](https://docs.aspose.cloud/email/reference-api/)
- All SDK methods have code examples with parameters initialization (for example: [EmailCloud.Email.AsFile](http://localhost:1313/email/reference-email-api/#asfile) method).
- Initialization examples have been added for some of the models in all SDKs (for example: [EmailDto](http://localhost:1313/email/reference-model-email-dto/#example) model).