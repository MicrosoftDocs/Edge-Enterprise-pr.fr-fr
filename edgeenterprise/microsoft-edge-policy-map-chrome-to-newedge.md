---
title: Mappage de Google Chrome vers la stratégie Microsoft Edge
ms.author: brianalt
author: brianalt
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Mappage de Google Chrome vers la stratégie Microsoft Edge
ms.openlocfilehash: 9c422c66df9f2892e54ad9d935f4d6de6f88eae3
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642840"
---
# <a name="google-chrome-to-microsoft-edge-policy-mapping"></a>Mappage de Google Chrome vers la stratégie Microsoft Edge

Cet article présente la mise en correspondance les stratégies Google Chrome avec les stratégies Microsoft Edge appropriées qui sont prises en charge dans la version80. Pour en savoir plus sur les stratégies Microsoft Edge héritées, voir l’article [Mappage de Microsoft Edge hérité vers la stratégie Microsoft Edge](/deployedge/microsoft-edge-policy-map-chrome-to-newedge?branch=master).

> [!NOTE]
> Le mappage fourni ci-dessous est destiné à vous aider dans le cadre de votre déploiement initial de la version80 de Microsoft Edge. Pour obtenir la liste établie des dernières stratégies, voir:
> - [Référence de stratégie du navigateur](/deployedge/microsoft-edge-policies)
> - [Référence de stratégie de mise à jour](/deployedge/microsoft-edge-update-policies)

## <a name="google-chrome-to-microsoft-edge-policy-map"></a>Mise en correspondance de Google Chrome avec la stratégie Microsoft Edge

