---
title: Dagatöl og aðaláætlanagerð
description: Þetta efnisatriði veitir yfirlit yfir aðfangakeðjudagatöl og hvernig þau hafa áhrif á aðaláætlanagerð.
author: t-benebo
manager: AnnBe
ms.date: 05/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: t-benebo
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ca473de65135ddddea12ddc72e902056cc7b1db7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845295"
---
# <a name="calendars-and-master-planning"></a>Dagatöl og aðaláætlanagerð

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir yfirlit yfir aðfangakeðjudagatöl og hvernig þau hafa áhrif á aðaláætlanagerð.  Mismunandi dagatölin sem eru notuð í kerfi aðaláætlanagerðar eru útskýrð, þ.á.m. hvernig þau hafa áhrif á sendingar- og móttökudaga í áætluðum pöntunum. Að lokum eru tilmæli um úthlutun, notkun og uppfærslu á dagatölum gefin.

## <a name="definition-of-a-calendar"></a>Skilgreining á dagatali

Hægt er að skilgreina dagatal til að nota í fyrirtækinu á síðunni í **Fyrirtækisstjórnun > Uppsetning > Dagatöl > Dagatöl**. 

Hver dagsetningarfærsla í dagatali getur verið **opin** eða **lokuð** eða **Grunndagatal**. Þetta er tilgreint í dálknum **Stýring** á síðunni **Vinnutímar**. Fyrir hvern dag: 
- **Opin** - Sýnir að vinna er framkvæmd á völdum degi. Dagbókin verður uppfærð í samræmi við sniðmát vinnutíma.
- **Lokuð** - Sýnir vinnu sem er ekki framkvæmd á deginum. 
- **Grunndagatal** - Sýnir að tiltekin dagsetning mun öðlast vinnutímana og opin/lokuð úr grunndagatalinu. Þess vegna þegar grunndagatali er uppfært mun valið dagatal öðlast aðgerðatíma úr því. 

Fyrir lokaðar dagsetningar mun gátreiturinn **Lokað fyrir afhendingu** vera úthlutað sjálfvirkt. Fyrir opnar dagsetningar er hægt að velja handvirkt valkostinn **Lokað fyrir afhendingu**. Þetta sýnir að vinna er framkvæmd á dagsetningunni, en afhending er ekki framkvæmd. 

## <a name="calendars-that-affect-master-planning"></a>Dagatöl sem hafa áhrif á aðaláætlanagerð

### <a name="calendar-for-a-coverage-group"></a>Dagatal fyrir þekjuflokk
Þekjuflokkur sýnir algengt safn af færibreytum sem eru notaðar til áfyllingar á vörunum sem tilheyra umræddum þekjuflokki. 

Til að bæta við dagatali fyrir þekjuflokk skal fara í **Aðaláætlanagerð > Uppsetning > Þekja > Þekjuflokkar**. Finndu þekjuflokkinn sem þú vilt úthluta dagatalinu til og veldu hann svo í reitnum **Dagatal**.

Hægt er að úthluta þekjuflokknum á mismunandi síður: 
    - Á síðunni **Upplýsingar um losaðar afurðir** fyrir vöru. Til að sjá þekjuflokk fyrir vöru skal fara í **Afurðarupplýsingastjórnun > Afurðir > Útgefnar afurðir** og velja vöruna sem á að fara á síðuna **Upplýsingar um útgefnar afurðir**. Hægt er að sjá þekjuflokk vöru undir flýtiflipanum **Áætlun**.
    - Á síðunni **Vöruþekja**. Á upplýsingasíðu útgefinna afurða skal smella á **Vöruþekja** til að fara á vöruþekjusíðuna. Í yfirlitsflipanum er hægt að sjá mismunandi færibreytur fyrir áfyllingu sem fer eftir svæði, vöruhúsi og afurðarvíddum. Þekjuflokkur hverrar vöru verður afritaður úr þekjuflokknum á síðunni **Upplýsingar um útgefnar afurðir**. Hægt er að hnekkja þessu með **Nota tilteknar stillingar** eða **Stillingar hnekkingarflokks** í flipanum **Almennt**.
    - Á síðunni **Færibreytur áætlanagerðar**. Ef vara er ekki með þekjuflokk stilltan á fyrri síðu, mun aðaláætlanagerð nota almenna þekjuflokkinn sem er stilltur í færibreytum aðaláætlanagerðar. Þetta er sett upp í **Aðaláætlanagerð > Uppsetning > Færibreytur áætlanagerðar** í reitnum **Almennur þekjuflokkur**. 

### <a name="calendar-for-a-vendor"></a>Dagatal fyrir lánardrottin
Til að sýna vinnudaga lánardrottins er hægt að úthluta innkaupadagatali á lánardrottin á síðunni **Sjálfgildi innkaupapöntunar** fyrir lánardrottin. 

