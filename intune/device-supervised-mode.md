---
# required metadata

title: Turn on iOS supervised mode with Microsoft Intune 
titleSuffix: 
description: Learn how to turn on iOS supervised mode with Intune.
keywords:
author: ErikjeMS
ms.author: erikje
manager: dougeby
ms.date: 02/15/2018
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 8190814-07f0-42d8-9b3a-87c67dd2b7ed

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
#ms.reviewer: ilwu
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-azure

---

# Turn on iOS supervised mode


[!INCLUDE[azure_portal](./includes/azure_portal.md)]

Apple iOS supervised mode gives administrators more options when managing Apple devices, making it useful for corporate-owned devices deployed at scale. For example, you can restrict AirDrop or prevent users from changing the name of the device. For a list of settings which require supervised mode, see [iOS device restrictionC settings in Intune](device-restrictions-ios.md).

Intune supports supervised mode as part of the Apple [Device Enrollment Program (DEP)](device-enrollment-program-enroll-ios.md).

For a list of Apple controls that require supervision, see Apple’s [Payload settings reference](http://help.apple.com/configurator/mac/2.4/#/cad5370d089).

## Turn on supervised mode during enrollment

In Intune, you can turn on supervised mode for devices when you [create an Apple enrollment profile in DEP](https://docs.microsoft.com/en-us/intune/device-enrollment-program-enroll-ios#create-an-apple-enrollment-profile). Under **Device Management Settings**, check the **Supervised** box.

## Turn on supervised mode after enrollment

After enrollment, the only way to turn on supervised mode is to connect an iOS device to a Mac and [use the Apple Configurator](apple-configurator-enroll-ios.md) (which will reset the device). You can’t configure a device for Supervised mode in Intune after enrollment.

## Identify a supervised device

To determine if a device is supervised, check the lock screen or **About** page:
- On the device's lock screen, it will say **This iPhone is managed by "Company Name".**
- On the device's **About** page, it will say **This iPhone is supervised. Company name can monitor your Internet traffic and locate this device.**

## Next steps

For other device management options, see [What is Microsoft Intune device management?](device-management.md)
