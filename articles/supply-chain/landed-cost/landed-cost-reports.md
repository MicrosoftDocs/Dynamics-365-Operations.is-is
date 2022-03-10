---
title: Skýrslur heildarkostnaðar
description: Þetta efnisatriði lýsir því hvernig á að finna og nota ýmsar gerðir skýrslna sem eru í boði fyrir Heildarkostnaður eininguna.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: cb0ea44c0924fc5d2c295a9285701d1f678c3473
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571738"
---
# <a name="landed-cost-reports"></a>Skýrslur heildarkostnaðar

[!include [banner](../../includes/banner.md)]

## <a name="outstanding-invoices"></a>Ógreiddir reikningar

Skýrsla um ógreidda reikninga inniheldur lista yfir alla ógreidda reikninga á ýmsum kostnaðarstigum sem tengjast hverri ferð. Hún er notuð til að afstemma ferð og kostnað ferðar ásamt lista yfir fjárhagsfærslur með reglulegu millibili. Þegar sameiginlegur kostnaður hefur verið reikningsfærður er hann fjarlægður úr skýrslunni.

Til að búa til skýrslu um ógreidda reikninga skal fylgja þessum skrefum.

1. Farið í **Heildarkostnaður \> Skýrslur \> Rakning \> Ógreiddir reikningar**.
1. Í svarglugganum **Ógreiddir reikningar**, í reitnum **Á dagsetningu**, skal tilgreina dagsetningu. Allir reikningar sem voru ógreiddir á eða fyrir þann dag verða hafðir með í úttakinu.
1. Undir **Sýna** skal velja einn af eftirfarandi valkostum:

    - **Kostnaður ekki reikningsfærður** – Hafið með kostnað vegna reikningsfærðra sendinga sem eru með áætlað kostnaðarvirði en engan raunverulegan kostnað.
    - **Birgðir ekki reikningsfærðar** – Hafið með kostnað sem hefur verið reikningsfærður, en innkaupapöntunin hefur ekki enn verið móttekin.
    - **Allt ekki reikningsfært** – Hafið með niðurstöður fyrir bæði valkostinn **Kostnaður ekki reikningsfærður** og valkostinn **Birgðir ekki reikningsfærðar**.

1. Stillið valkostinn **Taka með nýjan kostnað** á *Já* til að hafa með kostnað sem er ekki enn kominn með raunverulegan kostnað og þær birgðir hafa ekki enn verið mótteknar. Ef það er stillt á *Nei* mun skýrslan aðeins taka til kostnaðar sem hefur verið reikningsfærður.
1. Í hlutanum **Yfirlit** skal virkja þær tegundir upplýsinga sem á að hafa með í skýrslunni.
1. Eins og gert er fyrir aðrar skýrslugerðir í Microsoft Dynamics 365 Supply Chain Management skal nota flýtiflipann **Áfangastaður** til að velja úttakssnið skýrslunnar.
1. Eins og gert er fyrir aðrar skýrslugerðir í Supply Chain Management skal nota flýtiflipann **Færslur til að taka með** til að takmarka færslurnar enn frekar sem verða hafðar með í skýrslunni.
1. Veldu **Í lagi** til að stofna skýrsluna.

## <a name="activityprovider-analysis-reports"></a>Greiningarskýrslur verkþáttar/veitu

Greiningarskýrslur verkþáttar/veitu gera kleift að fara yfir nákvæmni tímaáætlana fyrir hverja veitu.

Til að búa til greiningarskýrslu verkþáttar/veitu skal fylgja þessum skrefum.

1. Fylgja skal einu af þessum skrefum, eftir því hvaða gerð skýrslna á að stofna:

    - Farið í **Heildarkostnaður \> Skýrslur \> Greining á verkþætti/veitu eftir verkþætti**. Í þessu tilfelli verða línuáætlanir flokkaðar eftir verkþætti.
    - Farið í **Heildarkostnaður \> Skýrslur \> Greining á verkþætti/veitu eftir veitu**. Í þessu tilfelli verða línuáætlanir flokkaðar eftir veitu.

    Annaðhvort birtist svarglugginn **Greining á verkþætti/veitu eftir verkþætti** eða svarglugginn **Greining á verkþætti/veitu eftir veitu**. Báðir svargluggarnir bjóða upp á sömu valkostina.

1. Eins og gert er fyrir aðrar gerðir skýrslna í Supply Chain Management skal nota flýtiflipann **Áfangastaður** til að velja úttakssnið skýrslunnar.
1. Eins og gert er fyrir aðrar skýrslugerðir í Supply Chain Management skal nota flýtiflipann **Færslur til að taka með** til að takmarka færslurnar enn frekar sem verða hafðar með í skýrslunni.
1. Veldu **Í lagi** til að stofna skýrsluna.

## <a name="voyage-costing-reports"></a>Skýrsla um kostnað ferðar

Skýrslur um kostnað ferðar sýna kostnað varanna og innflutningskostnað á fólíó, gám eða ferð eftir því hvaða valkostir eru valdir þegar skýrslan er sett saman. Í hverri skýrslu um kostnað ferðar er hægt að skoða áætlaðan kostnað ferðar í samanburði við raunverulegan kostnað og hægt er að sundurliða hann eftir ýmsum auðkennandi þáttum.

Til að búa til kostnaðarskýrslu ferðar fylgirðu þessum skrefum.