|Stratégie Google Chrome|Stratégie Microsoft Edge|
|-|-|
|[AbusiveExperienceInterventionEnforce](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AbusiveExperienceInterventionEnforce)|Non applicable|
|[AdsSettingForIntrusiveAdsSites](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AdsSettingForIntrusiveAdsSites)|[AdsSettingForIntrusiveAdsSites](./microsoft-edge-policies.md#adssettingforintrusiveadssites)|
|[AllowCrossOriginAuthPrompt](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowCrossOriginAuthPrompt)|[AllowCrossOriginAuthPrompt](./microsoft-edge-policies.md#allowcrossoriginauthprompt)|
|[AllowDeletingBrowserHistory](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowDeletingBrowserHistory)|[AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory)|
|[AllowDinosaurEasterEgg](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowDinosaurEasterEgg)|Non applicable|
|[AllowedDomainsForApps](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowedDomainsForApps)|Non applicable|
|[AllowFileSelectionDialogs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowFileSelectionDialogs)|[AllowFileSelectionDialogs](./microsoft-edge-policies.md#allowfileselectiondialogs)|
|[AllowOutdatedPlugins](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowOutdatedPlugins)|Non applicable|
|[AllowPasswordProtectedFiles](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowPasswordProtectedFiles)|Non applicable|
|[AllowPopupsDuringPageUnload](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowPopupsDuringPageUnload)|[AllowPopupsDuringPageUnload](./microsoft-edge-policies.md#allowpopupsduringpageunload)|
|[AllowSyncXHRInPageDismissal](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AllowSyncXHRInPageDismissal)|[AllowSyncXHRInPageDismissal](./microsoft-edge-policies.md#allowsyncxhrinpagedismissal)|
|[AlternateErrorPagesEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AlternateErrorPagesEnabled)|[AlternateErrorPagesEnabled](./microsoft-edge-policies.md#alternateerrorpagesenabled)|
|[AlternativeBrowserParameters](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AlternativeBrowserParameters)|Afficher MicrosoftEdge avec le Mode Internet Explorer|
|[AlternativeBrowserPath](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AlternativeBrowserPath)|Afficher MicrosoftEdge avec le Mode Internet Explorer|
|[AlwaysOpenPdfExternally](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AlwaysOpenPdfExternally)|[AlwaysOpenPdfExternally](./microsoft-edge-policies.md#alwaysopenpdfexternally)|
|[AmbientAuthenticationInPrivateModesEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AmbientAuthenticationInPrivateModesEnabled)|Non applicable|
|[ApplicationLocaleValue](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ApplicationLocaleValue)|[ApplicationLocaleValue](./microsoft-edge-policies.md#applicationlocalevalue)|
|[AudioCaptureAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AudioCaptureAllowed)|[AudioCaptureAllowed](./microsoft-edge-policies.md#audiocaptureallowed)|
|[AudioCaptureAllowedUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AudioCaptureAllowedUrls)|[AudioCaptureAllowedUrls](./microsoft-edge-policies.md#audiocaptureallowedurls)|
|[AudioSandboxEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AudioSandboxEnabled)|Non applicable|
|[AuthNegotiateDelegateByKdcPolicy](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AuthNegotiateDelegateByKdcPolicy)|Non applicable|
|[AuthNegotiateDelegateWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AuthNegotiateDelegateWhitelist)|[AuthNegotiateDelegateAllowlist](./microsoft-edge-policies.md#authnegotiatedelegateallowlist)|
|[AuthSchemes](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AuthSchemes)|[AuthSchemes](./microsoft-edge-policies.md#authschemes)|
|[AuthServerWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AuthServerWhitelist)|[AuthServerAllowlist](./microsoft-edge-policies.md#authserverallowlist)|
|[AutofillAddressEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AutofillAddressEnabled)|[AutofillAddressEnabled](./microsoft-edge-policies.md#autofilladdressenabled)|
|[AutofillCreditCardEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AutofillCreditCardEnabled)|[AutofillCreditCardEnabled](./microsoft-edge-policies.md#autofillcreditcardenabled)|
|[AutoplayAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AutoplayAllowed)|[AutoplayAllowed](./microsoft-edge-policies.md#autoplayallowed)|
|[AutoplayWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AutoplayWhitelist)|Non applicable|
|[AutoSelectCertificateForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=AutoSelectCertificateForUrls)|[AutoSelectCertificateForUrls](./microsoft-edge-policies.md#autoselectcertificateforurls)|
|[BackgroundModeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BackgroundModeEnabled)|[BackgroundModeEnabled](./microsoft-edge-policies.md#backgroundmodeenabled)|
|[BlockExternalExtensions](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BlockExternalExtensions)|Non applicable|
|[BlockLargeFileTransfer](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BlockLargeFileTransfer)|Non applicable|
|[BlockThirdPartyCookies](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BlockThirdPartyCookies)|[BlockThirdPartyCookies](./microsoft-edge-policies.md#blockthirdpartycookies)|
|[BookmarkBarEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BookmarkBarEnabled)|[FavoritesBarEnabled](./microsoft-edge-policies.md#favoritesbarenabled)|
|[BrowserAddPersonEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserAddPersonEnabled)|[BrowserAddProfileEnabled](./microsoft-edge-policies.md#browseraddprofileenabled)|
|[BrowserGuestModeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserGuestModeEnabled)|[BrowserGuestModeEnabled](./microsoft-edge-policies.md#browserguestmodeenabled)|
|[BrowserGuestModeEnforced](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserGuestModeEnforced)|Non applicable|
|[BrowserNetworkTimeQueriesEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserNetworkTimeQueriesEnabled)|[BrowserNetworkTimeQueriesEnabled](./microsoft-edge-policies.md#browsernetworktimequeriesenabled)|
|[BrowserSignin](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSignin)|[BrowserSignin](./microsoft-edge-policies.md#browsersignin)|
|[BrowserSwitcherChromeParameters](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherChromeParameters)|Afficher MicrosoftEdge avec le Mode Internet Explorer|
|[BrowserSwitcherChromePath](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherChromePath)|Afficher MicrosoftEdge avec le Mode Internet Explorer|
|[BrowserSwitcherDelay](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherDelay)|Afficher MicrosoftEdge avec le Mode Internet Explorer|
|[BrowserSwitcherEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherEnabled)|Afficher MicrosoftEdge avec le Mode Internet Explorer|
|[BrowserSwitcherExternalGreylistUrl](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherExternalGreylistUrl)|Afficher MicrosoftEdge avec le Mode Internet Explorer|
|[BrowserSwitcherExternalSitelistUrl](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherExternalSitelistUrl)|Afficher MicrosoftEdge avec le Mode Internet Explorer|
|[BrowserSwitcherKeepLastChromeTab](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherKeepLastChromeTab)|Afficher MicrosoftEdge avec le Mode Internet Explorer|
|[BrowserSwitcherUrlGreylist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherUrlGreylist)|Afficher MicrosoftEdge avec le Mode Internet Explorer|
|[BrowserSwitcherUrlList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherUrlList)|Afficher MicrosoftEdge avec le Mode Internet Explorer|
|[BrowserSwitcherUseIeSitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BrowserSwitcherUseIeSitelist)|Afficher MicrosoftEdge avec le Mode Internet Explorer|
|[BuiltInDnsClientEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=BuiltInDnsClientEnabled)|[BuiltInDnsClientEnabled](./microsoft-edge-policies.md#builtindnsclientenabled)|
|[CertificateTransparencyEnforcementDisabledForCas](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CertificateTransparencyEnforcementDisabledForCas)|[CertificateTransparencyEnforcementDisabledForCas](./microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforcas)|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CertificateTransparencyEnforcementDisabledForLegacyCas)|[CertificateTransparencyEnforcementDisabledForLegacyCas](./microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforlegacycas)|
|[CertificateTransparencyEnforcementDisabledForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CertificateTransparencyEnforcementDisabledForUrls)|[CertificateTransparencyEnforcementDisabledForUrls](./microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls)|
|[CheckContentCompliance](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CheckContentCompliance)|Non applicable|
|[ChromeCleanupEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ChromeCleanupEnabled)|Non applicable|
|[ChromeCleanupReportingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ChromeCleanupReportingEnabled)|Non applicable|
|[ClickToCallEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ClickToCallEnabled)|Non applicable|
|[CloudExtensionRequestEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudExtensionRequestEnabled)|Non applicable|
|[CloudManagementEnrollmentMandatory](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudManagementEnrollmentMandatory)|Non applicable|
|[CloudManagementEnrollmentToken](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudManagementEnrollmentToken)|Non applicable|
|[CloudPolicyOverridesPlatformPolicy](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudPolicyOverridesPlatformPolicy)|Non applicable|
|[CloudPrintProxyEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudPrintProxyEnabled)|Non applicable|
|[CloudPrintSubmitEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudPrintSubmitEnabled)|Non applicable|
|[CloudReportingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CloudReportingEnabled)|Non applicable|
|[CoalesceH2ConnectionsWithClientCertificatesForHosts](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CoalesceH2ConnectionsWithClientCertificatesForHosts)
|[CommandLineFlagSecurityWarningsEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CommandLineFlagSecurityWarningsEnabled)
|[ComponentUpdatesEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ComponentUpdatesEnabled)|[ComponentUpdatesEnabled](./microsoft-edge-policies.md#componentupdatesenabled)|
|[CookiesAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CookiesAllowedForUrls)|[CookiesAllowedForUrls](./microsoft-edge-policies.md#cookiesallowedforurls)|
|[CookiesBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CookiesBlockedForUrls)|[CookiesBlockedForUrls](./microsoft-edge-policies.md#cookiesblockedforurls)|
|[CookiesSessionOnlyForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CookiesSessionOnlyForUrls)|[CookiesSessionOnlyForUrls](./microsoft-edge-policies.md#cookiessessiononlyforurls)|
|[CorsLegacyModeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CorsLegacyModeEnabled)|Non applicable|
|[CorsMitigationList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=CorsMitigationList)|Non applicable|
|[DefaultBrowserSettingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultBrowserSettingEnabled)|[DefaultBrowserSettingEnabled](./microsoft-edge-policies.md#defaultbrowsersettingenabled)|
|[DefaultCookiesSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultCookiesSetting)|[DefaultCookiesSetting](./microsoft-edge-policies.md#defaultcookiessetting)|
|[DefaultDownloadDirectory](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultDownloadDirectory)|Non applicable|
|[DefaultGeolocationSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultGeolocationSetting)|[DefaultGeolocationSetting](./microsoft-edge-policies.md#defaultgeolocationsetting)|
|[DefaultImagesSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultImagesSetting)|[DefaultImagesSetting](./microsoft-edge-policies.md#defaultimagessetting)|
|[DefaultInsecureContentSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultInsecureContentSetting)|[DefaultInsecureContentSetting](./microsoft-edge-policies.md#defaultinsecurecontentsetting)|
|[DefaultJavaScriptSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultJavaScriptSetting)|[DefaultJavaScriptSetting](./microsoft-edge-policies.md#defaultjavascriptsetting)|
|[DefaultNotificationsSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultNotificationsSetting)|[DefaultNotificationsSetting](./microsoft-edge-policies.md#defaultnotificationssetting)|
|[DefaultPluginsSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultPluginsSetting)|[DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting)|
|[DefaultPopupsSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultPopupsSetting)|[DefaultPopupsSetting](./microsoft-edge-policies.md#defaultpopupssetting)|
|[DefaultPrinterSelection](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultPrinterSelection)|[DefaultPrinterSelection](./microsoft-edge-policies.md#defaultprinterselection)|
|[DefaultSearchProviderAlternateURLs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderAlternateURLs)|Non applicable|
|[DefaultSearchProviderEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderEnabled)|[DefaultSearchProviderEnabled](./microsoft-edge-policies.md#defaultsearchproviderenabled)|
|[DefaultSearchProviderEncodings](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderEncodings)|[DefaultSearchProviderEncodings](./microsoft-edge-policies.md#defaultsearchproviderencodings)|
|[DefaultSearchProviderIconURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderIconURL)|Non applicable|
|[DefaultSearchProviderImageURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderImageURL)|[DefaultSearchProviderImageURL](./microsoft-edge-policies.md#defaultsearchproviderimageurl)|
|[DefaultSearchProviderImageURLPostParams](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderImageURLPostParams)|[DefaultSearchProviderImageURLPostParams](./microsoft-edge-policies.md#defaultsearchproviderimageurlpostparams)|
|[DefaultSearchProviderKeyword](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderKeyword)|[DefaultSearchProviderKeyword](./microsoft-edge-policies.md#defaultsearchproviderkeyword)|
|[DefaultSearchProviderName](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderName)|[DefaultSearchProviderName](./microsoft-edge-policies.md#defaultsearchprovidername)|
|[DefaultSearchProviderNewTabURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderNewTabURL)|Non applicable|
|[DefaultSearchProviderSearchURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderSearchURL)|[DefaultSearchProviderSearchURL](./microsoft-edge-policies.md#defaultsearchprovidersearchurl)|
|[DefaultSearchProviderSearchURLPostParams](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderSearchURLPostParams)|Non applicable|
|[DefaultSearchProviderSuggestURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderSuggestURL)|[DefaultSearchProviderSuggestURL](./microsoft-edge-policies.md#defaultsearchprovidersuggesturl)|
|[DefaultSearchProviderSuggestURLPostParams](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultSearchProviderSuggestURLPostParams)|Non applicable|
|[DefaultWebBluetoothGuardSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultWebBluetoothGuardSetting)|[DefaultWebBluetoothGuardSetting](./microsoft-edge-policies.md#defaultwebbluetoothguardsetting)|
|[DefaultWebUsbGuardSetting](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DefaultWebUsbGuardSetting)|[DefaultWebUsbGuardSetting](./microsoft-edge-policies.md#defaultwebusbguardsetting)|
|[DelayDeliveryUntilVerdict](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DelayDeliveryUntilVerdict)|Non applicable|
|[DeveloperToolsAvailability](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DeveloperToolsAvailability)|[DeveloperToolsAvailability](./microsoft-edge-policies.md#developertoolsavailability)|
|[Disable3DAPIs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=Disable3DAPIs)|[Disable3DAPIs](./microsoft-edge-policies.md#disable3dapis)|
|[DisableAuthNegotiateCnameLookup](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DisableAuthNegotiateCnameLookup)|[DisableAuthNegotiateCnameLookup](./microsoft-edge-policies.md#disableauthnegotiatecnamelookup)|
|[DisablePrintPreview](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DisablePrintPreview)|[UseSystemPrintDialog](./microsoft-edge-policies.md#usesystemprintdialog)|
|[DisableSafeBrowsingProceedAnyway](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DisableSafeBrowsingProceedAnyway)|[PreventSmartScreenPromptOverride](./microsoft-edge-policies.md#preventsmartscreenpromptoverride)|
|[DisableScreenshots](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DisableScreenshots)|[DisableScreenshots](./microsoft-edge-policies.md#disablescreenshots)|
|[DiskCacheDir](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DiskCacheDir)|[DiskCacheDir](./microsoft-edge-policies.md#diskcachedir)|
|[DiskCacheSize](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DiskCacheSize)|[DiskCacheSize](./microsoft-edge-policies.md#diskcachesize)|
|[DNSInterceptionChecksEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DNSInterceptionChecksEnabled)|[DNSInterceptionChecksEnabled](./microsoft-edge-policies.md#dnsinterceptionchecksenabled)|
|[DnsOverHttpsMode](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DnsOverHttpsMode)|Non applicable|
|[DnsOverHttpsTemplates](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DnsOverHttpsTemplates)|Non applicable|
|[DownloadDirectory](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DownloadDirectory)|[DownloadDirectory](./microsoft-edge-policies.md#downloaddirectory)|
|[DownloadRestrictions](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=DownloadRestrictions)|[DownloadRestrictions](./microsoft-edge-policies.md#downloadrestrictions)|
|[EditBookmarksEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EditBookmarksEnabled)|[EditFavoritesEnabled](./microsoft-edge-policies.md#editfavoritesenabled)|
|[EnableAuthNegotiatePort](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EnableAuthNegotiatePort)|[EnableAuthNegotiatePort](./microsoft-edge-policies.md#enableauthnegotiateport)|
|[EnableDeprecatedWebPlatformFeatures](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EnableDeprecatedWebPlatformFeatures)|[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures)|
|[EnableMediaRouter](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EnableMediaRouter)|[EnableMediaRouter](./microsoft-edge-policies.md#enablemediarouter)|
|[EnableOnlineRevocationChecks](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EnableOnlineRevocationChecks)|[EnableOnlineRevocationChecks](./microsoft-edge-policies.md#enableonlinerevocationchecks)|
|[EnterpriseHardwarePlatformAPIEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=EnterpriseHardwarePlatformAPIEnabled)|[EnterpriseHardwarePlatformAPIEnabled](./microsoft-edge-policies.md#enterprisehardwareplatformapienabled)|
|[ExtensionAllowedTypes](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionAllowedTypes)|[ExtensionAllowedTypes](./microsoft-edge-policies.md#extensionallowedtypes)|
|[ExtensionInstallBlacklist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallBlacklist)|[ExtensionInstallBlocklist](./microsoft-edge-policies.md#extensioninstallblocklist)|
|[ExtensionInstallForcelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallForcelist)|[ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist)|
|[ExtensionInstallListsMergeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallListsMergeEnabled)|Non applicable|
|[ExtensionInstallSources](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallSources)|[ExtensionInstallSources](./microsoft-edge-policies.md#extensioninstallsources)|
|[ExtensionInstallWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallWhitelist)|[ExtensionInstallAllowlist](./microsoft-edge-policies.md#extensioninstallallowlist)|
|[ExtensionSettings](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionSettings)|[ExtensionSettings](./microsoft-edge-policies.md#extensionsettings)|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExternalProtocolDialogShowAlwaysOpenCheckbox)|[ExternalProtocolDialogShowAlwaysOpenCheckbox](./microsoft-edge-policies.md#externalprotocoldialogshowalwaysopencheckbox)|
|[ForceEphemeralProfiles](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ForceEphemeralProfiles)|[ForceEphemeralProfiles](./microsoft-edge-policies.md#forceephemeralprofiles)|
|[ForceGoogleSafeSearch](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ForceGoogleSafeSearch)|[ForceGoogleSafeSearch](./microsoft-edge-policies.md#forcegooglesafesearch)|
|[ForceNetworkInProcess](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ForceNetworkInProcess)|[ForceNetworkInProcess](./microsoft-edge-policies.md#forcenetworkinprocess)|
|[ForceYouTubeRestrict](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ForceYouTubeRestrict)|[ForceYouTubeRestrict](./microsoft-edge-policies.md#forceyoutuberestrict)|
|[FullscreenAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=FullscreenAllowed)|[FullscreenAllowed](./microsoft-edge-policies.md#fullscreenallowed)|
|[GloballyScopeHTTPAuthCacheEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=GloballyScopeHTTPAuthCacheEnabled)|Non applicable|
|[HardwareAccelerationModeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=HardwareAccelerationModeEnabled)|[HardwareAccelerationModeEnabled](./microsoft-edge-policies.md#hardwareaccelerationmodeenabled)|
|[HideWebStoreIcon](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=HideWebStoreIcon)|Non applicable|
|[HomepageIsNewTabPage](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=HomepageIsNewTabPage)|[HomepageIsNewTabPage](./microsoft-edge-policies.md#homepageisnewtabpage)|
|[HomepageLocation](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=HomepageLocation)|[HomepageLocation](./microsoft-edge-policies.md#homepagelocation)|
|[HSTSPolicyBypassList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=HSTSPolicyBypassList)|[HSTSPolicyBypassList](./microsoft-edge-policies.md#hstspolicybypasslist)|
|[ImagesAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImagesAllowedForUrls)|[ImagesAllowedForUrls](./microsoft-edge-policies.md#imagesallowedforurls)|
|[ImagesBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImagesBlockedForUrls)|[ImagesBlockedForUrls](./microsoft-edge-policies.md#imagesblockedforurls)|
|[ImportAutofillFormData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportAutofillFormData)|[ImportAutofillFormData](./microsoft-edge-policies.md#importautofillformdata)|
|[ImportBookmarks](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportBookmarks)|[ImportFavorites](./microsoft-edge-policies.md#importfavorites)|
|[ImportHistory](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportHistory)|[ImportHistory](./microsoft-edge-policies.md#importhistory)|
|[ImportHomepage](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportHomepage)|[ImportHomepage](./microsoft-edge-policies.md#importhomepage)|
|[ImportSavedPasswords](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportSavedPasswords)|[ImportSavedPasswords](./microsoft-edge-policies.md#importsavedpasswords)|
|[ImportSearchEngine](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ImportSearchEngine)|[ImportSearchEngine](./microsoft-edge-policies.md#importsearchengine)|
|[IncognitoModeAvailability](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=IncognitoModeAvailability)|[InPrivateModeAvailability](./microsoft-edge-policies.md#inprivatemodeavailability)|
|[InsecureContentAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=InsecureContentAllowedForUrls)|[InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls)|
|[InsecureContentBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=InsecureContentBlockedForUrls)|[InsecureContentBlockedForUrls](./microsoft-edge-policies.md#insecurecontentblockedforurls)|
|[IsolateOrigins](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=IsolateOrigins)|[IsolateOrigins](./microsoft-edge-policies.md#isolateorigins)|
|[JavaScriptAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=JavaScriptAllowedForUrls)|[JavaScriptAllowedForUrls](./microsoft-edge-policies.md#javascriptallowedforurls)|
|[JavaScriptBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=JavaScriptBlockedForUrls)|[JavaScriptBlockedForUrls](./microsoft-edge-policies.md#javascriptblockedforurls)|
|[LegacySameSiteCookieBehaviorEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=LegacySameSiteCookieBehaviorEnabled)|[LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled)|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=LegacySameSiteCookieBehaviorEnabledForDomainList)|[LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist)|
|[LocalDiscoveryEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=LocalDiscoveryEnabled)|Non applicable|
|[ManagedBookmarks](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ManagedBookmarks)|[ManagedFavorites](./microsoft-edge-policies.md#managedfavorites)|
|[MaxConnectionsPerProxy](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=MaxConnectionsPerProxy)|[MaxConnectionsPerProxy](./microsoft-edge-policies.md#maxconnectionsperproxy)|
|[MaxInvalidationFetchDelay](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=MaxInvalidationFetchDelay)|Non applicable|
|[MediaRouterCastAllowAllIPs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=MediaRouterCastAllowAllIPs)|[MediaRouterCastAllowAllIPs](./microsoft-edge-policies.md#mediaroutercastallowallips)|
|[MetricsReportingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=MetricsReportingEnabled)|[MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled)|
|[NativeMessagingBlacklist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NativeMessagingBlacklist)|[NativeMessagingBlocklist](./microsoft-edge-policies.md#nativemessagingblocklist)|
|[NativeMessagingUserLevelHosts](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NativeMessagingUserLevelHosts)|[NativeMessagingUserLevelHosts](./microsoft-edge-policies.md#nativemessaginguserlevelhosts)|
|[NativeMessagingWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NativeMessagingWhitelist)|[NativeMessagingAllowlist](./microsoft-edge-policies.md#nativemessagingallowlist)|
|[NetworkPredictionOptions](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NetworkPredictionOptions)|[NetworkPredictionOptions](./microsoft-edge-policies.md#networkpredictionoptions)|
|[NewTabPageLocation](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NewTabPageLocation)|[NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation)|
|[NotificationsAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NotificationsAllowedForUrls)|[NotificationsAllowedForUrls](./microsoft-edge-policies.md#notificationsallowedforurls)|
|[NotificationsBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NotificationsBlockedForUrls)|[NotificationsBlockedForUrls](./microsoft-edge-policies.md#notificationsblockedforurls)|
|[NtlmV2Enabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NtlmV2Enabled)|[NtlmV2Enabled](./microsoft-edge-policies.md#ntlmv2enabled)|
|[NTPCustomBackgroundEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=NTPCustomBackgroundEnabled)|Non applicable|
|[OverrideSecurityRestrictionsOnInsecureOrigin](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=OverrideSecurityRestrictionsOnInsecureOrigin)|[OverrideSecurityRestrictionsOnInsecureOrigin](./microsoft-edge-policies.md#overridesecurityrestrictionsoninsecureorigin)|
|[PasswordLeakDetectionEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PasswordLeakDetectionEnabled)|Non applicable|
|[PasswordManagerEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PasswordManagerEnabled)|[PasswordManagerEnabled](./microsoft-edge-policies.md#passwordmanagerenabled)|
|[PasswordProtectionChangePasswordURL](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PasswordProtectionChangePasswordURL)|[PasswordProtectionChangePasswordURL](./microsoft-edge-policies.md#passwordprotectionchangepasswordurl)|
|[PasswordProtectionLoginURLs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PasswordProtectionLoginURLs)|[PasswordProtectionLoginURLs](./microsoft-edge-policies.md#passwordprotectionloginurls)|
|[PasswordProtectionWarningTrigger](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PasswordProtectionWarningTrigger)|[PasswordProtectionWarningTrigger](./microsoft-edge-policies.md#passwordprotectionwarningtrigger)|
|[PaymentMethodQueryEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PaymentMethodQueryEnabled)|[PaymentMethodQueryEnabled](./microsoft-edge-policies.md#paymentmethodqueryenabled)|
|[PluginsAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PluginsAllowedForUrls)|[PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls)|
|[PluginsBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PluginsBlockedForUrls)|[PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls)|
|[PolicyAtomicGroupsEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PolicyAtomicGroupsEnabled)|Non applicable|
|[PolicyDictionaryMultipleSourceMergeList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PolicyDictionaryMultipleSourceMergeList)|Non applicable|
|[PolicyListMultipleSourceMergeList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PolicyListMultipleSourceMergeList)|Non applicable|
|[PolicyRefreshRate](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PolicyRefreshRate)|Non applicable|
|[PopupsAllowedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PopupsAllowedForUrls)|[PopupsAllowedForUrls](./microsoft-edge-policies.md#popupsallowedforurls)|
|[PopupsBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PopupsBlockedForUrls)|[PopupsBlockedForUrls](./microsoft-edge-policies.md#popupsblockedforurls)|
|[PrinterTypeDenyList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrinterTypeDenyList)|Non applicable|
|[PrintHeaderFooter](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrintHeaderFooter)|[PrintHeaderFooter](./microsoft-edge-policies.md#printheaderfooter)|
|[PrintingAllowedBackgroundGraphicsModes](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrintingAllowedBackgroundGraphicsModes)|Non applicable|
|[PrintingBackgroundGraphicsDefault](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrintingBackgroundGraphicsDefault)|Non applicable|
|[PrintingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrintingEnabled)|[PrintingEnabled](./microsoft-edge-policies.md#printingenabled)|
|[PrintPreviewUseSystemDefaultPrinter](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PrintPreviewUseSystemDefaultPrinter)|[PrintPreviewUseSystemDefaultPrinter](./microsoft-edge-policies.md#printpreviewusesystemdefaultprinter)|
|[PromotionalTabsEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PromotionalTabsEnabled)|[PromotionalTabsEnabled](./microsoft-edge-policies.md#promotionaltabsenabled)|
|[PromptForDownloadLocation](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=PromptForDownloadLocation)|[PromptForDownloadLocation](./microsoft-edge-policies.md#promptfordownloadlocation)|
|[ProxyBypassList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ProxyBypassList)|[ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist)|
|[ProxyMode](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ProxyMode)|[ProxyMode](./microsoft-edge-policies.md#proxymode)|
|[ProxyPacUrl](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ProxyPacUrl)|[ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl)|
|[ProxyServer](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ProxyServer)|[ProxyServer](./microsoft-edge-policies.md#proxyserver)|
|[ProxySettings](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ProxySettings)|[ProxySettings](./microsoft-edge-policies.md#proxysettings)|
|[QuicAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=QuicAllowed)|[QuicAllowed](./microsoft-edge-policies.md#quicallowed)|
|[RegisteredProtocolHandlers](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RegisteredProtocolHandlers)|[RegisteredProtocolHandlers](./microsoft-edge-policies.md#registeredprotocolhandlers)|
|[RelaunchNotification](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RelaunchNotification)|[RelaunchNotification](./microsoft-edge-policies.md#relaunchnotification)|
|[RelaunchNotificationPeriod](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RelaunchNotificationPeriod)|[RelaunchNotificationPeriod](./microsoft-edge-policies.md#relaunchnotificationperiod)|
|[RemoteAccessHostAllowClientPairing](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostAllowClientPairing)|Non applicable|
|[RemoteAccessHostAllowFileTransfer](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostAllowFileTransfer)|Non applicable|
|[RemoteAccessHostAllowGnubbyAuth](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostAllowGnubbyAuth)|Non applicable|
|[RemoteAccessHostAllowRelayedConnection](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostAllowRelayedConnection)|Non applicable|
|[RemoteAccessHostAllowUiAccessForRemoteAssistance](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostAllowUiAccessForRemoteAssistance)|Non applicable|
|[RemoteAccessHostClientDomainList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostClientDomainList)|Non applicable|
|[RemoteAccessHostDomainList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostDomainList)|Non applicable|
|[RemoteAccessHostFirewallTraversal](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostFirewallTraversal)|Non applicable|
|[RemoteAccessHostMatchUsername](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostMatchUsername)|Non applicable|
|[RemoteAccessHostRequireCurtain](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostRequireCurtain)|Non applicable|
|[RemoteAccessHostTalkGadgetPrefix](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostTalkGadgetPrefix)|Non applicable|
|[RemoteAccessHostTokenUrl](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostTokenUrl)|Non applicable|
|[RemoteAccessHostTokenValidationCertificateIssuer](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostTokenValidationCertificateIssuer)|Non applicable|
|[RemoteAccessHostTokenValidationUrl](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostTokenValidationUrl)|Non applicable|
|[RemoteAccessHostUdpPortRange](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RemoteAccessHostUdpPortRange)|Non applicable|
|[RendererCodeIntegrityEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RendererCodeIntegrityEnabled)|[RendererCodeIntegrityEnabled](./microsoft-edge-policies.md#renderercodeintegrityenabled)|
|[ReportExtensionsAndPluginsData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportExtensionsAndPluginsData)|Non applicable|
|[ReportMachineIDData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportMachineIDData)|Non applicable|
|[ReportPolicyData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportPolicyData)|Non applicable|
|[ReportSafeBrowsingData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportSafeBrowsingData)|Non applicable|
|[ReportUserIDData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportUserIDData)|Non applicable|
|[ReportVersionData](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ReportVersionData)|Non applicable|
|[RequireOnlineRevocationChecksForLocalAnchors](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RequireOnlineRevocationChecksForLocalAnchors)|[RequireOnlineRevocationChecksForLocalAnchors](./microsoft-edge-policies.md#requireonlinerevocationchecksforlocalanchors)|
|[RestoreOnStartup](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RestoreOnStartup)|[RestoreOnStartup](./microsoft-edge-policies.md#restoreonstartup)|
|[RestoreOnStartupURLs](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RestoreOnStartupURLs)|[RestoreOnStartupURLs](./microsoft-edge-policies.md#restoreonstartupurls)|
|[RestrictSigninToPattern](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RestrictSigninToPattern)|[RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern)|
|[RoamingProfileLocation](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RoamingProfileLocation)|Non applicable|
|[RoamingProfileSupportEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RoamingProfileSupportEnabled)|Non applicable|
|[RunAllFlashInAllowMode](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=RunAllFlashInAllowMode)|[RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode)|
|[SafeBrowsingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SafeBrowsingEnabled)|[SmartScreenEnabled](./microsoft-edge-policies.md#smartscreenenabled)|
|[SafeBrowsingExtendedReportingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SafeBrowsingExtendedReportingEnabled)|Non applicable|
|[SafeBrowsingForTrustedSourcesEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SafeBrowsingForTrustedSourcesEnabled)|[SmartScreenForTrustedDownloadsEnabled](./microsoft-edge-policies.md#smartscreenfortrusteddownloadsenabled)|
|[SafeBrowsingWhitelistDomains](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SafeBrowsingWhitelistDomains)|[SmartScreenAllowListDomains](./microsoft-edge-policies.md#smartscreenallowlistdomains)|
|[SafeSitesFilterBehavior](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SafeSitesFilterBehavior)|Non applicable|
|[SavingBrowserHistoryDisabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SavingBrowserHistoryDisabled)|[SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled)|
|[SearchSuggestEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SearchSuggestEnabled)|[SearchSuggestEnabled](./microsoft-edge-policies.md#searchsuggestenabled)|
|[SecurityKeyPermitAttestation](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SecurityKeyPermitAttestation)|[SecurityKeyPermitAttestation](./microsoft-edge-policies.md#securitykeypermitattestation)|
|[SendFilesForMalwareCheck](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SendFilesForMalwareCheck)|Non applicable|
|[SharedClipboardEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SharedClipboardEnabled)|Non applicable|
|[ShowAppsShortcutInBookmarkBar](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ShowAppsShortcutInBookmarkBar)|[ShowOfficeShortcutInFavoritesBar](./microsoft-edge-policies.md#showofficeshortcutinfavoritesbar)|
|[ShowCastIconInToolbar](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ShowCastIconInToolbar)|[ShowCastIconInToolbar](./microsoft-edge-policies.md#showcasticonintoolbar)|
|[ShowHomeButton](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ShowHomeButton)|[ShowHomeButton](./microsoft-edge-policies.md#showhomebutton)|
|[SignedHTTPExchangeEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SignedHTTPExchangeEnabled)|[SignedHTTPExchangeEnabled](./microsoft-edge-policies.md#signedhttpexchangeenabled)|
|[SitePerProcess](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SitePerProcess)|[SitePerProcess](./microsoft-edge-policies.md#siteperprocess)|
|[SpellcheckEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SpellcheckEnabled)|[SpellcheckEnabled](./microsoft-edge-policies.md#spellcheckenabled)|
|[SpellcheckLanguage](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SpellcheckLanguage)|[SpellcheckLanguage](./microsoft-edge-policies.md#spellchecklanguage)|
|[SpellcheckLanguageBlacklist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SpellcheckLanguageBlacklist)|[SpellcheckLanguageBlocklist](./microsoft-edge-policies.md#spellchecklanguageblocklist)|
|[SpellCheckServiceEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SpellCheckServiceEnabled)|Non applicable|
|[SSLErrorOverrideAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SSLErrorOverrideAllowed)|[SSLErrorOverrideAllowed](./microsoft-edge-policies.md#sslerroroverrideallowed)|
|[SSLVersionMin](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SSLVersionMin)|[SSLVersionMin](./microsoft-edge-policies.md#sslversionmin)|
|[StricterMixedContentTreatmentEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=StricterMixedContentTreatmentEnabled)|Non applicable|
|[SuppressUnsupportedOSWarning](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SuppressUnsupportedOSWarning)|[SuppressUnsupportedOSWarning](./microsoft-edge-policies.md#suppressunsupportedoswarning)|
|[SyncDisabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SyncDisabled)|[SyncDisabled](./microsoft-edge-policies.md#syncdisabled)|
|[SyncTypesListDisabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=SyncTypesListDisabled)|Non applicable|
|[TabFreezingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=TabFreezingEnabled)|[TabFreezingEnabled](./microsoft-edge-policies.md#tabfreezingenabled)|
|[TaskManagerEndProcessEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=TaskManagerEndProcessEnabled)|[TaskManagerEndProcessEnabled](./microsoft-edge-policies.md#taskmanagerendprocessenabled)|
|[ThirdPartyBlockingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ThirdPartyBlockingEnabled)|Non applicable|
|[TLS13HardeningForLocalAnchorsEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=TLS13HardeningForLocalAnchorsEnabled)|Non applicable|
|[TotalMemoryLimitMb](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=TotalMemoryLimitMb)|[TotalMemoryLimitMb](./microsoft-edge-policies.md#totalmemorylimitmb)|
|[TranslateEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=TranslateEnabled)|[TranslateEnabled](./microsoft-edge-policies.md#translateenabled)|
|[UnsafeEventsReportingEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=UnsafeEventsReportingEnabled)|Non applicable|
|[URLBlacklist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=URLBlacklist)|[URLBlocklist](./microsoft-edge-policies.md#urlblocklist)|
|[UrlKeyedAnonymizedDataCollectionEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=UrlKeyedAnonymizedDataCollectionEnabled)|Non applicable|
|[URLsToCheckComplianceOfDownloadedContent](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=URLsToCheckComplianceOfDownloadedContent)|Non applicable|
|[URLsToCheckForMalwareOfUploadedContent](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=URLsToCheckForMalwareOfUploadedContent)|Non applicable|
|[URLsToNotCheckComplianceOfUploadedContent](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=URLsToNotCheckComplianceOfUploadedContent)|Non applicable|
|[URLWhitelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=URLWhitelist)|[URLAllowlist](./microsoft-edge-policies.md#urlallowlist)|
|[UserDataDir](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=UserDataDir)|[UserDataDir](./microsoft-edge-policies.md#userdatadir)|
|[UserFeedbackAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=UserFeedbackAllowed)|[UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed)|
|[VariationsRestrictParameter](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=VariationsRestrictParameter)|Non applicable|
|[VideoCaptureAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=VideoCaptureAllowed)|[VideoCaptureAllowed](./microsoft-edge-policies.md#videocaptureallowed)|
|[VideoCaptureAllowedUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=VideoCaptureAllowedUrls)|[VideoCaptureAllowedUrls](./microsoft-edge-policies.md#videocaptureallowedurls)|
|[WebAppInstallForceList](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebAppInstallForceList)|[WebAppInstallForceList](./microsoft-edge-policies.md#webappinstallforcelist)|
|[WebComponentsV0Enabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebComponentsV0Enabled)|[WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled)|
|[WebRtcEventLogCollectionAllowed](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebRtcEventLogCollectionAllowed)|Non applicable|
|[WebRtcLocalIpsAllowedUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebRtcLocalIpsAllowedUrls)|[WebRtcLocalIpsAllowedUrls](./microsoft-edge-policies.md#webrtclocalipsallowedurls)|
|[WebRtcUdpPortRange](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebRtcUdpPortRange)|[WebRtcUdpPortRange](./microsoft-edge-policies.md#webrtcudpportrange)|
|[WebUsbAllowDevicesForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebUsbAllowDevicesForUrls)|[WebUsbAllowDevicesForUrls](./microsoft-edge-policies.md#webusballowdevicesforurls)|
|[WebUsbAskForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebUsbAskForUrls)|[WebUsbAskForUrls](./microsoft-edge-policies.md#webusbaskforurls)|
|[WebUsbBlockedForUrls](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WebUsbBlockedForUrls)|[WebUsbBlockedForUrls](./microsoft-edge-policies.md#webusbblockedforurls)|
|[WPADQuickCheckEnabled](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=WPADQuickCheckEnabled)|[WPADQuickCheckEnabled](./microsoft-edge-policies.md#wpadquickcheckenabled)|

## <a name="see-also"></a>Voir également

- [Page d’accueil MicrosoftEdge Entreprise](https://aka.ms/EdgeEnterprise)
- [Configuration de MicrosoftEdge](configure-microsoft-edge.md)
- [Référence de stratégie du navigateur](microsoft-edge-policies.md)