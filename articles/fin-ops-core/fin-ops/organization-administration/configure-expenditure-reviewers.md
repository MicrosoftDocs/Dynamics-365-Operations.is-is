---
title: Skilgreina skoðunarmenn útgjalda
description: Í þessu efnisatriði er lýst hvernig eigi að nota skoðunarmenn útgjalda til að velja á gagnvirkan hátt notandann sem fær úthlutað verkflæði, samþykki eða handvirka ákvörðun.
author: rachel-profitt
ms.date: 06/25/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2021-06-24
ms.openlocfilehash: b0de3d9280c43fc7e2bb2568d4a57250da4dfebf
ms.sourcegitcommit: 9f3b6c00f82694b5f8eb1bda75411801c0fccf4a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2021
ms.locfileid: "6315680"
---
# <a name="configure-expenditure-reviewers"></a>Skilgreina skoðunarmenn útgjalda
[!include[banner](../includes/banner.md)]

Hægt er að setja upp gagnvirka skoðunarmenn útgjalda til að senda útgjöld til endurskoðunar samkvæmt annaðhvort notandanum sem fær verkhlutverki úthlutað eða fjárhagsvíddinni þar sem útgjöldin eru gjaldfærð. Verkflæðisferlið notar tilgreindan eiganda verkhlutverks eða fjárhagsvíddar til að ákvarða hvert á að senda útgjöldin.

Hægt er að tilgreina eina eða fleiri skilgreiningar skoðunarmanns útgjalda og síðan velja skilgreiningu þegar verkflæði er stofnað. Hægt er að skilgreina gildi skoðunarmanns útgjalda fyrir hvern lögaðila í fyrirtækinu. Eftir að skilgreining skoðunarmanns útgjalda hefur verið skilgreind má úthluta skilgreiningunni. Hægt er að úthluta skoðunarmönnum útgjalda á verkferla, samþykki og handvirkar ákvarðanir.

> [!NOTE]
> Þótt skoðunarmenn útgjalda séu ekki áskildir geta þeir stuðlað að einfaldari skilgreiningu á verkflæði. Til dæmis þarf ekki að búa til eina skilyrta ákvörðun til að athuga hverja vídd kostnaðarstaðar og síðan búa til aðra einingu til að úthluta samþykkinu eða verkinu á tiltekinn notanda eða hóp notenda. Þess í stað er hægt að skilgreina eiganda kostnaðarstaðarvíddarinnar og nota skoðunarmann útgjalda til að velja réttan notanda á gagnvirkan hátt. Á þennan hátt, þegar eignarhald eða úthlutun kostnaðarstaða breytist, verður þú bara að uppfæra reitinn **Eigandi** fyrir fjárhagsvíddina.

## <a name="types-of-expenditure-reviewers"></a>Gerðir skoðunarmanna útgjalda

Ekki öll verkflæði styðja hugmyndina á bak við skoðunarmenn útgjalda. Hægt er að skilgreina skoðunarmenn útgjalda sjálfgefið fyrir innkaupabeiðnir, innkaupapantanir, lánardrottinsreikninga og kostnaðarskýrslur. Allar þessar verkflæðisgerðir þurfa á skilgreiningu skoðunarmanna útgjalda að halda á aðskildri síðu sem er tilheyrir eiginleikanum og einingunni. Fyrir hvert skjal sem stutt er hægt að nota skoðunarmenn útgjalda með annaðhvort verkflæði á hausstigi eða línustigi.

Eftirfarandi tafla sýnir hvert á að fara til að skilgreina skoðunarmann útgjalda fyrir hvert stutt skjal.