Til að setja dagatal fyrir lánardrottin þarf að stofna dagatalið í **Fyrirtækisstjórnun > Dagatöl > Dagatöl**. Eftir að dagatalið er búið til þarf að úthluta því á lánardrottin. Farið í **Viðskiptaskuldir > Lánardrottnar > Allir lánardrottnar** og veljið lánardrottin sem á að fá dagatalinu úthlutað. Því næst skal á lánardrottnasíðunni, í flýtiflipanum **Sjálfgildi innkaupapöntunar**, úthluta nýja innkaupadagatalinu með því að nota fellivalmyndina. 

Dagatal fyrir lánardrottin sýnir dagana þegar þeir samþykkja innkaupapöntun sem lögð er fram og dagsetningarnar þegar þeir geta afhent pantanirnar til fyrirtækisins þíns. Af því leiðir að pöntunardagsetningar fyrir innkaupapantanir fyrir lánardrottin með innkaupadagatal verða dagsetningar sem eru skilgreindar sem opnar í dagatalinu. Afhendingardagarnir fyrir þessar pantanir verða einnig á opnum dögum og hafa þar af leiðandi áhrif á afhendingartíma keyptrar vöru. 

#### <a name="define-the-lead-time-for-a-purchased-item"></a>Skilgreina afhendingartíma fyrir keypta vöru

Til að tilgreina afhendingartíma innkaupa (og ef eingöngu á að taka tillit til vinnudaga) fyrir vöru er nauðsynlegt að fara á síðu sjálfgefinna pöntunarstillinga fyrir afurðina, sem má finna undir **Afurðarupplýsingastjórnun > Afurðir > Útgefnar afurðir** og velja **Sjálfgefnar pöntunarstillingar**. 

> [!Note]
> **Vinnudagar** undir afhendingartíma innkaupa sýna vinnudaga lánardrottins. Til dæmis dagatal fyrir afhendingu eingöngu á þriðjudögum með afhendingartíma upp á 10 daga og valinn gátreitur fyrir vinnudaga sýnir að það tæki 10 vikur (10 þriðjudaga) að fá vöruna afhenda.
Þannig að í flestum tilfellum ekki mælt með að velja vinnudaga fyrir afhendingartíma innkaupapöntunar.

#### <a name="define-lead-times-from-the-trade-agreements-page"></a>Skilgreina afhendingartíma á síðu viðskiptasamninga

Hægt er að setja upp aðaláætlanagerð þannig að hún innihaldi viðskiptasamninga fyrir lánardrottna. Viðskiptasamningar eru föst verð eða afsláttarsamningar sem eru settir upp fyrir einn eða fleiri viðskiptavini eða lánardrottna vegna sölu eða kaupa á einni eða mörgum afurðum. Farið í **Aðaláætlanagerð > Uppsetning > Færibreytur áætlanagerðar** og í flipanum **Áætlaðar pantanir** skal velja **Finna viðskiptasamninga** til að hafa viðskiptasamningana með í áætlanagerð. Aðaláætlanagerð getur valið lánardrottin með **Lágmarksafhendingartími** eða með **Lægsta einingaverð**.

### <a name="calendar-for-a-warehouse"></a>Dagatal fyrir vöruhús
Hægt er að úthluta dagatali til vöruhúss til að sýna dagsetningar sem eru opnar fyrir móttöku og afhendingu. Ef engu dagatali hefur verið úthlutað til vöruhúss er ályktað að það sé opið alla daga. 

> [!Note]
> Úthlutun dagatals til flutningsvöruhúss hefur engin áhrif. Flutningsvöruhús eru notuð til að styðja við flutningspantanir. Hentugar afhendinga- og móttökudagsetningar fyrir pantanir eru skilgreindar eftir opnum dagsetningum innan „Frá“ vöruhúsi og „Til“ vöruhúss og dagatali flutningsmáta.

#### <a name="closed-for-pickup-policy"></a>Regla um lokun á afhendingu
Til að sýna að vöruhús er opið fyrir móttöku en ekki er hægt að sækja er hægt að nota **Regla um lokun á afhendingu** innan dagatals vöruhúss. Þetta á einnig við um þegar viðskiptavinir sækja. 

### <a name="transport-calendar"></a>Flutningsdagatal 
Til að sýna dagana sem í boði eru til að senda flutningspantanir frá **Frá vöruhúsi** er hægt að úthluta **Flutningsdagatal**. Hægt er að setja upp flutningsdagatal fyrir hvern flutningsmáta eða fyrir hvern flutningsmáta og frá vöruhúsi. Flutningsdagatalið er sett upp í **Sala og markaðssetning > Uppsetning > Dreifing > Flutningsmátar**. Veljið flutningsmáta og smellið á hnappinn **Flutningsdagatal**.

