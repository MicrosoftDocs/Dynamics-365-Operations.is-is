---
title: Grunnstilla gerðir viðburða
description: Microsoft Dynamics 365 Human Resources notar gerðir viðburða til að skilgreina viðburði til að uppfæra fríðindaskráningu starfsmanns.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aab35d40af43caff7010998ddce51350584228a1
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071746"
---
# <a name="configure-life-event-types"></a>Grunnstilla gerðir viðburða


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources notar **Tegundir lífsviðburða** að skilgreina atburði þar sem gilt er að uppfæra innritun starfsmannakjara, svo sem að gifta sig eða eignast barn. Auðkenni hvers lífsviðburðar má aðeins tengjast einni tegund atburðar. Til dæmis, ef þú býrð til a **Auðkenni lífsatburðar** kallaði **Heimilisfangsbreyting** sem tengist tegund lífsatburðar **Breyting á heimilisfangi starfsmanna**, þú getur ekki búið til annað auðkenni merkt **Breyting á heimilisfangi starfsmanna** og tengja það við tegund lífsatburðar **Breyting á heimilisfangi starfsmanna**. Ef gerð viðburðar er ekki tengd við gerð áætlunar mun gerð viðburðar ekki koma af stað viðburði. Nánari upplýsingar sjá [Stofna áætlunargerðir](hr-benefits-setup-plan-types.md).

## <a name="create-a-life-event-type"></a>Búðu til viðburðagerð

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Gerðir viðburða**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Auðkenni gerðar viðburðar** | Einkvæmt auðkenni viðburðargerðar. |
   | **Lýsing** | Lýsing á gerð viðburðar. |
   | **Gerð viðburðar** | Hvati til að uppfæra skráningu starfsmanna á fríðindum. Sjá lista yfir atburði í lífinu [Viðburðir](hr-benefits-setup-payment-frequencies.md?life-events) hér að neðan. |

4. Veljið **Vista**.

## <a name="view-attached-plans"></a>Skoða viðhengdar áætlanir

Þú getur séð lista yfir áætlanir sem fylgja völdum **Tegund lífsatburðar**. Viðburðir eru tengdir áætlunartegundum og áætlunartegundir tengjast áætlun.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Gerðir viðburða**.

2. Velja **Aðgerðir**.

3. Veldu **Meðfylgjandi áætlanir**.

## <a name="life-events"></a>Viðburðir

Þú getur valið úr eftirfarandi lífsviðburðum þegar þú býrð til gerð atburðar í lífinu:

