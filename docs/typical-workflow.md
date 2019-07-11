---
title: Typical workflow
nav_order: 3
has_toc: false
---

###### [DigitalPersona Access Management API ](https://hidglobal.github.io/digitalpersona-access-management-api/)/ [Native API](..\index.html) / Typical workflow&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[\| View Repo \|](https://github.com/hidglobal/digitalpersona-native-api)

![](assets/HID-DPAM-native-api.png)

## Typical Workflow

This chapter describes the standard workflow for using the DigitalPersona Native API and lists the functions provided.  

Two sample applications are provided, one for C++ and one for .NET.  

The information in this chapter is extracted from <mark style="color:Red;">DPAltusAuthSdkApi.h</mark>.  

For terminology and concepts, see the DigitalPersona Administrator Guides and the DigitalPersona CLient Guide.  

The typical workflow is:  

```  
Call DPAlInit to initialize
...
Call functions in the API
... If a API function returned an array, string or BLOG, call DPAlFreeBuffer to release the memory.  

...  
Call DPAlTerm to release resources  
```  
Note that if you are calling only one function in the API, then you don’t need to call DPAlInit and DPAlTerm directly because the function will initialize and terminate for itself automatically. However when you are making multiple calls, it is faster and more efficient to initialize and terminate directly.  

The API provides:  

- Authentication: Verifying that a user is who they claim to be by checking that the provided credentials (password, fingerprint, etc.) match their username's credentials in the DigitalPersona database.  

  The DPAlAuthenticate function displays the multi-factor authentication dialog and matches the supplied credentials against the user's enrolled credentials. The customizable dialog box accepts the credentials required by the authentication policy set by the DigitalPersona administrator.  

  Optional: On successful authentication, DPAlAuthenticate can return user secrets and the type of credential(s) that the user provided for authentication.
- Identification: Searching in Active Directory to find the user and authenticate them. For Kiosk environments only.  

  The DPAlIdentAuthenticate function displays the multi-factor identification dialog and identifies the user based on the credentials supplied. The customizable dialog box allows the user to provide the credentials required by the current authentication policy.  

  Optional: If the identification succeeds, DPAlIdentAuthenticate can return the user name, the type of credential(s) used to authenticate and user secrets.
#### Authentication Policies
The simplest option provided by the  DigitalPersona Native API is to authenticate a user using the session authentication policy defined by the DigitalPersona administrator. In this case, you do not need to know how policies work and you may simply pass NULLs to the API for all parameters that take an authentication policy.  

For more information on authentication policies, see the section [Custom Authentication Policies](custom-auth-policies.md).  
