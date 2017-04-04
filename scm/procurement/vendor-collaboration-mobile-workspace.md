---
title: "Lánardrottinn fartæki samvinnusvæði fyrir Microsoft Dynamics 365 fyrir Aðgerðir forrits"
description: "Með lánardrottins fartæki samvinnusvæðið, lánardrottnana vera uppfærðir í innkaupapöntunum sem hafa verið sendar til þeirra fyrir samþykki og skoða upplýsingar um nýjar og uppfæra innkaupapantanir og tengiliði."
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

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Lánardrottinn fartæki samvinnusvæði fyrir Microsoft Dynamics 365 fyrir Aðgerðir forrits

Með lánardrottins fartæki samvinnusvæðið, lánardrottnana vera uppfærðir í innkaupapöntunum sem hafa verið sendar til þeirra fyrir samþykki og skoða upplýsingar um nýjar og uppfæra innkaupapantanir og tengiliði.

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
<td>Lesa um Microsoft Dynamics 365 fyrir fartæki svæðis Aðgerðir</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 fyrir fartæki svæðis Aðgerðir</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 fyrir Aðgerðir</td>
<td>Verið viss um að afskriftareglur eru umhverfi sem er með Microsoft Dynamics 365 Aðgerðir útgáfu 1611 og uppfærslu Microsoft Dynamics fyrir Aðgerðir svæðis (Nóvember 2016) 3.</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Lýsingarlína fartækis með Dynamics 365 fyrir Aðgerðir forrits uppsett</span></td>
<td><span style="color: #000000;">Sækja Dynamics 365 fyrir Aðgerðir forrits úr verslunin fartæki forrits.</span></td>
</tr>
<tr class="even">
<td>Bráðabót KB 3215650</td>
<td>Setja upp bráðabót til að virkja skal vinnusvæðin sem veittar eru í Dynamics 365 aðgerða.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Bráðabót KB 3216943</span> </span></td>
<td>Setja upp bráðabót til að virkja lánardrottin fartæki samvinnusvæðið.</td>
</tr>
<tr class="even">
<td>Notanda lánardrottins verður að hafa aðgang að vefviðmótið samvinnusvæði lánardrottins í Dynamics 365 aðgerða og setja upp samvinnusvæði notanda lánardrottins.</td>
<td>Fylgja skal skrefunum sem lýst er í eftirfarandi efnisatriði til að setja upp og vinna með vefviðmótið samvinnusvæði lánardrottins.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Samvinnusvæði lánardrottins er notuð til að vinna með ytri lánardrottna</a></li>
<li><a href="manage-vendor-collaboration-users.md">Stjórna notendum fyrir samstarf lánardrottna</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Setja upp og viðhalda samstarf lánardrottna</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Notið samvinnusvæði lánardrottinn til að vinna með viðskiptavini í Dynamics 365 fyrir Aðgerðir</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Yfirlit
Lánardrottinn fartæki samvinnusvæðið heldur halda sér upplýstum um nýjar innkaupapantanir þannig að þeir sjá og svara innkaupapöntunum í Dynamics 365 vefbiðlari Aðgerðir fyrir lánardrottna.  

**Athugasemd:** fartæki vinnusvæði ætti að nota sem viðauki vefviðmótið samvinnusvæði lánardrottins, en ekki í staðinn.  

Með Lánardrottins fartæki samvinnusvæðið, lánardrottnana skoða nýjar innkaupapantanir sem eru send til samþykkis. Hann birtir upplýsingar á innkaupapöntun afurðir, magn og umbeðnar afhendingardagsetningar. Upplýsingar um Verð er tiltækir, eftir skilgreiningu fyrir hvern lánardrottinn.  

Þegar notandi skráir sig inn sem lánardrottinn, þeir sjá innkaupapantanir sem hafa verið svarað eða innkaupapantanir sem eru enn bíður eftir aðgerð viðskiptavinar. Lánardrottinn gæti hafa verið stungið upp á aðra afhendingardagsetningu sem er ekki enn verið samþykkt viðskiptavinar svo innkaupapöntun bíður eftir aðgerð viðskiptavinar. Lánardrottinn verður einnig að sjá lista yfir innkaupapantanir sem eru staðfestar en hefur enn ekki verið afhent.  

