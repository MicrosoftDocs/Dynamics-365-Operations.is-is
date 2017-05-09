---
title: "Lánardrottinn fartæki samvinnusvæði fyrir forritið Microsoft Dynamics 365 for Operations"
description: "Með vinnusvæði samstarfs lánardrottna fyrir fartæki geta lánardrottnar fylgst með innkaupapöntunum sem hafa verið sendar til þeirra fyrir samþykki og skoða upplýsingar um nýjar og uppfærðar innkaupapantanir og tengiliði."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 36 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: fe8e912d-8446-4584-8a24-d8892e9028cd
ms.search.region: global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 9f441508b745d22218316128572c9ec6aeb7207b
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Lánardrottinn fartæki samvinnusvæði fyrir forritið Microsoft Dynamics 365 for Operations

Með vinnusvæði samstarfs lánardrottna fyrir fartæki geta lánardrottnar fylgst með innkaupapöntunum sem hafa verið sendar til þeirra fyrir samþykki og skoða upplýsingar um nýjar og uppfærðar innkaupapantanir og tengiliði.

<a name="prerequisites"></a>Forkröfur
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Skilyrði</th>
<th>lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lesa um Microsoft Dynamics 365 for Operations verkvang</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Microsoft Dynamics 365 for Operations verkvangur</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for Operations</td>
<td>Vertu viss um að þú sért að nota umhverfi sem er með Microsoft Dynamics 365 for Operations útgáfu 1611 og uppfærslu verkvangs Microsoft Dynamics for Operations 3 (nóvember 2016).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Lýsingarlína fartækis með forritið Dynamics 365 for Operations uppsett</span></td>
<td><span style="color: #000000;">Sækja forritið Dynamics 365 for Operations úr forritaverslun fartækis.</span></td>
</tr>
<tr class="even">
<td>Bráðabót KB 3215650</td>
<td>Setja upp bráðabót til að virkja skal vinnusvæðin sem veittar eru í Dynamics 365 for operations.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Bráðabót KB 3216943</span> </span></td>
<td>Setja upp bráðabót til að virkja vinnusvæði samstarfs lánardrottna fyrir fartæki.</td>
</tr>
<tr class="even">
<td>Notanda lánardrottins verður að hafa aðgang að vefviðmótið samvinnusvæði lánardrottins í Dynamics 365 for Operations og setja upp samvinnusvæði notanda lánardrottins.</td>
<td>Fylgja skal skrefunum sem lýst er í eftirfarandi efnisatriði til að setja upp og vinna með vefviðmóti samstarfs lánardrottna.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Nota samstarf lánardrottna við ytri lánardrottna</a></li>
<li><a href="manage-vendor-collaboration-users.md">Stjórna notendum fyrir samstarf lánardrottna</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Setja upp og viðhalda samstarf lánardrottna</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Notið samvinnusvæði lánardrottinn til að vinna með viðskiptavini í Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Yfirlit
Lánardrottinn fartæki samvinnusvæðið heldur halda sér upplýstum um nýjar innkaupapantanir þannig að þeir sjá og svara innkaupapöntunum í vefbiðlara Dynamics 365 for Operations fyrir lánardrottna.  

**Athugasemd:** Vinnusvæði fartækis ætti að nota sem viðauka við vefviðmót samstarfs lánardrottna, en ekki í staðinn.  

Með vinnusvæði samstarfs lánardrottna fyrir fartæki geta lánardrottnar skoðað nýjar innkaupapantanir sem eru sendar til samþykkis. Það birtir upplýsingar á innkaupapöntun, eins og afurðir, magn og umbeðnar afhendingardagsetningar. Upplýsingar um Verð eru tiltækar, eftir skilgreiningu fyrir hvern lánardrottinn.  

Þegar notandi skráir sig inn sem lánardrottinn, sér hann hvaða innkaupapöntunum hefur verið svarað eða hvaða innkaupapantanir bíða enn eftir aðgerð viðskiptavinar. Lánardrottinn gæti hafa stungið upp á annarri afhendingardagsetningu sem hefur ekki enn verið samþykkt af viðskiptavini svo að innkaupapöntun bíður eftir aðgerð viðskiptavinar. Lánardrottinn mun einnig sjá lista yfir innkaupapantanir sem eru staðfestar en hafa enn ekki verið afhentar.  

