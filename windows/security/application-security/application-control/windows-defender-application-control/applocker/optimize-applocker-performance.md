---
title: Optimize AppLocker performance
description: This topic for IT professionals describes how to optimize AppLocker policy enforcement.
ms.localizationpriority: medium
ms.topic: conceptual
ms.date: 09/21/2017
---

# Optimize AppLocker performance

>[!NOTE]
>Some capabilities of Windows Defender Application Control are only available on specific Windows versions. Learn more about the [Windows Defender Application Control feature availability](/windows/security/threat-protection/windows-defender-application-control/feature-availability).

This topic for IT professionals describes how to optimize AppLocker policy enforcement.

## Optimization of Group Policy

AppLocker policies can be implemented by organization unit (OU) using Group Policy. If so, your Group Policy infrastructure should be optimized and retested for performance when AppLocker policies are added to existing Group Policy Objects (GPOs) or new GPOs are created, as you do with adding any policies to your GPOs.

For more info, see the [Optimizing Group Policy Performance](/previous-versions/technet-magazine/cc137720(v=msdn.10)) article in TechNet Magazine.

### AppLocker rule limitations

The more rules per GPO, the longer AppLocker requires for evaluation. There is no set limitation on the number of rules per GPO, but the number of rules that can fit into a 100 MB GPO varies based on the complexity of the rule, such as the number of file hashes included in a single file hash 
condition.

### Using the DLL rule collection

When the DLL rule collection is enabled, AppLocker must check each DLL that an application loads. The more DLLs, the longer AppLocker requires to complete the evaluation.