Til að svara innkaupapöntun hefur lánardrottins til að nota lánardrottins samvinnusvæði vefviðmótið sem er tiltæk í 365 Dynamics fyrir vefbiðlari Aðgerðir. Þetta er einnig þar sem lánardrottinn fá frekari upplýsingar um afhendingaraðsetrið á hverja línu og gjöld sem eru tengdar við lánardrottinn, pöntun, til dæmis skjal í viðhengi.  

Með sérstökum öryggishlutverk lánardrottinn hægt er að skoða hvaða tengiliður einstaklinga eru skráðar fyrir lykil lánardrottins. Með sömu öryggishlutverk lánardrottins hægt er að skoða stöðu notandabeiðni sem hefur verið sent.  

Stofna nýja tengiliðir og senda nýja notandabeiðni verður unnið í samvinnusvæði viðmót lánardrottins sem er tiltæk í Dynamics 365 fyrir vefbiðlari Aðgerðir.  

Með fartæki vinnusvæði lánardrottninum geta:

-   Skoða nýjar innkaupapantanir sem hafa verið sendar til lánardrottins.
-   Skoða innkaupapantanir sem lánardrottinn hefur svarað og bíða eftir aðgerð viðskiptavinar.
-   Skoða innkaupapantanir sem eru í staðfestum ríkis og hafa ekki verið móttekið að fullu.
-   Skoða upplýsingar um tengilið sem er skráð fyrir reikning lánardrottins (krefst auka öryggi hlutverk).
-   Skoða upplýsingar og fylgja stöðu notandabeiðni sem lánardrottininn sendi (krefst auka öryggi hlutverk).

## <a name="get-started"></a>Hefjast handa
Til að byrja á því fartækis:

1.  Verslunin fartæki forritið á að sækja og setja upp Microsoft Dynamics 365 fyrir Aðgerðir forrits.
2.  Byrja forritið þitt tækis.
3.  Færið inn Vefslóð skal Dynamics 365.
4.  Færið inn fyrirtæki að skrá sig inn á. Til dæmis inn **USMF**.
5.  Í fyrsta sinn sem þú skráir þig inn, verið beðið um notandanafn og aðgangsorð fyrir notanda Microsoft Dynamics 365 fyrir Aðgerðir. 

Þegar búið er að skrá inn í forritið, engin vinnusvæða sýnileg. Til að skoða vinnusvæða fartæki forritið, er verður fyrst að birta skal vinnusvæðin sem óskað er eftir að Dynamics 365 fyrir Aðgerðir forrits. Kerfið stjórnun heimild til að birta vinnusvæðið þarf.

1.  Ræsa Dynamics 365 aðgerða.
2.  Fara í **kerfisstjórnun**&gt;**Uppsetningu**&gt;**kerfisfæribreytum**.
3.  Veljið **Stjórna fartæki forrits**.
4.  Velja vinnusvæðið **Lánardrottins samvinnusvæði** til að birta í fartæki svæðis.
5.  Velja **Birta vinnusvæði**.
6.  Endurnýja skal tæki til að sjá birt vinnusvæði.
7.  Velja skal **samvinnusvæði Lánardrottins** vinnusvæðisins. Eftirfarandi síðu verður.

