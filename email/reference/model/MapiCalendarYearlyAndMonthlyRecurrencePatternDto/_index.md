---
title: "MapiCalendarYearlyAndMonthlyRecurrencePatternDto"
type: docs
url: /reference-model-mapi-calendar-yearly-and-monthly-recurrence-pattern-dto/
weight: 1
---
Represents the yearly and monthly recurrence pattern of the mapi calendar             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Day** | **int?** | Day of the month on which the recurrence falls.              | 
**DayOfWeek** | **List&lt;string&gt;** | Days of week at which the event occurs.              Items: Enumerates the days of week of the mapi calendar recurrence pattern. Enum, available values: Saturday, Friday, Thursday, Wednesday, Tuesday, Monday, Sunday | [optional] 
**Position** | **string** | Day positions, typically found in a month. Enum, available values: None, First, Second, Third, Fourth, Last | 

Parent class: [MapiCalendarRecurrencePatternDto](/email/reference-model-mapi-calendar-recurrence-pattern-dto/)

