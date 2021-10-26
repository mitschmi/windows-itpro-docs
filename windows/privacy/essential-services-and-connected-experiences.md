---
title: Essential services and connected experiences for Windows
description: Explains what the essential services and connected experiences are for Windows
keywords: privacy, manage connections to Microsoft
ms.prod: w10
ms.mktglfcycl: manage
ms.sitesec: library
ms.localizationpriority: high
audience: ITPro
author: siosulli
ms.author: dansimp
manager: dansimp
ms.date: 
---

# Essential services and connected experiences for Windows

**Applies to**

- Windows 11
- Windows 10, version 1903 and later

Windows includes features that connect to the internet to provide enhanced experiences and additional service-based capabilities. These features are called connected experiences. For example, Microsoft Defender Antivirus is a connected experience that delivers updated protection to keep the devices in your organization secure.

When a connected experience is used, data is sent to and processed by Microsoft to provide that connected experience. This data is crucial because this information enables us to deliver these cloud-based connected experiences. We refer to this data as required service data. Required service data can include information related to the operation of the connected experience that is needed to keep the underlying service secure, up to date, and performing as expected. Required service data can also include information needed by a connected experience to perform its task, such as configuration information about Windows.

The connected experiences you choose to use in Windows will impact what required service data is sent to us.

Required service data is also collected and sent to Microsoft for essential services. Essential services are used to keep the product **secure, up to date, performing as expected** or are **integral** to how the product works. For example, the licensing service that confirms that you’re properly licensed to use Windows.

Although enterprise admins can turn off most essential services, we recommend, where applicable, you consider hosting the services on-premises and carefully assess the impact of turning off remaining services. The following list describes the essential services and connected experiences that are available to you in Windows and provides links to further information about each one.

> [!NOTE]
> The information in this article describes the most common connected experiences and essential services. We will continue to update our list of connected experiences over time as Windows evolves.

## Windows essential services

