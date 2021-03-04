---
title: Kerfiskröfur Talent
description: Þetta efnisatriði inniheldur lista yfir kröfur Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 509827d5736887f56e7754a0760af7dea76277f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461503"
---
# <a name="talent-system-requirements"></a>Kerfiskröfur Talent

[!include [banner](includes/banner.md)]

Þetta efnisatriði útskýrir kröfur fyrir Microsoft Dynamics 365 Talent, þ.m.t. Attract og Onboard. Það gefur líka upp löndin og svæðin þar sem Talent er tiltækt, ásamt upplýsingum um tungumál og staðfæringar fyrir gögn Talent. Þetta efnisatriði veitir að auki uppfærsluregluna fyrir Talent.

## <a name="supported-web-browsers"></a>Studdir vafrar

Microsoft Dynamics 365 Talent er hægt að keyra í eftirfarandi vöfrum sem keyra á tilgreindum stýrikerfum: 

*   Microsoft Edge (nýjasta almenna útgáfa) á Windows-10
*   Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7
*   Google Chrome (síðasta almenna útgáfan)
*   Apple Safari (síðasta almenna útgáfan)

Farið á vefsvæði hugbúnaðarframleiðandans til að finna nýjustu útgáfu hvers vafra. 

> [!NOTE]
> * Til að sækja myndir sem eru myndaðar úr Verkskráningu og hafa þær með í Microsoft Word-skjöl, verður að hafa viðauka við Króm uppsett. 
> * Verkflæðisritillinn er ræstur sem ClickOnce-forrit. Aðeins Microsoft Edge og Internet Explorer (á studdri útgáfu af Microsoft Windows) styðja ClickOnce-forrit. Verkflæðisritlinum ClickOnce hugbúnaðurinn krefst á 64-bita samhæfar stýrikerfi.
> * Til að forskoða PDF-skrár er mælt með því að notaðir séu nýjustu vafrarnir eins og Microsoft Edge (nýjasta tiltæka útgáfa fyrir almenning) Windows 10 eða Google Chorme (nýjasta tiltæka útgáfa fyrir almenning) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölvu.
>   Netþarfir
> * Dynamics 365 Talent er hannað fyrir net með biðtíma minni en 250-300 millisekúndum (ms.). Þetta er biðtíma vafra biðlara Microsoft Azure gagnamiðstöðvar sem hýsir Talent. Mælt er með er prófað biðtíma á netinu á [www.azurespeed.com](https://www.azurespeed.com "Azure biðtímapróf").
> * Bandvíddarþarfir fyrir Talent fara eftir aðstæðum. Flestar dæmigerðar aðstæður krefjast bandvíddar yfir meira en 50 kílóbætum á sekúndu (KBps).
> 
> [!WARNING]
> Ekki skal reikna bandvíddarkröfur úr biðlarastaðsetningu með því að margfalda fjölda notenda með lágmarks bandvíddarkröfum. Samtímanotkun á tiltekinni staðsetningu er mjög erfitt að reikna út. Nota sýnisútgáfa af Talent fyrir viðskiptavini sem hafa áhyggjur af bandvíddaþörf.

## <a name="supported-microsoft-office-applications"></a>Studd Microsoft Office forrit

* Til að keyra Microsoft Excel og Word innbætur verður Microsoft Office 2016 fyrir Windows eða Mac að vera uppsett. Sjá frekari upplýsingar um þarfir útgáfu í [Úrrætðaleit samþættingar á Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "Úrræðaleit fyrir Office-samþættingu").
* Til að skoða skjöl sem eru mynduð af virkninni Flytja inn í Excel eða Flytja inn í Word verður að hafa Microsoft Office 2007 eða nýrri útgáfu uppsetta.

## <a name="regional-availability-languages-and-localization"></a>Svæði í boði, tungumál og staðfærsla

Hægt er að hlaða niður PDF skrá yfir lönd, svæði og tungumál sem Talent styður á [Alþjóðlegt framboð á Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability). 

> [!NOTE]
> Á meðan notandaviðmót er staðfært á önnur tungumál eru öll gögn notanda geymd á því tungumáli sem þau voru færð inn á. Hægt er að búa til tölvupósta og sniðmát á öðrum tungumálum, en gögn á borð við upplýsingar um áætlanagerð eru einungis í boði á ensku sem stendur.

Ef þú ert þróunaraðili og hefur áhuga á að búa til lands- eða svæðisbundnar sérstillingar, eða að finna lausnir fyrir land eða svæði sem Microsoft styður ekki sem stendur skaltu skoða [Alþjóðavæðing](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).



[!INCLUDE[footer-include](../includes/footer-banner.md)]