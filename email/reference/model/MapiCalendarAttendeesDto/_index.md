---
title: "MapiCalendarAttendeesDto"
type: docs
url: /reference-model-mapi-calendar-attendees-dto/
weight: 1
---
Mapi calendar attendees.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**AppointmentRecipients** | [**List&lt;MapiRecipientDto&gt;**](/email/reference-model-mapi-recipient-dto/) | List of attendees.              | [optional] 
**AppointmentUnsendableRecipients** | [**List&lt;MapiRecipientDto&gt;**](/email/reference-model-mapi-recipient-dto/) | List of unsendable attendees.              | [optional] 
**NotAllowPropose** | **bool?** | Value indicating whether attendees are not allowed to propose a new date and/or time for the meeting.              | 
**ResponseRequested** | **bool?** | Value indicating whether a response is requested to a Message object.              | 


