---
title: Eiginleikastjórnunaryfirlit
description: Þetta efni lýsir eiginleikastjórnun og hvernig þú getur notað hana.
author: Peakerbl
ms.date: 01/10/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: c98bdbd64ee5488da20de3f5b23ae18ebce8c23f
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068010"
---
# <a name="feature-management-overview"></a>Eiginleikastjórnunaryfirlit

[!include [banner](../../includes/banner.md)]


[!INCLUDE [PEAP](../../../../includes/peap-1.md)]

Eiginleikum er bætt við og þeir uppfærðir í hverri útgáfu. Upplifun eiginleikastjórnunar veitir vinnusvæði þar sem hægt er að skoða lista yfir eiginleika sem hafa verið gefnir út í hverri útgáfu. Þú getur síðan notað vinnusvæðið til að skoða fylgigögn eiginleika og til að virkja eða slökkva á eiginleikum.

## <a name="the-feature-management-workspace"></a>Vinnusvæði eiginleikastjórnunar

Hægt er að opna vinnusvæðið **Eiginleikastjórnun** með því að velja viðeigandi reit yfirlit. Þú munt sjá síðu sem sýnir lista yfir eiginleika fyrir allar útgáfur sem upplifun eiginleikastjórnunar styður. 

Eiginleikalistinn inniheldur eftirfarandi upplýsingar:

- **Heiti eiginleika** - Lýsing á eiginleika sem var bætt við.
- **Staða** - Tákn tilgreinir hvort kveikt er á eiginleika (gátmerki), slökkt (autt), er áætlað að verði kveikt á (klukka), er áskilið (lás), þarfnast athugunar áður en kveikt er á honum (viðvörunartákn) eða ekki hægt að kveikja á (X). Stillingin sem er sýnd er notuð fyrir alla lögaðila. Athugið að jafnvel þegar kveikt hefur verið á eiginleika er honum samt stjórnað af öryggi. Eiginleikinn verður þar af leiðandi aðeins tiltækur notendum sem eru með aðgang að honum, samkvæmt öryggishlutverki þeirra. Hann verður einnig eingöngu tiltækur í lögaðila sem notandi hefur aðgang að.
- **Virkja dagsetningu** - Dagsetningin þegar kveikt var á eiginleikanum eða verður kveikt á samkvæmt áætlun.
- **Eiginleika bætt við** - Dagsetningin þegar eiginleikanum var bætt við umhverfið þitt. Þessi dagsetning er slegin inn sjálfvirkt þegar umhverfið er uppfært í mánaðarlega útgáfuferlinu.
- **Staða eiginleika** – Núverandi líftímastaða eiginleikans: **Forútgáfa**, **Útgefið** (sýnt sem autt), **Sjálfgefið kveikt** og **Áskilið**. Fjallað er betur um stöðurnar síðar í þessu efnisatriði. 
- **Eining** - Einingin sem nýja útgáfan hefur áhrif á.

> [!NOTE]
> Dálkurinn **Staða eiginleika** fylgir með frá og með útgáfu 10.0.21.

Þegar eiginleiki er valinn birtast meiri upplýsingar á upplýsingasvæðinu hægra megin við eiginleikalistann. Efst á svæðinu sérðu heiti eiginleikans, dagsetningin þegar eiginleikanum var bætt við, einingin sem útgáfan hefur áhrif á og tengilinn **Frekari upplýsingar**. Veljið þennan tengil til að skoða fylgiskjöl útgáfunnar. Ef fylgiskjölin eru ekki tiltæk ferðu yfir á bráðabirgðasíðu. Upplýsingasvæðið inniheldur einnig reitinn **Athugasemdir** þar sem hægt er að bæta við eigin athugasemdum um útgáfuna.

Vinnusvæðið **Eiginleikastjórnun** er einnig með nokkra flipa sem hver um sig sýnir lista yfir eiginleika.

