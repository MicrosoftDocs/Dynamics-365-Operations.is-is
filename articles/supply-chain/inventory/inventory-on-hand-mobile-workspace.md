---
title: Birgðir á lager eftir fartækjavinnusvæði
description: Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið Birgðir á lager. Þetta vinnusvæði hjálpar þér að fá yfirsýn gegnum fartæki yfir pantaðar og tiltækar birgðir, hvar og hvenær sem er.
author: yufeihuang
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yufeihuang
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b380da99b02fe9b7cd834eabac3498ee3b8e54a4
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811467"
---
# <a name="inventory-on-hand-mobile-workspace"></a>Birgðir á lager eftir fartækjavinnusvæði

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið **Birgðir á lager**. Þetta vinnusvæði hjálpar þér að fá yfirsýn yfir fráteknar og tiltækar birgðir, hvar og hvenær sem er.

Þetta farsímavinnusvæði er ætlað til notkunar með Finance and Operations (Dynamics 365) farsímaforritinu.

## <a name="overview"></a>Yfirlit
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

## <a name="prerequisites"></a>Forkröfur
Forkröfur eru mismunandi eftir þeirri útgáfu Supply Chain Management sem hefur verið innleidd í fyrirtækinu.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Forkröfur ef þú notar Supply Chain Management
Ef Supply Chain Management hefur verið innleitt í fyrirtækinu verður kerfisstjóri að birta fartækjavinnusvæðið **Birgðir á lager**. Leiðbeiningar er að finna í [Fartækjavinnusvæði birt](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-platform-update-3-or-later"></a>Skilyrði ef þú notar verkvangsuppfærslu 3 eða nýrri 
Ef verkvangsuppfærsla 3 eða síðar hefur verið sett upp fyrir fyrirtækið þitt, verður kerfisstjórinn að ljúka eftirfarandi skilyrðum. 

<table>
<thead>
<tr class="header">
<th>Skilyrði</th>
<th>Hlutverk</th>
<th>lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Innleiða KB 4013633.</td>
<td>Kerfisstjóri</td>

<td>KB 4013633 er X++ uppfærsla eða lýsigagnabráðabót sem inniheldur fartækjavinnusvæðið <strong>Birgðir á lager</strong>. Til að setja upp KB 4013633 verður kerfisstjóri að fylgja eftirfarandi skrefum.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Sækja bráðabót lýsigagna frá Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Setja upp bráðabót lýsigagna</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Stofna virkjanlegan pakka</a> sem inniheldur <strong>SCMMobile</strong> líkanið og hlaða síðan virkjanlega pakkann í LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Notaðu virkjanlega pakkann</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Birta fartækjavinnusvæðið <strong>Birgðir á lager</strong>.</td>
<td>Kerfisstjóri</td>
<td>Sjáið <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Fartækjavinnusvæði birt</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Sæktu og settu upp fartækjaforritið

Sæktu og settu upp Finance and Operations (Dynamics 365) farsímaforritið:

-   [Fyrir Android síma](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Fyrir iPhone síma](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Innskráning í fartækjaforritið

1.  Ræstu forritið í fartækinu þínu.
2.  Færðu inn vefslóð þína fyrir Dynamics 365.
3.  Í fyrsta sinn sem þú skráir þig inn, er beðið um notandanafn og aðgangsorð þitt. Færðu inn skilríki
4.  Eftir að þú hefur skráð þig inn, birtast tiltæk vinnusvæði fyrir fyrirtækið. Athugið að ef kerfisstjóri gefur út nýtt vinnusvæði síðar, verður að endurræsa listann yfir fartækjavinnusvæði.

    [![Togið upp til að uppfæra.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>Skoða birgðir á lager fyrir afurð með því að nota fartækjavinnusvæðið Birgðir á lager.

1.  Í farsímanum velurðu vinnusvæðið **birgðir á lager**.

2.  Veldu **Kanna birgðir á lager fyrir vöru**. Þá sérðu lista yfir vörur sem er hlaðið upp í forritið til notkunar utan nets. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta. Til að fá frekari upplýsingar ættu þróunaraðilar að skoða [Fartækjaverkvangur](../../fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
3.  Ef varan þín er ekki á listanum velurðu **Leita áfram**. Leitaðu eftir vörunúmeri eða skiptu í leit eftir vöruheiti.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
