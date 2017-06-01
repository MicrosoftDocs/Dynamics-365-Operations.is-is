---
title: "Birgðir á lager eftir fartækjavinnusvæði"
description: "Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið birgðir á lager sem er tiltækt fyrir Microsoft Dynamics 365 for Operations farsímaforritið. Þetta vinnusvæði hjálpar þér að fá yfirsýn gegnum fartæki yfir pantaðar og tiltækar birgðir, hvar og hvenær sem er."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7387df37e047d5ab7a90b696a6ffa249094499c4
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-on-hand-mobile-workspace"></a>Birgðir á lager eftir fartækjavinnusvæði

[!include[banner](../includes/banner.md)]


Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið birgðir á lager sem er tiltækt fyrir Microsoft Dynamics 365 for Operations farsímaforritið. Þetta vinnusvæði hjálpar þér að fá yfirsýn gegnum fartæki yfir pantaðar og tiltækar birgðir, hvar og hvenær sem er.

<a name="overview-of-the-inventory-on-hand-mobile-workspace"></a>Yfirlit yfir fartækjavinnusvæðið birgðir á lager
--------------------------------------------------

Yfirleitt eru fyrirtæki með margar sendingar og margar vörumóttökur á degi hverjum. Slíkar hreyfingar breyta birgðastöðu á lager sífellt. Fartækjavinnusvæðið **Birgðir á lager** gerir þér kleift að sjá birgðastöðu á lager þvert á fyrirtæki og fá nýjasta yfirlit yfir birgðastöðugögn á fartækinu sem þú vilt helst nota. Hvort sem þú vinnur í vöruhúsi, í innkaupum, sölu, framleiðslu eða stjórnun eða hefur önnur hlutverk getur þú fengið yfirlit yfir birgðastöðu á lager hvar og hvenær sem er. 

Fartækjavinnusvæði veitir fljótlegt yfirlit yfir birgðastöðu þvert á svæði. Það veitir yfirlit yfir birgðastöðu á lager þvert á fyrritæki, núverandi efnislegar frátektir og óbókaðar birgðir á lager. Þú getur einnig fært inn vörunúmer til að spyrjast fyrir um birgðastöðu á lager og framkvæmt síaða leit að afurðum eða tilbrigðum eftir birgðastöðu á lager. 

Fartækjavinnusvæði tryggir einkum eftirfarandi eiginleika:

-   Leit eftir vörunúmeri eða vöruheiti til að finna afurðir til að skoða birgðastöðu á lager fyrir þær vörur.

-   Hægt er að skoða eftirfarandi upplýsingar fyrir valdar vörur:
    -   Birgðastaða á lager eftir svæðum
    -   Birgðastaða á lager eftir vöruhúsum
    -   Birgðastaða á lager eftir staðsetningu
    -   Birgðastaða á lager eftir runum (fyrir runustýrðar vörur)
    -   Birgðastaða á lager eftir birgðastöðu
    
-   Birgðastaða á lager fyrir vörur er sýnd með eftirfarandi hætti:
    -   Eftir efnislegum birgðum (Þetta yfirlit táknar heildarmagn).
    -   Eftir efnislegum frátektum (Þetta yfirlit táknar frátekið magn).
    -   Eftir efnislegu vörum sem eru tiltækar (þetta yfirlit táknar tiltækt magn sem ekki er bókað).