- **Nýtt** - Þessi flipi sýnir alla eiginleika sem hefur verið bætt við frá síðustu mánaðarlegu uppfærslunni. Ef þú hefur sleppt einhverjum mánaðarlegum uppfærslum, sýnir flipinn alla nýja eiginleika sem hefur verið bætt við síðan þú uppfærðir síðast. Nýjustu eiginleikar birtast efst á listanum. Heildarfjöldi nýrra eiginleika er einnig sýndur í reit efst á síðunni.
- **Ekki gert virkt** – Þessi flipi sýnir alla eiginleika sem ekki er kveikt á. Nýjustu eiginleikar birtast efst á listanum. Auk þess sýnir reitur efst á síðunni heildarfjöldi nýrra eiginleika sem er slökkt á sem stendur.
- **Áætlað** - Þessi flipi sýnir alla eiginleika sem áætlað er að verði kveikt á í framtíðinni. Eiginleikarnir sem eru með fyrstu áætluðu dagsetningu birtast efst á listanum. Auk þess sýnir reitur efst á síðunni heildarfjölda tímasettra eiginleika.
- **Allir** - Þessi flipi sýnir alla eiginleika. Nýjustu eiginleikar birtast efst á listanum.

## <a name="feature-states"></a>Stöður eiginleika
Eiginleikar geta færst á milli ýmis konar staða, frá því að vera kynntir í eiginleikastjórnun þar til þeir verða að lokum áskildir í afurðinni. Í þessum hluta eru gildum stöðum eiginleika lýst.

### <a name="preview-features-optional"></a>Forskoðunareiginleikar (valfrjálst)

Afurðarteymi getur ákveðið að láta nýjan eiginleika byrja sem forskoðunareiginleika. Forskoðunareiginleikar eru ekki sjálfkrafa virkjaðir og þeir eru valfrjálsir. Afurðarteymið mun uppfæra eiginleika í útgefna eftir að þeir hafa lokið forskoðunartímabili á fullnægjandi hátt.

