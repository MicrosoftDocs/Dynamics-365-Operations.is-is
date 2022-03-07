---
title: Kerfiskröfur
description: Þetta efnisatriði sýnir kerfiskröfur fyrir Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 15770595a0639c03df1138ec25010ca8168bd9a8
ms.sourcegitcommit: 49f7528d3268abe15e40f719956e1ec8696a6f4e
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/18/2021
ms.locfileid: "7393474"
---
# <a name="system-requirements"></a>Kerfiskröfur

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði sýnir kerfiskröfur fyrir Microsoft Dynamics 365 Human Resources. Það gefur líka upp löndin og svæðin þar sem Human Resources er tiltækt og upplýsingar um tungumál og staðfæringar fyrir gögn Human Resources.

## <a name="supported-web-browsers"></a>Studdir vafrar

Notendur geta opnað Microsoft Dynamics 365 Human Resources með því að nota einhvern af eftirfarandi netvöfrum sem keyra í tilgreindum stýrikerfum: 

*   Microsoft Edge (nýjasta almenna útgáfa) á Windows-10
*   Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7
*   Google Chrome (síðasta almenna útgáfan)
*   Apple Safari (síðasta almenna útgáfan)

Farið á vefsvæði hugbúnaðarframleiðandans til að finna nýjustu útgáfu hvers vafra. 

## <a name="special-considerations"></a>Sérstök umhugunsarefni

* Til að virkja verkskráningu til að sækja skjámyndir og hafa þær með í Microsoft Word skjölum sem eru búin til þarftu að setja upp forútgáfu Chrome-viðbótar.
* Verkflæðisritillinn er ræstur sem ClickOnce-forrit. Aðeins Microsoft Edge og Internet Explorer (á studdri útgáfu af Microsoft Windows) styðja ClickOnce-forrit. Verkflæðisritlinum ClickOnce hugbúnaðurinn krefst á 64-bita samhæfar stýrikerfi.
* Til að forskoða PDF-skrár er mælt með því að notaðir séu nýjustu vafrarnir eins og Microsoft Edge (nýjasta tiltæka útgáfa fyrir almenning) Windows 10 eða Google Chorme (nýjasta tiltæka útgáfa fyrir almenning) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölvu.

## <a name="network-requirements"></a>Netþarfir

* Human Resources er hannað fyrir net með biðtíma minni en 250-300 millisekúndum (ms.). Þetta er biðtíma vafra biðlara Microsoft Azure gagnamiðstöðvar sem hýsir Human Resources. Mælt er með er prófað biðtíma á netinu á [www.azurespeed.com](https://www.azurespeed.com "Azure biðtímapróf").
* Bandvíddarþarfir fyrir Human Resources fara eftir aðstæðum. Dæmigerðar aðstæður krefjast bandvíddar sem er meira en 50 kílóbæti á sekúndu (KBps).
 
> [!WARNING]
> Ekki skal reikna bandvíddarkröfur úr biðlarastaðsetningu með því að margfalda fjölda notenda með lágmarks bandvíddarkröfum. Samtímanotkun á tiltekinni staðsetningu er mjög erfitt að reikna út. Nota sýnisútgáfa af Human Resources fyrir viðskiptavini sem hafa áhyggjur af bandvíddaþörf.

## <a name="supported-microsoft-office-applications"></a>Studd Microsoft Office forrit

* Til að keyra Microsoft Excel og Word innbætur verður Microsoft Office 2016 fyrir Windows eða Mac að vera uppsett. Sjá frekari upplýsingar um þarfir útgáfu í [Úrrætðaleit samþættingar á Office](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Úrræðaleit fyrir Office-samþættingu").
* Til að skoða skjöl sem eru mynduð af virkninni Flytja inn í Excel eða Flytja inn í Word verður að hafa Microsoft Office 2007 eða nýrri útgáfu uppsetta.

## <a name="regional-availability-languages-and-localization"></a>Svæði í boði, tungumál og staðfærsla

Hægt er að hlaða niður PDF skrá yfir lönd, svæði og tungumál sem Human Resources styður á [Alþjóðlegt framboð á Microsoft Dynamics 365](/dynamics365/get-started/availability). 

> [!NOTE]
> Á meðan notandaviðmót er staðfært á önnur tungumál eru öll gögn notanda geymd á því tungumáli sem þau voru færð inn á. Hægt er að búa til tölvupósta og sniðmát á öðrum tungumálum, en gögn á borð við upplýsingar um áætlanagerð eru einungis í boði á ensku sem stendur.

Ef þú ert þróunaraðili og hefur áhuga á að búa til lands- eða svæðisbundnar sérstillingar, eða að finna lausnir fyrir land eða svæði sem Microsoft styður ekki sem stendur skaltu skoða [Alþjóðavæðing](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