| **Essential service** | **Description** |
| --- | --- |
|Authentication|The authentication service is required to enable sign in to work or school accounts. It validates a user’s identity and provides access to multiple apps and system components like OneDrive and activity history. Using a work or school account to sign in to Windows enables Microsoft to provide a consistent experience across your devices. If the authentication service is turned off, many apps and components may lose functionality and users may not be able to sign in. <br/>To turn it off, see [Microsoft Account](manage-connections-from-windows-operating-system-components-to-microsoft-services.md#12-microsoft-account).|
|Certificates|Certificates are digital files, stored on client devices, used to both encrypt data and verify the identity of an individual or organization. Trusted root certificates issued by a certification authority (CA), are stored in a certificate trust list (CTL). The Automatic Root Certificates Update mechanism contacts Windows Updates to update the CTL. If a new version of the CTL is identified, the list of trusted root certificates cached on the local device will be updated. Untrusted certificates are certificates that are publicly known to be fraudulent. Untrusted certificates are also stored in a list on the local device and updated by the Automatic Root Certificates Update mechanism. <br/>If automatic updates are turned off, applications and websites may stop working because they did not receive an updated root certificate that the application uses. Additionally, the list of untrusted certificates will no longer be updated, which increases the attack vector on the device. <br/>To turn it off, see [Automatic Root Certificates Update](manage-connections-from-windows-operating-system-components-to-microsoft-services.md#automatic-root-certificates-update).|
| Services Configuration | Services Configuration is used by Windows components and apps, such as the telemetry service, to dynamically update their configuration. If you turn off this service, apps using this service may stop working. <br/>To turn it off, see [Services Configuration](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#31-services-configuration).|
| Licensing | Licensing services are used for the activation of Windows, and apps purchased from the Microsoft Store. If you disable the Windows License Manager Service or the Software Protection Platform Service, it may prevent activation of genuine Windows and store applications. <br/>To turn off licensing services, see [License Manager](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#9-license-manager) and [Software Protection Platform](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#19-software-protection-platform).|
| Networking | Networking in Windows provides connectivity to and from your devices to the local intranet and internet. If you turn off networking, Windows devices will lose network connectivity. <br/>To turn off Network Adapters, see [Disable-NetAdapter](/powershell/module/netadapter/disable-netadapter).|
| Device setup | The first time a user sets up a new device, the Windows out-of-box experience (OOBE) guides the user through the steps to accept the license agreement, connect to the internet, sign in to (or sign up for) a Microsoft account, and takes care of other important tasks. Most settings can also be changed after setup is completed. <br/>To customize the initial setup experience, see [Customize Setup](/windows-hardware/customize/desktop/customize-oobe).|
| Diagnostic Data | Microsoft collects diagnostic data including error data about your devices with the help of the telemetry service. Diagnostic data gives every user a voice in the operating system’s development and ongoing improvement. It helps us understand how Windows behaves in the real world, focus on user priorities, find and fix problems, and improve services. This data allows Microsoft to improve the Windows experience. Setting diagnostic data to off means important information to help fix issues and improve quality will not be available to Microsoft. <br/>To turn it off, see [Telemetry Services](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#1816-feedback--diagnostics).|
| Update | Windows Update ensures devices are kept up to date and secure by downloading the latest updates and security patches for Windows. This service also enables users download apps from the Microsoft Store and keep them up to date. Turning off Windows Update will potentially leave your Windows devices in a vulnerable state and more prone to security threats. <br/>Other services like Device metadata retrieval and Font streaming also ensure that the content on your devices is kept up to date. <br/>To turn off updates, see [Windows Update](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#29-windows-update), [Device Metadata Retrieval](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#4-device-metadata-retrieval), and [Font Streaming](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#6-font-streaming).|
| Microsoft Store | Microsoft Store enables users to purchase and download apps, games, and digital content. The Store also enables the developers of these apps to send toast, tile, badge, and raw updates from their own cloud service. This provides a mechanism to deliver new updates to store apps in a power-efficient and dependable way. The Store can also revoke malicious apps. <br/>To turn it off, see [Microsoft Store](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#26-microsoft-store).|

## Windows connected experiences

| **Connected experience** | **Description** |
| --- | --- |
|Activity History|Activity History shows a history of activities a user has performed and can even synchronize activities across multiple devices for the same user. Synchronization across devices only works when a user signs in with the same account. <br/>To turn it off, see [Activity History](manage-connections-from-windows-operating-system-components-to-microsoft-services.md#1822-activity-history). |
|Cloud Clipboard|Cloud Clipboard enables users to copy images and text across all Windows devices when they sign in with the same account. Users can paste from their clipboard history and also pin items.<br/>To turn it off, see [Cloud Clipboard](manage-connections-from-windows-operating-system-components-to-microsoft-services.md#30-cloud-clipboard). |
| Date and Time | The Windows Time service is used to synchronize and maintain the most accurate date and time on your devices. It's installed by default and starts automatically on devices that are part of a domain. It can be started manually on other devices. If this service is stopped, date and time synchronization will be unavailable and any services that explicitly depend on it will fail to start. <br/>To turn it off, see [Date and Time](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#3-date--time). |
| Delivery Optimization | Delivery Optimization is a cloud-managed, peer-to-peer client and a downloader service for Windows updates, upgrades, and applications to an organization's networked devices. Delivery Optimization allows devices to download updates from alternate sources, such as other peers on the network, in addition to Microsoft servers. This helps when you have a limited or unreliable Internet connection and reduces the bandwidth needed to keep all your organization's devices up to date. <br/>If you have Delivery Optimization Peer-to-Peer option turned on, devices on your network may send and receive updates and apps to other devices on your local network, if you choose, or to devices on the Internet. By default, devices running Windows will only use Delivery Optimization to get and receive updates for devices and apps on your local network. <br/>To turn it off, see [Delivery Optimization](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#28-delivery-optimization). |
| Emojis and more | The Emoji and more menu allows users to insert a variety of content like emoji, kaomoji, GIFs, symbols, and clipboard history. This connected experience is new in Windows 11. <br/>To turn it off, see [Emojis availability](/windows/client-management/mdm/policy-csp-textinpu.md#textinput-touchkeyboardemojibuttonavailability). |
| Find My Device | Find My Device is a feature that can help users locate their Windows device if it's lost or stolen. This feature only works if a Microsoft account is used to sign in to the device, the user is an administrator on the device, and when location is turned on for the device. Users can find their device by logging in to [https://account.microsoft.com/devices](https://account.microsoft.com/devices) under the Find My Device tab. <br/>To turn it off, see [Find My Device](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#5-find-my-device). |
| Location services | The device location setting enables certain Windows features such as auto setting the time zone or Find My Device to function properly. When the device location setting is enabled, the Microsoft location service will use a combination of global positioning service (GPS), nearby wireless access points, cell towers, and IP address to determine the device’s location. Depending on the capabilities of the device, its location can be determined with varying degrees of accuracy and may in some cases be determined precisely. <br/>To turn it off, see [Location services](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#182-location). |
| Microsoft Defender Antivirus | Microsoft Defender Antivirus provides cloud-delivered protection against new and emerging threats for the devices in your organization. Turning off Microsoft Defender Antivirus will potentially leave your Windows devices in a vulnerable state and more prone to security threats. <br/>To turn it off, see [Microsoft Defender Antivirus](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#bkmk-defender). |
| Microsoft Defender SmartScreen | Microsoft Defender SmartScreen is a feature of Windows, Internet Explorer, and Microsoft Edge. It helps protect users against phishing or malware websites and applications, and the downloading of potentially malicious files. Turning off Microsoft Defender SmartScreen means you cannot block a website or warn users they may be accessing a malicious site. <br/>To turn it off, see [Microsoft Defender SmartScreen](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#241-microsoft-defender-smartscreen). |
| OneDrive | OneDrive is a cloud storage system that allows you to save your files and photos, and access them from any device, anywhere. <br/>To turn off OneDrive, see [OneDrive](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#16-onedrive). |
| Troubleshooting Service | Windows troubleshooting service will automatically fix critical issues like corrupt settings that keep critical services from running. The service will also make adjustments to work with your hardware, or make other specific changes required for Windows to operate with the hardware, apps, and settings you’ve selected. In addition, it will recommend troubleshooting for other problems that aren’t critical to normal Windows operation but might impact your experience. <br/>To turn it off, see [Troubleshooting service](/windows/client-management/mdm/policy-csp-troubleshooting). |
| Voice Typing | Voice typing (also referred to as Windows dictation in earlier versions of Windows) allows users to write text by speaking by using Microsoft’s online speech recognition technology. <br/>To turn it off, see [Speech recognition](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#186-speech). |
| Windows backup | When settings synchronization is turned on, a user's settings are synced across all Windows devices when they sign in with the same account. <br/>To turn it off, see [Sync your settings](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#21-sync-your-settings). |
| Windows Dashboard Widgets | Windows Dashboard widget is a dynamic view that shows users personalized content like news, weather, their calendar and to-do list, and recent photos. It provides a quick glance view, which allows users to be productive without needing to go to multiple apps or websites. This connected experience is new in Windows 11. |
| Windows Insider Program | The Windows Insider Preview program lets you help shape the future of Windows, be part of the community, and get early access to builds of Windows. Once you've registered for the program, you can run Insider Preview builds on as many devices as you want, each in the channel of your choice. Learn how to join the Windows Insider program by visiting the program’s [website](https://insider.windows.com/). <br/>To turn it off, see [Windows Insider Program](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#7-insider-preview-builds). |
| Windows Search | Windows Search lets users use the search box on the taskbar to find what they are looking for, whether it’s on their device, in the cloud, or on the web. Windows Search can provide results for items from the device (including apps, settings, and files), the users account (including OneDrive, SharePoint, and other Microsoft services), and the internet. <br/>To turn it off, see [Windows Search](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#2-cortana-and-search). |
| Windows Spotlight | Windows Spotlight displays new background images on the lock screen each day. Additionally, it provides feature suggestions, fun facts, and tips on the lock screen background. <br/>Administrators can turn off Windows Spotlight features to prevent users from using the Windows Spotlight background. <br/>To turn it off, see [Windows Spotlight](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#25-windows-spotlight). |

## Microsoft Edge essential services and connected experiences

Windows ships with Microsoft Edge and Internet Explorer on Windows devices. Microsoft Edge is the default browser and is recommended for the best web browsing experience.</br> You can find details on all of Microsoft Edge's connected experiences and essential services [here](/microsoft-edge/privacy-whitepaper). To turn off specific Microsoft Edge feature, see [Microsoft Edge](manage-connections-from-windows-operating-system-components-to-microsoft-services.md#13-microsoft-edge).

## IE essential services and connected experiences

Internet Explorer shares many of the Windows essential services listed above. The following table provides more details on the essential services and connected experiences specific to Internet Explorer.

> [!NOTE]
> Apart from ActiveX Filtering, which is an essential service, all other features listed below are connected experiences.</br> To turn off specific connected experiences, see [Internet Explorer](manage-connections-from-windows-operating-system-components-to-microsoft-services.md#8-internet-explorer).

| **Connected experience** | **Description** |
| --- | --- |
|ActiveX Filtering|ActiveX controls are small apps that allow websites to provide content such as videos and games, and let users interact with controls like toolbars and stock tickers. However, these apps can sometimes malfunction, and in some cases, they might be used to collect information from user devices, install software without a user's agreement, or be used to control a device remotely without a user's permission.</br> ActiveX Filtering in Internet Explorer prevents sites from installing and using these apps which, can help keep users safer as they browse, but it can also affect the user experience of certain sites as interactive content might not work when ActiveX Filtering is on. <br/>Note: To further enhance security, Internet Explorer also allows you to block out-of-date ActiveX controls. |
|Suggested Sites|Suggested Sites is an online experience that recommends websites, images, or videos a user might be interested in. When Suggested Sites is turned on, a user’s web browsing history is periodically sent to Microsoft.|
| Address Bar and Search suggestions | With search suggestions enabled, users will be offered suggested search terms as they type in the Address Bar. As users type information, it will be sent to the default search provider. |
| Auto-complete feature for web addresses | The auto-complete feature suggests possible matches when users are typing web addresses in the browser address bar. |
| Compatibility logging | This feature is designed for use by developers and IT professionals to determine the compatibility of their websites with Internet Explorer. It is disabled by default and needs to be enabled to start logging Internet Explorer events in the Windows Event Viewer. These events describe failures that might have happened on the site and can include information about specific controls and webpages that failed. |
| Compatibility View | Compatibility View helps make websites designed for older browsers look better when viewed in Internet Explorer. The compatibility view setting allows you to choose whether an employee can fix website display problems they encounter while browsing. |
| Flip ahead | Flip ahead enables users to flip through web content quickly by swiping across the page or by clicking forward. When flip ahead is turned on, web browsing history is periodically sent to Microsoft. If you turn off this setting, users will no longer be able swipe across a screen or click forward to go to the next pre-loaded page of a website. |
| Web Slices | A Web Slice enables users to subscribe to and automatically receive updates to content directly within a web page. Disabling the RSS Feeds setting will turn off background synchronization for feeds and Web Slices. |
| Accelerators | Accelerators are menu options in Internet Explorer that help automate common browser-related tasks. In Internet Explorer, when you right-click selected text, Accelerators appear in the list of available options. <br/>For example, if you select a word, you can use the "Translate with Bing" Accelerator to obtain a translation of that word. |
| Pinning websites to Start | When a user pins a website to the Start menu, it displays as a tile similar to the way apps are displayed. Like Microsoft Store apps, website tiles might display updates if the website has been designed to do so. For example, an online email website might send updates to the tile indicating how many new messages a user has. |

## Related links

- [Manage connections from Windows operating system components to Microsoft services](manage-connections-from-windows-operating-system-components-to-microsoft-services.md)
- [Connected Experiences in Office](/deployoffice/privacy/connected-experiences.md)
- [Essential Services in Office](/deployoffice/privacy/essential-services.md)

To view endpoints for Windows Enterprise, see:

- [Manage connection endpoints for Windows 11](manage-windows-11-endpoints.md)
- [Manage connection endpoints for Windows 10, version 21H1](manage-windows-21H1-endpoints.md)
- [Manage connection endpoints for Windows 10, version 20H2](manage-windows-20h2-endpoints.md)
- [Manage connection endpoints for Windows 10, version 1909](manage-windows-1909-endpoints.md)
- [Manage connection endpoints for Windows 10, version 1903](manage-windows-1903-endpoints.md)
- [Manage connection endpoints for Windows 10, version 1809](manage-windows-1809-endpoints.md)
- [Manage connection endpoints for Windows 10, version 1803](manage-windows-1803-endpoints.md)
- [Manage connection endpoints for Windows 10, version 1709](manage-windows-1709-endpoints.md)

To view endpoints for non-Enterprise Windows editions, see:

- [Windows 11 connection endpoints for non-Enterprise editions](windows-11-endpoints-non-enterprise-editions.md)
- [Windows 10, version 21H1, connection endpoints for non-Enterprise editions](windows-endpoints-21H1-non-enterprise-editions.md)
- [Windows 10, version 20H2, connection endpoints for non-Enterprise editions](windows-endpoints-20H2-non-enterprise-editions.md)
- [Windows 10, version 1909, connection endpoints for non-Enterprise editions](windows-endpoints-1909-non-enterprise-editions.md)
- [Windows 10, version 1903, connection endpoints for non-Enterprise editions](windows-endpoints-1903-non-enterprise-editions.md)
- [Windows 10, version 1809, connection endpoints for non-Enterprise editions](windows-endpoints-1809-non-enterprise-editions.md)
- [Windows 10, version 1803, connection endpoints for non-Enterprise editions](windows-endpoints-1803-non-enterprise-editions.md)
- [Windows 10, version 1709, connection endpoints for non-Enterprise editions](windows-endpoints-1709-non-enterprise-editions.md)