| Skjal | Slóð |
|----------|-----------------|
| Kostnaðarskýrslur | Útgjaldastýring \> Uppsetning \> Reglur \> Skoðunarmenn útgjalda |
| Innkaupapantanir | Innkaup og aðföng \> Uppsetning \> Reglur \> Skoðunarmenn útgjalda vegna innkaupapöntunar |
| Innkaupabeiðnir | Innkaup og aðföng \> Uppsetning \> Reglur \> Skoðunarmenn útgjalda vegna innkaupabeiðni |
| Reikningar frá lánardrottni | Viðskiptaskuldir \> Uppsetning reglu \> Skoðunarmenn útgjalda vegna reiknings lánardrottins |

## <a name="expenditure-reviewer-assignments"></a>Úthlutanir skoðunarmanna

Tvær gerðir úthlutanna eru í boði fyrir hvern skoðunarmann útgjalda: *verkdreifingar* og *dreifingar fyrirtækis*. Fyrir verkdreifingu er hægt að velja á milli verkyfirvalda og fjárhagsvídda. Fyrir dreifingu fyrirtækis er hægt að velja fjárhagsvíddir.

Verkyfirvald felur í sér verkefnisstjóra, ábyrgðaraðila verkefnis og sölustjóra verkefnis. Þú skilgreinir þessi yfirvöld beint í verkinu þínu með því að velja starfsmann í viðeigandi reitum.

Fjárhagsvíddum er stýrt með lykilskipulaginu í hverjum lögaðila. Fyrir hvern lögaðila er hægt að velja hvaða fjárhagsvíddir verða notaðar með skoðunarmanni útgjalda. Víddirnar geta annaðhvort komið frá verkinu (ef víddirnar eru valdar í flipanum **Dreifingar verks**) eða skjalinu (ef víddirnar eru valdar í flipanum **Dreifingar fyrirtækis**). Í reitnum **Eigandi** á síðunni **Gildi fjárhagsvídda** er hægt að velja starfsmann fyrir hverja fjárhagsvídd.

## <a name="example-1-expenditure-reviewers-based-on-organization-distributions"></a>Dæmi 1: Skoðunarmenn útgjalda samkvæmt dreifingum fyrirtækis

Þú vinnur fyrir Contoso Appliances og fyrirtækið er með sex deildir og 10 kostnaðarstaði. Þegar ný innkaupabeiðni er send inn þarf samþykki að koma fyrst frá deildarstjóra og síðan frá framkvæmdastjóra kostnaðarstaðar.

Í þessum dæmi verða tveir *skoðunarmenn útgjalda vegna innkaupabeiðni* skilgreindir:

- Fyrir fyrri skoðunarmanninn er heiti deildarinnar gefið upp og síðan fjárhagsvíddin **Deild** valin í flipanum **Dreifingar fyrirtækis**. 
- Fyrir seinni skoðunarmanninn er heiti kostnaðarstaðarins gefið upp og síðan fjárhagsvíddin **Kostnaðarstaður** valin í flipanum **Dreifingar fyrirtækis**.

Þegar verkflæðið er skilgreint er tvö samþykktarskref búin til. Það fyrra er fyrir deildina og það seinna er fyrir kostnaðarstaðinn. Fyrir hvora samþykktareiningu skal velja **Þátttakanda** í reitnum **Úthlutunargerð** í flipanum **Byggt á hlutverki**, velja **Þátttakendur í útgjöldum** í reitnum **Gerð þátttakanda** og síðan velja viðeigandi þátttakanda í reitnum **Þátttakandi**.

Þegar innkaupabeiðnin er búin til er fjárhagsvíddum deildar og kostnaðarstaðar úthlutað á línur innkaupabeiðninnar. Þegar verkflæðið er sent inn leggur kerfið fyrst mat á deildina í innkaupabeiðninni og úthlutar samþykktareiningunni á notandann sem tengist starfsmanninum sem var valinn fyrir deildina. Þegar fyrra samþykktarskrefinu er lokið leggur kerfið mat á seinna samþykktarskrefið og úthlutar seinni samþykktareiningunni á notandann sem tengist starfsmanninum sem var valinn fyrir kostnaðarstaðinn.