1. Fylgja skal einu af þessum skrefum, eftir því hvaða gerð skýrslna á að stofna:

    - Farið í **Heildarkostnaður \> Skýrslur \> Kostnaðarútreikningur \> Kostnaður ferðar eftir einstökum kostnaði**. Í þessu tilfelli mun valkostur fyrir einstakan kostnað sýna innflutningskostnað á kostnaðarþátt fyrir hvern kóða kostnaðargerðar.
    - Farið í **Heildarkostnaður \> Skýrslur \> Kostnaður \> Kostnaður ferðar eftir skýrslugerðarflokki**. Í þessu tilfelli verður innflutningskostnaðurinn sundurliðaður í ýmsa skýrslugerðarflokka. Kostnaðargerðir eru flokkaðar eftir skýrslugerðarflokkum.

    Annaðhvort birtist svarglugginn **Kostnaður ferðar eftir einstökum kostnaði** eða svarglugginn **Kostnaður ferðar eftir skýrslugerðarflokki**. Þessir svargluggar eru svipaðir. Allur munur er tekinn fram í því sem eftir er af þessu ferli.

1. Ef svarglugginn **Kostnaður ferðar eftir skýrslugerðarflokki** í reitnum **Kostnaður** opnaður skal velja eitt af eftirfarandi gildum:

    - **Kostnaðarvirði** – Gildið er annaðhvort reiknað með því að nota sjálfvirkan kostnað eða stofnað handvirkt í kostnaðarsvæðinu.
    - **Áætlað** – Eftir að vörurnar hafa verið mótteknar er áætlaður kostnaður stilltur.
    - **Raunverulegt** – Þegar pöntunin hefur verið reikningsfærð er raunverulegur kostnaður stilltur á kostnað í reikningnum.
    - **Besta** – Kerfið mun nota einn af þremur fyrrnefndu valkostum eftir því hver er nákvæmastur. (Mælt er með að velja þennan valkost.)

1. Stillið valkostinn **Eftir vöru** á *Já* til að sýna kostnað eftir vöru. Stillið það á *Nei* til að sýna kostnað á hverja ferð.
1. Í hlutanum **Yfirlit** skal velja flokkana til að sundurliða kostnað eftir.
1. Í hlutanum **Víddir** skal velja víddirnar sem hafa á með í skýrslunni.
1. Eins og gert er fyrir aðrar gerðir skýrslna í Supply Chain Management skal nota flýtiflipann **Áfangastaður** til að velja úttakssnið skýrslunnar.
1. Eins og gert er fyrir aðrar skýrslugerðir í Supply Chain Management skal nota flýtiflipann **Færslur til að taka með** til að takmarka færslurnar enn frekar sem verða hafðar með í skýrslunni.
1. Veldu **Í lagi** til að stofna skýrsluna.

## <a name="shipping-container-receipts-list"></a>Komulisti yfir gáma

Komulisti yfir gáma inniheldur allt magn sem ekki hefur verið móttekið og er á lokadag á eða fyrir áætlaða dagsetningu. Starfsmenn í vöruhúsi geta notað þessa skýrslu til að bera kennsl á væntanlegar vörur í gámi. Einnig er hægt að nota hana til að staðfesta vörur handvirkt þegar þær eru mótteknar í gámi.

Til að búa til komulista yfir gáma skal fylgja þessum skrefum.

1. Farið í **Heildarkostnaður \> Skýrslur \> Rakning \> Komulisti yfir gáma**.
1. Í svarglugganum **Komulisti yfir gáma**, í reitnum **Væntanleg dagsetning**, skal tilgreina dagsetningu. Magn sem var ekki búið að móttaka á eða fyrir þá dagsetningu verður haft með í úttakinu.
1. Í hlutanum **Víddir** skal velja víddirnar sem hafa á með í skýrslunni.
1. Eins og gert er fyrir aðrar gerðir skýrslna í Supply Chain Management skal nota flýtiflipann **Áfangastaður** til að velja úttakssnið skýrslunnar.
1. Eins og gert er fyrir aðrar skýrslugerðir í Supply Chain Management skal nota flýtiflipann **Færslur til að taka með** til að takmarka færslurnar enn frekar sem verða hafðar með í skýrslunni.
1. Veldu **Í lagi** til að stofna skýrsluna.

## <a name="expected-delivery-report"></a>Skýrsla um væntanlegar afhendingar

Skýrsla um væntanlegar afhendingar inniheldur grunnupplýsingar um ferð, gám, fólíó, vörur og væntanlega dagsetningu afhendingar.

Til að búa til skýrslu um væntanlega afhendingu skal fylgja þessum skrefum.

1. Farið í **Heildarkostnaður \> Skýrslur \> Rakning \> Áætluð afhending**.
1. Í svarglugganum **Væntanleg afhending**, í reitnum **Væntanleg dagsetning**, skal velja dagsetninguna þegar búist er við að afhending á vörum í vöruhús á áfangastað eigi sér stað. Allar línur ferðar sem er með væntanlega dagsetningu á eða fyrir þá dagsetningu og sem hafa ekki enn verið mótteknar verða hafðar með í úttakinu.
1. Valfrjálst: Í reitnum **Lánardrottnalykill** skal velja lánardrottnalykil til að hafa aðeins með afhendingar frá ákveðnum lánardrottni.
1. Í hlutanum **Víddir** skal velja víddirnar sem hafa á með í skýrslunni.
1. Eins og gert er fyrir aðrar gerðir skýrslna í Supply Chain Management skal nota flýtiflipann **Áfangastaður** til að velja úttakssnið skýrslunnar.
1. Eins og gert er fyrir aðrar skýrslugerðir í Supply Chain Management skal nota flýtiflipann **Færslur til að taka með** til að takmarka færslurnar enn frekar sem verða hafðar með í skýrslunni.
1. Veldu **Í lagi** til að stofna skýrsluna.
