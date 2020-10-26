---
title: "DiscoverEmailConfigRequest"
type: docs
url: /reference-model-discover-email-config-request/
weight: 1
---
Discover email configuration request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Address** | **string** | Email address to discover.              | 
**FastProcessing** | **bool?** | Turns on fast processing. All discover systems will run in parallel. First discovered result will be returned.              | 
**Login** | **string** | Email account login. If not specified, address used as a login.              | [optional] 


