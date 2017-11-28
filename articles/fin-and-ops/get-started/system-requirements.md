---
title: "Kerfiskröfur fyrir uppsetningu í skýi"
description: "Í þessu efnisatriði er listi yfir kerfiskröfur fyrir núverandi útgáfu Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, fyrir uppsetningar skýs."
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 83637b4b2ccc01950e68569b3b8bee1a7cd69855
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="system-requirements-for-cloud-deployments"></a>Kerfiskröfur fyrir uppsetningu í skýi

[!include[banner](../includes/banner.md)]

Í þessu efnisatriði er listi yfir kerfiskröfur fyrir núverandi útgáfu Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, fyrir uppsetningar skýs. Áður en Finance and Operations er sett upp skal, þegar viðeigandi, tryggja að kerfið sem verið er að vinna með uppfylli eða fari fram úr lágmarks kröfum um net, vél- og hugbúnað.

## <a name="supported-web-browsers"></a>Studdir vafrar
Vefforritið getur keyrt í eftirfarandi vöfrum sem keyra á tilgreindum stýrikerfum:

-   Microsoft Edge (nýjasta almenna útgáfa) á Windows-10
-   Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7
-   Google Chrome (nýjasta almenna útgáfa) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölva
-   Apple Safari (nýjasta almenna útgáfa) á Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) 10.12 (Sierra) eða Apple iPad

Farið á vefsvæði hugbúnaðarframleiðandans til að finna nýjustu útgáfu hvers vafra. 

> [!NOTE]
> -   Þú verður að setja upp prufuútgáfu af Chrome viðauka til að virkja Verkskráningu til að sækja skjámyndir og hafa þær með í Microsoft Word skjölum sem eru búin til. <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> -   Verkflæðisritillinn er ræstur sem ClickOnce-forrit. Aðeins Edge Microsoft og Internet Explorer (á studdri útgáfu af Microsoft Windows) styðja ClickOnce forrit. Verkflæðisritillinn í ClickOnce-hugbúnaðurinn krefst á 64-bita samhæfðs stýrikerfis.
> -   Hönnunarviðmót fyrir fjárhagsskýrslugerð er ræst sem ClickOnce forritsins. Það krefst á 64-bita samhæfðs stýrikerfis. Ef verið er að nota Chrome, verður að setja upp ClickOnce viðauka til að sækja skýrslu hönnuður biðlara. Ef verið er að nota Chrome með nafnlausum afhendingarmáta, skal ganga úr skugga um að ClickOnce viðaukanum verður einnig virkur fyrir nafnlausan ham.
> -   Til að forskoða PDF-skrár er mælt með því að notaðir séu vafrar eins og Microsoft Edge (nýjasta tiltæka útgáfa fyrir almenning) Windows 10 eða Google Chorme (nýjasta tiltæka útgáfa fyrir almenning) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölvu.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Studdir vafrar fyrir sölustað smásöluskýs

Retail Cloud POS getur keyrt í eftirfarandi vöfrum sem keyra á tilgreindum stýrikerfum:

-   Microsoft Edge (nýjasta almenna útgáfa) á Windows-10
-   Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7
-   Chrome (síðustu almennu útgáfu) á Windows 10, Windows 8.1 eða Windows 7

## <a name="network-requirements"></a>Netþarfir
-   Finance and Operations er hannað fyrir net með biðtíma upp á 250–300 millisekúndum (ms.) eða minna. Þetta er biðtími frá vafra biðlara til Microsoft Azure gagnamiðstöðvar sem hýsir Finance and Operations. Mælt er með er prófað biðtíma á netinu á <http://www.azurespeed.com>.
-   Bandvíddarkröfur fyrir Finance and Operations fara eftir aðstæðum. Flestar dæmigerðar aðstæður krefjast bandvíddar yfir meira en 50 kílóbætum á sekúndu (KBps). Hins vegar fyrir aðstæður sem hafa miklar farmþarfir, eins og aðstæður sem fela í sér vinnusvæði eða yfirgripsmikil sérsnið, er mælt með fleiri bandvíddum.

Almennt séð, er Finance and Operations bestuð fyrir Internetið. Fjöldi ferða fram og til baka frá biðlara vafra til Azure gagnamiðstöð er mjög lítill og allt farmur þjöppuð. 

> [!WARNING]
> Ekki reikna þarfir bandvídd frá staðsetningu biðlara með því að margfalda notendur eftir þörfum lágmarksbandvíddar. Samtímanotkun á tiltekinni staðsetningu er mjög erfitt að reikna út. Viðskiptavinir sem hafa áhyggjur af bandvíddaþörf ættu að nota sýnisútgáfa af Finance and Operations.

