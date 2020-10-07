---
title: "MapiCalendarEventRecurrenceDto"
type: docs
url: /reference-model-mapi-calendar-event-recurrence-dto/
weight: 1
---
Recurrence properties of calendar object.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**AppointmentTimeZoneDefinitionRecur** | [**MapiCalendarTimeZoneDto**](/email/reference-model-mapi-calendar-time-zone-dto/) | Time zone information that describes how to convert the meeting date and time on a recurring series to and from UTC.              | [optional] 
**ClipEnd** | **DateTime?** | Date of the last instance.              | 
**ClipStart** | **DateTime?** | Date of the first instance.              | 
**IsException** | **bool?** | Value indicating whether the object represents an exception.              | 
**RecurrencePattern** | [**MapiCalendarRecurrencePatternDto**](/email/reference-model-mapi-calendar-recurrence-pattern-dto/) | Recurrence pattern.              | [optional] 
**TimeZoneStruct** | [**MapiCalendarTimeZoneDto**](/email/reference-model-mapi-calendar-time-zone-dto/) | Time zone information for a recurring meeting.              | [optional] 


