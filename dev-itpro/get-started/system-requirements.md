---
title: "Kerfiskröfur"
description: "Í þessu efnisatriði er listi yfir kerfiskröfur fyrir núverandi útgáfu Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 724ee7ec29f8a9c4e8cc0b244193cd6c83c37f03
ms.contentlocale: is-is
ms.lasthandoff: 06/13/2017


---

# <a name="system-requirements"></a>Kerfiskröfur

[!include[banner](../includes/banner.md)]


Í þessu efnisatriði er listi yfir kerfiskröfur fyrir núverandi útgáfu Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

<a name="supported-web-browsers"></a>Studdir vafrar
----------------------

Vefforritið getur keyrt í eftirfarandi vöfrum sem keyra á tilgreindum stýrikerfum:

-   Microsoft Edge (nýjasta almenna útgáfa) á Windows-10
-   Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7
-   Google Chrome (nýjasta almenna útgáfa) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölva
-   Apple Safari (nýjasta almenna útgáfa) á Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) 10.12 (Sierra) eða Apple iPad

Farið á vefsvæði hugbúnaðarframleiðandans til að finna nýjustu útgáfu hvers vafra. 

**Athugasemdir :**

-   Í prufuútgáfa Króm nafnauka verður sett upp til þess að leyfa screenshot myndir að vera áfram með Verkskráningu og í myndaðri skjöl í Microsoft Word. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
-   Verkflæðisritillinn er ræstur sem ClickOnce-forrit. Aðeins Edge Microsoft og Internet Explorer (á studdri útgáfu af Microsoft Windows) styðja ClickOnce forrit. Verkflæðisritlinum ClickOnce hugbúnaðurinn krefst á 64-bita samhæfar stýrikerfi.
-   Hönnunarviðmót fyrir fjárhagsskýrslugerð er ræst sem ClickOnce forritsins. Það krefst 64-bita samhæfs stýrikerfis. Ef verið er að nota Króm, verður að setja upp ClickOnce viðauka til að sækja skýrsluhönnuð biðlara. Ef verið er að nota Króm með nafnlausum afhendingarmáta, ganga úr skugga um að ClickOnce viðaukanum verður einnig virkur fyrir nafnlausan ham.
-   Til að forskoða PDF-skrár er mælt með því að notaðir séu vafrar eins og Microsoft Edge (nýjasta tiltæka útgáfa fyrir almenning) Windows 10 eða Google Chorme (nýjasta tiltæka útgáfa fyrir almenning) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölvu.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Studdir vafrar fyrir sölustað smásöluskýs

Retail Cloud POS getur keyrt í eftirfarandi vöfrum sem keyra á tilgreindum stýrikerfum:

-   Microsoft Edge (nýjasta almenna útgáfa) á Windows-10
-   Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7
-   Chrome (síðustu almennu útgáfu) á Windows 10, Windows 8.1 eða Windows 7

## <a name="network-requirements"></a>Netþarfir
-   Dynamics 365 for Finance and Operations, Enterprise edition er hannað fyrir net með minni biðtíma en 250-300 millisekúndur (ms.). Þetta er biðtími vafra biðlara Microsoft Azure gagnamiðstöðvar sem hýsir Dynamics 365 for Finance and Operations. Mælt er með er prófað biðtíma á netinu á <http://www.azurespeed.com>.
-   Bandvídd fara í því tilfelli. Flestar dæmigerðar aðstæður krefjast bandvíddar yfir meira en 50 kílóbætum á sekúndu (KBps). Hins vegar fyrir aðstæður sem hafa miklar farmþarfir, eins og vinnusvæðin eða aðstæður sem fela í sér upp á yfirgripsmikil sérsnið, er mælt með fleiri bandvíddum.

Almennt séð, er Finance and Operations bestuð fyrir Internetið. Fjöldi ferða frá biðlara vafra Azure gagnamiðstöð eru lágar og allt farmur þjöppuð. 

**Viðvörun:** ekki að reikna þarfir bandvídd staðsetningu biðlara með því að margfalda notendur eftir þörfum lágmarksbandvíddar. Erfitt er að reikna út samtímanotkun á tiltekinni staðsetningu. Nota sýnisútgáfa af Finance and Operations fyrir viðskiptavini sem hafa áhyggjur af bandvíddaþörf.

