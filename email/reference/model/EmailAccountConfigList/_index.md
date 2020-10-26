---
title: "EmailAccountConfigList"
type: docs
url: /reference-model-email-account-config-list/
weight: 1
---
List of email accounts             

Properties:

Class has no properties

Parent class: [ListResponseOfEmailAccountConfig](/email/reference-model-list-response-of-email-account-config/)

## Example

{{< tabs tabTotal="6" tabID="email_account_config_list_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var emailAccountConfigList = new EmailAccountConfigList
{
    Value = new List<EmailAccountConfig>
    {
        new EmailAccountConfig
        {
            DisplayName = "Google Mail",
            Host = "imap.gmail.com",
            Port = 993,
            SocketType = "SSLAuto",
            AuthenticationTypes = new List<AuthenticationType>
            {
                "PasswordCleartext",
                "OAuth2"
            },
            ExtraInfo = new List<NameValuePair>
            {
                new NameValuePair
                {
                    Name = "Enable: You need to enable IMAP access",
                    Value = "https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop"
                }
            }
        },
        new EmailAccountConfig
        {
            DisplayName = "Google Mail",
            ProtocolType = "SMTP",
            Host = "smtp.gmail.com",
            Port = 465,
            SocketType = "SSLAuto",
            AuthenticationTypes = new List<AuthenticationType>
            {
                "PasswordCleartext",
                "OAuth2"
            },
            ExtraInfo = new List<NameValuePair>
            {
                new NameValuePair
                {
                    Name = "Enable: You need to enable IMAP access",
                    Value = "https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop"
                }
            }
        },
        new EmailAccountConfig
        {
            DisplayName = "Google Mail",
            ProtocolType = "POP3",
            Host = "pop.gmail.com",
            Port = 995,
            SocketType = "SSLAuto",
            AuthenticationTypes = new List<AuthenticationType>
            {
                "PasswordCleartext",
                "OAuth2"
            },
            ExtraInfo = new List<NameValuePair>
            {
                new NameValuePair
                {
                    Name = "Enable: You need to enable IMAP access",
                    Value = "https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop"
                }
            }
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailAccountConfigList emailAccountConfigList = Models.emailAccountConfigList()
    .value(Arrays.<EmailAccountConfig>asList(
        Models.emailAccountConfig()
            .displayName("Google Mail")
            .host("imap.gmail.com")
            .port(993)
            .socketType("SSLAuto")
            .authenticationTypes(Arrays.<AuthenticationType>asList(
                "PasswordCleartext",
                "OAuth2"))
            .extraInfo(Arrays.<NameValuePair>asList(
                Models.nameValuePair()
                    .name("Enable: You need to enable IMAP access")
                    .value("https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop")
                    .build()))
            .build(),
        Models.emailAccountConfig()
            .displayName("Google Mail")
            .protocolType("SMTP")
            .host("smtp.gmail.com")
            .port(465)
            .socketType("SSLAuto")
            .authenticationTypes(Arrays.<AuthenticationType>asList(
                "PasswordCleartext",
                "OAuth2"))
            .extraInfo(Arrays.<NameValuePair>asList(
                Models.nameValuePair()
                    .name("Enable: You need to enable IMAP access")
                    .value("https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop")
                    .build()))
            .build(),
        Models.emailAccountConfig()
            .displayName("Google Mail")
            .protocolType("POP3")
            .host("pop.gmail.com")
            .port(995)
            .socketType("SSLAuto")
            .authenticationTypes(Arrays.<AuthenticationType>asList(
                "PasswordCleartext",
                "OAuth2"))
            .extraInfo(Arrays.<NameValuePair>asList(
                Models.nameValuePair()
                    .name("Enable: You need to enable IMAP access")
                    .value("https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop")
                    .build()))
            .build()))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
email_account_config_list = models.EmailAccountConfigList(
    value=[
        models.EmailAccountConfig(
            display_name='Google Mail',
            host='imap.gmail.com',
            port=993,
            socket_type='SSLAuto',
            authentication_types=[
                'PasswordCleartext',
                'OAuth2'],
            extra_info=[
                models.NameValuePair(
                    name='Enable: You need to enable IMAP access',
                    value='https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop')]),
        models.EmailAccountConfig(
            display_name='Google Mail',
            protocol_type='SMTP',
            host='smtp.gmail.com',
            port=465,
            socket_type='SSLAuto',
            authentication_types=[
                'PasswordCleartext',
                'OAuth2'],
            extra_info=[
                models.NameValuePair(
                    name='Enable: You need to enable IMAP access',
                    value='https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop')]),
        models.EmailAccountConfig(
            display_name='Google Mail',
            protocol_type='POP3',
            host='pop.gmail.com',
            port=995,
            socket_type='SSLAuto',
            authentication_types=[
                'PasswordCleartext',
                'OAuth2'],
            extra_info=[
                models.NameValuePair(
                    name='Enable: You need to enable IMAP access',
                    value='https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop')])])
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
email_account_config_list = EmailAccountConfigList.new(
  value: [
    EmailAccountConfig.new(
      display_name: 'Google Mail',
      host: 'imap.gmail.com',
      port: 993,
      socket_type: 'SSLAuto',
      authentication_types: [
        'PasswordCleartext',
        'OAuth2'],
      extra_info: [
        NameValuePair.new(
          name: 'Enable: You need to enable IMAP access',
          value: 'https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop')]),
    EmailAccountConfig.new(
      display_name: 'Google Mail',
      protocol_type: 'SMTP',
      host: 'smtp.gmail.com',
      port: 465,
      socket_type: 'SSLAuto',
      authentication_types: [
        'PasswordCleartext',
        'OAuth2'],
      extra_info: [
        NameValuePair.new(
          name: 'Enable: You need to enable IMAP access',
          value: 'https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop')]),
    EmailAccountConfig.new(
      display_name: 'Google Mail',
      protocol_type: 'POP3',
      host: 'pop.gmail.com',
      port: 995,
      socket_type: 'SSLAuto',
      authentication_types: [
        'PasswordCleartext',
        'OAuth2'],
      extra_info: [
        NameValuePair.new(
          name: 'Enable: You need to enable IMAP access',
          value: 'https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop')])])
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let emailAccountConfigList = Models.emailAccountConfigList()
    .value([
        Models.emailAccountConfig()
            .displayName('Google Mail')
            .host('imap.gmail.com')
            .port(993)
            .socketType('SSLAuto')
            .authenticationTypes([
                'PasswordCleartext',
                'OAuth2'])
            .extraInfo([
                Models.nameValuePair()
                    .name('Enable: You need to enable IMAP access')
                    .value('https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop')
                    .build()])
            .build(),
        Models.emailAccountConfig()
            .displayName('Google Mail')
            .protocolType('SMTP')
            .host('smtp.gmail.com')
            .port(465)
            .socketType('SSLAuto')
            .authenticationTypes([
                'PasswordCleartext',
                'OAuth2'])
            .extraInfo([
                Models.nameValuePair()
                    .name('Enable: You need to enable IMAP access')
                    .value('https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop')
                    .build()])
            .build(),
        Models.emailAccountConfig()
            .displayName('Google Mail')
            .protocolType('POP3')
            .host('pop.gmail.com')
            .port(995)
            .socketType('SSLAuto')
            .authenticationTypes([
                'PasswordCleartext',
                'OAuth2'])
            .extraInfo([
                Models.nameValuePair()
                    .name('Enable: You need to enable IMAP access')
                    .value('https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop')
                    .build()])
            .build()])
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$emailAccountConfigList = Models::emailAccountConfigList()
    ->value(array(
        Models::emailAccountConfig()
            ->displayName('Google Mail')
            ->host('imap.gmail.com')
            ->port(993)
            ->socketType('SSLAuto')
            ->authenticationTypes(array(
                'PasswordCleartext',
                'OAuth2'))
            ->extraInfo(array(
                Models::nameValuePair()
                    ->name('Enable: You need to enable IMAP access')
                    ->value('https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop')
                    ->build()))
            ->build(),
        Models::emailAccountConfig()
            ->displayName('Google Mail')
            ->protocolType('SMTP')
            ->host('smtp.gmail.com')
            ->port(465)
            ->socketType('SSLAuto')
            ->authenticationTypes(array(
                'PasswordCleartext',
                'OAuth2'))
            ->extraInfo(array(
                Models::nameValuePair()
                    ->name('Enable: You need to enable IMAP access')
                    ->value('https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop')
                    ->build()))
            ->build(),
        Models::emailAccountConfig()
            ->displayName('Google Mail')
            ->protocolType('POP3')
            ->host('pop.gmail.com')
            ->port(995)
            ->socketType('SSLAuto')
            ->authenticationTypes(array(
                'PasswordCleartext',
                'OAuth2'))
            ->extraInfo(array(
                Models::nameValuePair()
                    ->name('Enable: You need to enable IMAP access')
                    ->value('https://mail.google.com/mail/?ui=2&shva=1#settings/fwdandpop')
                    ->build()))
            ->build()))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

