---
title: "EmailThreadList"
type: docs
url: /reference-model-email-thread-list/
weight: 1
---
List of email threads             

Properties:

Class has no properties

Parent class: [ListResponseOfEmailThread](/email/reference-model-list-response-of-email-thread/)

## Example

{{< tabs tabTotal="6" tabID="email_thread_list_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var emailThreadList = new EmailThreadList
{
    Value = new List<EmailThread>
    {
        new EmailThread
        {
            Id = "123",
            Subject = "Some email subject",
            Messages = new List<EmailDto>
            {
                new EmailDto
                {
                    Date = DateTime.Today,
                    From = new MailAddress
                    {
                        Address = "from@aspose.com"
                    },
                    MessageId = "1",
                    Subject = "Some email subject",
                    To = new List<MailAddress>
                    {
                        new MailAddress
                        {
                            Address = "to@aspose.com"
                        }
                    }
                },
                new EmailDto
                {
                    Date = DateTime.Today,
                    From = new MailAddress
                    {
                        Address = "from@aspose.com"
                    },
                    MessageId = "3",
                    Subject = "Re: Some email subject",
                    To = new List<MailAddress>
                    {
                        new MailAddress
                        {
                            Address = "to@aspose.com"
                        }
                    }
                }
            }
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailThreadList emailThreadList = Models.emailThreadList()
    .value(Arrays.<EmailThread>asList(
        Models.emailThread()
            .id("123")
            .subject("Some email subject")
            .messages(Arrays.<EmailDto>asList(
                Models.emailDto()
                    .date(Calendar.getInstance().getTime())
                    .from(Models.mailAddress()
                        .address("from@aspose.com")
                        .build())
                    .messageId("1")
                    .subject("Some email subject")
                    .to(Arrays.<MailAddress>asList(
                        Models.mailAddress()
                            .address("to@aspose.com")
                            .build()))
                    .build(),
                Models.emailDto()
                    .date(Calendar.getInstance().getTime())
                    .from(Models.mailAddress()
                        .address("from@aspose.com")
                        .build())
                    .messageId("3")
                    .subject("Re: Some email subject")
                    .to(Arrays.<MailAddress>asList(
                        Models.mailAddress()
                            .address("to@aspose.com")
                            .build()))
                    .build()))
            .build()))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
email_thread_list = models.EmailThreadList(
    value=[
        models.EmailThread(
            id='123',
            subject='Some email subject',
            messages=[
                models.EmailDto(
                    date=datetime.today(),
                    _from=models.MailAddress(
                        address='from@aspose.com'),
                    message_id='1',
                    subject='Some email subject',
                    to=[
                        models.MailAddress(
                            address='to@aspose.com')]),
                models.EmailDto(
                    date=datetime.today(),
                    _from=models.MailAddress(
                        address='from@aspose.com'),
                    message_id='3',
                    subject='Re: Some email subject',
                    to=[
                        models.MailAddress(
                            address='to@aspose.com')])])])
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
email_thread_list = EmailThreadList.new(
  value: [
    EmailThread.new(
      id: '123',
      subject: 'Some email subject',
      messages: [
        EmailDto.new(
          date: DateTime.now,
          from: MailAddress.new(
            address: 'from@aspose.com'),
          message_id: '1',
          subject: 'Some email subject',
          to: [
            MailAddress.new(
              address: 'to@aspose.com')]),
        EmailDto.new(
          date: DateTime.now,
          from: MailAddress.new(
            address: 'from@aspose.com'),
          message_id: '3',
          subject: 'Re: Some email subject',
          to: [
            MailAddress.new(
              address: 'to@aspose.com')])])])
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let emailThreadList = Models.emailThreadList()
    .value([
        Models.emailThread()
            .id('123')
            .subject('Some email subject')
            .messages([
                Models.emailDto()
                    .date(new Date())
                    .from(Models.mailAddress()
                        .address('from@aspose.com')
                        .build())
                    .messageId('1')
                    .subject('Some email subject')
                    .to([
                        Models.mailAddress()
                            .address('to@aspose.com')
                            .build()])
                    .build(),
                Models.emailDto()
                    .date(new Date())
                    .from(Models.mailAddress()
                        .address('from@aspose.com')
                        .build())
                    .messageId('3')
                    .subject('Re: Some email subject')
                    .to([
                        Models.mailAddress()
                            .address('to@aspose.com')
                            .build()])
                    .build()])
            .build()])
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$emailThreadList = Models::emailThreadList()
    ->value(array(
        Models::emailThread()
            ->id('123')
            ->subject('Some email subject')
            ->messages(array(
                Models::emailDto()
                    ->date(new DateTime())
                    ->from(Models::mailAddress()
                        ->address('from@aspose.com')
                        ->build())
                    ->messageId('1')
                    ->subject('Some email subject')
                    ->to(array(
                        Models::mailAddress()
                            ->address('to@aspose.com')
                            ->build()))
                    ->build(),
                Models::emailDto()
                    ->date(new DateTime())
                    ->from(Models::mailAddress()
                        ->address('from@aspose.com')
                        ->build())
                    ->messageId('3')
                    ->subject('Re: Some email subject')
                    ->to(array(
                        Models::mailAddress()
                            ->address('to@aspose.com')
                            ->build()))
                    ->build()))
            ->build()))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

