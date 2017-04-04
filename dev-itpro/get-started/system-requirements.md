---
title: "Kerfiskröfur"
description: "Þetta efnisatriði telur upp kerfiskröfur gildandi útgáfu af Microsoft Dynamics 365 aðgerða."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 9220c093d3f6d6700127c93651db4083be300311
ms.lasthandoff: 03/31/2017


---

# <a name="system-requirements"></a>Kerfiskröfur

Þetta efnisatriði telur upp kerfiskröfur gildandi útgáfu af Microsoft Dynamics 365 aðgerða.

<a name="supported-web-browsers"></a>Studdir vafrar
----------------------

Microsoft Dynamics 365 fyrir Aðgerðir vefforrit hægt er að keyra í eftirfarandi vafrar sem keyra á tilgreindum stýrikerfi:

-   Microsoft Edge (síðustu krafist tiltæk útgáfa) á Windows-10
-   Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7
-   Google Króm (síðustu útgáfu krafist tiltækar) spjaldtölvunni Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10
-   Apple Safari (síðustu útgáfu sem krafist er tiltækur) í Mac OS X 10,10 (Yosemite), 10.11 (El Capitan) eða 10.12 (Síerra) eða Apple iPad

Farið á vefsvæði hugbúnaðarframleiðandans til að finna nýjustu útgáfu hvers vafra. **Athugasemdir :**

-   Til að sækja myndir sem eru myndaðar úr Verkskráningu og hafa þær með í Microsoft Word skjöl, verður að hafa nafnauka við Króm uppsett. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   Ritill Verkflæðis er hafin sem ClickOnce forritsins. Aðeins Edge Microsoft og Internet Explorer (á studdri útgáfu af Microsoft Windows) styðja ClickOnce umsóknir. Verkflæðisritlinum ClickOnce hugbúnaðurinn krefst á 64-bita samhæfar stýrikerfi.
-   Hönnunarviðmót fyrir fjárhagsskýrslugerð hefst sem ClickOnce forritsins. Það krefst á 64-bita samhæfar stýrikerfi. Ef verið er að nota Króm, verður að setja upp ClickOnce nafnauka til að sækja skýrslu hönnuður biðlara. Ef verið er að nota Króm með incognito afhendingarmáta, ganga úr skugga um að ClickOnce nafnaukanum verður einnig virkur fyrir incognito ham.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Studdir vafrar fyrir sölustað smásöluskýs

Retail POS Skýi fyrir Dynamics 365 fyrir Aðgerðir sem hægt er að keyra í eftirfarandi vafrar sem keyra á tilgreindum stýrikerfi:

-   Microsoft Edge (síðustu krafist tiltæk útgáfa) á Windows-10
-   Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7
-   Króm (síðustu útgáfu krafist tiltækar) á Windows 10, Windows 8.1 eða Windows 7

## <a name="network-requirements"></a>Net-þarfir
-   Dynamics 365 aðgerða er hannaður fyrir net með biðtíma minni en 150 millisekúndum (ms.). Þetta er biðtíma vafra biðlara Microsoft Azure gögn center sem hýsir Dynamics 365 fyrir Aðgerðir. Mælt er með er prófað biðtíma á netinu við <http://www.azurespeed.com>.
-   Við aðstæður bandvídd þarfir fyrir Dynamics 365 aðgerða háð. Flestar dæmigerðar aðstæður krefjast bandvídd yfir meira en 50 kílóbætum á sekúndu (KBps). Hins vegar fyrir aðstæður sem hafa mikla farmur þarfir vinnusvæðin eða aðstæður sem fela í sér upp á yfirgripsmikla sérsnið fleiri bandvídd er mælt með.

Almennt séð, 365 Dynamics aðgerða bestuð fyrir Internetið. Ferðir frá biðlara vafra Azure gagnamiðstöð eru mjög lágar og allt farmur þjöppuð. **Viðvörun:** ekki að reikna þarfir bandvídd staðsetningu biðlara með því að margfalda notendur eftir þörfum lágmarks bandvídd. Samtíma notkun á tiltekinni staðsetningu er mjög erfitt að reikna út. Nota sýnisútgáfa af Dynamics 365 fyrir Aðgerðir fyrir viðskiptavini sem eru angi um þarfir bandvídd.

