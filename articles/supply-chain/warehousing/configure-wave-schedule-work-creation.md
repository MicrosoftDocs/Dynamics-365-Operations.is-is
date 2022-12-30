---
title: Áætla stofnun vinnu í bylgju
description: Þessi grein lýsir því hvernig á að setja upp og nota vinnsluaðferð bylgju fyrir áætla stofnun vinnu.
author: Mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8b4505d66c37134bc8f672b38d195f4f677df9bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852071"
---
# <a name="schedule-work-creation-during-wave"></a>Áætla stofnun vinnu í bylgju

[!include [banner](../../includes/banner.md)]

Notið eiginleikann *Áætla stofnun vinnu* sem hluta af bylgjuferlinu til að auka gegnumstreymi bylgjuvinnslu með því að láta kerfið stofna vinnu með samhliða vinnslu.

Þegar aðgerðin er virkjuð verður áætluð vinna stofnuð sjálfkrafa sem kerfið mun að lokum vinna úr til að stofna raunverulega vinnu. Ef fjöldi hleðslulína bylgju nær fyrirframskilgreindum þröskuldi mun kerfið stofna raunverulega vinnu á fljótlegri hátt með því að nota samhliða, ósamstillta vinnslu.

## <a name="turn-on-the-scheduled-work-creation-features-in-feature-management"></a>Kveikja á eiginleikum áætlaðrar vinnustofnunar í eiginleikastjórnun