| Viðburður | Staðsetning | Kveikja |
| --- | --- | --- |
| **Breyting á hjúskaparstöðu** | **Verkamaður > Snið > Persónulegar upplýsingar > Hjúskaparstaða**| Breyting á hjúskaparstöðu |
| **Breyting á atvinnustöðu** |**Starfsmaður > Atvinna > Starfsferill síða** | Fyrir starfsmann með núverandi starfsupplýsingar mun stofnun nýrra starfsmannaupplýsinga með annarri ráðningarstöðu koma af stað viðburði.  Uppfærsla á fyrirliggjandi starfsupplýsingum með annarri starfsstöðu mun einnig setja af stað viðburð.  |
| **Breyting á heimilisfangi starfsmanns** |**Verkamaður > Forstilling > Heimilisföng**</li><li>**Verkamaður > Persónulegar upplýsingar > Persónulegir tengiliðir > Heimilisfang**</li></ul> | Breyting á heimilisfangi. Heimilisfang verður að vera **Aðalheimilisfang** til að koma af stað viðburði. |
| **Breyting á skjólstæðingi** |<br><ul><li>**Starfsmaður > Prófíll > Persónulegar upplýsingar > Persónulegir tengiliðir** /li><li>**Sjálfsafgreiðsla starfsmanns**</li></ul> | Bæta við persónulegum tengiliði sem tilgreinir þá sem háðan og skilgreinir **Gildir frá**. Uppfærið tengdar upplýsingar fyrir **Gildir til** hjá persónulegum tengilið. Persónuleg tengsl verða að vera barn, maki, sambýlismaður/-kona eða fyrrverandi maki.  |
| **Fæðing eða ættleiðing (skjólstæðingur)** |<br><ul><li>**Verkamaður > Forstilling > Persónulegar upplýsingar > Persónulegir tengiliðir**</li><li>**Sjálfsafgreiðsla starfsmanns > Breyta persónuupplýsingum > Persónulegir tengiliðir**</li></ul>| **Fæðingardagur** eða **Ættleiðingardagur** er bætt við eða uppfært. **Fæðingardagur** barnsins er áskilinn. |
| **Missir tryggingar (maki/sambúðaraðili)** | Verkamaður > Prófíll > Persónulegar upplýsingar > Persónulegir tengiliðir > upplýsingar um skjólstæðing > Missir tryggingar | **Missir tryggingar** valinn fyrir persónulegan tengilið ásamt **Gildistökudagur** |
| Breytingar á atvinnu sambúðaraðila | **Starfskraftur > Prófíll > Persónulegar upplýsingar > Persónulegir tengiliðir > Upplýsingar um skjólstæðing > Ráðin(n)** | Búa til persónulegan tengilið og stilla **Ráðin(n)** á **Já**. Uppfærsla persónulegs tengiliðar og breyta **Ráðin(n)**.  |
| **Fjarvistarleyfi (maki/sambúðaraðili)** | **Verkamaður > Prófíll > Persónulegar upplýsingar > Persónulegir tengiliðir > upplýsingar um skjólstæðing > Fjarvistarleyfi** | Persónulegur tengiliður stofnaður og **Gildisdagsetning fjarvistaleyfis** skilgreint. **Fjarvistaleyfi** persónulegs tengiliðar er uppfært. **Gildistími fjarvistaleyfis** persónulegs tengiliðar er uppfært.  |
| **Breyting á tryggingu (stöðu)** |<br><ul><li>**Starfskraftur > Stöðuúthlutun > Stöðuúthlutanir starfskrafta**</li><li>**Stöður > Stöður**</li></ul>| Breyting á stöðunni í færslu stöðuverkefnis starfsmanns. Breyting á verkefni starfsmanns í stöðunni. |
| **Breyting á tryggingu (launum)** |<br><ul><li>**Starfskraftur > Bætur > Föst áætlun**</li><li>**Starfskraftur > Persónuupplýsingar > Árslaun**</li></ul>| Ef **Fríðindastjórnun > Samnýtt færibreytur mannauðs > Fríðindi > Fríðindi árslaun** er ekki virkt, uppfærir **Starfsmaður > Laun > Föst áætlun** mun skapa lífsviðburð. Ef **Fríðindastjórnun > Samnýtt færibreytur mannauðs > Fríðindi > Fríðindi árslaun** er virkt, uppfærir **Starfsmaður > Persónulegar upplýsingar > Fríðindi árslaun** mun skapa lífsviðburð. |
| **Medicare (starfsmaður/skjólstæðingur)** | **Verkamaður > Prófíll > Persónulegar upplýsingar > Persónulegir tengiliðir > upplýsingar um skjólstæðing > Gildisdagsetning Medicare** | Að bæta við eða uppfæra **Medicare gildisdagsetningu** fyrir persónulegan tengilið skapar þennan viðburð. |
| **Stuðningur samkvæmt dómsúrskurði** | **Starfsmaður > Prófíll > Persónulegar upplýsingar > Persónulegir tengiliðir > Ásjáandi > Stuðningur sem skipaður er dómstóll** (QMSCO/QDRO) og gildandi dagsetningar | Við stofnun persónulegs tengiliðs verður stofnaður viðburður ef **Stuðningur samkvæmt dómsúrskurði** er stillt á **Já**. Uppfærsla **Stuðnings samkvæmt dómsúrskurði** eða **Lokadagsetning samkvæmt dómsúrskurði** mun einnig setja af stað viðburð. |
| **Látin(n)** | **Verkamaður > Snið > Persónulegar upplýsingar > Dagsetning andláts** | **Dagsetning andláts** er færð inn eða uppfærð. |
| **Sönnun fyrir tryggingu** | **Verkamaður > Verkamaður > Útgáfur > Atvinnusaga > Dagsetningastjóri > Upplýsingar um bætur** | **Sönnun fyrir tryggingarhæfi** eru stillt á **Já**. **Staðfestingardagsetning sönnunar fyrir tryggingarhæfi** er skilgreind. |
| **Rétthafi** | **Verkamaður > Forstilling > Persónulegar upplýsingar > Persónulegir tengiliðir** | Persónulegum tengilið er bætt við og reitirnir **Rétthafi** og **Gildisdagsetning** eru fylltir út. Persónulegur tengiliður verður að vera af gerðinni **Barn**, **Maki**, **Sambúðaraðili**, **Systkin**, **Fjölskyldutengiliður**, **Annar tengiliður** eða **Foreldri**. |
| **Medicare starfsmanns** | **Verkamaður > Verkamaður > Útgáfur > Atvinnusaga > Dagsetningastjóri > Upplýsingar um bætur** | **Gjaldgeng(ur) í Medicare** er stillt á **Já**. **Dagsetning gjaldgengis í Medicare** er breytt. |
| **Fæðingardagur** | **Fríðindastjórnun > Breyting á viðburði í vinnslu** | Þessir viðburðir eru búnir til úr **Breyting á viðburði í vinnslu**. Ferlið greinir valið tímabil og lögaðila og finnur tengda starfskrafta. Það reiknar út síðasta afmælisdag þeirra og stofnar til afmælisviðburð ef enginn hefur verið stofnaður. |
| **Breytingar á hæfi starfsmanna (ekki sérstakar í Bandaríkjunum)** |<br><ul><li>**Starfskraftur > Starf**</li><li>**Verkamaður > Verkamaður > Útgáfa > Atvinnusaga**</li></ul>| Stofnar viðburð þegar:<br><ul><li>Búa til nýja atvinnu, og það er fyrri atvinna, og tegund starfsmanns breytist.</li><li>Að búa til upplýsingar um nýja ráðningu og til eru eldri upplýsingar um ráðningu og gerð ráðningar eða flokkur hennar breytist.</li><li>Uppfærsla á starfsskrá og annarri gerð starfskrafts er skilgreind.</li><li>Uppfærsla á starfsupplýsingafærslu og annari starfstegund eða flokki er tilgreind.</li></ul> |
| **Nýr hnekki á hæfi (ekki sérstakur í Bandaríkjunum)** | **Human resources háþróaður > Fríðindi > Áætlanir > Fríðindi > Hæfisregla hnekkt** | Notkun lífsviðburða<br>Að stofna hnekkingu á hæfi nýrrar fríðindaáætlunar fyrir starfsmann setur þennan viðburð af stað.<br>BenefitEligibilityRuleOverride.ValidFrom. |
| **Breyting á hnekkingu hæfisreglu (ekki sértækt fyrir Bandaríkjunum)** | **Human resources háþróaður > Fríðindi > Áætlanir > Fríðindi > Hæfisregla hnekkt** | Að uppfæra **Gildir frá** eða **Gildir til** í hnekkingu á hæfi fríðindaáætlunar setur þennan viðburð af stað. |
| **Gildislok á hnekkingu hæfisreglu (ekki sértækt fyrir Bandaríkjunum)** | Fríðindastjórnun > Breyting á viðburði í vinnslu  | Þessir viðburðir eru búnir til úr **Breyting á viðburði í vinnslu**. Ferlið greinir valið tímabil og lögaðila og finnur tengdar hnekkingar á hæfi fríðindaáætlunar. Það skapar viðburði ef aðgerðirnar eru útrunnar. |
| **Ný bótakerfi (ekki sérstök í Bandaríkjunum)** | **Human resources háþróaður > Fríðindi > Áætlanir > Nýtt** | Valkostum fyrir gjaldgengi er bætt við núverandi áætlun. Nýrri áætlun með hæfisvalkostum sem fylgja með er bætt við.</br></br>Starfsmenn HR ættu að stjórna hæfileikaframkvæmdum í Lífsmóti í þessu tilfelli. |
| **Breyting á hæfisreglu (ekki sértækt fyrir Bandaríkjunum)** | **Fríðindastjórnun > Hæfnisreglur** | Hæfisvinnsla á Notkun lífsviðburða. Skráð þegar **BenefitEligibilityRule** færslur eru með eftirfarandi gildi breytt: **UseEmplCategory**, **UseEmplStatus** eða **UseEmplType**. Aðeins uppfærir viðskipti með lífatburði sem þegar eru til vegna breyttrar reglu eða hæfisskilyrða. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