## <a name="net-framework-requirements"></a>.NET framework þarfir
Dynamics 365 aðgerða krefst .NET Framework útgáfu 4.6.2 fyrir allar smellið-einu sinni forrit, svo skjal leiðaraðgerð fulltrúa. Sjá leiðbeiningar með uppsetningu, [Uppsetningu .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Studd forrit Microsoft Office
-   Til að keyra Microsoft Excel og Word-viðbætur, verður að hafa Microsoft Office 2016 fyrir Windows eða Mac uppsett. Sjá frekari upplýsingar um þarfir útgáfu [Office samþættingu úrræðaleit](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Til að skoða skjöl sem eru myndaðar Út í Excel- eða Útflutnings í Word virkni, sem verður að hafa Microsoft Office 2007 eða sett upp síðar.

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS þarfir
### <a name="supported-operating-systems"></a>Studd stýrikerfi

-   Retail Modern POS er hugbúnaður 32-bita, en hún mun keyra á x86 og x64 architectures.
-   Retail Modern POS er aðeins studd í editions Windows 10 Pro Enterprise og Enterprise Langt Hugtak Viðskiptavinasetri Grein (LTSB).

### <a name="minimum-system-requirements"></a>Lágmarks kerfiskröfur

-   Lágmarks studd lausn er 1280 × 1024.
-   Í tölvu sem keyrir Retail Modern POS á verður að uppfylla þær þarfir:
    -   Það verður að hafa, lágmarki tvískiptur kjarnauppsetning gjörva sem keyrir á minna en 2 gigahertz (GHz).
    -   Það verður að hafa, lágmarki 3 gígabæt (GB) af RAM.
    -   Það verður að hafa aðgang á Internetinu.

## <a name="retail-hardware-station-requirements"></a>Retail hardware station þarfir
### <a name="supported-operating-systems"></a>Studd stýrikerfi

-   Vélbúnaðarstöð smásölu er 32-bita, en hún mun keyra á x86 og x64 architectures.
-   Vélbúnaðarstöð smásölu er stutt á eftirfarandi stýrikerfi:
    -   Windows 7 Professional Enterprise og Endanlegs editions **Athugasemd:** Windows 7 er studd ef Internet Explorer 11 er uppsett handvirkt í kerfinu.
    -   Windows 8.1 Update 1 Professional Enterprise og Embedded editions
    -   Windows 10 Pro Enterprise og Enterprise LTSB editions

### <a name="minimum-system-requirements"></a>Lágmarks kerfiskröfur

Tölvunni verður að uppfylla alla kerfiskröfur fyrir uppsetningu og notkun eftirfarandi atriðum:

-   Internet Upplýsingaþjónusta (IIS)
-   Vélbúnaður þriðja aðila

## <a name="retail-store-scale-unit-requirements"></a>Retail Store Vigt Einingu þarfir
### <a name="supported-operating-systems"></a>Studd stýrikerfi

-   Smásöluverslun Vigt er hugbúnaður 32-bita, en hún mun keyra á x86 og x64 architectures.
-   Smásöluverslun Vigt er studd á eftirfarandi stýrikerfi:
    -   Windows 7 Professional Enterprise og Endanlegs editions
    -   Windows 8.1 Update 1 Professional Enterprise og Embedded editions
    -   Windows 10 Pro Enterprise og Enterprise LTSB editions

### <a name="minimum-system-requirements"></a>Lágmarks kerfiskröfur

-   4 GB RAM
-   1.6 GHz ferðatímabilinu CPU hraða á kjarnauppsetning (kjarna Tvær eru lágmarks.)
-   Að minnsta kosti 10 GB af lausu rými (gagnagrunnur rásar er hægt að krefjast háar pláss.)

### <a name="recommended-system-requirements"></a>Mælt er með kerfiskröfur

-   6 GB RAM
-   2.4 GHz i7 (eða jafngildi) ferðatímabilinu CPU hraða á kjarnauppsetning (Fjórum kjarna ráðlagðar.)
-   Að minnsta kosti 10 GB af lausu rými (gagnagrunnur rásar er hægt að krefjast háar pláss.)

## <a name="requirements-for-development-on-local-vms"></a>Kröfur til þróunar á staðbundna VMs
Sjá upplýsingar um þarfir fyrir þróun á staðbundna hýsilsheiti vélar (VMs) [VL keyrslu á verslunarsvæðis](/dynamics365/operations/dev-itpro/dev-tools/access-instances#vm-that-is-running-in-premises).

<a name="see-also"></a>Sjá einnig
--------

[Sækja við mat á afrit af Dynamics 365 fyrir Aðgerðir](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)


