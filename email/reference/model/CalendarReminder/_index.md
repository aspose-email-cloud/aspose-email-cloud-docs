---
title: "CalendarReminder"
type: docs
url: /reference-model-calendar-reminder/
weight: 1
---
Provides a grouping of component properties that define an alarm.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Action** | **string** | Defines the action to be invoked when an alarm is triggered./nEnum, available values: Audio, Display, Email, Procedure, None | 
**Attachments** | **List&lt;string&gt;** | Collection of Reminder Attachments. Could be an absolute URI or Base64 string representation of attachment content              | [optional] 
**Attendees** | [**List&lt;ReminderAttendee&gt;**](/email/reference-model-reminder-attendee/) | Contains collection of ReminderAttendee objects.              | [optional] 
**Description** | **string** | Provides a more complete description of the alarm. | [optional] 
**Duration** | **long?** | Specifies the delay period in ticks, after which the alarm will repeat.              | [optional] 
**Repeat** | **int?** | Defines the number of time the alarm should be repeated, after the initial trigger.              | 
**Summary** | **string** | Defines a short summary or subject for the alarm. | [optional] 
**Trigger** | [**ReminderTrigger**](/email/reference-model-reminder-trigger/) | Specifies when an alarm will trigger. | [optional] 