[![lánardrottinn-samvinnusvæði-gátt fyrir fartæki-forrits](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Tengiliðir
Í **Tengiliðir** síðu gerir það mögulegt að sjá alla tengiliði sem hafa verið sett upp fyrir lykil lánardrottins. Hún sýnir tengiliðar heiti aðalnetfang og auknefni notendur, ef hún er tiltæk. Hún sýnir einnig tengiliðar notandareikningurinn er virk. Þegar tengilið er að sjá upplýsingar um tengilið, svo sem hvaða lögaðila einstaklingurinn er tengiliður fyrir, og upplýsingar eins og símanúmer eða annað netfang tengiliðar.

## <a name="user-requests"></a>Notandabeiðnir
Í **notandabeiðnir** síðunni kleift að sjá allar notandi biður um hafa vefsíðu vefviðmótið samvinnusvæði lánardrottna og stöðu fylgja. Þegar beiðni notanda, er hægt sjá hvað beðið var um, bæta eða gera notanda óvirkan, breyta öryggi og sjá öryggishlutverk sem var beðið um fyrir notanda.

## <a name="purchase-orders-ready-for-review"></a>Innkaupapantanir sem eru tilbúnar til endurskoðunar
Í **innkaupapantanir sem eru tilbúnar til endurskoðunar** síðu kleift að sjá öllum innkaupapöntunum sem voru sendar af viðskiptavini og hefur ekki verið svarað. Hægt er að skoða valda upplýsingar um pöntunina, eins og hefur verið beðið um hvaða afurðir og hvenær á að afhenda. Upplýsingar um Verð er aðeins tiltækt ef þetta er skilgreint fyrir lánardrottinn.  

Hægt er að sjá hvort innkaupapöntunin hefur athugasemdir eða viðhengi. Til að opna viðhengi, þarf að nota lánardrottin samvinnusvæði í vefhlutanum biðlara. Velja **Innkaupapöntunarlínu** til að sjá allar línur með upplýsingum. Athugið að fyrir hverja línu vísi mun sýna hvort að það eru athugasemdir eða viðhengi eða ef er afhendingaraðsetur er annað en það er birt í haus.  

Til að bregðast við innkaupapöntun, nota vefbiðlari samvinnusvæði lánardrottins.

## <a name="awaiting-customer-action"></a>Beðið eftir aðgerð viðskiptavinar
Í **bíður Eftir aðgerð viðskiptavinar** síðunni kleift að finna innkaupapantanir sem þú, eða einhver innan fyrirtækisins sem hefur aðgang að samvinnusvæði lánardrottins, einnig hafa svarað. Innkaupapantanir eru aðeins sýnilegt í þessum lista ef viðskiptavinurinn þarf að framkvæma eitt af eftirfarandi aðgerðum í innkaupapöntuninni.

-   Ef innkaupapöntunin var hafnað myndi viðskiptavinurinn annaðhvort þarf að uppfæra sent pöntunina og senda aftur, eða hætta við pöntunina og endursenda. Þegar pöntunin er send aftur, hún verður hverfa úr á **bíður Eftir aðgerð viðskiptavinar** síðu.
-   Ef innkaupapöntunin var með breytingum viðskiptavinar mundi þurfa að uppfæra upphaflegu og endursenda til skoðunar eða uppfæra þær samkvæmt breytingar og staðfesta strax. Í báðum tilvikum innkaupapöntun mun hverfa úr á **bíður Eftir aðgerð viðskiptavinar** síðu.
-   Ef innkaupapöntunin var samþykkt og birtist í **bíður Eftir aðgerð viðskiptavinar** síðu er vegna þess að innkaupapöntunin var ekki sjálfkrafa staðfesta þegar móttöku var lokið. Hún bíður þess innkaupaaðila til að breyta Staðfest. Venjulega innkaupapöntun myndi má skoðast sem samningur milli viðskiptavinar og lánardrottins um leið og lánardrottinn tekur á móti pöntuninni. Byrjað innkaupapöntun er Staðfest ríki væri að formality.

Með því að velja innkaupapöntun, birtast frekari upplýsingar um svarið. Hægt er að sjá upplýsingar um og svar fyrir hverja línu. Staðan sýnir línu sem eftirfarandi svör hefur verið gefið.

-   Samþ.  
-   Hafnað
-   Samþykkt með breytingum
-   Skipt út/Staðgengill
-   Skipta í áætlun/áætlunarlínu

Athugið vísi sýnir **Delivering**= já/nei, sem er notuð til að gefa til kynna að línurnar ekki afhent. Þetta gæti verið þar sem línan var hafnað eða sett í staðinn þar sem upprunalega línurnar eru ekki búist við að afhenda eða línu sem hefur verið skipt í marga línur afhendingaráætlunar og í upphaflegu línunni er ekki búist við að afhenda sem beðið var um í mótteknar pöntunarlínur.  

Allar breytingar á svar línu innkaupapöntunar birtast, nema hlaðið var upp athugasemdir og viðhengjum, sem hægt er að sjá með vefviðmótið samvinnusvæði lánardrottins.

## <a name="open-confirmed-orders"></a>Staðfestar pantanir
Þegar innkaupapöntun er staðfest af viðskiptavini, sem þýðir að innkaupapöntun er breytt í stöðuna Staðfest það mun birtast í opinni pöntun staðfest. Það áfram á listanum þar til hún er skráð sem viðskiptavinurinn fær.


