---
title: MoNA - Installation, configuration and start of the application
layout: post
post-image: https://github.com/Forensic-Science-Investigation-Lab/mona/blob/487436845b6a457d986f63632f71deec9149639c/docs/assets/images/quick_start_guide.png
description: This tutorial will guide you to install and configure MoNA and take the first steps to analyze mobile devices.
version: 4.0.3
tags:
- how to
- setup
- configuration
---

# Installation
------------
1. Download the current version of MoNA (from the Moodle website).
2. Extract the downloaded archive.
3. Move the main folder to a disk drive without access restrictions.
4. Windows users:  Add the MoNA main folder as an exception in the Windows Defender settings (see the added section on "Adjusting of Windows Defender" for details).
5. Copy the license file in the subdirectory `./configurations` in the MoNA folder.
6. Start the application by double clicking `mona.exe`.

The startup splash screen shows the validity and expiration date of your license.
Please contact [Michael Spranger](mailto:spranger@hs-mittweida.de) in time before the license expires to apply for an extension!

# Configuration: mona.ini
-----------------------
For MoNA to be able to process large data volumes, the configuration file `mona.ini` residing in the installation folder of MoNA can/must be adjusted.
It is possible to change the maximum amount of RAM memory that is availabe to MoNA from a default value of 8GB to a higher value, which depends on the available RAM memory of the device MoNA is running on.

The responsible line in the configuration file is by default like this:
`-Xmx8g`

This can be adjusted for 16GB of RAM like this:
`-Xmx16g`

> A suggestion would be to not use the complete amount of RAM memory of a device for MoNA, depending on the number of programs running parallel to MoNA, a fourth of the overal RAM memory should stay unreserved.
The amount of RAM specified in the configuration file of MoNA will also be allocated dynamically and only when needed by MoNA.

# Configuration: Adjusting of Windows Defender
--------------------------------------------
To prevent a exteme slow data import process of mobile phone data on Microsoft Windows, the MoNA installation directory has to be added as an exception to the Windows Defender service.

1. Open the setting dialog *Virus & threat protection* in system settings (*Start -> Settings -> Update & Security -> Windows Security -> Virus & threat protection*).
2. Open the entry *Manage setting* under *Settings for Virus & thread protection*.
3. Select the entry *Add or remove exclusions* under the section *Exclusions*.
4. Add the MoNA installation directory via selecting *+ Add an exclusion*.