---
title: Staðsetningarleiðbeiningar fyrir aldursgreiningu birgðatínslu
description: Þetta efnisatriði útskýrir hvernig á að nota fyrst inn, fyrst út (FIFO) og síðast inn , fyrst út (LIFO) aðferðir staðsetningarleiðbeiningarinnar við tiltekt.
author: Mirzaab
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSWorkTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 229dd0033e3eae4bdd33acca6736b7a9feec8c9b
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676272"
---
# <a name="location-directive-inventory-picking-aging"></a>Staðsetningarleiðbeiningar fyrir aldursgreiningu birgðatínslu

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að nota fyrst inn, fyrst út (FIFO) og síðast inn , fyrst út (LIFO) aðferðir staðsetningarleiðbeiningarinnar við tiltekt. Þessar aðferðir vinna saman með aldursdagsetningarnar sem eru skráðar fyrir staðsetningar til að rekja þegar birgðir voru fyrst færðar inn í vöruhúsið. Eiginleikinn *Staðsetningarleiðbeining fyrir aldursgreiningu birgðatínslu* notar dagsetningu í staðsetningunni til að ákvarða aldur. Eiginleikinn *Staðsetningarstaða vöruhúss* uppfærir dagsetninguna í staðsetningunni út frá dagsetningunni í númeraplötunni.

Hægt er að nota FIFO og LIFO-áætlanir til að senda bæði runuraktar vörur og ekki runuraktar vörur, byggt á dagsetningunni þegar birgðir voru færðar inn í vöruhúsið. Þessi eiginleiki getur verið mjög gagnlegur fyrir birgðir án runurakningar þar sem enga lokadagsetningu er hægt að nota til að raða eftir.

Þegar birgðir eru fyrst mótteknar eða stofnaðar í vöruhúsi uppfærir kerfið viðeigandi númeraplötu þannig að núverandi dagsetning er sýnd sem aldursdagsetning. Þessi dagsetning er síðan notuð af áætlunum staðsetningarleiðbeiningar til að finna elstu eða nýjustu birgðirnar í vöruhúsinu. Ef birgðir eru fluttar á staðsetningu sem er ekki rakin af númeraplötu er staðsetningin sjálf uppfærð með upplýsingum um aldur og þessar upplýsingar verða svo notaðar af áætlunum.

## <a name="turn-on-the-feature"></a>Kveikja á eiginleikanum

Til að gera þennan eiginleika tiltækan skaltu kveikja á eftirfarandi eiginleika í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) í þessari röð:

1. Staðsetningarstaða vöruhúss
1. Staðsetningarleiðbeiningar fyrir aldursgreiningu birgðatínslu

## <a name="feature-requirements"></a>Kröfur eiginleika

Til að nota þennan eiginleika verður að stilla valkostinn **Virkja staðsetningarstöðu** á *Já* fyrir allar [staðsetningarforstillingar](tasks/create-location-profile.md) sem notaðar eru til að geyma birgðir. Til að stilla þennan valkost fyrir staðsetningarforstillingu skal fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Staðsetningarforstillingar** og velja staðsetningarforstillinguna. Hægt er að finna valkostinn í flýtiflipanum **Almennt**.

## <a name="feature-scenarios"></a>Aðstæður eiginleika

Í þessum hluta eru dæmi sem sýna hvernig á að setja upp og nota FIFO og LIFO áætlanir.

> [!TIP]
> Þessi hluti býður upp á tvær aðstæður, eina fyrir FIFO og eina fyrir LIFO. Aðferðirnar sem eru veittar gera ráð fyrir að þú gerir báðar aðstæðurnar, í röð. Mælt er með því að gera báðar aðstæðurnar þannig að hægt sé að upplifa muninn á milli þeirra tveggja.

### <a name="make-sample-data-available"></a>Gera sýnigögn tiltæk