> [!NOTE]
> Forskoðunareiginleikar eru háðir sérstökum [skilmálum](https://go.microsoft.com/fwlink/?linkid=2105274) forskoðunar. 

### <a name="released-features-optional"></a>Útgefnir eiginleikar (valfrjálst)

Dálkurinn **Staða eiginleika** fyrir þessa eiginleika er auður. Ekki er sjálfgefið kveikt á eiginleikum sem var bætt við þegar þeir voru gefnir út og það er valfrjálst að virkja þá. Eiginleikar sem eru uppfærðir úr forskoðun munu halda virkri stöðu sinni.

### <a name="on-by-default-features-optional"></a>Eiginleikar sem er sjálfgefið kveikt á (valfrjálst)

Sjálfgefið er kveikt á eiginleikum sem eru uppfærðir í **Sjálfgefið kveikt**, en hægt er að slökkva á þeim. Eftir að eiginleikar sem hægt er að slökkva á hafa verið með stöðuna **Útgefið** í a.m.k. sex mánuði er gert ráð fyrir að þeir fari í þessa stöðu í næstu stóru útgáfu. Gert er ráð fyrir að eiginleikar sem fara yfir í **Sjálfgefið kveikt** verði í efnisatriðinu [Nýjungar](../whats-new-changed.md) fyrir útgáfuna. Uppfærslan er hafin af vöruteymi sem á vöruna.

> [!NOTE]
> Þar sem þessir eiginleikar verða sjálfkrafa virkir er mikilvægt að þú ákveðir hvort fyrirtækið þitt sé tilbúið að taka upp þessa eiginleika, eða hvort þurfti meiri tíma. Ef þörf er á lengri tíma kann að reynast nauðsynlegt að slökkva tímabundið á þessum eiginleikum. Athugaðu að flutningur á eiginleika í **Sjálfgefið kveikt** er yfirleitt gerður í stórri útgáfu áður en stefnt er að því að gera eiginleikann **Áskilinn**. Á þeim tímapunkti verður ekki hægt að slökkva á eiginleikanum. 

### <a name="mandatory"></a>Skylda

**Skylt** er væntanleg lokastaða fyrir eiginleika. Það gefur til kynna að kveikt sé á eiginleikunum og að þú getir ekki slökkt á þeim án þess að hafa samband við Microsoft. Ætla má að valfrjálsir eiginleikar verði áskildir eftir tvær stórar útgáfur. Mikilvægir eiginleikar geta með undantekningu verið kynntir sem áskildir.

## <a name="example-of-expected-feature-lifecycles"></a>Dæmi um væntanlegan stuðningstíma eiginleika

Gert er ráð fyrir að eiginleikar sem hægt er að slökkva á og sem var áður bætt við sem útgefnum og valfrjálsum eða sem hluti af útgáfunni í apríl verði fluttir í **Sjálfgefið kveikt** í útgáfunni fyrir október. Þá er gert ráð fyrir að þeir verðir **Áskildir** í apríl á næsta ári.

Gert er ráð fyrir að eiginleiki sem ekki er hægt að slökkva á og sem var áður bætt við sem útgefnum og valfrjálsum eða sem hluti af útgáfunni í apríl verði fluttir í **Áskilinn** í apríl á næsta ári.

## <a name="enable-a-feature"></a>Virkja eiginleika

Ef ekki hefur verið kveikt á eiginleika birtist hnappurinn **Virkja núna** á upplýsingasvæðinu. Þú getur notað þennan hnapp til að kveikja á aðgerðinni.

Suma eiginleika er ekki hægt að gera óvirka eftir að þeir hafa verið virkjaðir. Ef reynt er að kveikja á eiginleika sem ekki er hægt að virkja birtist viðvörun. Á þessum tímapunkti er hægt að velja **Hætta við** til að hætta við aðgerðina og hafa slökkt á eiginleikanum. Ef hins vegar er valið **Virkja** til að virkja eiginleikann er ekki hægt að gera hann óvirkan seinna.

Sumar aðgerðir sýna skilaboð sem veita frekari upplýsingar áður en þú kveikir á þeim. Þessir eiginleikar eru auðkenndir með gulu viðvörunarmerki. Þú ættir að lesa viðbótarupplýsingarnar vandlega til að skilja betur hvað gerist þegar aðgerðin er virk. Þú getur samt valið **Virkja** til að virkja eiginleikann.

Sumar aðgerðir sýna skilaboð um að ekki sé hægt að virkja aðgerðina fyrr en gripið er til aðgerða. Þessir eiginleikar eru auðkenndir með rauðu X-merki. Þú verður að grípa til aðgerða sem lýst er í lýsingunni áður en aðgerðin er virk. Til dæmis, ef þú getur ekki notað aðgerð fyrr en stillingarlykill er óvirkur, verður þú að slökkva á stillingarlyklinum fyrst og fara síðan aftur í Eiginleikastjórnun til að virkja aðgerðina.

Eftir að eiginleikinn hefur verið virkjaður birtast skilaboð fyrir neðan tengilinn **Frekari upplýsingar** á upplýsingasvæðinu. Þessi skilaboð gefa annaðhvort upp að eiginleikinn hafi verið virkjaður eða gefur til kynna hvenær eiginleikinn verður gerður virkur í framtíðinni. Þau birtast í hvert skipti sem þú velur eiginleikann úr eiginleikalistanum.

Eiginleikar sem áætlað er að virkja í framtíðinni birtast í flipanum **Á áætlun**. Runuvinnsla virkjar þá á miðnætti á tilgreindum degi, sem byggist á tímabeltinu sem kerfisdagsetningin sýnir.

## <a name="reschedule-a-feature"></a>Endurtímasetja eiginleika

Ef áætlað er að kveikja á eiginleika fram í tímann birtist hnappurinn **Áætla** á upplýsingasvæðinu. Hægt er að nota þennan hnapp til að breyta gildinu **Virkja dagsetningu** í aðra dagsetningu.

1. Veljið áætlaðan eiginleika sem á að endurtímasetja og síðan á upplýsingasvæðinu skal velja **Áætla**.
2. Í svarglugganum sem birtist, í reitnum **Virkja dagsetningu** skal tilgreina nýja dagsetningu þegar kveikja skal á eiginleikanum.
3. Veljið **Gera virkt** til að endurtímasetja eiginleikann eða **Gera óvirkt** til að hætta við áætlunina.

## <a name="disable-a-feature"></a>Gera eiginleika óvirkan

Ef eiginleiki hefur verið virkjaður birtist hnappurinn **Gera óvirkt** á upplýsingasvæðinu. Þú getur notað þennan hnapp til að slökkva á aðgerðinni. Hnappurinn **Gera óvirkt** er ekki tiltækur ef ekki er hægt að gera eiginleikann óvirkan. 

Eftir að eiginleikinn hefur verið gerður óvirkur birtast skilaboð fyrir neðan tengilinn **Frekari upplýsingar** á upplýsingasvæðinu. Þessi skilaboð gefa til kynna að eiginleikinn hafi ekki verið virkjaður. Þau birtast í hvert skipti sem þú velur eiginleikann úr eiginleikalistanum. Eiginleikar sem hafa ekki verið virkjaðir birtast í flipanum **Ekki gert virkt**.

## <a name="features-that-must-be-enabled"></a>Eiginleikar sem verða að vera virkir

Stundum verður mikilvægur eiginleiki afhentur sem verður að virkja sjálfkrafa við uppfærslu. Kveikt verður á þessum eiginleikum sjálfkrafa á deginum sem er tilgreindur í reitnum **Virkja dagsetningu**. Fyrir þessa eiginleika birtast skilaboð fyrir neðan tengilinn **Frekari upplýsingar** á upplýsingasvæðinu. Þessi skilaboð gefa annaðhvort upp að eiginleikinn hafi verið virkjaður eða gefur til kynna hvenær eiginleikinn verður gerður virkur í framtíðinni. Þau birtast í hvert skipti sem þú velur eiginleikann úr eiginleikalistanum.

## <a name="enable-all-features"></a>Virkja alla eiginleika

Þú getur virkjað alla eiginleika með því að velja hnappinn **Virkja allt**. 

Þegar þú velur **Virkja allt** birtist valkostur þar sem þú þarft að veita eftirfarandi upplýsingar:

- Listi yfir alla eiginleika sem þarfnast staðfestingar áður en hægt er að virkja þá. Ef þú vilt virkja aðgerðirnar á listanum skaltu velja **Já** fyrir hnappinn **Virkja aðgerðir sem krefjast staðfestingar**.
- Listi yfir alla eiginleika sem ekki er hægt að virkja verður sýndur. Þessir eiginleikar verða ekki gerðir virkir.

Allir aðgerðir sem hægt er að virkja verða gerðar virkar. Ef áætlun er þegar áætluð til að vera virkjuð í framtíðinni breytist áætlunin ekki. 

## <a name="enable-all-features-automatically"></a>Virkja alla eiginleika sjálfkrafa

Ef þú vilt hins vegar kveikja sjálfkrafa á öllum eiginleikum er hægt að nota fellilistann undir titli vinnusvæðis til að breyta því sem gerist þegar nýjum eiginleikum er bætt við.

- Veldu **Virkja nýja eiginleika sjálfkrafa** til að virkja alla eiginleika sjálfkrafa þegar þeim er bætt við umhverfið.
- Veldu **Ekki virkja nýja eiginleika sjálfkrafa** ef allir nýir eiginleikar sem eiga við ættu að vera sjálfgefið slökkt á þegar þeim er bætt við umhverfi þitt.

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

- Ef gildinu í reitnum **Virkjað** er breytt í **Já** verður eiginleikinn virkjaður og reiturinn **Virkja dagsetningu** er stilltur á daginn í dag.
- Ef gildinu í reitnum **Virkjað** er breytt í **Nei** eða reiturinn **EnableDate** er skilinn eftir auður verður eiginleikinn gerður óvirkur og reiturinn **Virkja dagsetningu** er hreinsaður. Ekki er hægt að gera áskilinn eiginleika óvirkan eða eiginleika sem ekki er hægt að gera óvirkan eftir að hann er virkjaður.
- Ef gildinu í reitnum **EnableDate** er breytt í dagsetningu fram í tímann er eiginleikinn áætlaður á þeim degi.
- Ef gildinu í reitnum **Virkjað** er breytt í **Já** og gildinu í reitnum **EnableDate** er breytt í dagsetningu fram í tímann er eiginleikinn áætlaður á þeim degi. 
- Ef gildinu í reitnum **Virkjað** er breytt í **Nei** en gildinu í reitnum **EnableDate** er einnig breytt í dagsetningu fram í tímann er eiginleikinn áætlaður á þeim degi.
- Ef eiginleiki er virkjaður og bætt er við reit **EnableDate** sem er settur fram í tímann verður eiginleikinn áfram virkur. Til að enduráætla eiginleikann er nauðsynlegt að breyta gildinu í reitnum **Virkjað** á **Nei**.

## <a name="feature-management-and-flighting"></a>Eiginleikastjórnun og tilraunaútgáfa

Eiginleikastjórnun gerir þér kleift að stjórna eiginleikunum sem eru gefnir út í hverri útgáfu. Tilraunaútgáfa gerir Microsoft Teams kleift að gefa út eiginleika til takmarkaðs fjölda viðskiptavina svo hægt sé að prófa og staðfesta þessa eiginleika án þess að hafa áhrif á alla viðskiptavini. Eiginleikastjórnun stýrir ekki tilraunaútgáfu fyrir neina eiginleika.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Að nota eiginleikastjórnun til að kveikja á eiginleika óháðs hugbúnaðarsala eða sérsniðnum eiginleikum

Eiginleikastjórnun er ekki tiltæk sem stendur fyrir eiginleika frá óháðum hugbúnaðarsölum og sérsniðna eiginleika. Hins vegar er Microsoft að bæta við frekari virkni til að bæta eiginleikastjórnun. Eftir að þessum viðbótum er lokið gerir Microsoft eiginleikastjórnun tiltæka fyrir alla eiginleika og býður upp á leiðbeiningar um uppfærslu á eiginleikunum til að nota þær.

## <a name="frequently-asked-questions-faq"></a>Algengar spurningar

### <a name="when-are-features-added-removed-or-changed"></a>Hvenær er eiginleikum bætt við, breytt eða þeir fjarlægðir? 
Eiginleikum er bætt við, breytt og þeir fjarlægðir í gegnum breytingar á kóðum sem teymi afurðareiganda gerir. Uppfæra þarf umhverfi til að fá þessar breytingar.

### <a name="does-a-feature-become-mandatory-automatically"></a>Verður eiginleiki áskilinn sjálfkrafa? 
Nei, eiginleiki verður ekki sjálfkrafa skylda. Starfsfólkið sem á vöruna verður að breyta kóðanum.

### <a name="why-isnt-there-a-specific-mandatory-enabled-date"></a>Af hverju er ekki til sérstök „áskilin dagsetning virkjunar“? 
Tímasetning uppfærslu er breytileg, tímasetning á uppfærslu umhverfis er breytileg og viðskiptavinir geta valið um að sleppa sumum uppfærslum. Fyrir vikið er erfitt að ákveða tilteknar dagsetningar. 

### <a name="wheres-the-documentation-for-features-that-are-mandatory"></a>Hvar eru fylgigögnin fyrir eiginleika sem eru áskildir? 
Þessi fylgigögn koma frá hverju teymi Dynamics 365-forrita fyrir sig. Oft eru þessir eiginleikar nefndir í [Uppfærslur á eiginleikastöðum biðlara ](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/updates-client-feature-states) eða [Fjarlægðir eða úreltir eiginleikar](../../../dev-itpro/migration-upgrade/deprecated-features.md). 

### <a name="is-there-an-in-product-notification-or-signal-that-a-feature-is-going-to-be-mandatory-enabled"></a>Er tilkynning um vöru eða merki um að eiginleiki verði áskilið virkjaður? 
Tilkynningakerfi sem tengist því að gera eiginleika áskilinn er ekki til í dag.

### <a name="do-features-ever-get-enabled-without-the-customer-knowing-about-it"></a>Verða eiginleikar einhvern tímann virkjaðir án þess að viðskiptavinurinn viti um það? 
Já, hægt er að virkja eiginleika án vitneskju viðskiptavinar við eftirfarandi aðstæður:
- Eiginleiki er færður í **Sjálfgefið kveikt**. Í þessari stöðu er enn hægt að gera eiginleikann óvirkan. 
- Eiginleiki er uppfærður í **Áskilinn**. Þessi breyting kemur aðeins fram í tengslum við stóra útgáfu. Mikilvægir eiginleikar gætu með undantekningu verið færðir í **Áskilið** við uppfærslu.

### <a name="what-is-feature-flighting-and-how-does-it-relate-to-feature-management"></a>Hvað er tilraunaútgáfa eiginleika og hvernig tengist hún eiginleikastjórnun? 
Tilraunaútgáfur eiginleika eru rauntímaskipting milli kveikt/slökkt sem Microsoft stýrir. Þær eru aðskildar frá stjórnun viðskiptavinar sem eiginleikastjórnun býður upp á. 
- Eiginleikar einkaforskoðunar verða ekki sýndir í eiginleikastjórnun fyrr en þeir tilraunaútgáfa þeirra er gefin út. Við framleiðslu þarf viðskiptavinurinn að samþykkja að vera hluti af sérstakri áætlun til að það geti átt sér stað.
- Opin forútgáfa og útgefnir (almennt í boði) eiginleikar verða sýndir í eiginleikastjórnun nema tilraunaútgáfa sé tekin úr umferð. Að taka tilraunaútgáfu úr umferð er talið síðasta úrræði fyrir vöruteymi ef alvarlegt vandamál kemur upp og venjulega tengt aðgerð viðskiptavinar.

### <a name="do-features-ever-get-flighted-off-without-the-customer-knowing-about-it"></a>Eru eiginleikar einhvern tímann teknir úr umferð án þess að viðskiptavinurinn viti um það? 
Já, ef eiginleikinn hefur áhrif á virkni umhverfis sem þjónar engum tilgangi er hægt að virkja hann að sjálfgefnu.

### <a name="how-can-feature-enablement-be-checked-in-code"></a>Hvernig er hægt að athuga virkjun eiginleika í kóða?
Nota skal aðferðina **isFeatureEnabled** í klasanum **FeatureStateProvider**, láta hana fá tilvik af klasa eiginleikans. Dæmi: 

```xpp
if (FeatureStateProvider::isFeatureEnabled(BatchContentionPreventionFeature::instance()))
```

### <a name="how-can-feature-enablement-be-checked-in-metadata"></a>Hvernig er hægt að athuga virkjun eiginleika í lýsigögnum?
Eiginleikann **FeatureClass** er hægt að nota til að gefa til kynna að einhver lýsigögn tengist eiginleika. Nota ætti klasaheitið fyrir eiginleikann, svo sem **BatchContentionPreventionFeature**. Þetta lýsigögn eru aðeins sýnileg í þessum eiginleika. Eiginleikinn **FeatureClass** er tiltækur í valmyndum, valmyndaratriðum, fasttextagildum og töflu-/yfirlitsreitum.

### <a name="what-is-a-feature-class"></a>Hvað er eiginleikaklasi?
Eiginleikar í eiginleikastjórnun eru skilgreindir sem *eiginleikaklasar*. Klasaeiginleiki **innleiðir IFeatureMetadata** og notar eigind eiginleikaklasans til að gera grein fyrir sér á vinnusvæði eiginleikastjórnunar. Til eru fjölmörg dæmi um eiginleikaklasa sem eru í boði sem hægt er að athuga fyrir virkjun í kóða með því að nota **FeatureStateProvider** API í lýsigögnum með eiginleikanum **FeatureClass**. Dæmi: 

```xpp
[ExportAttribute(identifierStr(Microsoft.Dynamics.ApplicationPlatform.FeatureExposure.IFeatureMetadata))]
internal final class BankCurrencyRevalGlobalEnableFeature implements IFeatureMetadata
```

### <a name="what-is-the-ifeaturelifecycle-implemented-by-some-feature-classes"></a>Hvað er IFeatureLifecycle sem innleitt er af sumum eiginleikaklösum?
IFeatureLifecycle er innri starfsemi Microsoft til að tilgreina stig stuðningstíma eiginleikans. Eiginleikar geta verið:
- `PrivatePreview` - Þarfnast forútgáfu til að vera sýnilegt.
- `PublicPreview` - Sýnt að sjálfgefnu en með viðvörun um að eiginleikinn sé í forútgáfu.
- `Released` - Útgefið að fullu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
