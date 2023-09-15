---
title: Configure an AppLocker policy for enforce rules
description: This topic for IT professionals describes the steps to enable the AppLocker policy enforcement setting.
ms.localizationpriority: medium
ms.topic: conceptual
ms.date: 09/21/2017
---

# Configure an AppLocker policy for enforce rules

>[!NOTE]
>Some capabilities of Windows Defender Application Control are only available on specific Windows versions. Learn more about the [Windows Defender Application Control feature availability](/windows/security/threat-protection/windows-defender-application-control/feature-availability).

This topic for IT professionals describes the steps to enable the AppLocker policy enforcement setting.

>**Note:**  When AppLocker policy enforcement is set to **Enforce rules**, rules are enforced for the rule collection and all events are audited.
 
For info about how AppLocker policies are applied within a GPO structure, see [Understand AppLocker rules and enforcement setting inheritance in Group Policy](understand-applocker-rules-and-enforcement-setting-inheritance-in-group-policy.md).

You can perform this task by using the Group Policy Management Console for an AppLocker policy in a Group Policy Object (GPO) or by using the Local Security Policy snap-in for an AppLocker policy on a local computer or in a security template. For info how to use these MMC snap-ins to administer AppLocker, see [Administer AppLocker](administer-applocker.md#bkmk-using-snapins).

**To enable the Enforce rules enforcement setting**

1.  From the AppLocker console, right-click **AppLocker**, and then click **Properties**.
2.  On the **Enforcement** tab of the **AppLocker Properties** dialog box, select the **Configured** check box for the rule collection that you're editing, and then verify that **Enforce rules** is selected.
3.  Click **OK**.

For info about viewing the events generated from rules enforcement, see [Monitor app usage with AppLocker](monitor-application-usage-with-applocker.md).