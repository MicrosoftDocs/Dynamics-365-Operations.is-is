---
title: Fartækjavinnusvæði samstarfs lánardrottna
description: Þetta efnisatriði veitir upplýsingar um lánardrottnasamvinnu á fartækjavinnusvæði. Þessi vinnusvæði gerir lánardrottnum kleift að fylgjast með innkaupapöntunum sem hafa verið sendar til þeirra til samþykktar. Þeir geta einnig skoðað upplýsingar um nýjar og uppfærðar innkaupapantanir og tengiliði.
author: mkirknel
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: fc73fe415ec2b9a266dda6b7f1b3469b7a77f256
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430612"
---
# <a name="vendor-collaboration-mobile-workspace"></a>Fartækjavinnusvæði samstarfs lánardrottna

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um **lánardrottnasamvinnu** á fartækjavinnusvæði. Þessi vinnusvæði gerir lánardrottnum kleift að fylgjast með innkaupapöntunum sem hafa verið sendar til þeirra til samþykktar. Þeir geta einnig skoðað upplýsingar um nýjar og uppfærðar innkaupapantanir og tengiliði.

Þetta fartækjavinnusvæði er ætlað til að nota með farsímaforritið Finance and Operations.

## <a name="overview"></a>Yfirlit 
Fartækjavinnusvæðið **Samstarf lánardrottna** heldur lánardrottnum upplýstum um nýjar innkaupapantanir svo að hægt sé að skoða innkaupapantanir og síðan svara þeim í vefbiðlara. 

>[!NOTE]
> Vinnusvæði fartækis ætti að nota sem viðauka við vefviðmót samstarfs lánardrottna, en ekki í staðinn fyrir það. 

Með vinnusvæði **samstarfs lánardrottna** fyrir fartæki geta lánardrottnarnir skoðað nýjar innkaupapantanir sem eru sendar til þeirra til samþykkis. Það birtir upplýsingar á innkaupapöntun, eins og afurðir, magn og umbeðnar afhendingardagsetningar. Upplýsingar um verð eru einnig tiltækar, eftir skilgreiningu fyrir hvern lánardrottinn. 

Notandi sem skráir sig inn sem lánardrottinn sér hvaða innkaupapöntunum hefur verið svarað og hvaða innkaupapantanir bíða enn eftir aðgerð viðskiptavinar. Til dæmis gæti innkaupapöntun beðið eftir aðgerð viðskiptavinar vegna þess að lánardrottinn stakk upp á annarri afhendingardagsetningu en viðskiptavinurinn hefur ekki enn samþykkt þá dagsetnignu. Lánardrottinn mun einnig sjá lista yfir innkaupapantanir sem hafa verið staðfestar en hafa enn ekki verið afhentar. 

Til að svara innkaupapöntun verður lánardrottinn að nota lánardrottins samvinnusvæði vefviðmótið sem er tiltæk í vefbiðlara. Þar getur lánardrottinn einnig fengið frekari upplýsingar um pöntunina, eins og fylgiskjöl, afhendingaraðsetrið á hverja línu og gjöld sem eru tengdar við lánardrottinn. 

Lánardrottnar sem hafa sérstakt öryggishlutverk geat séð hvaða tengiliðir einstaklinga eru skráðir fyrir lykil lánardrottins. Sama öryggishlutverk gerir lánardrottni kleift að skoða stöðu allra notandabeiðna sem hafa verið sendar. 

Vefmót lánardrottnasamvinnu í vefbiðlaranum verður að nota til að stofna nýja tengiliði og senda inn nýjar notandabeiðnir. 

Fartækjavinnusvæðið **Samvinna lánardrottna** gerir lánardrottni kleift að framkvæma þessar aðgerðir:

-   Skoða nýjar innkaupapantanir sem eru sendar lánardrottni.
-   Skoða innkaupapantanir sem lánardrottinn hefur svarað og sem bíða eftir aðgerð viðskiptavinar.
-   Skoða innkaupapantanir sem hafa verið staðfestar en hafa ekki enn verið mótteknar að fullu.
-   Skoða persónuupplýsingar tengiliðar sem skráðar eru fyrir lykil lánardrottins. (Verkið krefst auka öryggishlutverks.)
-   Skoða upplýsingar um notandabeiðni sem lánardrottinn sendi og fylgt stöðu beiðninnar. (Verkið krefst auka öryggishlutverks.)