Hægt er að búa til línu fyrir hvert vöruhús og hvern flutningsmáta þar sem dagatalinu er bætt við í dálkinn **Flutningsdagatal**. Hún mun tilgreina flutningsdagatalið sem verður notað þegar vörur eru sendar úr vöruhúsi með umræddum flutningsmáta. Til að nota flutningsdagatal fyrir allar sendingar sem nota umræddan flutningsmáta er hægt að búa til línu án þess að tilgreina vöruhúsið.  Það mun hafa áhrif á allar sendingar sem nota uppgefinn flutningsmáta, óháð vöruhúsinu. 

Ef engu flutningsdagatali er úthlutað er gert ráð fyrir því að allir dagar séu opnir fyrir flutning.

### <a name="calendar-for-a-customer"></a>Dagatal fyrir viðskiptavin
Til að sýna dagsetningarnar þegar viðskiptavinur getur samþykkt afhendingar, er hægt að úthluta móttökudagatali á viðskiptavininn. Ef engu dagatali er úthlutað á viðskiptavin er gert ráð fyrir því að viðskiptavinurinn geti móttekið pantanir alla daga. Þetta mun hafa áhrif á móttökudagsetningu á sölupöntunarlínum. Ef valin er dagsetning í sölupöntunarlínum sem er ekki „opin“ í dagatali viðskiptavinar mun kerfið sýna að móttökudagsetningin er ekki gild. 

Athugið að ekki er mögulegt að hafa eitt dagatal á hvern viðskiptavin. Ef nauðsynlegt er að hafa með dagatal fyrir hvert aðsetur fyrir sig fyrir viðskiptavin er hægt að stofna einn viðskiptavin á hvert aðsetur og síðan úthluta honum viðeigandi dagatal. 

Umbeðin móttökudagsetning á sölupöntunarlínum verður fyrir áhrifum af dagatali viðskiptavinar og stýringaraðferð afhendingardags. Hægt er að lesa meira um hvernig fyrsti afhendingardagurinn er reiknaður út í [Pöntun lofað](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/delivery-dates-available-promise-calculations).

### <a name="shipping-calendar-for-a-legal-entity"></a>Sendingadagatal fyrir lögaðila
Til að sýna dagsetningarnar þar sem lögaðili getur sent vörur er hægt að setja upp sendingadagatal undir **Fyrirtækisstjórnun > Fyrirtæki > Lögaðilar**. Veljið lögaðilann og bætið við dagatalinu í flipanum **Erlend viðskipti og vörustjórnun** í reitnum **Sendingadagatal**. Sendingadagatalið virkar sem uppruni sjálfgilda fyrir öll dagatöl vöruhúsa í lögaðilanum. 

## <a name="how-calendars-affect-dates-in-planning"></a>Hvernig dagatöl hafa áhrif á dagsetningar í áætlun

### <a name="order-date-of-a-planned-purchase-order"></a>Pöntunardagur fyrirhugaðrar innkaupapöntunar 
Pöntunardagurinn í fyrirhugaðri innkaupapöntun sýnir dagsetninguna þegar pöntun er gerð. Það verður opin dagsetning bæði í dagatali lánardrottins og í dagatali þekjuflokks. Stundum þurfa lánardrottnar nokkra daga til að hlaupa upp á frá því þeir móttaka innkaupapöntun og þar til þeir geta sent vörurnar. Þessar dagsetningar eru tilgreindir í öryggismarkadögum lánardrottins. Ef keyptri vöru er hins vegar úthlutað á þekjuflokk með öryggismarkadögum munu þessir dagar hnekkja öryggismarkadögum lánardrottins.

### <a name="delivery-date-of-a-planned-purchase-order"></a>Afhendingardagur á fyrirhugaðri innkaupapöntun
Móttökudagsetning innkaupa sýnir daginn sem vörurnar verða mótteknar. Það verður opin dagsetning í dagatalinu. Dagatalið sem verður tekið til greina til að sýna dagana sem hægt er að móttaka innkaupapantanirnar eru í eftirfarandi röð, frá hæsta til lægsta forgangs: 
    1. Dagatal lánardrottins
    2. Dagatal þekjuflokks
    3. Dagatal vöruhúss fyrir móttökuvöruhús

Athugið að hægt er að setja dagatal þekjuflokks á mismunandi síður og forgangur verður í eftirfarandi röð:
    1. Þekjuflokkur vöru á síðunni **Upplýsingar um útgefnar afurðir**
    2. Þekjuflokkur vöru á síðunni **Vöruþekja**
    3. Sjálfgefinn þekjuflokkur vöru í **Færibreytur áætlanagerðar**

