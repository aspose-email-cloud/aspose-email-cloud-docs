---
title: "Aspose.Email Cloud 20.7 Release Notes"
type: docs
url: /aspose-email-cloud-20-7-release-notes/
weight: 130
---

## **New features**
## **MAPI message files API**
{{% alert color="primary" %}} 

To see how to work with MAPI Message Files API use the [Introduction to MAPI Message Files API](/email/introduction-to-mapi-message-files-api/).

{{% /alert %}} 

New models for representing MAPI message files have been added to Aspose Email Cloud:

- MapiMessageDto - represents the Microsoft Outlook message.
- MapiCalendarDto - represents the Microsoft Outlook calendar object.
- MapiContactDto - represents the Microsoft Outlook contact information.

All these models can be converted to corresponding DTO objects:

- MapiMessageDto <-> EmailDto.
- MapiCalendarDto <-> CalendarDto.
- MapiContactDto <-> ContactDto.

Also, the methods to save these models to MSG files are provided now.
## **Recurrence pattern support for CalendarDto improved**
In the previous versions, there was the only method to set recurrence in CalendarDto using RecurrenceString. For example, to set daily recurrence:

```csharp
calendar.RecurrenceString = "FREQ=DAILY;COUNT=10;WKST=MO";
```

In the current version, a new Recurrence property has been added, so there is a better way to set recurrence patterns:

```csharp
calendar.Recurrence = new DailyRecurrencePatternDto
{
    Occurs = 10,
    WeekStart = "Monday"
};
```

## **SDK changes**
- Some corrections in null value handling during a model serialization.
- Discriminator property has been added to ContactPhoto because it is now inherited by MapiContactPhotoDto.
- Bug with the lost model property types information has been fixed.
- Added TNEF format support to email message converters.
