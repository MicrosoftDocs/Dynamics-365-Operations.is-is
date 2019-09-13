---
title: Eiginleikastjórnunaryfirlit
description: Þetta efnisatriði lýsir eiginleika eiginleikastjórnunar og hvernig hægt er að nota hann.
author: mikefalkner
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 6aeb5383520f799223d62420f6e0c1079c6c961f
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887112"
---
# <a name="feature-management-overview"></a>Eiginleikastjórnunaryfirlit

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Eiginleikum er bætt við og þeir uppfærðir í hverri útgáfu af Microsoft Dynamics 365 for Finance and Operations. Upplifun eiginleikastjórnunar veitir vinnusvæði þar sem hægt er að skoða lista yfir eiginleika sem hafa verið gefnir út í hverri útgáfu. Sjálfgefið er að slökkt sé á nýjum eiginleikum. Hægt er að nota vinnusvæðið til að kveikja á þeim og skoða fylgiskjölin fyrir þá.

## <a name="the-feature-management-workspace"></a>Vinnusvæði eiginleikastjórnunar

Hægt er að opna vinnusvæðið **Eiginleikastjórnun** með því að velja viðeigandi reit yfirlit. Þú munt sjá síðu sem sýnir lista yfir eiginleika fyrir allar útgáfur sem upplifun eiginleikastjórnunar styður. Með tímanum mun Microsoft auka upplifun eiginleikastjórnunar svo hún innihaldi viðbótarvirkni til að hjálpa til við stjórnun eiginleika.

Eiginleikalistinn inniheldur eftirfarandi upplýsingar:

- **Heiti eiginleika** - Lýsing á eiginleika sem var bætt við.
- **Virkjuð staða** - Tákn tilgreinir hvort kveikt hafi verið á eiginleika (gátmerki), hefur ekki verið kveikt á (autt), er áætlað að verði kveikt á (klukka) eða er áskilið haft kveikt á (lás), krefjist athugunar áður en kveikt er á honum (viðvörun) eða ekki hægt að virkja (X). Stillingin sem er sýnd er notuð fyrir alla lögaðila. Athugið að jafnvel þegar kveikt hefur verið á eiginleika er honum samt stjórnað af öryggi. Eiginleikinn verður þar af leiðandi aðeins tiltækur notendum sem eru með aðgang að honum, samkvæmt öryggishlutverki þeirra. Hann verður einnig eingöngu tiltækur í lögaðila sem notandi hefur aðgang að.
- **Virkja dagsetningu** - Dagsetningin þegar kveikt var á eiginleikanum eða verður kveikt á samkvæmt áætlun.
- **Eiginleika bætt við** - Dagsetningin þegar eiginleikanum var bætt við umhverfið þitt. Þessi dagsetning er slegin inn sjálfvirkt þegar umhverfið er uppfært í mánaðarlega útgáfuferlinu.
- **Eining** - Einingin sem nýja útgáfan hefur áhrif á.

Þegar eiginleiki er valinn birtast viðbótarupplýsingar á upplýsingasvæðinu hægra megin við eiginleikalistann. Efst á svæðinu sérðu heiti eiginleikans, dagsetningin þegar eiginleikanum var bætt við, einingin sem útgáfan hefur áhrif á og tengilinn **Frekari upplýsingar**. Veljið þennan tengil til að skoða fylgiskjöl útgáfunnar. Ef fylgiskjölin eru ekki tiltæk ferðu yfir á bráðabirgðasíðu. Upplýsingasvæðið inniheldur einnig reitinn **Athugasemdir** þar sem hægt er að bæta við eigin athugasemdum um útgáfuna.

Vinnusvæðið **Eiginleikastjórnun** er einnig með nokkra flipa sem hver um sig sýnir lista yfir eiginleika.

- **Nýtt** - Þessi flipi sýnir alla eiginleika sem hefur verið bætt við frá síðustu mánaðarlegu uppfærslunni. Ef þú hefur sleppt einhverjum mánaðarlegum uppfærslum, sýnir flipinn alla nýja eiginleika sem hefur verið bætt við síðan þú uppfærðir síðast. Nýjustu eiginleikar birtast efst á listanum. Heildarfjöldi nýrra eiginleika er einnig sýndur í reit efst á síðunni.
- **Ekki gert virkt** - Þessi flipi sýnir alla eiginleika sem hefur ekki verið kveikt á. Nýjustu eiginleikar birtast efst á listanum. Heildarfjöldi nýrra eiginleika sem hefur ekki verið kveikt á er einnig sýndur í reit efst á síðunni.
- **Áætlað** - Þessi flipi sýnir alla eiginleika sem áætlað er að verði kveikt á í framtíðinni. Eiginleikarnir sem eru með fyrstu áætluðu dagsetningu birtast efst á listanum. Heildarfjöldi nýrra áætlaðra eiginleika er einnig sýndur í reit efst á síðunni.
- **Allir** - Þessi flipi sýnir alla eiginleika. Nýjustu eiginleikar birtast efst á listanum.

