---
title: "MapiCalendarExceptionInfoDto"
type: docs
url: /reference-model-mapi-calendar-exception-info-dto/
weight: 1
---
An exception specifies changes to an instance of a recurring series.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Attachments** | [**List&lt;MapiAttachmentDto&gt;**](/email/reference-model-mapi-attachment-dto/) | Attachments in the recurrence exception.              | [optional] 
**Body** | **string** | Body.              | [optional] 
**BusyStatus** | **string** | Enumerates the mapi calendar possible busy status./nEnum, available values: Free, Tentative, Busy, OutOfOffice | 
**EndDateTime** | **DateTime?** | End date.              | 
**HasAttachment** | **bool?** | Value of this field specifies whether the Exception Embedded Message object contains attachments.              | 
**Location** | **string** | Location.              | [optional] 
**MeetingType** | **string** | Enumerates the appointment state./nEnum, available values: Meeting, Received, Canceled | 
**OriginalStartDate** | **DateTime?** | Original start date.              | 
**OverrideFlags** | **List&lt;string&gt;** | Override flags.              Items: Specifies what data in the MapiCalendarOverride structure has a value different from the recurring series./nEnum, available values: Subject, MeetingType, ReminderDelta, Reminder, Location, BusyStatus, Attachment, Subtype, AppointmentColor, ExceptionalBody | [optional] 
**ReminderDelta** | **int?** | Reminder delta.              | 
**ReminderSet** | **bool?** | Value for the PidLidReminderSet property.              | 
**StartDateTime** | **DateTime?** | Start date.              | 
**Subject** | **string** | Subject.              | [optional] 
**SubType** | **int?** | SubType.              | 


