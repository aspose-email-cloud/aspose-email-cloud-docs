---
title: "Aspose.Email Cloud 20.1 Release Notes"
type: docs
url: /aspose-email-cloud-20-1-release-notes/
weight: 190
---

## **New features**
### **1. New Model API for VCard, iCalendar and Email message**
This model is a business card scanner, as it allows you to convert the captured business card and name card images into a vCard format to store contacts. You may also convert images into the VCard file.

{{% alert color="primary" %}} **iCalendar** is a MIME type that allows users to exchange and store calendaring and scheduling information such as journal entries, events, free/busy information, and ToDo, etc. {{% /alert %}} 

In the previous versions, there were only property sets based API. For example, in order to create iCalendar file using .Net SDK you had to use the following code:

```csharp
var calendar = new HierarchicalObject("CALENDAR", null, new List<BaseObject>
{
    new PrimitiveObject("LOCATION", null, "location"),
    new PrimitiveObject("STARTDATE", null, startDate.ToString("u")),
    new PrimitiveObject("ENDDATE", null, endDate.ToString("u")),
    new HierarchicalObject("ORGANIZER", null, new List<BaseObject>
    {
        new PrimitiveObject("ADDRESS", null, "organizer@aspose.com"),
        new PrimitiveObject("DISPLAYNAME", null, "Organizer Name")
    }),
    new HierarchicalObject("ATTENDEES", null, new List<BaseObject>
    {
        new IndexedHierarchicalObject("ATTENDEE", null, 0, new List<BaseObject>
        {
            new PrimitiveObject("ADDRESS", null, "attendee@aspose.com"),
            new PrimitiveObject("DISPLAYNAME", null, "Attendee Name")
        })
    })
});
```

In the current version, we have simplified the approach to work with iCalendar files. Now the same object can be represented by using new **CalendarDto** model: 

```csharp
 var calendar = new CalendarDto
{
    Attendees = new List<MailAddress>{new MailAddress("Attendee Name", "attendee@aspose.com", null)},
    Organizer = new MailAddress("Organizer Name", "organizer@aspose.com", null),
    StartDate = startDate,
    EndDate = endDate,
    Location = "location"
};
```

**You can use both ways to work with iCalendar files.** 

Model API does not have separate methods to operate with attachments. Therefore, Attachments can be operated directly by transforming files into Base64 strings:

```csharp
var bytes = File.ReadAllBytes(filePath);
var base64Data = Convert.ToBase64String(bytes);
calendar.Attachments.Add(new Attachment
{
    Base64Data = base64Data,
    Name = "attachment-name.txt"
});
```

More examples available on corresponding tutorials: [Email](/email/email-message-files/), [VCard](/email/quick-start-with-vcard-api/), [iCalendar](/email/quick-start-with-icalendar-api/).
### **2. Files conversion**
{{% alert color="primary" %}} Aspose.Email Cloud supports MSG, MHTM, HTML and EML file formats to store emails. {{% /alert %}} 

In the latest release version, we have introduced new methods to inter-convert the supported file formats. For example, in order to convert MSG to EML, you may use the following code snippet:

```csharp
Stream convertedFile = await emailApi.ConvertEmailAsync(
   new ConvertEmailRequest("Eml", File.OpenRead("msg/file/on/disk")));
```

More details on tutorial [Convert Email, Calendar and Contact Files](/email/convert-email-calendar-and-contact-files/).

Also, we added iCalendar to an AlternateView converter. Now it can be properly attached to an email message:

```csharp
var alternate = await emailApi.ConvertCalendarModelToAlternateAsync(
    new ConvertCalendarModelToAlternateRequest(
        new CalendarDtoAlternateRq(calendar, "Create", null)));
email.AlternateViews.Add(alternate); 
```
## **SDK changes**
- All SDKs now have wiki pages: [.Net](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/wiki), [Java](https://github.com/aspose-email-cloud/aspose-email-cloud-java/wiki), [Python](https://github.com/aspose-email-cloud/aspose-email-cloud-python/wiki), [Ruby](https://github.com/aspose-email-cloud/aspose-email-cloud-ruby/wiki), [Typescript](https://github.com/aspose-email-cloud/aspose-email-cloud-node/wiki), [PHP](https://github.com/aspose-email-cloud/aspose-email-cloud-php/wiki)
- Fixed bug with Date serialization in Typescript SDK
- SDK docstrings improved