## <a name="prerequisites"></a>Frumskilyrði
Áður en hægt er að nota í **Birgðir á lager** fartækjavinnusvæðið skal ganga úr skugga um að kerfisstjórinn hafi eftirfarandi forsendur í stað.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Skilyrði</th>
<th>Hlutverk</th>
<th>lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Verður að innleiða Microsoft Dynamics 365 útgáfu 1611 með svæðisuppfærslu 3 eða síðar.</td>
<td>Kerfisstjóri</td>
<td>Ef ekki er þegar Dynamics 365 for Operations starfrækt í fyrirtækinu, skal kerfisstjóri sjá <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Deploy Microsoft Dynamics 365 fyrir Operations sýnigögn prófunarumhverfi</a>.</td>
</tr>
<tr class="even">
<td>KB 4013633 verður að vera innleitt.</td>
<td>Kerfisstjóri</td>
<td>KB 4013633 (X++ uppfærsla eða lýsigögn bráðabót) inniheldur fjögur fartækjavinnusvæði fyrir afgangakeðju stjórnun. Til að setja upp KB 4013633 verður kerfisstjóri að fylgja eftirfarandi skrefum:
<ol>
<li>Sækja KB 4013633 af Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Setja upp bráðabót lýsigagna</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Stofna virkjanlegan pakka</a> sem inniheldur <strong>SCMMobile</strong> líkanið og hlaða síðan virkjanlega pakkann í LCS.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Setja virkjanlega pakkann</a> í þitt Microsoft Dynamics 365 fyrir Operations kerfið.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>Birgðir á lager</strong> fartækjavinnusvæðið verður að vera birt í Dynamics 365 for Operations farsímaforritinu.</td>
<td>Kerfisstjóri</td>
<td><ol>
<li>Opnaðu Dynamics 365 fyrir Operations í vafranum þínum.</li>
<li>Á <strong>kerfisfæribreytum</strong> síðunni, veljið <strong>Stjórna fartækja vinnusvæði</strong>.</li>
<li>Veldu vinnusvæðið <strong>Lagerbirgðir</strong>.</li>
<li>Klikkaðu á <strong>Birta fartækjavinnusvæði</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Sæktu og settu upp Dynamics 365 fyrir Operations farsímaforrit
Sæktu forritið Microsoft Dynamics 365 fyrir Operations úr forritaverslun farsímans og settu það upp.

-   Fyrir Android: [Dynamics 365 fyrir Operations í Google Play Store](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   Fyrir iPhone: [Dynamics 365 fyrir Operations í iTunes forrita versluninni](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Skráðu þig inn í Dynamics 365 fyrir Operations farsímaforritið
1.  Ræstu forritið í fartækinu þínu.
2.  Skrifaðu þitt Dynamics 365 fyrir Operations vefslóð.
3.  Skráðu fyrirtækið sem á að skrá sig inn á . Til dæmis: Færið inn **USMF**.
4.  Fyrsta skipti sem þú skráir þig inn verðurðu beðin um notandanafn og aðgangsorð fyrir þinn Microsoft Dynamics 365 fyrir Operations reikning. Færðu inn skilríki
5.  Eftir að þú skrá inn, sérðu tiltækt vinnusvæði fyrir Þitt fyrirtæki. Athugið að ef kerfisstjóra gefur út nýja vinnusvæði síðar, geturðu togað til að uppfæra listann yfir fartækja vinnusvæði. 

    [![Togið upp til að uppfæra](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-onhand-inventory-for-a-product-by-using-the-inventory-onhand-mobile-workspace"></a>Skoða tiltækar birgðir á lager fyrir vöru með því að nota vinnusvæðið lagerbirgðir.
1.  Í farsímanum velurðu vinnusvæðið **birgðir á lager**.
2.  Veldu **Kanna birgðir á lager fyrir vöru**. Þá sérðu lista yfir vörur sem er hlaðið upp í forritið til notkunar utan nets. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta. Forritarar nálgist nánari upplýsingar í [Dynamics 365 fyrir Operations á fartækja svæði](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
3.  Ef þitt atriði er ekki á listanum skal velja **Leita áfram** til að framkvæma leit á netinu í  Dynamics 365 for Operations. Leitaðu eftir vörunúmeri eða skiptu í leit eftir vöruheiti.
4.  Veljið afurð. Ef mynd fylgir vörunni er myndin sýnd.
5.  Veldu einn af eftirfarandi valkostum til að skoða birgðastöðu á lager:
    -   Skoða birgðastöðu á lager eftir svæði
    -   Skoða birgðastöðu á lager eftir vöruhúsi
    -   Skoða birgðastöðu á lager eftir staðsetningu
    -   Birgðastaða á lager eftir runum (fyrir runustýrðar vörur)
    -   Skoða birgðastöðu á lager eftir stöðu birgða

    Birgðastaða á lager fyrir vörur er sýnd með eftirfarandi hætti:
    -   Eftir efnislegum birgðum (Þetta yfirlit táknar heildarmagn).
    -   Eftir efnislegum frátektum (Þetta yfirlit táknar frátekið magn).
    -   Eftir efnislegu vörum sem eru tiltækar (þetta yfirlit táknar tiltækt magn sem ekki er bókað).