## <a name="prerequisites"></a>Forkröfur
Skilyrðin eru mismunandi, háð útgáfu Microsoft Dynamics 365 sem hefur verið sett upp fyrir fyrirtækið þitt.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Forkröfur ef þú notar Supply Chain Management
Ef Supply Chain Management hefur verið innleitt í fyrirtækinu verður kerfisstjóri að birta fartækjavinnusvæðið **Samstarf lánardrottna**. Leiðbeiningar er að finna í [Fartækjavinnusvæði birt](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Skilyrði ef þú notar Microsoft Dynamics 365 for Operations útgáfu 1611 með verkvangsuppfærslu 3 eða nýrri
Ef Microsoft Dynamics 365 for Operations útgáfa 1611 með verkvangsuppfærslu 3 eða síðar hefur verið sett upp fyrir fyrirtækið þitt, verður kerfisstjórinn að ljúka eftirfarandi skilyrðum. 

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
<td>KB 3216943 verður að vera innleitt ef verkvangsuppfærsla 3 er notuð.&#39;</td>
<td>Kerfisstjóri</td>
<td>KB 3216943 er tvíundaruppfærsla sem er nauðsynleg ef verkvangsuppfærsla 3 er notuð.&#39; Til að setja þetta KB upp verður kerfisstjóri að fylgja eftirfarandi skrefum.
<ol>
<li>Sækja KB 3216943 frá Microsoft Dynamics Lifecycle Services (LCS).</li>
<li>Setja upp tvíundakerfisuppfærslu, sem er afhent sem dreifanlegur pakki. Sjá upplýsingar um hvernig á að nota dreifanlega pakka <a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Nota dreifanlegan pakka</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>KB 4013633 verður að vera innleitt.</td>
<td>Kerfisstjóri</td>
<td>KB 4013633 er X++ uppfærsla eða lýsigagnabráðabót sem inniheldur fartækjavinnusvæðið <strong>Birgðir á lager</strong>. Til að setja upp KB 4013633 verður kerfisstjóri að fylgja eftirfarandi skrefum.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Sækja bráðabót lýsigögn úr LCS</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Setja upp bráðabót lýsigagna</a>.</li><li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Stofna virkjanlegan pakka</a> sem inniheldur <strong>SCMMobile</strong> líkanið og hlaða síðan virkjanlega pakkann í LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Notaðu virkjanlega pakkann</a>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Það verður að birta fartækjavinnusvæðið <strong>Samvinna lánardrottna</strong>.</td><td>Kerfisstjóri</td>
<td>Sjáið <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Fartækjavinnusvæði birt</a>.</td>
</tr>
<tr class="even">
<td>Notandi lánardrottins verður að hafa aðgang að vefviðmótinu Samvinnusvæði lánardrottins í vefbiðlaranum og verður að setja upp samvinnusvæði notanda lánardrottins.</td><td>Innkaupasérfræðingar og kerfisstjóri</td>
<td>Fylgja skal skrefunum í eftirfarandi efnisatriði til að setja upp og vinna með vefviðmóti samstarfs lánardrottna.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Nota samstarf lánardrottna við ytri lánardrottna</a></li>
<li><a href="manage-vendor-collaboration-users.md">Stjórna notendum fyrir samstarf lánardrottna</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Uppsetning og viðhald samstarfs lánardrottna</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Notið samvinnusvæði lánardrottinn til að vinna með viðskiptavini í Supply Chain Management</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Sæktu og settu upp fartækjaforritið

Sæktu og settu upp fartækjaforritið Finance and Operations:

-   [Fyrir Android síma](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Fyrir iPhone síma](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Innskráning í fartækjaforritið
1.  Ræstu forritið í fartækinu þínu.
2.  Færðu inn vefslóð þína fyrir Microsoft Dynamics 365.
4.  Í fyrsta sinn sem þú skráir þig inn er beðið um notandanafn og aðgangsorð þitt. Færðu inn skilríki
5.  Eftir að þú hefur skráð þig inn, birtast tiltæk vinnusvæði fyrir fyrirtækið. Athugið að ef kerfisstjóri gefur út nýtt vinnusvæði síðar, verður að endurræsa listann yfir fartækjavinnusvæði.

    [![Togið upp til að uppfæra](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="use-the-vendor-collaboration-mobile-workspace"></a>Notaðu fartækjavinnusvæði samstarfs lánardrottna
Þegar valið er vinnusvæðið **Samstarf lánardrottna** sérðu eftirfarandi valkosti.

![Fartækjavinnusvæði samstarfs lánardrottna](./media/vendor-collaboration-mobile-app.png)

Vinnusvæðið **Samvinna lánardrottna** felur í sér eftirfarandi síður.

### <a name="contacts"></a>Tengiliðir
Síðan **Tengiliðir** gerir mögulegt að sjá alla tengiliði sem hafa verið settir upp fyrir lánardrottnalykil. Það sýnir nafn tengiliðar, aðalnetfang og auknefni notandans, ef tengiliðurinn hefur auknefni. Þessi síða sýnir einnig hvort notandareikningur tengiliðar er virkur. Þegar tengiliður er valinn sjást tengilið upplýsingum á borð við lögaðila sem starfsmaður tengiliður fyrir. Þú sérð einnig tengiliðarupplýsingar, eins og símanúmer eða annað netfang.

### <a name="user-requests"></a>Notandabeiðnir
Síðan **Notandabeiðnir** gera þér kleift að sjá allar notandabeiðnir sem þú hefur sent í gegnum vefviðmót samstarfs lánardrottna og fylgja stöðunni. Einnig er hægt að fylgja stöðu þessara beiðna. Þegar beiðni notanda er valin, er hægt sjá hvað beðið var um, bæta við eða gera notanda óvirkan, breyta öryggi og sjá hvaða öryggishlutverk voru umbeðin fyrir notanda.

### <a name="purchase-orders-ready-for-review"></a>Innkaupapantanir tilbúnar til skoðunar
Síðan **Innkaupapantanir sem eru tilbúnar til endurskoðunar** gera kleift að sjá allar innkaupapantanir sem viðskiptavinurinn hefur sent en sem hefur ekki enn verið svarað. Hægt er að skoða valdar upplýsingar um pöntunina, eins og hefur hvaða afurðir hefur verið beðið og hvenær á að afhenda þær afurðir. Upplýsingar um verð eru einnig tiltækar, eftir skilgreiningu fyrir lánardrottinninn.

Einnig er hægt að sjá hvort innkaupapöntunin hefur athugasemdir eða viðhengi. Hins vegar, til að skoða athugasemdir og viðhengi verður að nota vefviðmót samvinnu lánardrottna í vefbiðlara. Veldu **Innkaupapöntunarlínu** til að sjá allar línur ásamt með upplýsingunum. Fyrir hverja línu mun vísir sýna hvort að það eru athugasemdir eða viðhengi eða ef afhendingaraðsetur er annað en það sem er birt í haus.

Til að bregðast við innkaupapöntun, verður að nota vefviðmótið samstarf lánardrottna í vefbiðlara.

### <a name="awaiting-customer-action"></a>Beðið eftir aðgerð viðskiptavinar
Síðan **Beðið eftir aðgerð viðskiptavinar** gerir kleift að finna innkaupapantanir sem þú eða einhver annar innan fyrirtækisins sem hefur einnig aðgang að samstarfi lánardrottna, hefur svarað. Innkaupapantanir eru aðeins sýnilegar í þessum lista ef viðskiptavinurinn verður að framkvæma eina af eftirfarandi aðgerðum í innkaupapöntuninni:

-   Ef innkaupapöntuninni var hafnað þarf viðskiptavinurinn annaðhvort að uppfæra eða hætta við upprunalega pöntun og síðan senda hana aftur. Þegar pöntunin er send aftur birtist hún ekki lengur á síðunni **Beðið eftir aðgerð viðskiptavinar**.
-   Ef innkaupapöntunin var samþykkt með breytingum verður viðskiptavinur annaðhvort að uppfæra upphaflega pöntun og síðan senda hana aftur til skoðunar eða uppfæra pöntunina samkvæmt umbeðnum breytingum og síðan staðfesta hana strax. Í báðum tilfellum birtist pöntunin ekki lengur á síðunni **Bíður eftir aðgerð viðskiptavinar**.
-   Ef innkaupapöntunin var samþykkt og birtist samt á síðunni **Beðið eftir aðgerð viðskiptavinar** er það vegna þess að innkaupapöntunin var ekki sjálfkrafa staðfest þegar hún var samþykkt. Hún bíður nú að innkaupaaðili breyti stöðu pöntunar í **Staðfest**. Venjulega myndi innkaupapöntun vera skoðuð sem samningur milli viðskiptavinar og lánardrottins um leið og lánardrottinn tekur á móti pöntuninni. Þar af leiðandi er uppfærsla í stöðuna **Staðfest** yfirleitt aðeins formlegheit.

Þegar þú velur innkaupapöntun, birtast frekari upplýsingar um svarið. Hægt er að sjá upplýsingar um og svar fyrir hverja línu. Línustaðan sýnir hver eftirfarandi svara voru gefin:

-   Samþ.
-   Hafnað
-   Samþykkt með breytingum
-   Skipt út/Staðgengill
-   Skipta í áætlun/áætlunarlínu

Athugið að svæðið **Afhending** er stillt á annaðhvort **Já** eða **Nei** til að gefa til kynna hvort afhenda eigi línurnar. Lína kann að verða ekki afhent vegna eftirfarandi ástæðna:

- Línunni var hafnað.
- Skipti voru gerð og þess er ekki vænst að upprunaleg lína sé afhent eins og beðið er um í móttekinni pöntun.
- Línunni var skipt upp í margar áætlunarlínur og þess er ekki vænst að upprunaleg lína sé afhent eins og beðið er um í móttekinni pöntun.

Allar breytingar sem gerðar voru í svari raðarlínu eru sýndar. Hins vegar eru upphlaðnar athugasemdir og viðhengi ekki sýnd. Til að skoða athugasemdir og viðhengi verður að nota vefviðmót samvinnu lánardrottna í vefbiðlara.

### <a name="open-confirmed-orders"></a>Opna staðfestar pantanir
Þegar innkaupapöntun er staðfest af viðskiptavini (það er að segja, stöðu innkaupapöntunar er breytt í stöðuna **Staðfest**) birtist hún í opinni staðfestri pöntun. Hún verður áfram á listanum þar til hún er skráð sem móttekin af viðskiptavini.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]