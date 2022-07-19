---
layout: post
title:  "Call SharePoint REST API from Postman using OAuth2 Authorization Flow"
description: "Call SharePoint REST API from Postman using OAuth2 Authorization Flow"
---
**Article-in-progress**

In this Article, You'll learn how to **Call SharePoint REST API** from Postman using **OAuth2.0 Authorization Flow**

### Prerequisites:

* SharePoint Site Collection in M365 Tenant
* Azure AD access to register app (Azure Subscription linked to the Azure AD used by your M365 tenant)
* Basic knowledge on [SharePoint REST API](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/complete-basic-operations-using-sharepoint-rest-endpoints).
* Postman tool to send HTTP Request


### Implementation Steps:

1. Register an application in Azure AD
1. Configure HTTP Request in Postman to Obtain OAuth2 access token
1. Send HTTP Request to SharePoint with OAuth2 access Token from Postman

#### Step 1: Register an application in Azure AD
1. Go to Azure AD (Azure Subscription linked to the Azure AD used by your Office 365 tenant)
1. Select App Registration > New Registration > Fill out the form

![screenshot](https://vstudio365.github.io/blog/assets/app-registration-form-01.jpg)

1. Generate Secret
1. Set Permission
        API Permissions > Add a Permission > SharePoint > Application Permissions > Select Sites.FullControl.All or desired > Add Permissions

#### Step 2: Configure HTTP Request in Postman to Obtain OAuth2 access token and call

1. Goto Postman
1. Create HTTP Request

```
HTTP Method :   GET  
HTTP Request :  https://<tenant>.sharepoint.com/_api/web/lists  
Headers : 
| Accept           | application/json;odata=verbose
```

| Accept           | application/json;odata=verbose

1. Go to **Authorization** tab, select Oauth 2.0, and Fill values as below and click on **Get New Access Token**

```
Token Name:         <friendly name>
Auth URL :          https://login.microsoftonline.com/common/oauth2/authorize?     resource=https%3A%2F%2F<tenant_name>.sharepoint.com  
Access Token URL :  https://login.microsoftonline.com/common/oauth2/token  
Client ID :         <Application_ID>  
Client Secret :     <KEY>  
Grant Type :        Authorization Code 
Callback URL :      https://oauth.pstmn.io/v1/callback
Scope :             <Leave empty>
State :             <Leave empty>
```

1. After Authentication Complete, click proceed > Use Token

#### Step 3: Send HTTP Request to SharePoint with OAuth2 access Token from Postman

1. Click Send and 
1. Check reponse from SharePoint