## <a name="turn-on-a-feature"></a>Kveikja á eiginleika

Ef ekki hefur verið kveikt á eiginleika birtist hnappurinn **Virkja núna** á upplýsingasvæðinu. Þú getur notað þennan hnapp til að kveikja á eiginleikanum.

- Veljið eiginleikann sem á að kveikja á og síðan á upplýsingasvæðinu skal velja **Virkja núna**. Kveikt er á eiginleikanum.

Ekki er hægt að slökkva á sumum eiginleikum eftir að kveikt hefur verið á þeim. Ef reynt er að kveikja á eiginleika sem ekki er hægt að slökkva á birtist viðvörun. Á þessum tímapunkti er hægt að velja **Hætta við** til að hætta við aðgerðina og hafa slökkt á eiginleikanum. Ef þú hinsvegar velur **Virkja** til að kveikja á eiginleikanum geturðu ekki slökkt á honum seinna.

Sumar aðgerðir sýna skilaboð sem veita frekari upplýsingar áður en þú kveikir á þeim. Þessir eiginleikar eru auðkenndir með gulu viðvörunarmerki. Þú ættir að lesa viðbótarupplýsingarnar vandlega til að skilja betur hvað gerist þegar aðgerðin er virk. Þú getur samt valið **Virkja** til að kveikja á eiginleikanum.

Sumar aðgerðir sýna skilaboð um að ekki sé hægt að virkja aðgerðina fyrr en gripið er til aðgerða. Þessir eiginleikar eru auðkenndir með rauðu X-merki. Þú verður að grípa til aðgerða sem lýst er í lýsingunni áður en aðgerðin er virk. Til dæmis, ef þú getur ekki notað aðgerð fyrr en stillingarlykill er óvirkur, verður þú að slökkva á stillingarlyklinum fyrst og fara síðan aftur í Eiginleikastjórnun til að virkja aðgerðina.

Eftir að kveikt hefur verið á eiginleika birtast skilaboð fyrir neðan tengilinn **Frekari upplýsingar** á upplýsingasvæðinu. Þessi skilaboð kveða annaðhvort á um að kveikt hafi verið á eiginleikanum eða tilgreina dagsetningu fram í tímann þegar áætlað er að kveikja á eiginleikanum. Þau birtast í hvert skipti sem þú velur eiginleikann úr eiginleikalistanum.

Eiginleikar sem áætlað er að kveikja á í framtíðinni birtast í flipanum **Á áætlun**. Runuvinnsla kveikir á þeim á miðnætti á tilgreindum degi, sem byggist á tímabeltinu sem kerfisdagsetningin sýnir.

## <a name="reschedule-a-feature"></a>Endurtímasetja eiginleika

Ef áætlað er að kveikja á eiginleika fram í tímann birtist hnappurinn **Áætla** á upplýsingasvæðinu. Hægt er að nota þennan hnapp til að breyta gildinu **Virkja dagsetningu** í aðra dagsetningu.

1. Veljið áætlaðan eiginleika sem á að endurtímasetja og síðan á upplýsingasvæðinu skal velja **Áætla**.
2. Í svarglugganum sem birtist, í reitnum **Virkja dagsetningu** skal tilgreina nýja dagsetningu þegar kveikja skal á eiginleikanum.
3. Veljið **Gera virkt** til að endurtímasetja eiginleikann eða **Gera óvirkt** til að hætta við áætlunina.

## <a name="turn-off-a-feature"></a>Slökkva á eiginleika

Ef þegar hefur verið kveikt á eiginleika birtist hnappurinn **Gera óvirkt** á upplýsingasvæðinu. Þú getur notað þennan hnapp til að slökkva á eiginleikanum. Hnappurinn **Gera óvirkt** er ekki tiltækur ef ekki er hægt að slökkva á eiginleikanum eftir að kveikt hefur verið á honum.

- Veljið eiginleikann sem á að slökkva á og síðan á upplýsingasvæðinu skal velja **Gera óvirkt**. Slökkt er á eiginleikanum og reiturinn **Virkja dagsetningu** er hreinsaður.

