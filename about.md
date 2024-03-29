---
layout: page
title: Getting Started
permalink: /about/
nav_order: 2
---

GetIN Mobile App & Sana Mobile Client
==================
{: .no_toc }

Overview
--------


GetIN App is built on the android platform and is developed using the Sana- MIT mobile client.
The new client code is intended to be a self-contained, modularized, project 
including all necessary support libraries and unit testing code. 
1. TOC
{:toc}
### Development Requirements
1.  [Android Studio](http://developer.android.com/sdk/index.html) Additional prerequisites are required for installing Android 
Studio. Please see the [System Requirements](http://developer.android.com/sdk/index.html#Requirements) 
for Android Studio for your platform.
2. The Android support libraries available for installation through the SDK manager.
3. Emulator or Hardware device connected via USB with API level 8 or higher.

**Notes** 
1. If you do not have a hardware device available, additional instructions for
creating an emulator are available on the Android Developer Site’s [Managing Virtual Devices](http://developer.android.com/tools/devices/index.html) page.
2. If your workstation includes an Intel processor with hardware virtualization support
and you are developing on Windows, you will find the emulator runs significantly faster 
if you also install the  Intel Hardware Accelerated Execution Manager available through
the SDK manager.

###Source Code
Source code for the Android based mobile client is available by cloning the GetIN mobile or  sana.mobile 
repository.

*GetIN APP repository*

`git clone https://github.com/UNFPAInnovation/GetIn_Mobile/`

*Sana Mobile Client Repository*

`git clone https://github.com/SanaMobile/sana.mobile.git`


We highly recommend creating a Github account and forking the repository in lieu of 
directly cloning the repository so that any changes that you may make may be more easily 
contributed to the platform later via a pull request.

Import, Build, and Run instructions
-----------------------------------
The recommended method for building the code is to use Android Studio. The following steps 
should allow you to obtain, build, and run the code with minimal difficulty.

1. Open Android studio.
2. Import project from Version control.
3. Enter either the url for the official Sana repository listed above or a fork under 
4. your own account if you created one.
5. Select the defaults presented on the import page.
6. When the gradle project has finished importing and building, select the app module and press run.
When the app starts you will be presented with an authentication screen. The resources in the 
source code includes a flag that loads a set of default credentials which will successfully 
authenticate against a Sana demo server.

For additional details on working with Android Studio, including testing and debugging, please 
consult the [Workflow](http://developer.android.com/tools/workflow/index.html) page on the 
Android Developer site.

Code Structure
--------------
The gradle based project is split into three distinct modules.
1. **api** – A pure java library that includes the POJO’s, network functions, and utilities for processing data.
2. **api-android** – Android implementation and wrappers around the pure Java api.
3. **app** – The code and resources for the Android based application.

The motivation for splitting the project into the three discrete modules was to allow developers
who may be interested wished to implement an alternate frontend, develop a client on another
platform, or otherwise may find some portion of the libraries useful to do so more easily.
The following sections contain additional details and features of each project that should
assist developers working with the code.

### api Module
The **api** module provides a pure Java library that contains the POJO’s that correlate with the 
data model used by the client, basic network code for communicating with the Sana middleware,
and a number of utility functions.

### api-android Module
The **api-android** module contains source code for non-application classes and interface to work 
with the Sana mobile code including communication with MDS.

### app Module
The **app** module contains the source code for the front end visual components and classes 
specific to the application.

Licensing
---------
This software is released under the BSD License. Please see LICENSE for a full
copy of the license and copyright information. Licensing information for
additional software included with this product can be found in the NOTICE.

Cryptographic Software Notice
-----------------------------

This distribution may include software that has been designed for use
with cryptographic software. The country in which you currently reside
may have restrictions on the import, possession, use, and/or re-export
to another country, of encryption software. BEFORE using any encryption
software, please check your country's laws, regulations and policies
concerning the import, possession, or use, and re-export of encryption
software, to see if this is permitted. See <http://www.wassenaar.org/>
for more information.

The U.S. Government Department of Commerce, Bureau of Industry and
Security (BIS), has classified this software as Export Commodity
Control Number (ECCN) 5D002.C.1, which includes information security
software using or performing cryptographic functions with asymmetric
algorithms. The form and manner of this Apache Software Foundation
distribution makes it eligible for export under the License Exception
ENC Technology Software Unrestricted (TSU) exception (see the BIS
Export Administration Regulations, Section 740.13) for both object
code and source code.

The following provides more details on the included software that
may be subject to export controls on cryptographic software:

  Apache HttpComponents Client interfaces with the
  Java Secure Socket Extension (JSSE) API to provide

    - HTTPS support

  Apache HttpComponents Client does not include any
  implementation of JSSE.
  
  
Contact
-------
Additional information can be found at, or is linked from, the main project 
site: http://sana.mit.edu
