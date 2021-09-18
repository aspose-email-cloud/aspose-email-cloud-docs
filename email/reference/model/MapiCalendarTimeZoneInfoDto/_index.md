---
title: "MapiCalendarTimeZoneInfoDto"
type: docs
url: /reference-model-mapi-calendar-time-zone-info-dto/
weight: 1
---
Represents the mapi calendar time zone rule.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Bias** | **int?** | Time zone&#39;s offset in minutes from UTC.              | 
**DaylightBias** | **int?** | Offset in minutes from lBias during daylight saving time.              | 
**DaylightDate** | [**MapiCalendarTimeZoneRuleDto**](/email/reference-model-mapi-calendar-time-zone-rule-dto/) | Date and local time that indicate when to begin using the DaylightBias.              | [optional] 
**StandardBias** | **int?** | Offset in minutes from lBias during standard time.              | 
**StandardDate** | [**MapiCalendarTimeZoneRuleDto**](/email/reference-model-mapi-calendar-time-zone-rule-dto/) | Date and local time that indicate when to begin using the StandardBias.              | [optional] 
**TimeZoneFlags** | **List&lt;string&gt;** | Individual bit flags that specify information about this TimeZoneRule.              Items: Enumerates the individual bit flags that specify information about TimeZoneRule./nEnum, available values: TzRuleFlagRecurCurrentTzReg, TzRuleFlagEffectiveTzReg | [optional] 
**Year** | **int?** | Year in which this rule is scheduled to take effect.              | 