Til að svara innkaupapöntun hefur lánardrottins til að nota lánardrottins samvinnusvæði vefviðmótið sem er tiltæk í vefbiðlara Dynamics 365 for Operations. Þetta er einnig þar sem lánardrottinn fær frekari upplýsingar um pöntunina, eins og fylgiskjöl, afhendingaraðsetrið á hverja línu og gjöld sem eru tengdar við lánardrottinn.  

Með sérstöku öryggishlutverki getur lánardrottinn skoðað hvaða tengiliðir einstaklinga eru skráðir fyrir lykil lánardrottins. Með sama öryggishlutverki getur lánardrottinn skoðað stöðu allra notandabeiðna sem hafa verið sendar.  

Stofna nýja tengiliðir og senda nýja notandabeiðni verður unnið í samvinnusvæði viðmót lánardrottins sem er tiltæk í vefbiðlara Dynamics 365 for Operations.  

Með vinnusvæði fartækias getur lánardrottinn:

-   Skoðað staðfestar innkaupapantanir sem voru sendar lánardrottni.
-   Skoðað innkaupapantanir sem lánardrottinn hefur svarað og bíða eftir aðgerð viðskiptavinar.
-   Skoðað innkaupapantanir sem eru með staðfesta stöðu og hafa ekki verið mótteknar að fullu.
-   Skoðað upplýsingar um tengilið sem er skráður fyrir reikning lánardrottins (krefst auka öryggishlutverks).
-   Skoðað upplýsingar og fylgt stöðu notandabeiðni sem lánardrottinn sendi (krefst auka öryggishlutverks).

## <a name="get-started"></a>Hefjast handa
Til að hefjast handa í fartækinu þínu:

1.  Sæktu forritið Dynamics 365 for Operations úr forritaverslun farsímans og settu það upp.
2.  Ræstu forritið í snjallsímanum.
3.  Færðu inn vefslóð þína fyrir Dynamics 365.
4.  Skráðu fyrirtækið sem á að skrá sig inn á . Til dæmis: Færið inn **USMF**.
5.  Fyrsta skipti‘ sem þú skráir þig inn verðurðu beðin um notandanafn og aðgangsorð fyrir þinn Microsoft Dynamics 365 for Operations reikning. 

Þegar búið er að skrá inn í forritið eru vinnusvæð sýnileg. Til að skoða vinnusvæði í farsímaforritinu verður fyrst að gefa út æskileg vinnusvæði í forritið Dynamics 365 for Operations. Þú þarft heimild kerfisstjóra til að birta vinnusvæðið.

1.  Ræstu Dynamics 365 for Operations.
2.  Opnaðu **Kerfisstjórnun** &gt; **Uppsetning** &gt; **kerfisfæribreytur**.
3.  Veldu **Stjórna fartækjaforriti**.
4.  Velja vinnusvæðið **Samstarf lánardrottna** til að birta í verkvangi farsíma.
5.  Veldu **Birta vinnusvæði**.
6.  Endurhlaða Þitt tæki til að sjá útgefin vinnusvæði.
7.  Veldu vinnusvæðið **Samstarf lánardrottna**. Eftirfarandi síða birtist.