## <a name="example-2-expenditure-reviewers-based-on-project-distributions"></a>Dæmi 2: Skoðunarmenn útgjalda samkvæmt dreifingum verks

Þú vinnur fyrir þjónustudeild Contoso Appliances. Fyrirtækið gerir kröfu um að verkefnisstjórinn fyrir hverja innkaupapöntun verði að samþykkja útgjöldin. Auk þess verður yfirmaður kostnaðarstaðar fyrir verkið að samþykkja þau. Samþykktirnar er hægt að gera samtímis. Í hvoru tilfellinu sem er, þá verða báðir notendurnir að samþykkja innkaupapöntunina áður en verkflæðið getur haldið áfram.

Í þessu dæmi skal útbúa einn *skoðunarmann útgjalda vegna innkaupapöntunar* sem heitir **Verkefnastjóri og kostnaðarstaður**. Þú velur gátreitinn **Verkefnastjóri** og stillir valkostinn **Vídd kostnaðarstaðar** á **Já** í flipanum **Dreifingar verks** á síðunni **Skoðunarmaður útgjalda vegna innkaupapöntunar**. Sem hluti af uppsetningunni verður þú að tryggja að reiturinn fyrir **Verkefnastjóra** sé stilltur fyrir öll verk og að eigandi sé tilgreindur fyrir alla kostnaðarstaði á síðunni **Gildi fjárhagsvídda**.

Þegar verkflæðið er skilgreint þarf eina samþykktareiningu. Þú velur **Þátttakanda** í reitnum **Úthlutunargerð**. Í flipanum **Byggt á hlutverki** skal síðan velja **Þátttakendur í útgjöldum** í reitnum **Gerð þátttakanda** og velja verkefnisstjórann og kostnaðarstaðinn í reitnum **Þátttakandi**. Til að tryggja að verkflæðið geti ekki haldið áfram fyrr en bæði verkefnastjóri og eigandi kostnaðarstaðar samþykkja verkflæðið skal stilla reitinn **Regla um lok** á **Allir samþykktaraðilar**.

Þegar innkaupapöntunin er stofnuð verður að tilgreina reitinn **Verk**. Ef þú þarft ekki verk fyrir allar innkaupapantanirnar ættirðu að bæta skilyrtri ákvörðun við verkflæðið til að athuga verk áður samþykktarskrefið er keyrt. Kerfið metur síðan verkið sem er tilgreint fyrir innkaupapöntunina og úthlutar samþykktareiningunni á notandann sem tengist starfsmanninum í reitnum **Verkefnastjóri**. Að auki býr kerfið til verk og úthlutar því á notandann sem tengist starfsmanninum sem þú velur í reitnum **Eigandi** fyrir kostnaðarstaðinn í verkinu. Athugaðu að þetta dæmi notar kostnaðarstað verksins, ekki kostnaðarstað innkaupapöntunarinnar.

## <a name="set-up-expenditure-reviewers"></a>Setja upp skoðunarmenn útgjalda