## <a name="net-framework-requirements"></a>.NET Framework þarfir
Finance and Operations krefst Microsoft .NET Framework útgáfu 4.6.2 fyrir öll ClickOnce forrit, eins og leiðarmiðlara skjals. Sjá leiðbeiningar með uppsetningu, [Uppsetningu .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Studd forrit Microsoft Office
Eftirfarandi forrit Microsoft Office eru studd í skýi og innanhúsnýtingu Finance and Operations:

-   Til að nota Office-innbætur fyrir Microsoft Excel og Word verður Microsoft Office 2016 fyrir Windows eða Mac að vera uppsett. Sjá frekari upplýsingar um þarfir útgáfu [Office samþættingu úrræðaleit](../../dev-itpro/office-integration/office-integration-troubleshooting.md).
-   Til að skoða skjöl sem eru myndaðar Út í Excel- eða Útflutnings í Word virkni, sem verður að hafa Microsoft Office 2007 eða sett upp síðar.

## <a name="retail-modern-pos-requirements"></a>Þarfir Retail Modern POS

> [!NOTE]
> Ef Modern POS Smásala mun nota ótengdan gagnagrunn, verður tölvan að uppfylla öll kerfisskilyrði fyrir Microsoft SQL Server. Gagnagrunnur fyrir Retail Modern POS mun virka á Microsoft SQL Server 2012 með Þjónustupakka 3 eða nýrri, Microsoft SQL Server 2014 með Þjónustupakka 2 eða nýrri, og Microsoft SQL Server 2016. Við mælum með því að þú notir ávalt nýjustu fáanlegu útgáfu og að þú setjir upp alla nýjustu þjónustupakkana.

### <a name="supported-operating-systems"></a>Studd stýrikerfi

-   Retail Modern POS er 32-bita hugbúnaður en hún mun keyra á x86 og x64 hönnun.
-   Retail Modern POS er aðeins studd í útgáfum Windows 10 Pro, Enterprise og Enterprise Long Term Servicing Branch (LTSB).

### <a name="minimum-system-requirements"></a>Lágmarksþörf kerfis

-   Lágmarks studd lausn er 1280 × 1024.
-   Í tölvu sem keyrir Retail Modern POS á verður að uppfylla þær þarfir:

    -   Það verður að hafa, lágmarki tvískiptur kjarnauppsetning gjörva sem keyrir á minna en 2 gigahertz (GHz).
    -   Hún verður að hafa, að lágmarki, 3 gígabæt (GB) af RAM.
    -   Hún verður að hafa aðgang á Internetinu.

## <a name="retail-hardware-station-requirements"></a>Kjarnapakki fyrir Retail Hardware Station.
### <a name="supported-operating-systems"></a>Studd stýrikerfi

-   Retail Hardware Station er 32-bita hugbúnaður, en hún mun keyra á x86 og x64 hönnun.
-   Retail Hardware Station er stutt á eftirfarandi stýrikerfum:

    -   Windows 7 Professional, Enterprise og Embedded editions 
    
        > [!NOTE]
        > Windows 7 er eingöngu stutt ef Internet Explorer 11 er uppsett handvirkt í kerfinu.

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

-   Tengillinn fyrir Microsoft Dynamics AX er með tvö mismunandi uppsetningarforrit, eitt fyrir Async Server Connector service og annað fyrir Real-time service for Dynamics AX 2012 R3.
-   Báðir íhlutir eru 32-bita hugbúnaður, en munu keyra bæði á x86 og x64 hönnun.
-   Bæði íhlutir eru studdir stýrikerfi eftirfarandi:

    -   Windows 7 Professional, Enterprise og Embedded editions
    -   Windows 8.1 Update 1 Professional Enterprise og Embedded editions
    -   Windows 10 Pro Enterprise og Enterprise LTSB editions
    -   Microsoft Windows Server 2012 R2 og Microsoft Windows Server 2016

### <a name="minimum-system-requirements"></a>Lágmarksþörf kerfis
-   2 GB af RAM (Mælt er með 4 GB af RAM.)
-   1.6 GHz ferðatímabilinu CPU hraða á kjarnauppsetning (kjarna Tvær eru lágmarks.)
-   Að minnsta kosti 10 GB af lausu rými (gagnagrunnur rásar getur þurft mikið rými.)

## <a name="requirements-for-development-on-local-vms"></a>Kröfur til þróunar á staðbundna VMs
Sjá upplýsingar um þarfir fyrir þróun á staðbundna hýsilsheiti vélar (VMs) [VL keyrslu á verslunarsvæðis](../../dev-itpro/dev-tools/access-instances.md).


## <a name="see-also"></a>Sjá einnig

[Sækja um mat afrit af Dynamics 365 til Fjármála og Aðgerðir Enterprise edition](../../dev-itpro/dev-tools/get-evaluation-copy.md)