Til að nota eiginleikana sem lýst er í þessari grein verður að kveikja á þeim fyrir kerfið. Notið [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnusvæðið til að kveikja á eftirfarandi eiginleikum í eftirfarandi röð:

1. **Vinnulokun fyrir allt fyrirtækið** - Nauðsynlegt fyrir bæði handvirka og sjálfvirkra grunnstillingu fyrir áætlaða vinnu með áætlaða vinnustofnun. (Frá og með útgáfu 10.0.21 af Supply Chain Management er sjálfkrafa kveikt á þessum eiginleika og ekki er hægt að slökkva á honum aftur.)
1. **Áætla stofnun vinnu** - Nauðsynlegt fyrir bæði handvirka og sjálfvirkra grunnstillingu fyrir áætlaða vinnu með áætlaða vinnustofnun.
1. **Vinnulokun fyrir allt fyrirtækið** - Nauðsynlegt fyrir sjálfvirkra grunnstillingu fyrir áætlaða vinnu með áætlaða vinnustofnun. Ekki þarf að nota þennan eiginleika aðeins er notuð handvirk grunnstilling.

<a name="Auto-enable-schedule-work-creation"></a>

## <a name="automatically-configure-scheduled-work-creation"></a>Skilgreina sjálfkrafa áætlaða vinnustofnun

Ef eiginleikinn *Bylgjuaðferðin „Áætla stofnun vinnu“ fyrir allt fyrirtækið* er virkjaður gerist eftirfarandi sjálfkrafa í kerfinu:

- Bylgjuaðferðinni *Áætla stofnun vinnu* (`WHSScheduleWorkCreationWaveStepMethod`) er bætt við og stillt á að keyra samhliða í öllum lögaðilum.
- Bylgjusniðmát frá öllum lögaðilum sem eru með **Bylgjusniðmátsgerð** stillta á *Afhending* og **Staða sniðmáts** stillt á *Gilt* munu fá aðferðina *Áætla stofnun vinnu* í staðinn fyrir *Stofna vinnu*. Hins vegar verður bylgjusniðmátum frá lögaðilum þar sem endurtaka má aðferðina *Stofna vinnu* ekki breytt.
- Verkskilgreiningar fyrir aðferðina *Áætla stofnun vinnu* verða búnar til fyrir öll vöruhús frá öllum lögaðilum sem eru með **Nota ferli vöruhúsakerfis** virkjað. Þetta þýðir að aðferðin *Áætla stofnun vinnu* muni nú keyra samhliða að sjálfgefnu. Fyrirliggjandi vöruhús þar sem **Nota ferli vöruhúsastjórnunar** er breytt úr *Nei* í *Já* mun einnig keyra þessa aðferð samhliða sjálfkrafa.
- Allir lögaðilar munu vinna úr bylgjum í runum og **Bíða eftir læsingu** verður stillt á sjálfgefna gildið *60.000* ms ef það var áður stillt á *0* ms.
- Öll nýju bylgjusniðmátin sem verða búin til eru með bylgjuaðferðina *Áætla stofnun vinnu* í staðinn fyrir aðferðina *Stofna vinnu*.

Fyrirliggjandi skilgreiningum verks og bylgjuúrvinnslu verður einnig haldið fyrir alla lögaðila sem eru þegar skilgreindir til að vinna úr bylgjum í runum, og fyrir vöruhús sem eru þegar skilgreind til að nota aðferðina *Áætla stofnun vinnu* samhliða.

Ef þörf er á er hægt að snúa við öllum stillingum sem voru gerðar sjálfkrafa þegar eiginleikinn *Bylgjuaðferðin „Áætla stofnun vinnu“ fyrir allt fyrirtækið* var virkjaður með því að gera eftirfarandi:

- Fyrir bylgjusniðmát skal fara í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**. Skipta út aðferðinni *Áætla stofnun vinnu* fyrir *Stofna vinnu*.
- Fyrir færibreytur vöruhúss skal fara í **Vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**. Í flipanum **Bylgjuvinnsla** skal nota æskileg gildi fyrir **Vinna bylgjur í runu** og **Bíða eftir læsingu (ms)**.
- Fyrir bylgjuaðferðir skal fara í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Vinnsluaðferðir bylgju**. Veljið `WHSScheduleWorkCreationWaveStepMethod` og á aðgerðasvæðinu velja **Skilgreining verks**. Breytið eða eyðið fjölda runuverka og úthlutuðum runuflokki fyrir hvert birt vöruhús eftir þörfum.

## <a name="manually-configure-scheduled-work-creation"></a>Skilgreina handvirkt áætlaða vinnustofnun

Ef eiginleikinn [*Bylgjuaðferðin „Áætla stofnun vinnu“ fyrir allt fyrirtækið* eiginleikinn](#Auto-enable-schedule-work-creation) var ekki virkjaður, þá er hægt að nota ferlin sem boðið er upp á í þessum hluta til að skilgreina handvirkt áætlaða stofnun vinnu eftir þörfum.

### <a name="manually-enable-batch-processing-of-waves"></a>Virkja handvirkt runuvinnslur fyrir bylgjur

Til að nýta sér samhliða ósamstillta aðferð til að stofna vöruhúsavinnu verður bylgjuferlið að vera keyrt í runu. Til að setja þetta upp:

1. Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
1. Í flipanum **Almennt** skal stilla **Vinna bylgjur í runu** á *Já*. Einnig er hægt að velja sérstakan **Runuflokk bylgjuvinnslu** til að koma í veg fyrir að úrvinnsla runubiðraðar verði keyrð á sama tíma og önnur ferli.
1. Stillið **Biðtími læsingar (ms)** sem verður notaður þegar kerfið vinnur úr nokkrum bylgjum samtímis. Fyrir flest stærri bylgjuferli er mælt með gildinu *60000*.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>Virkja nýja bylgjuskrefsaðferð handvirkt fyrir fyrirliggjandi bylgjusniðmát

Byrjið á því að stofna nýja bylgjuskrefsaðferð og virkið hana fyrir ósamstillta verkvinnslu.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Vinnsluaðferðir bylgju**.
1. Veljið **Endurgera aðferð** og athugið að *WHSScheduleWorkCreationWaveStepMethod* hefur verið bætt við listann yfir aðferðir bylgjuferlis sem hægt er að nota í bylgjusniðmátum sendingar.
1. Veljið færsluna með **Heiti aðferðar** *WHSScheduleWorkCreationWaveStepMethod* og veljið **Verkskilgreiningu**.
1. Til að bæta nýrri línu við hnitanetið skal velja **Ný** á aðgerðasvæðinu og nota eftirfarandi stillingar:

    - **Vöruhús** - Veljið vöruhúsið sem nota á til að tímasetja vinnslu á stofnun vinnu.
    - **Hámarksfjöldi runuverka** - Tilgreinið hámarksfjölda runuverka. Í flestum tilfellum ætti þetta gildi að vera á bilinu 8-16, hins vegar mælum við með því að þið prófið ykkur áfram til að finna út bestu stillinguna fyrir ykkar aðstæður.
    - **Runuflokkur bylgjuvinnslu** - Veljið sérstakan runuflokk bylgjuvinnslu til að fínstilla vinnslu runubiðraðar.

Nú er hægt að uppfæra fyrirliggjandi bylgjusniðmát (eða búa til nýtt) til að nota bylgjuvinnsluaðferðina *Áætla stofnun vinnu*.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Á listasvæðinu skal velja bylgjusniðmátið sem á að uppfæra (ef verið er að prófa með sýnigögnum, þá er hægt að nota *24 Sjálfgefin sending*).
1. Stækkið flýtiflipann **Aðferðir** og veljið línuna með **Heitinu** *Áætla stofnun vinnu* í hnitanetinu **Eftirstandandi aðferðir**.
1. Veljið örina sem vísar í **Valdar aðferðir** til að fara valda línu í þeim dálki. (Aðeins er hægt að hafa eina valda aðferð í einu sem notar annaðhvort `WHSScheduleWorkCreationWaveStepMethod` eða `createWork` þannig að fyrirliggjandi lína með **Heiti aðferðar** `createWork` færist sjálfkrafa í hnitanetið **Eftirstandandi aðferðir**.)

## <a name="set-wave-task-processing-threshold-data"></a>Stilla þröskuldsgögn fyrir úrvinnslu bylgjuverks

Kerfið stofnar sjálfgefin þröskuldsgögn fyrir úrvinnslu bylgjuverks í fyrsta skipti sem bylgjuferli er keyrt með því að nota einhverja verktengda vinnslu. Gögnin eru notuð til að stjórna því hvenær bylgjuvinnsla mun keyra ósamstillt og vera tengd verki, sem gerir henni kleift að vinna úr og stofna vinnu samhliða.

Sjálfgefin gögn munu í upphafi nota þröskuldsgildið 15 fyrir lágmarksfjölda hleðslulína (`MINIMUMWAVELOADLINES`). Þetta þýðir að þegar kerfið vinnur úr bylgju með fleiri en 15 hleðslulínum notar það ósamstæða verkvinnslu. Hægt er að setja inn/uppfæra þessi gögn handvirkt í `WHSWaveTaskProcessingThresholdParameters` töflunni í prófunarumhverfinu. Ef breyta þarf þessari stillingu í vinnsluumhverfi verður að hafa samskipti við notendaþjónustu Microsoft til að óska eftir uppfærslunni.

## <a name="work-with-the-scheduled-work-creation"></a>Vinna með áætlaða vinnustofnun

Frekari upplýsingar um hvernig á að vinna með áætlaða stofnun vinnu er að finna í [Stofnun og meðhöndlun bylgju](wave-processing.md). 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