Þetta dæmi sýnir hvernig á að skilgreina skoðunarmann útgjalda vegna innkaupabeiðni. Til að skilgreina aðrar gerðir af skoðunarmönnum útgjalda skal skipta út slóðinni í skrefi 1 fyrir viðeigandi slóð úr töflunni í hlutanum [Gerðir skoðunarmanna útgjalda](configure-expenditure-reviewers.md#types-of-expenditure-reviewers) fyrr í þessu efnisatriði.

1. Farðu í **Innkaup og aðföng \> Uppsetning \> Reglur \> Skoðunarmenn útgjalda vegna innkaupabeiðni**.
2. Á síðunni **Skoðunarmenn útgjalda vegna innkaupabeiðni** skal velja **Nýr**.
3. Í reitinn **Heiti** skal slá inn heiti á skilgreiningu skoðunarmanns útgjalda, t.d. **kostnaðarstaður**.
4. Í flýtiflipanum **Skoðunarmenn útgjalda eftir lögaðila** skal velja lögaðilann sem á að skilgreina.
5. Fyrir dreifingu verks skal velja gátreitinn fyrir hvert verkyfirvald og velja **Já** fyrir hverja fjárhagsvídd sem á að virkja. 
6. Fyrir dreifingu fyrirtækis, í flipanum **Dreifingar fyrirtækis**, skal velja **Já** fyrir hverja fjárhagsvídd sem á að virkja.
7. Endurtakið skref 4 til 6 fyrir hvern lögaðila til viðbótar.

## <a name="assign-owners-to-financial-dimensions"></a>Úthluta eigendum á fjárhagsvíddir

Til að úthluta eiganda á fjárhagsvídd skal fylgja þessum skrefum.

1. Farðu í **Fjárhagur \> Bókhaldslyklar \> Víddir \> Fjárhagsvíddir**.
2. Í listanum skal velja fjárhagsvíddina sem úthluta á eigendum á.
3. Veldu **Víddargildi**.
4. Veldu **Breyta** til að gera breytingar á víddargildunum.
5. Í listanum skal velja víddargildið sem á að fá eiganda úthlutaðan.
6. Í reitnum **Eigandi** skal velja starfsmanninn sem á að fá víddargildinu úthlutað.

## <a name="configure-project-distributions"></a>Skilgreina verkdreifingar

Til að úthluta verkyfirvöldum á verk skal fylgja þessum skrefum.

1. Opnaðu **Verkefnastjórnun og bókhald \> Verk \> Öll verk**.
2. Veldu verkið sem á að fá úthlutað yfirvaldi.
3. Veldu **Breyta** til að gera breytingar á verkinu.
4. Í flýtiflipanum **Almennt**, í hlutanum **Ábyrgur**, skal velja starfsmann fyrir reitina **Sölustjóri**, **Verkefnastjóri** og **Stjórnandi verks** eftir þörfum.
5. Í flýtiflipanum **Fjárhagsvíddir** skal velja nauðsynlegar fjárhagsvíddir fyrir verkið.

## <a name="assign-expenditure-reviewers-to-a-workflow-task"></a>Úthluta skoðunarmönnum útgjalda á verkflæðisverk

Þetta dæmi sýnir hvernig á að skilgreina verkflæði innkaupabeiðni þannig að það noti skoðunarmann útgjalda vegna innkaupabeiðni. Til að skilgreina aðrar gerðir af verkflæðum gæti verkflæðissíðan sem þarf að opna í skrefi 1 í einingunni **Útgjaldastýring** eða **Viðskiptaskuldir** í staðinn fyrir einingunni **Innkaup og aðföng**.

Til að úthluta skoðunarmönnum útgjalda vegna innkaupabeiðni á verkflæðisverk skal fylgja þessum skrefum:

1. Opnið **Innkaup og aðföng \> Uppsetning \> Verkflæði innkaupa og aðfanga**.
2. Pikkaðu tvisvar (eða tvísmelltu) á fyrirliggjandi verkflæði eða búðu til nýtt verkflæði.
3. Í verkflæðisritlinum, í glugganum **Verkflæði**, skal velja verkið sem á að fá úthlutaða skilgreiningu skoðunarmanns útgjalda. Á **Aðgerðarsvæðinu** í hópnum **Sýna** skal síðan velja **Eiginleikar**.
4. Vinstra megin á síðunni **Eiginleikar** skal velja **Úthlutun**.
5. Í flipanum **Úthlutunargerð** skal velja **Þátttakandi**.
6. Í flipanum **Byggt á hlutverki**, í reitnum **Gerð þátttakanda**, skal velja **Þátttakendur í útgjöldum**. Í reitnum **Þátttakandi** skal síðan velja skilgreiningu skoðunarmanns útgjalda til að nota í verkflæðisverkinu.
