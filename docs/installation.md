---
title: Installation
nav_order: 2
has_toc: false
---


###### [DigitalPersona Access Management API ](https://hidglobal.github.io/digitalpersona-access-management-api/)/ [Native API](..\index.html) / Installation&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[\| View Repo \|](https://github.com/hidglobal/digitalpersona-native-api)  

![](docs/assets/HID-DPAM-native-api.png)  

## Installation  

The DigitalPersona Native API is automatically installed as part of the following DigitalPersona clients:
- DigitalPersona AD and LDS Workstation  
- DigitalPersona AD and LDS Kiosk
- DigitalPersona Lite Client  

### Preparing the DigitalPersona Server

Since the DigitalPersona Native API is part of a client-server solution, use of the SDK requires installation of a DigitalPersona AD or LDS Server and client, plus additional steps on the server to prepare it for use with the SDK.  

The necessary steps for installation and setup of the DigitalPersona Native API are summarized below.  

- Install a DigitalPersona AD or LDS Server      
- (Optionally) Install the DigitalPersona Web Management Components  
- Install a DigitalPersona client  

### Install a DigitalPersona AD or LDS Server  

For instructions on installing and configuring a DigitalPersona AD or LDS Server, see the DigitalPersona AD Administrator Guide or the DigitalPersona LDS Administrator Guide.  

### (Optionally) Install the DigitalPersona Web Management Components  

Note that installation of the DigitalPersona Web Management Component is optional.  

These components are primarily used when there is a firewall between the computer using the SDK and the DigitalPersona Server. In this scenario, you can install only the DigitalPersona Internet Proxy by selecting *Advanced Configuration* in the DigitalPersona Web Management Components configuration wizard and deselecting all other components.  

To install the DigitalPersona Web Management Components
1. Locate the Web Management Components folder within the DigitalPersona Native API package.  

2. Launch the Web Management Components installer by clicking the Setup.exe file.  

3. Follow the instructions provided in the installation wizard. For additional detailed instructions, see the Web
Management Components Installation chapter in the DigitalPersona AD or LDS Administrator Guide.  

4. If Internet Information Services (IIS) was not previously installed, the wizard will install it. Note that it is best to
allow the wizard to install IIS, since the wizard does some configuration of IIS (adding features) during the
installation.  

  If you do install IIS separately, see the DigitalPersona Administrator Guide for a list of required IIS features.

### Install a DigitalPersona client  

To run the DigitalPersona Native API sample code or to run and test your application, you should have a DigitalPersona client installed on your development machine.  

Additionally, if you are developing for the DigitalPersona AD or LDS Kiosk or Lite Client environment, you should test your application with those clients.  

For a list of supported versions of  DigitalPersona clients, refer to Supported
DigitalPersona Products [Need link here].  

Complete instructions on installing DigitalPersona clients is provided in the
DigitalPersona Client Guide, which can be downloaded from our website at https://www.crossmatch.com/company/support/documentation/
