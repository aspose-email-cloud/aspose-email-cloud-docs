---
title: "EmailClientAccountOauthCredentials"
type: docs
url: /reference-model-email-client-account-oauth-credentials/
weight: 1
---
Represents email client account OAuth 2.0 credentials             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**ClientId** | **string** | The client ID obtained from the Google Cloud Console during application registration.              | 
**ClientSecret** | **string** | The client secret obtained during application registration.              | 
**RefreshToken** | **string** | OAuth 2.0 refresh token              | 
**RequestUrl** | **string** | The url to obtain access token. If not specified, will try to discover from email client account host.              | [optional] 

Parent class: [EmailClientAccountCredentials](/email/reference-model-email-client-account-credentials/)