### <a name="shipping-date-of-a-planned-transfer-order"></a>Sendingadagsetning á áætlaðri flutningspöntun
Þegar stofnuð er flutningspöntun milli tveggja vöruhúsa eru sendingadagsetning og móttökudagsetning innifaldar í flutningspöntunarhaus, ásamt „Frá“ vöruhúsi og „Til“ vöruhúss. Munurinn milli þessara tveggja dagsetninga er væntanlegur flutningstími (í dögum) milli vöruhúsanna.

Sendingadagsetning á áætlaðri flutningspöntun sýnir daginn sem vörurnar eru sendar frá „Frá“ vöruhúsi. Dagatölin sem eru notuð til að tilgreina tiltæka sendingadagsetningu eru útlistuð eftir forgangi: 
    1. Dagatal vöruhúss fyrir „Frá“ vöruhúsi
    2. Dagatal þekjuflokks (sjá vararöð fyrir þetta dagatal hér að ofan) Ef dagatal vöruhúss er stillt verður sendingadagsetningin opin dagur í dagatalinu. Ef dagatal vöruhúss er ekki stillt, verður dagatal þekjuflokks notað. 

### <a name="receipt-date-of-a-planned-transfer-order"></a>Móttökudagsetning á áætlaðri flutningspöntun
Móttökudagsetningin fyrir flutningspöntun sýnir daginn sem vörurnar eru mótteknar í „Til“ vöruhúsi.

Dagatölin sem eru notuð til að tilgreina móttökudagsetningu eru þau sem eru útlistuð eftir forgangi: 
    1. Dagatal þekjuflokks 
    2. Dagatal vöruhúss fyrir „Til“ vöruhús. Ef dagatal þekjuflokks er stillt verður móttökudagsetningin opinn dagur í dagatalinu. Ef dagatal þekjuflokks er ekki stillt, verður dagatal vöruhúss notað. 

Þegar sending og móttökudagsetningar fyrir áætlaðan flutning eru fundnar, verður munurinn sem notandinn setur á fyrir sendingu og móttöku einnig tekinn til greina. 

## <a name="using-calendars-in-master-planning"></a>Notkun dagatala í aðaláætlanagerð

### <a name="assignment-of-scm-calendars"></a>Úthlutun SCM dagatala
Mikilvægt er að stilla dagatölin til að bera kennsl á vinnudaga fyrirtækisins. Besta innleiðingin er að stilla dagatal fyrir hvern þátt með mismunandi vinnudögum. Með öðrum orðum, öll ytri dagatöl (viðskiptavinur, lánardrottinn) og allt innra (vöruhús, þekjuflokkur og flutningsmáti) sem tengjast fyrirtækinu.

### <a name="recommendation-on-warehouse-calendars"></a>Ráðleggingar um dagatöl vöruhúss
Mælt er með því að nota eitt dagatal á hvert vöruhús til að hafa með tilgreindar breytingar sem hafa eingöngu áhrif á vöruhúsið. Til dæmis gætu tvö eða fleiri vöruhús verið með sömu vinnudagana en mismunandi reglu um afhendingu. Í því tilviki er dagatal fyrir hvert vöruhúsanna með sínar eigin reglur um afhendingu besta innleiðingin fyrir kerfið til að hafa með bestu dagsetningarnar fyrir áætluð innkaup, flutning og framleiðslupantanir. Ef engin dagatöl vöruhúss eru stillt er hægt að nota dagatal lögaðila sem uppruni sjálfgilda fyrir dagatal vöruhúss. 

### <a name="recommendation-of-coverage-group-calendars"></a>Ráðleggingar um dagatöl þekjuflokks
Varðandi dagatal þekjuflokks er mikilvægt að hafa í huga að það býr yfir hegðun hnekkingar hvað varðar móttökudagsetningar í aðaláætlanagerð. Því er mælt með að nota það af varkárni. Það er sérstaklega gagnlegt í tilfellum þegar gera þarf áfyllingu á ákveðnum dögum vikunnar. 

### <a name="updating-scm-related-calendars"></a>Uppfærsla á SCM tengdum dagatölum
Mikilvægt er að öllum viðeigandi dagatölum sé úthlutað á viðeigandi staði (lánardrottinn, viðskiptavinur, vöruhús, flutningsmáti eða þekjuflokkur), en að sama skapi er mikilvægt að uppfæra þau svo þau endurspegli breytingarnar. Kerfið mun skilgreina dagsetningar framleiðslu, flutnings, innkaupa og sölupöntunar, háð samsetningu úthlutaðra dagatala. Bestu starfsvenjur eru að fá úr því skorið hver beri ábyrgð á úthlutun og uppfærslu dagatalanna á svæðunum sem við eiga. Í tilfelli bilunar eða annarra óvenjulegra breytinga á vinnudögum er nauðsynlegt að uppfæra dagatölin í samræmi við það. Öll verk sem eru háð dagatölum, t.d. aðaláætlanagerð og framleiðsluröðun, verða að vera keyrð aftur þegar dagatöl eru uppfærð. 