Eftir að slökkt hefur verið á eiginleika birtast skilaboð fyrir neðan tengilinn **Frekari upplýsingar** á upplýsingasvæðinu. Þessi skilaboð kveða á um að ekki hafi enn verið kveikt á eiginleikanum. Þau birtast í hvert skipti sem þú velur eiginleikann úr eiginleikalistanum. Eiginleikar sem ekki hefur verið kveikt á birtast í flipanum **Ekki gert virkt**.

## <a name="features-that-must-be-turned-on"></a>Eiginleikar sem verður að kveikja á

Stundum verður mikilvægur eiginleiki afhentur sem verður að virkja sjálfkrafa við uppfærslu. Kveikt verður á þessum eiginleikum sjálfkrafa á deginum sem er tilgreindur í reitnum **Virkja dagsetningu**. Fyrir þessa eiginleika birtast skilaboð fyrir neðan tengilinn **Frekari upplýsingar** á upplýsingasvæðinu. Þessi skilaboð kveða annaðhvort á um að kveikt hafi verið á eiginleikanum eða tilgreina dagsetningu fram í tímann þegar kveikt verður á eiginleikanum. Þau birtast í hvert skipti sem þú velur eiginleikann úr eiginleikalistanum.

## <a name="enable-all-features"></a>Virkja alla eiginleika

Sjálfgefið er að slökkt sé á öllum eiginleikum sem er bætt við umhverfið þitt. Þú getur virkjað alla eiginleika með því að velja hnappinn **Virkja allt**. 

Þegar þú velur **Virkja allt** birtist valkostur þar sem þú þarft að veita eftirfarandi upplýsingar:
- Listi yfir alla eiginleika sem þarfnast staðfestingar áður en hægt er að virkja þá. Ef þú vilt virkja aðgerðirnar á listanum skaltu velja **Já** fyrir hnappinn **Virkja aðgerðir sem krefjast staðfestingar**.
- Listi yfir alla eiginleika sem ekki er hægt að virkja verður sýndur. Þessir eiginleikar verða ekki gerðir virkir.

Allir aðgerðir sem hægt er að virkja verða gerðar virkar. Ef áætlun er þegar áætluð til að vera virkjuð í framtíðinni breytist áætlunin ekki. 

## <a name="turn-on-all-features-automatically"></a>Kveikja á öllum eiginleikum sjálfkrafa

Sjálfgefið er að slökkt sé á öllum eiginleikum sem er bætt við umhverfið þitt, nema þeir séu áskildir eiginleikar. Ef þú vilt hins vegar kveikja sjálfkrafa á öllum eiginleikum er hægt að nota fellilistann undir titli vinnusvæðis til að breyta því sem gerist þegar nýjum eiginleikum er bætt við.

- Veljið **Virkja nýja eiginleika sjálfvirkt** til að kveikja sjálfkrafa á öllum nýjum eiginleikum þegar þeim er bætt við umhverfið þitt.
- Veljið **Ekki virkja nýja eiginleika sjálfvirkt** til að stilla alla nýja eiginleika sjálfkrafa á slökkt þegar þeim er bætt við umhverfið þitt.


Þegar þú kveikir á öllum eiginleikum sjálfkrafa gerir það kleift að gera alla þá eiginleika sem verða virkar þegar smellt er á hnappinn **Virkja allt**. Það gerir ekki kleift aðgerðir sem krefjast staðfestingar eða aðgerðir sem ekki er hægt að virkja fyrr en gripið er til aðgerða.

## <a name="check-for-updates"></a>Leita að uppfærslum

Eiginleikum er bætt við umhverfi þitt eftir hverja uppfærslu. Þú getur samt sem áður skoðað uppfærslur handvirkt með því að smella á hnappinn **Leita að uppfærslum**. Allir aðgerðir sem bættust við kerfið eftir uppfærsluna verður bætt á lista yfir eiginleika. Til dæmis, ef virkur aðgerð er virk eftir útgáfu, þá geturðu leitað að uppfærslum og aðgerðinni bætt við listann þinn.

## <a name="assigning-roles"></a>Úthlutun á hlutverkum

Kerfisstjórar geta opnað vinnusvæðið **Eiginleikastjórnun** og einnig notendur sem er úthlutað hlutverkunum Eiginleikastjóri eða Eiginleikabirtir. Þessi tvö hlutverk voru búin til til að styðja við umhverfi eiginleikastjórnunar. Notendur í hlutverki eiginleikastjórnunar geta kveikt og slökkt á hvaða eiginleikum sem er. Þeir geta einnig uppfært reitinn **Athugasemdir** fyrir eiginleikann. Notendur í hlutverkinu Eiginleikabirtir geta einungis skoðað vinnusvæðið **Eiginleikstjórnun**. Þeir geta ekki kveikt eða slökkt á eiginleikum.

