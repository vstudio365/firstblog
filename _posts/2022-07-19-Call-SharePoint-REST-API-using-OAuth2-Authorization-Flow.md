---
layout: post
title:  "Call SharePoint REST API from Postman using OAuth2 Authorization Flow"
description: "Call SharePoint REST API from Postman using OAuth2 Authorization Flow"
---
**INPROGRESS**
In this Article, You'll learn how to **Call SharePoint REST API** from Postman using **OAuth2.0 Authorization Flow**

### Prerequisites:
* SharePoint Site Collection in M365 Tenant
* Access to register app in Azure AD (Azure Subscription linked to the Azure AD used by your M365 tenant)
* Basic knowledge on [SharePoint REST API](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/complete-basic-operations-using-sharepoint-rest-endpoints).
* Postman tool to send HTTP Request


### Implementation Steps:
1. Register an application in Azure AD
1. Configure HTTP Request in Postman to Obtain OAuth2 access token
1. Send HTTP Request to SharePoint with OAuth2 access Token from Postman

#### Step 1: Register an application in Azure AD
1. Go to Azure AD (Azure Subscription linked to the Azure AD used by your Office 365 tenant)
1. Select App Registration > New Registration > Fill out the form

```
Name: {friendly-name}
Supported Account Types: ... Single Tenant
Redirect Uri: 
Web - https://oauth.pstmn.io/v1/callback 
// it means, redirect to Postman tool on successful authentication
```
![screenshot](https://github.com/vstudio365/blog/assets/app-registration-form-01.jpg)

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)



    
#### Step 2: Configure HTTP Request in Postman to Obtain OAuth2 access token

#### Step 3: Send HTTP Request to SharePoint with OAuth2 access Token from Postman
 This article focuses on `http://<site url>/_api/web/lists`