## <a name="net-framework-requirements"></a>.NET Framework þarfir
.NET framework útgáfu 4.6.2 er nauðsynleg fyrir öll ClickOnce forrit, eins og skjali leiðaraðgerð sölufulltrúa. Sjá leiðbeiningar með uppsetningu, [Uppsetningu .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Studd forrit Microsoft Office
-   Til að nota Office-innbætur fyrir Microsoft Excel og Word verður Microsoft Office 2016 fyrir Windows eða Mac að vera uppsett. Sjá frekari upplýsingar um þarfir útgáfu [Office samþættingu úrræðaleit](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Til að skoða skjöl sem eru myndaðar Út í Excel- eða Útflutnings í Word virkni, sem verður að hafa Microsoft Office 2007 eða sett upp síðar.

## <a name="retail-modern-pos-requirements"></a>Þarfir Retail Modern POS
### <a name="supported-operating-systems"></a>Studd stýrikerfi

-   Retail Modern POS er 32-bita hugbúnaður en hún mun keyra á x86 og x64 hönnun.
-   Retail Modern POS er aðeins studd í útgáfum Windows 10 Pro, Enterprise og Enterprise Long Term Servicing Branch (LTSB).

### <a name="minimum-system-requirements"></a>Lágmarksþörf kerfis

-   Lágmarks studd lausn er 1280 × 1024.
-   Í tölvu sem keyrir Retail Modern POS á verður að uppfylla þær þarfir:
    -   Það verður að hafa, lágmarki tvískiptur kjarnauppsetning gjörva sem keyrir á minna en 2 gigahertz (GHz).
    -   Það verður að hafa, lágmarki 3 gígabæt (GB) af RAM.
    -   Hún verður að hafa aðgang á Internetinu.

## <a name="retail-hardware-station-requirements"></a>Kjarnapakki fyrir Retail Hardware Station.
### <a name="supported-operating-systems"></a>Studd stýrikerfi

-   Retail Hardware Station er 32-bita hugbúnaður, en hún mun keyra á x86 og x64 hönnun.
-   Retail Hardware Station er stutt á eftirfarandi stýrikerfum:
    -   Útgáfur Windows 7 Professional, Enterprise og Ultimate **Athugasemd:** Windows 7 er studd ef Internet Explorer 11 er uppsett handvirkt í kerfinu.
    -   Windows 8.1 Update 1 Professional Enterprise og Embedded editions
    -   Windows 10 Pro Enterprise og Enterprise LTSB editions

### <a name="minimum-system-requirements"></a>Lágmarksþörf kerfis

Tölvan verður að uppfylla alla kerfiskröfur fyrir uppsetningu og notkun eftirfarandi atriða:

-   Internet Upplýsingaþjónusta (IIS)
-   Vélbúnaður þriðja aðila

## <a name="retail-store-scale-unit-requirements"></a>Þarfir fyrir Retail Store Scale Unit
### <a name="supported-operating-systems"></a>Studd stýrikerfi

-   Retail Store Scale Unit er 32-bita hugbúnaður, en hún mun keyra á x86 og x64 hönnun.
-   Retail Store Scale Unit er stutt á eftirfarandi stýrikerfum:
    -   Windows 7 Professional, Enterprise og Embedded editions
    -   Windows 8.1 Update 1 Professional Enterprise og Embedded editions
    -   Windows 10 Pro Enterprise og Enterprise LTSB editions

### <a name="minimum-system-requirements"></a>Lágmarksþörf kerfis

-   4 GB RAM
-   1.6 GHz ferðatímabilinu CPU hraða á kjarnauppsetning (kjarna Tvær eru lágmarks.)
-   Að minnsta kosti 10 GB af lausu rými (gagnagrunnur rásar getur þurft mikið rými.)

### <a name="recommended-system-requirements"></a>Ráðlagðar kerfisþarfir

-   6 GB RAM
-   2.4 GHz i7 (eða jafngildi) ferðatímabilinu CPU hraða á kjarnauppsetning (Fjórum kjarna ráðlagðar.)
-   Að minnsta kosti 10 GB af lausu rými (gagnagrunnur rásar getur þurft mikið rými.)

## <a name="connector-requirements"></a>Kröfur um connector
### <a name="supported-operating-systems"></a>Studd stýrikerfi

-   Connector í Microsoft Dynamics AX hefur tvær aðskildar installers á **þjónustu Þjóns Connector Async** og **rauntíma þjónustu fyrir Dynamics AX 2012 R3**.
-   Bæði íhlutir eru 32 bita forrit en keyrir á x86 og x64 architectures.
-   Bæði íhlutir eru studdir stýrikerfi eftirfarandi:
    -   Windows 7 Professional, Enterprise og Embedded editions
    -   Windows 8.1 Update 1 Professional Enterprise og Embedded editions
    -   Windows 10 Pro Enterprise og Enterprise LTSB editions
    -   Windows Server 2012 R2, Windows Server 2016

### <a name="minimum-system-requirements"></a>Lágmarksþörf kerfis

-   2 GB RAM 4 GB RAM ráðlagt
-   1.6 GHz ferðatímabilinu CPU hraða á kjarnauppsetning (kjarna Tvær eru lágmarks.)
-   Að minnsta kosti 10 GB af lausu rými (gagnagrunnur rásar getur þurft mikið rými.)

## <a name="requirements-for-development-on-local-vms"></a>Kröfur til þróunar á staðbundna VMs
Sjá upplýsingar um þarfir fyrir þróun á staðbundna hýsilsheiti vélar (VMs) [VL keyrslu á verslunarsvæðis](../dev-tools/access-instances.md).

<a name="see-also"></a>Sjá einnig
--------

[Sækja um mat afrit af Dynamics 365 til Fjármála og Aðgerðir Enterprise edition](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)





