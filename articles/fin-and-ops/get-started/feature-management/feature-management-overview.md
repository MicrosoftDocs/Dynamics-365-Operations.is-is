---
title: Eiginleikastjórnunaryfirlit
description: Þetta efnisatriði lýsir eiginleika eiginleikastjórnunar og hvernig hægt er að nota hann.
author: mikefalkner
manager: AnnBe
ms.date: 04/18/2019
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
ms.openlocfilehash: e75e42926db22d4fccda86c755b12d9d121a9c0e
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538693"
---
# <a name="feature-management-overview"></a>Eiginleikastjórnunaryfirlit

[!include[banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Eiginleikum er bætt við og þeir uppfærðir í hverri útgáfu af Microsoft Dynamics 365 for Finance and Operations. Upplifun eiginleikastjórnunar veitir vinnusvæði þar sem hægt er að skoða lista yfir eiginleika sem hafa verið gefnir út í hverri útgáfu. Sjálfgefið er að slökkt sé á nýjum eiginleikum. Hægt er að nota vinnusvæðið til að kveikja á þeim og skoða fylgiskjölin fyrir þá.

## <a name="the-feature-management-workspace"></a>Vinnusvæði eiginleikastjórnunar

Hægt er að opna vinnusvæðið **Eiginleikastjórnun** með því að velja viðeigandi reit yfirlit. Þú munt sjá síðu sem sýnir lista yfir eiginleika fyrir allar útgáfur sem upplifun eiginleikastjórnunar styður. Með tímanum mun Microsoft auka upplifun eiginleikastjórnunar svo hún innihaldi viðbótarvirkni til að hjálpa til við stjórnun eiginleika.

Eiginleikalistinn inniheldur eftirfarandi upplýsingar:

- **Heiti eiginleika** - Lýsing á eiginleika sem var bætt við.
- **Virkjuð staða** - Tákn gefur til kynna hvort eiginleiki hefur verið virkjaður (gátmerki), ekki virkjaður (autt), ráðgert að virkja (klukka) eða er virkjaður handvirkt (lás). Stillingin sem er sýnd hér er notuð fyrir alla lögaðila. Athugið að jafnvel þegar kveikt hefur verið á eiginleika er honum samt stjórnað af öryggi. Eiginleikinn verður þar af leiðandi aðeins tiltækur notendum sem eru með aðgang að honum, samkvæmt öryggishlutverki þeirra. Hann verður einnig eingöngu tiltækur fyrir lögaðila sem notandi hefur aðgang að.
- **Virkja dagsetningu** - Dagsetningin þegar kveikt var á eiginleikanum eða verður kveikt á ef dagsetningin er fram í tímann.
- **Eiginleika bætt við** - Dagsetningin þegar eiginleikanum var bætt við umhverfið þitt. Þessi dagsetning er slegin inn sjálfvirkt þegar umhverfið er uppfært í mánaðarlega útgáfuferlinu.
- **Eining** - Einingin sem nýja útgáfan hefur áhrif á.

Þegar eiginleiki er valinn birtast viðbótarupplýsingar á upplýsingasvæðinu hægra megin við eiginleikalistann. Efst á svæðinu sérðu heiti eiginleikans, dagsetningin þegar eiginleikanum var bætt við, einingin sem útgáfan hefur áhrif á og tengilinn **Frekari upplýsingar**. Veljið þennan tengil til að skoða fylgiskjöl útgáfunnar. Ef fylgiskjölin eru ekki tiltæk ferðu yfir á bráðabirgðasíðu. Upplýsingasvæðið inniheldur einnig reitinn **Athugasemdir** þar sem hægt er að bæta við eigin athugasemdum um útgáfuna.

Vinnusvæðið **Eiginleikastjórnun** inniheldur einnig ýmsa flipa sem geyma lista yfir eiginleika. 
- **Nýtt** - Sýnir alla eiginleika sem hefur verið bætt við frá síðustu mánaðarlegu uppfærslunni. Ef einhverjum mánaðarlegum uppfærslum hefur verið sleppt inniheldur hún alla nýju eiginleikana frá síðasta skipti sem var uppfært. Nýjustu eiginleikar birtast efst á listanum. Heildarfjöldi nýrra eiginleika er einnig sýndur í reit efst á síðunni.
- **Ekki gert virkt** - Sýnir alla eiginleika sem hafa ekki verið gerðir virkir. Nýjustu eiginleikar birtast efst á listanum. Heildarfjöldi nýrra eiginleika er einnig sýndur í reit efst á síðunni.
- **Á áætlun** - Sýnir alla eiginleika sem áætlað er að verði gerðir virkir á dagsetningu fram í tímann. Eiginleikarnir sem eru með fyrstu áætluðu dagsetningu birtast efst á listanum. Heildarfjöldi nýrra eiginleika er einnig sýndur í reit efst á síðunni.
- **Allt** - Sýnir alla eiginleika. Nýjustu eiginleikar birtast efst á listanum.


## <a name="enable-a-feature"></a>Virkja eiginleika

Ef eiginleiki hefur ekki verið virkjaður birtist hnappurinn **Virkja** á upplýsingasvæðinu. Þú getur notað þennan hnapp til að kveikja á aðgerðinni.

1. Veljið eiginleikann sem á að virkja og síðan á upplýsingasvæðinu skal velja **Virkja**.
2. Sleði birtist þar sem hægt er að tilgreina dagsetningu þegar virkja á eiginleika. Sjálfgefið er að þessi dagsetning sé stillt á núverandi dagsetningu.
3. Veljið **Virkja** til að virkja eiginleikann.

Suma eiginleika er ekki hægt að gera óvirka eftir að þeir hafa verið virkjaðir. Ef ekki er hægt að gera eiginleika óvirkan sem verið er að reyna að virkja, birtist aðvörun. Á þessum tímapunkti er hægt að velja **Hætta við** til að hætta við aðgerðina og skilija eiginleikann eftir óvirkan. Ef hins vegar er valið **Virkja** og eiginleikinn er virkjaður er ekki hægt að gera hann óvirkan seinna.

Eftir að eiginleikinn hefur verið virkjaður birtast skilaboð fyrir neðan tengilinn **Frekari upplýsingar** á upplýsingasvæðinu. Þessi skilaboð gefa annaðhvort upp að eiginleikinn hafi verið virkjaður eða gefur til kynna hvenær eiginleikinn verður gerður virkur í framtíðinni. Ef notuð er framtíðardagsetning verður eiginleikinn birtur á listanum **Á áætlun**. Þessi skilaboð birtast í hvert skipti sem eiginleikinn er valinn úr eiginleikalistanum. Eiginleikar sem eru áætlaðir fram í tímann verða virkjaðir á miðnætti af runuvinnslu samkvæmt tímabeltinu sem kerfisdagsetningin sýnir. 

## <a name="reschedule-a-feature"></a>Endurtímasetja eiginleika

Ef eiginleiki hefur verið virkjaður fram í tímann birtist hnappurinn **Endurtímasetja** á upplýsingasvæðinu. Hægt er að nota þennan hnapp til að breyta **Virkja dagsetningu** í aðra dagsetningu.

1. Veljið áætlaðan eiginleika sem á að endurtímasetja og síðan á upplýsingasvæðinu skal velja **Endurtímasetja**.
2. Sleði birtist þar sem hægt er að tilgreina dagsetningu þegar virkja á eiginleika. 
3. Veljið **Gera virkt** til að endurtímasetja eiginleikann eða **Gera óvirkt** til að hætta við áætlunina.

## <a name="disable-a-feature"></a>Gera eiginleika óvirkan

Ef eiginleiki hefur þegar verið virkjaður birtist hnappurinn **Gera óvirkt** á upplýsingasvæðinu. Þú getur notað þennan hnapp til að slökkva á aðgerðinni. Hnappurinn **Gera óvirkt** er ekki tiltækur ef ekki er hægt að gera eiginleikann óvirkan eftir að hann hefur verið virkjaður.

- Veljið eiginleikann sem á að gera óvirkan og síðan á upplýsingasvæðinu skal velja **Gera óvirkt**.

- Aðgerðin er óvirk og dagsetningin er hreinsuð.

Eftir að eiginleikinn hefur verið gerður óvirkur birtast skilaboð fyrir neðan tengilinn **Frekari upplýsingar** á upplýsingasvæðinu. Þessi skilaboð gefa til kynna að eiginleikinn hafi ekki enn verið gerður óvirkur og hann muni birtast á listanum **Ekki gert virkt**. Skilaboðin birtast í hvert skipti sem eiginleikinn er valinn úr eiginleikalistanum.

## <a name="features-that-must-be-enabled"></a>Eiginleikar sem verða að vera virkir

Hugsanlega verður mikilvægur eiginleiki afhentur sem verður að virkja sjálfkrafa við uppfærslu. Hann verður virkjaður sjálfkrafa í **Virkja dagsetningu**. Skilaboð birtast fyrir neðan tengilinn **Frekari upplýsingar** á upplýsingasvæðinu. Þessi skilaboð gefa til kynna að eiginleikinn verði gerður virkur eða óvirkur sjálfkrafa í **Virkja dagsetningu**. Skilaboðin birtast í hvert skipti sem eiginleikinn er valinn úr eiginleikalistanum.

## <a name="assigning-roles"></a>Úthlutun á hlutverkum

Kerfisstjórar geta opnað vinnusvæðið **Eiginleikastjórnun** og einnig notendur sem er úthlutað hlutverkunum Eiginleikastjóri eða Eiginleikabirtir sem voru stofnuð til að styðja upplifun eiginleikastjórnunar. Notendur í hlutverki eiginleikastjórnunar geta kveikt og slökkt á hvaða eiginleikum sem er. Þeir geta einnig uppfært athugasemdahlutann fyrir eiginleikann. Notendur í hlutverkinu Eiginleikabirtir geta einungis skoðað vinnusvæðið **Eiginleikstjórnun**. Þeir geta ekki kveikt eða slökkt á eiginleikum.

Hlutverkin Eiginleikastjóri og Eiginleikabirtir hnekkja ekki fyrirliggjandi öryggi sem notar hefur. Hlutverkin stýra aðeins aðgangi að því að virkja eiginleika. Þau veita ekki aðgang að sjálfum eiginleikunum.

## <a name="using-feature-management-to-enable-isv-features-or-custom-features"></a>Að nota eiginleikastjórnun til að virkja eiginleika óháðs hugbúnaðarsala eða sérsniðna eiginleika

Ferli eiginleikastjórnunar er ekki í boði sem stendur fyrir eiginleika óháðs hugbúnaðarsala eða sérsniðna eiginleika. Verið er að bæta við viðbótarvirkni til að endurbæta Eiginleikastjórnun og þegar þessum endurbótum er lokið verður eiginleikastjórnun opnuð fyrir alla eiginleika veita tilteknar leiðbeiningar um hvernig eigi að uppfæra eiginleikann til að nota hann.

## <a name="feature-management-and-flighting"></a>Eiginleikastjórnun og tilraunaútgáfa

Eiginleikastjórnun gerir þér kleift að stjórna eiginleikum sem eru afhentir í hverri útgáfu. Tilraunaútgáfa gerir Microsoft-teyminu kleift að gefa út eiginleika til takmarkaðs fjölda viðskiptavina svo hægt sé að prófa og staðfest eiginleikana án þess að hafa áhrif á alla viðskiptavini. Eiginleikastjórnun stýrir ekki tilraunaútgáfu fyrir neina eiginleika.
