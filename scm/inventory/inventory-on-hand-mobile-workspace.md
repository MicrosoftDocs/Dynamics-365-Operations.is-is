---
title: "Birgðir á lager eftir fartækjavinnusvæði"
description: "Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið Birgðir á lager. Þetta vinnusvæði hjálpar þér að fá yfirsýn gegnum fartæki yfir pantaðar og tiltækar birgðir, hvar og hvenær sem er."
author: Mirzaab
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: db41b3873755f93895aea7a32b65f2a8ed6a57fd
ms.openlocfilehash: 6e062ffa459b7d008fc5d24f27538f8df04d7e82
ms.contentlocale: is-is
ms.lasthandoff: 08/10/2017

---

# <a name="inventory-on-hand-mobile-workspace"></a>Birgðir á lager eftir fartækjavinnusvæði

[!include[banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið **Birgðir á lager**. Þetta vinnusvæði hjálpar þér að fá yfirsýn yfir fráteknar og tiltækar birgðir, hvar og hvenær sem er.

Þetta fartækjavinnusvæði er ætlað til notkunar með fartækjaforritinu Microsoft Dynamics 365 for Unified Operations.

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

## <a name="prerequisites"></a>Frumskilyrði
Forkröfur eru mismunandi eftir þeirri útgáfu Microsoft Dynamics 365 sem hefur verið innleidd í fyrirtækinu.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a>Forkröfur ef þú notar Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfa, uppfærsla í júlí 2017 
Hafi Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfa með uppfærslu frá júlí 2017 verið innleidd í fyrirtækinu, verður kerfisstjóri að gefa út fartækjavinnusvæðið **Birgðir á lager**. Leiðbeiningar er að finna í [Fartækjavinnusvæði birt](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Forkröfur ef verið er að nota Microsoft Dynamics 365 for Operations útgáfu 1611 með svæðisuppfærslu 3 eða síðar
Ef verið er að nota Microsoft Dynamics 365 for Operations útgáfu 1611 með svæðisuppfærslu 3 eða síðar í fyrirtækinu, verður kerfisstjóri að uppfylla eftirfarandi forkröfur. 

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
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Sæktu lýsigagnabráðabótina á Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Setja upp bráðabót lýsigagna</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Stofna virkjanlegan pakka</a> sem inniheldur <strong>SCMMobile</strong> líkanið og hlaða síðan virkjanlega pakkann í LCS.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Notaðu virkjanlega pakkann</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Birta fartækjavinnusvæðið <strong>Birgðir á lager</strong>.</td>
<td>Kerfisstjóri</td>
<td>Sjáið <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Fartækjavinnusvæði birt</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Sæktu og settu upp fartækjaforritið

Sæktu og settu upp fartækjaforritið Dynamics 365 for Unified Operations:

-   [Fyrir Android síma](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Fyrir iPhone síma](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Innskráning í fartækjaforritið

1.  Ræstu forritið í fartækinu þínu.
2.  Færðu inn vefslóð þína fyrir Dynamics 365.
3.  Í fyrsta sinn sem þú skráir þig inn, er beðið um notandanafn og aðgangsorð þitt. Færðu inn skilríki
4.  Eftir að þú hefur skráð þig inn, birtast tiltæk vinnusvæði fyrir fyrirtækið. Athugið að ef kerfisstjóri gefur út nýtt vinnusvæði síðar, verður að endurræsa listann yfir fartækjavinnusvæði.

    [![Togið upp til að uppfæra](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>Skoða birgðir á lager fyrir afurð með því að nota fartækjavinnusvæðið Birgðir á lager.

1.  Í farsímanum velurðu vinnusvæðið **birgðir á lager**.

2.  Veldu **Kanna birgðir á lager fyrir vöru**. Þá sérðu lista yfir vörur sem er hlaðið upp í forritið til notkunar utan nets. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta. Til að fá frekari upplýsingar ættu þróunaraðilar að skoða [Fartækjaverkvangur](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page).
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