Hlutverkin Eiginleikastjóri og Eiginleikabirtir hnekkja ekki fyrirliggjandi öryggi sem notar hefur. Þau stjórna því bara hvort notandinn geti kveikt eða slökkt á eiginleikum. Þau veita ekki aðgang að sjálfum eiginleikunum.

## <a name="features-that-use-configuration-keys"></a>Eiginleikar sem nota skilgreiningarlykla

Ef eiginleiki notar skilgreiningarlykil, en ekki er kveikt á skilgreiningarlykli, sýnir vinnusvæðið **Eiginleikastjórnun** ekki eiginleikann í lista yfir tiltæka eiginleika. Eftir að kveikt er á skilgreiningarlykli er nauðsynlegt að uppfæra eiginleikalistann með því að nota valmyndaratriðið **Leita að uppfærslu**. Eiginleikinn birtist þá í eiginleikalistanum.

Ef slökkt er á skilgreiningarlyklinum er eiginleikinn ekki fjarlægður úr eiginleikalistanum.

## <a name="data-entities"></a>Gagnaeiningar

Gagnaeining sem kallast **Eiginleikastjórnun** leyfir þér að flytja út stillingar Eiginleikastjórnunar úr einu umhverfi og síðan flytja þær inn í annað umhverfi. Þessi eining uppfærir aðeins núverandi eiginleika. Viðskiptagrunnurinn í einingunni auðveldar einnig að tryggja að sömu reglurnar sem eru notaðar á vinnusvæðinu **Eiginleikastjórnun** verði notaðar eftir innflutning. Til dæmis er ekki hægt að hunsa áskilda eiginleikastillingu með því að fjarlægja dagsetninguna við innflutning.

Eftirfarandi dæmi lýsa því hvað gerist þegar þú notar eininguna **Eiginleikastjórnun** til að flytja inn gögn.

- Ef gildinu í reitnum **Virkjað** er breytt í **Já** verður kveikt á eiginleikanum og reiturinn **Virkja dagsetningu** er stilltur á daginn í dag.
- Ef gildinu í reitnum **Virkjað** er breytt í **Nei** eða reiturinn **EnableDate** er skilinn eftir auður verður kveikt á eiginleikanum og reiturinn **Virkja dagsetningu** er hreinsaður. Ekki er hægt að slökkva á áskildum eiginleika sem ekki er hægt að slökkva á eftir að kveikt hefur verið á honum.
- Ef gildinu í reitnum **EnableDate** er breytt í dagsetningu fram í tímann er eiginleikinn áætlaður á þeim degi.
- Ef gildinu í reitnum **Virkjað** er breytt í **Já** og gildinu í reitnum **EnableDate** er breytt í dagsetningu fram í tímann er eiginleikinn áætlaður á þeim degi. 
- Ef gildinu í reitnum **Virkjað** er breytt í **Nei** en gildinu í reitnum **EnableDate** er einnig breytt í dagsetningu fram í tímann er eiginleikinn áætlaður á þeim degi.
- Ef kveikt er á eiginleika og bætt er við reit **EnableDate** sem er sett fram í tímann verður áfram kveikt á eiginleikanum. Til að enduráætla eiginleikann er nauðsynlegt að breyta reitnum **Virkjað** í **Nei**.

## <a name="feature-management-and-flighting"></a>Eiginleikastjórnun og tilraunaútgáfa

Eiginleikastjórnun gerir þér kleift að stjórna eiginleikunum sem eru gefnir út í hverri útgáfu. Tilraunaútgáfa gerir Microsoft Teams kleift að gefa út eiginleika til takmarkaðs fjölda viðskiptavina svo hægt sé að prófa og staðfesta þessa eiginleika án þess að hafa áhrif á alla viðskiptavini. Eiginleikastjórnun stýrir ekki tilraunaútgáfu fyrir neina eiginleika.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Að nota eiginleikastjórnun til að kveikja á eiginleika óháðs hugbúnaðarsala eða sérsniðnum eiginleikum

Eiginleikastjórnun er ekki tiltæk sem stendur fyrir eiginleika frá óháðum hugbúnaðarsölum og sérsniðna eiginleika. Hins vegar er Microsoft að bæta við frekari virkni til að bæta eiginleikastjórnun. Eftir að þessum viðbótum er lokið gerir Microsoft eiginleikastjórnun tiltæka fyrir alla eiginleika og býður upp á leiðbeiningar um uppfærslu á eiginleikunum til að nota þær.
