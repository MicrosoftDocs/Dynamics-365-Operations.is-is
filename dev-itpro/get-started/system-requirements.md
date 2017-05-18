---
title: "Kerfiskröfur"
description: "Í þessu efnisatriði er listi yfir kerfiskröfur fyrir núverandi útgáfu Microsoft Dynamics 365 for Operations."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 86053196a3aad6b7b5d7830860e1af347dd969d8
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="system-requirements"></a>Kerfiskröfur

[!include[banner](../includes/banner.md)]


Í þessu efnisatriði er listi yfir kerfiskröfur fyrir núverandi útgáfu Microsoft Dynamics 365 for Operations.

<a name="supported-web-browsers"></a>Studdir vafrar
----------------------

Microsoft Dynamics 365 for Operations vefforrit er hægt að keyra í eftirfarandi vöfrum sem keyra á tilgreindum stýrikerfum:

-   Microsoft Edge (nýjasta almenna útgáfa) á Windows-10
-   Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7
-   Google Chrome (nýjasta almenna útgáfa) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölva
-   Apple Safari (nýjasta almenna útgáfa) á Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) 10.12 (Sierra) eða Apple iPad

Farið á vefsvæði hugbúnaðarframleiðandans til að finna nýjustu útgáfu hvers vafra. **Athugasemdir :**

-   Til að sækja myndir sem eru myndaðar úr Verkskráningu og hafa þær með í Microsoft Word skjöl, verður að hafa viðauka við Króm uppsett. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   Verkflæðisritillinn er ræstur sem ClickOnce-forrit. Aðeins Edge Microsoft og Internet Explorer (á studdri útgáfu af Microsoft Windows) styðja ClickOnce forrit. Verkflæðisritlinum ClickOnce hugbúnaðurinn krefst á 64-bita samhæfar stýrikerfi.
-   Hönnunarviðmót fyrir fjárhagsskýrslugerð er ræst sem ClickOnce forritsins. Það krefst 64-bita samhæfs stýrikerfis. Ef verið er að nota Króm, verður að setja upp ClickOnce viðauka til að sækja skýrslu hönnuður biðlara. Ef verið er að nota Króm með nafnlausum afhendingarmáta, ganga úr skugga um að ClickOnce viðaukanum verður einnig virkur fyrir nafnlausan ham.
-   Til að forskoða PDF-skrár er mælt með því að notaðir séu nýjustu vafrarnir eins og Microsoft Edge (nýjasta tiltæka útgáfa fyrir almenning) Windows 10 eða Google Chorme (nýjasta tiltæka útgáfa fyrir almenning) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölvu.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Studdir vafrar fyrir sölustað smásöluskýs

Sölustað smásöluskýs fyrir Microsoft Dynamics 365 for Operations er hægt að keyra í eftirfarandi vöfrum sem keyra á tilgreindum stýrikerfum:

-   Microsoft Edge (nýjasta almenna útgáfa) á Windows-10
-   Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7
-   Chrome (síðustu almennu útgáfu) á Windows 10, Windows 8.1 eða Windows 7

## <a name="network-requirements"></a>Netþarfir
-   Dynamics 365 for Operations er hannað fyrir net með biðtíma minni en 150 millisekúndum (ms.). Þetta er biðtíma vafra biðlara Microsoft Azure gagnamiðstöðvar sem hýsir Dynamics 365 for Operations. Mælt er með er prófað biðtíma á netinu á <http://www.azurespeed.com>.
-   Bandvíddarþarfir fyrir Dynamics 365 for Operations fara eftir aðstæðum. Flestar dæmigerðar aðstæður krefjast bandvíddar yfir meira en 50 kílóbætum á sekúndu (KBps). Hins vegar fyrir aðstæður sem hafa miklar farmþarfir, eins og vinnusvæðin eða aðstæður sem fela í sér upp á yfirgripsmikil sérsnið, er mælt með fleiri bandvíddum.

Almennt séð, er Dynamics 365 for Operations bestuð fyrir Internetið. Fjöldi ferða frá biðlara vafra Azure gagnamiðstöð eru mjög lágar og allt farmur þjöppuð. **Viðvörun:** ekki að reikna þarfir bandvídd staðsetningu biðlara með því að margfalda notendur eftir þörfum lágmarksbandvíddar. Samtímanotkun á tiltekinni staðsetningu er mjög erfitt að reikna út. Nota sýnisútgáfa af Dynamics 365 for Operations fyrir viðskiptavini sem hafa áhyggjur af bandvíddaþörf.

## <a name="net-framework-requirements"></a>.NET Framework þarfir
Dynamics 365 for Operations krefst .NET Framework útgáfu 4.6.2 fyrir öll eins-smells forrit, eins og skjal leiðaraðgerð fulltrúa. Sjá leiðbeiningar með uppsetningu, [Uppsetningu .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Studd forrit Microsoft Office
-   Til að nota Office-innbætur fyrir Microsoft Excel og Word verður Microsoft Office 2016 fyrir Windows eða Mac að vera uppsett. Sjá frekari upplýsingar um þarfir útgáfu [Office samþættingu úrræðaleit](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
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

## <a name="requirements-for-development-on-local-vms"></a>Kröfur til þróunar á staðbundna VMs
Sjá upplýsingar um þarfir fyrir þróun á staðbundna hýsilsheiti vélar (VMs) [VL keyrslu á verslunarsvæðis](../dev-tools/access-instances.md).

<a name="see-also"></a>Sjá einnig
--------

[Sækja við mat á afrit af Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)