[![vendor-collaboration-mobile-app](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Tengiliðir
Síðan **Tengiliðir** gerir mögulegt að sjá alla tengiliði sem hafa verið settir upp fyrir lánardrottnalykil. Hún sýnir nafn tengiliðar, aðalnetfang og auknefni notenda, ef það er tiltækt. Hún sýnir einnig hvort notandareikningur tengiliðar er virkur. Þegar tengiliður er valinn sérðu upplýsingar um tengilið, eins og hvaða lögaðila einstaklingurinn er tengiliður fyrir, og upplýsingar eins og símanúmer eða annað netfang tengiliðar.

## <a name="user-requests"></a>Notandabeiðnir
Síðan **Notandabeiðnir** gera þér kleift að sjá allar notandabeiðnir í gegnum vefviðmót samstarfs lánardrottna og fylgja stöðunni. Þegar beiðni notanda er valin, er hægt sjá hvað beðið var um, bæta við eða gera notanda óvirkan, breyta öryggi og sjá hvaða öryggishlutverk voru umbeðin fyrir notanda.

## <a name="purchase-orders-ready-for-review"></a>Innkaupapantanir tilbúnar til skoðunar
Síðan **Innkaupapantanir sem eru tilbúnar til endurskoðunar** gera kleift að sjá allar innkaupapantanir sem voru sendar af viðskiptavini og hefur ekki verið svarað. Hægt er að skoða valdar upplýsingar um pöntunina, eins og hefur verið beðið um hvaða afurðir og hvenær á að afhenda. Upplýsingar um Verð er aðeins tiltækt ef þetta er skilgreint fyrir lánardrottinn.  

Hægt er að sjá hvort innkaupapöntunin hefur athugasemdir eða viðhengi. Til að opna viðhengi, þarf að nota samstarf lánardrottna í vefbiðlara. Velja **Innkaupapöntunarlínu** til að sjá allar línur með upplýsingum. Athugið að fyrir hverja línu mun vísir sýna hvort að það eru athugasemdir eða viðhengi eða ef afhendingaraðsetur er annað en það sem er birt í haus.  

Til að bregðast við innkaupapöntun, verður að nota vefbiðlara samstarfs lánardrottna.

## <a name="awaiting-customer-action"></a>Beðið eftir aðgerð viðskiptavinar
Síðan **Beðið eftir aðgerð viðskiptavinar** gerir kleift að finna innkaupapantanir sem þú, eða einhver innan fyrirtækisins sem hefur einnig aðgang að samstarfi lánardrottna, hefur svarað. Innkaupapantanir eru aðeins sýnilegar í þessum lista ef viðskiptavinurinn þarf að framkvæma eina af eftirfarandi aðgerðum í innkaupapöntuninni.

-   Ef innkaupapöntunin var hafnað myndi viðskiptavinurinn annaðhvort uppfæra senda pöntun og senda hana aftur, eða hætta við pöntunina og endursenda. Þegar pöntunin er send aftur mun hún hverfa af síðunni **Beðið eftir aðgerð viðskiptavinar**.
-   Ef innkaupapöntunin var samþykkt með breytingum myndi viðskiptavinur þurfa að uppfæra upphaflega pöntun og endursenda til skoðunar eða uppfæra hana samkvæmt breytingum og staðfesta strax. Í báðum tilfellum mun pöntunin hverfa af síðunni **Bíður eftir aðgerð viðskiptavinar**.
-   Ef innkaupapöntunin var samþykkt og birtist á síðunni **Beðið eftir aðgerð viðskiptavinar** er það vegna þess að innkaupapöntunin var ekki sjálfkrafa staðfest þegar móttöku var lokið. Hún bíður þess að innkaupaaðili breyti pöntun í Staðfest. Venjulega myndi innkaupapöntun vera skoðuð sem samningur milli viðskiptavinar og lánardrottins um leið og lánardrottinn tekur á móti pöntuninni. Flutningur innkaupapöntunar í stöðuna Staðfest væri formsatriði.

Með því að velja innkaupapöntun, birtast frekari upplýsingar um svarið. Hægt er að sjá upplýsingar um og svar fyrir hverja línu. Línustaðan sýnir hver eftirfarandi svara voru gefin.

-   Samþ.  
-   Hafnað
-   Samþykkt með breytingum
-   Skipt út/Staðgengill
-   Skipta í áætlun/áætlunarlínu

Athugið að vísir sýnir **Afhendir**= já/nei, sem er notuð til að gefa til kynna að línurnar verði ekki afhentar. Þetta gæti verið þar sem línunni var hafnað eða hún sett í staðinn þar sem ekki er búist við að upprunalega verði afhentar eða lína sem hefur verið skipt í marga línur afhendingaráætlunar og ekki er búist við að upphaflega línan sé afhent eins og beðið var um í mótteknum pöntunarlínum.  

Allar breytingar á svari línu innkaupapöntunar birtast, nema fyrir upphlaðnar athugasemdir og viðhengi, sem hægt er að sjá með notkun vefviðmóts samstarfs lánardrottna.

## <a name="open-confirmed-orders"></a>Opna staðfestar pantanir
Þegar innkaupapöntun er staðfest af viðskiptavini, sem þýðir að innkaupapöntun er breytt í stöðuna Staðfest, mun það birtast í opinni staðfestri pöntun. Hún verður áfram á listanum þar til hún er skráð sem móttekin af viðskiptavini.