Til að vinna í gegnum þessar sýniaðstæður með því að nota sýniskrárnar og sýnigildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu [sýnigögnin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

Einnig er hægt að nota þessa atburðarás sem leiðsögn fyrir notkun eiginleikans í framleiðslukerfi. Hins vegar, í því tilfelli, verður að skipta út eigin gildi fyrir hverja stillingu sem er lýst hér.

### <a name="set-up-the-scenarios"></a><a name="demo-set-up"></a>Setja upp aðstæður

Sýnigögnin útheimta uppsetningu og leiðréttingu birgða til að styðja við aðstæðurnar. Fylgið þessum skrefum til að stofna birgðagögn sem þarf til að vinna sig í gegnum FIFO og LIFO-aðstæður.

1. Skráðu þig inn í kerfið þar sem sýnigögnin eru uppsett og veldu lögaðilann **USMF**.
1. Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Veldu **FLOOR-05** á lista staðsetningarforstillinga.
1. Á flýtiflipanum **Almennt** skaltu stilla valkostinn **Virkja staðsetningarstöðu** á *Já*.
1. Veljið **Vista**.
1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Í listanum yfir staðsetningarleiðbeiningar skal velja **63 Tiltekt gámunar**.
1. Veldu **Breyta** til að setja síðuna í breytingastillingu.
1. Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal finna línuna þar sem reiturinn **Raðnúmer** er stilltur á *1* og fylgja einu af þessum skrefum:

    - Ef verið er að setja upp FIFO-aðstæður skal breyta gildinu í reitnum **Áætlun** í *FIFO aldursgreining staðsetningar*.
    - Ef verið er að setja upp LIFO-aðstæður skal breyta gildinu í reitnum **Áætlun** í *LIFO aldursgreining staðsetningar*.

1. Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn**.
1. Í svarglugga fyrirspurnar, í flipanum **Svið**, skal velja **Bæta við** til að bæta við línu og síðan stilla eftirfarandi gildi:

    - **Tafla:** *Staðir*
    - **Afleidd tafla:** *Staðsetningar*
    - **Reitur::** *Auðkenni svæðis*
    - **Skilyrði:** *Gólf*

1. Veldu **Í lagi** til að nota stillingarnar þínar og loka fyrirspurnarritilinum.
1. Smelltu á **Vista** til að vista breytingar á staðsetningarleiðbeiningunum þínum.
1. Í fartæki eða í forritinu *Dynamics 365 for Finance and Operations -Vöruhúsakerfi* í tölvunni skal fylgja þessum skrefum til að fjarlægja núverandi birgðir úr staðsetningu vöruhússins til að styðja við aðstæðurnar:

    1. Skráðu þig inn í vöruhús *63* með því að nota viðeigandi notandakenni og aðgangsorð.
    1. Í aðalvalmyndinni skal velja **Gæði**.
    1. Í valmyndinni **Gæðastjórnun** skal velja **Rýrnun**.
    1. Á síðunni **Rýrnun** skal velja reitinn **STAÐ/NP** og síðan slá inn *63\_1*.
    1. Veljið **Enter** eða **Í lagi**.
    1. Staðfestið upplýsingar um **Rýrnun** fyrir **Leiðrétting út** með því að velja **Enter** eða **Í lagi**.

    Þegar birgðir númeraplötunnar eru leiðréttar verða skilaboðin „Vinnu lokið“ send.

    Þessi skref skilja birgðir eftir á tveim stöðum í sýnigögnunum. Hver staðsetning er með aðra aldursdagsetningu. Staðsetning *FL-001* er með aldursdagsetningu 15. apríl 2017 og staðsetningu *FL-002* er með aldursdagsetningu 29. janúar 2017. Báðar staðsetningar innihalda vöru *A0001*.

    Til að skoða þessi gögn skal fara í **Birgðastjórnun \> Fyrirspurnir og skýrslur \> Listi á lager** og síðan sía vöruhús *63* og vöru *A0001*. Í línunum þar sem reiturinn **Staðsetning** er stilltur á *FL-001* eða *FL-002* skal velja línu sem er með jákvætt gildi fyrir **Efnislegar birgðir** og síðan, á aðgerðasvæðinu, skal velja **Færslur**. Reiturinn **Efnisleg dagsetning** mun sýna dagsetningu sem samsvarar einni af áðurnefndu aldursdagsetningum.

### <a name="scenario-1-set-up-and-use-fifo-location-aging"></a><a name="fifo-demo"></a>Aðstæður 1: Setja upp og nota FIFO aldursgreining staðsetningar

FIFO-aðferðin finnur staðsetningu sem inniheldur elstu aldursdagsetninguna og hún úthlutar tiltekt eftir þessari aldursdagsetningu.

1. Ef þú hefur ekki enn gert þetta, skaltu [undirbúa sýnigögnin](#demo-set-up) sem þurfa að vera fyrir þessar aðstæður.
1. Opnið **Sala og markaðssetning \> Sölupöntun \> Allar sölupantanir**.
1. Veljið **Nýtt**.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - Í flipanum **Viðskiptavinur** skaltu stilla reitinn **Reikningur viðskiptavinar** á *US-001*.
    - Í flýtiflipanum **Almennt** skal stilla reitinn **Vöruhús** á *63*.

1. Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.
1. Ný sölupöntun opnast. Hún felur í sér nýja, auða línu í hnitanetinu á flipanum **Sölupöntunarlínur**. Fyrir þessa pöntunarlínu skal stilla reitinn **Vörunúmer** á *A0001* og reitinn **Magn** á *1*.
1. Á valmyndinni **Birgðir** fyrir ofan hnitanetið smellir þú á **Frátekning**.
1. Í síðunni **Frátekning** skal velja **Frátektarlota** til að taka frá pantað magn af þessari vöru úr birgðum á völdu vöruhúsi.
1. Lokaðu síðunni **Frátekning**.
1. Á **Sölupöntun** síðunni, á aðgerðarrúðunni, á **Vöruhús** flipanum, í **Aðgerðir** hópnum, veldu **Losa í vöruhús**. Þú færð upplýsingaboð. Kerfið stofnar sendingu, bætir henni við nýja hleðslu og stofnar nauðsynlega vinnu.
1. Í flýtiflipanum **Sölupöntunarlínur**, í valmyndinni **Vöruhús**, skal velja **Upplýsingar um vinnu** til að opna vinnu sem var stofnuð fyrir þessa sölupöntun. Takið eftir að línan þar sem gildið **Vinnugerð** er *Tiltekt* sýnir gildi fyrir **Staðsetningu** á *FL-002*. Þessi staðsetning inniheldur númeraplötuna sem er með elstu aldursdagsetninguna (FIFO).
1. Veljið **Vöruhús \> Upplýsingar sendingar**.
1. Í flýtiflipanum **Almennt** skal punkta niður bylgjukennið svo hægt sé að nota það í aðstæðum 2.

### <a name="scenario-2-set-up-and-use-lifo-location-aging"></a>Aðstæður 2: Setja upp og nota LIFO aldursgreining staðsetningar

FIFO-aðferðin finnur staðsetningu sem inniheldur nýjustu aldursdagsetninguna og hún úthlutar tiltekt eftir þessari aldursdagsetningu. Í aðstæðum 2 munt þú breyta uppsetningunni fyrir aðstæður 1 (FIFO) og nota aftur sölupöntunina og bylgjuna sem voru stofnaðar í þeim aðstæðum.

1. Áður en hafist er handa með þessa atburðarás skal setja upp og ljúka FIFO-aðstæðunum eins og lýst er í [fyrri kafla](#fifo-demo). Í þessu dæmi notar þú aftur bylgjuna og stóran hluta uppsetningarinnar sem búin var til fyrir þessar aðstæður.
1. Breytið staðsetningarleiðbeiningunni **63 Tiltekt gámunar** svo hún noti aðferðina *LIFO aldursgreining staðsetningar*, eins og lýst er í fyrsta hluta ferlisins [Setja upp aðstæðurnar](#demo-set-up).

    Næst verður bylgjunni breytt sem stofnuð var fyrir sölupöntunina í aðstæðum 1, þannig að hún noti aðferðina *LIFO aldursgreining staðsetningar*.

1. Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.
1. Veldu og opnaðu bylgjuna sem inniheldur pöntunina sem var stofnuð fyrir FIFO-aðstæðurnar.
1. Á aðgerðasvæðinu, í flipanum **Vinna**, skal velja **Hætta við** til að hætta við vinnuna sem var stofnuð fyrir FIFO-aðstæðurnar.
1. Í Aðgerðasvæði, á flipanum **Bylgja** í hópnum **Bylgja** skal velja **Ferli**.
1. Þegar ferlinu er lokið, á Aðgerðasvæðinu, í flipanum **Bylgja**, í flokknum **Tengdar upplýsingar**, skal velja **Vinna** til að skoða vinnuna sem var búin til fyrir þessa bylgju.
1. Á síðunni **Vinna**, í flipanum **Yfirlit**, ættu að vera tvær línur. Veldu línuna þar sem svæðið **Vinnustaða** er stillt á *Opin*.
1. Takið eftir að línan þar sem gildið **Vinnugerð** er *Tiltekt* sýnir gildi fyrir **Staðsetningu** á *FL-001*. Þessi staðsetning inniheldur númeraplötuna sem er með nýjasta aldursdagsetninguna (LIFO).

Í þessum aðstæðum hefurðu séð hvernig aðferð aldursgreiningar staðsetningar stýrir vinnu á birgðastaðsetninguna sem er annaðhvort með elstu birgðirnar eða þær nýjustu, fer eftir því hvor aðferðin er valin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]