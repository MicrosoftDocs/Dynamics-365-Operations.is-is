---
title: Hafist handa með skattaútreikning
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp skattaútreikning.
author: wangchen
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b180a8cee1c5b7e9dda837915e6fdf94af30d06a
ms.sourcegitcommit: 8246ba3872a1f3eaa18c8bb1ba86d3c2142a6e10
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/31/2021
ms.locfileid: "7465078"
---
# <a name="get-started-with-tax-calculation"></a>Hafist handa með skattaútreikning

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Þetta efnisatriði veitir upplýsingar um hvernig hafist er handa við skattaútreikning. Það leiðir þig í gegnum grunnstillingarskrefin í Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS) Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Það fer síðan yfir almennu leiðina til að nota möguleika skattaútreiknings í færslum Finance og Supply Chain Management.

Þessi uppsetning samanstendur af fjórum meginskrefum:

1. Í LCS skal setja upp innbót skattaútreiknings.
2. Í RCS skal setja upp eiginleika skattaútreiknings. Þessi uppsetning á ekki við um neinn sérstakan lögaðila. Hægt er að nota hana í öllum lögaðilum í Finance og Supply Chain Management.
3. Í Finance og Supply Chain Management skal setja upp færibreytur skattaútreiknings eftir lögaðila.
4. Í Finance og Supply Chain Management skal stofna færslur á borð við sölupantanir og nota skattaútreikning til að ákvarða og reikna skatta.

## <a name="prerequisites"></a>Forkröfur

Áður en hægt er að klára ferlin í þessu efnisatriði þurfa eftirfarandi skilyrði að vera til staðar fyrir hverja gerð umhverfis.

### <a name="for-a-production-environment"></a>Fyrir vinnsluumhverfi

Fyrir vinnsluumhverfi þarf að uppfylla eftirfarandi skilyrði:

- Þú verður að hafa aðgang að LCS-reikningnum þínum og þú verður að hafa virkjað LCS-verk með umhverfi í lagi 2 (eða ofar) sem keyrir Dynamics 365 útgáfu 10.0.21 eða nýrri.
- Þú verður að búa til RCS umhverfi fyrir fyrirtækið og þú verður að hafa aðgang að reikningnum þínum. Nánari upplýsingar um hvernig á að stofna RCS-umhverfi er að finna í [Yfirlit Regulatory configuration service](rcs-overview.md).
- Kveikja þarf á eftirfarandi eiginleikum á vinnusvæðinu **Eiginleikastjórnun** ef þú settir upp umhverfi Finance eða Supply Chain Management eftir því hverjar rekstrarþarfir þínar eru:

    - Skattaútreikningsþjónusta
    - Styðja mörg VSK-skráningarnúmer
    - Skattar í flutningspöntun

- Kveikja þarf á eftirfarandi eiginleikum á vinnusvæðinu **Eiginleikastjórnun** fyrir uppsett RCS-umhverfi.

    - Altækir eiginleikar

### <a name="for-a-test-environment-public-preview"></a>Fyrir prófunarumhverfi (opin forútgáfa)

Fyrir prófunarumhverfi þarf að uppfylla eftirfarandi skilyrði:

- Þú verður að hafa aðgang að LCS-reikningnum þínum og þú verður að hafa virkjað LCS-verk með umhverfi í lagi 2 (eða ofar) sem keyrir Dynamics 365 útgáfu 10.0.21 eða nýrri.
- Þú verður að búa til RCS umhverfi fyrir fyrirtækið og þú verður að hafa aðgang að reikningnum þínum. Nánari upplýsingar um hvernig á að stofna RCS-umhverfi er að finna í [Yfirlit Regulatory configuration service](rcs-overview.md).
- Þú hafðir samband við Microsoft með því að senda póst á <taxcalc@microsoft.com> til að virkja forútgáfuna í uppsettu umhverfi þínu af Finance eða Supply Chain Management.
- Kveikja þarf á eftirfarandi eiginleikum á vinnusvæðinu **Eiginleikastjórnun** ef þú settir upp umhverfi Finance eða Supply Chain Management eftir því hverjar rekstrarþarfir þínar eru:

    - Skattaútreikningsþjónusta
    - Styðja mörg VSK-skráningarnúmer
    - Skattar í flutningspöntun

- Kveikja þarf á eftirfarandi eiginleikum á vinnusvæðinu **Eiginleikastjórnun** fyrir uppsett RCS-umhverfi.

    - Altækir eiginleikar

## <a name="set-up-tax-calculation-in-lcs"></a>Setja upp skattaútreikning í LCS

1. Skráðu þig inn í [LCS](https://lcs.dynamics.com)
2. Ljúkið uppsetningunni fyrir Microsoft Power Platform-samþættingu. Frekari upplýsingar er að finna í [Yfirlit innbóta](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Veljið eitt af uppsettu umhverfunum og veljið því næst **Setja upp nýja innbót**.
4. Veljið **Skattaútreikningur**.
5. Lesið og samþykkið skilmálana og veljið því næst **Setja upp**.

## <a name="set-up-tax-calculation-in-rcs"></a>Setja upp skattaútreikning í RCS

Skrefin í þessum hluta eru ekki tengd við sérstakan lögaðila. Aðeins þarf að ljúka þessu ferli einu sinni og hægt er að ljúka því í hvaða lögaðila sem er í RCS.

1. Skráðu þig inn í [RCS](https://marketing.configure.global.dynamics.com/).
2. Á vinnusvæðinu **Rafræn skýrslugerð**, skal bæta við nýrri skilgreiningarveitu. Notið heiti fyrirtækisins sem heiti veitunnar. Nánari upplýsingar er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Veljið skilgreiningarveituna sem var stofnuð og veljið síðan **Stilla sem virkt**.
4. Veljið skilgreiningarveituna **Microsoft** og veljið því næst **Geymslur**.
5. Í reitnum **Gerð** skal velja **Altæk**.
6. Veljið **Opna**.
7. Opnið **Gagnalíkan skatts**, stækkið skráartréð, og veljið síðan **Skattaskilgreining**.
8. Veldu rétta útgáfu skattaskilgreiningar samkvæmt útgáfu þinni af Finance og veldu svo **Flytja inn**.

    | Losunarútgáfa | Skattafbrigði                       |
    | --------------- | --------------------------------------- |
    | 10.0.18         | Skattstillingar - Evrópa 30.12.82     |
    | 10.0.19         | Skattaútreikningsstilling 36.38.193 |
    | 10.0.20         | Skattaútreikningsstilling 40.43.208 |
    | 10.0.21         | Skattaútreikningsstilling 40.46.212 |

9. Á vinnusvæðinu **Altækir eiginleikar** skal velja **Eiginleikar**, velja reitinn **Skattaútreikningur** og veljið því næst **Bæta við**.
10. Velja eina af eftirfarandi gerðum eiginleika:

    - **Nýr eiginleiki** – Búa til uppsetningu eiginleika sem er með tómt innihald.
    - **Byggt á fyrirliggjandi eiginleika** – Búa til eiginleika úr fyrirliggjandi eiginleika og afrita innihaldið úr fyrirliggjandi eiginleikauppsetningu.

11. Færið inn heiti og lýsingu á eiginleikanum og veljið svo **Stofna eiginleika**.

    Þegar eiginleikinn hefur verið búinn til verða útgáfudrög hans sjálfkrafa búin til. Þú getur valið **Sækja þessa útgáfu** til að endurreikna drögin á hvaða lokinni útgáfu sem er.

12. Veldu drög eiginleikans og svo **Breyta**. Fyllt er í síðuna **Uppsetning skattaútreiknings**.
13. Veljið **Útgáfa skilgreiningar**. Þú ættir að sjá grunnstillingarútgáfuna sem þú fluttir inn í skrefi 8.

    Microsoft veitir sjálfgefna skattaskilgreiningu fyrir skattaútreikning. Þessi skilgreining nær yfir flestar kröfur varðandi hegðun skattaútreikningsins. Hún verður uppfærð út frá ábendingum markaðarins. Ef ætlunin er að stækka skilgreininguna þannig að hún uppfylli tilteknar kröfur skal skoða [Hvernig á að smíða viðbót í skattþjónustu](./tax-service-add-data-fields-tax-integration-by-extension.md) til að fá upplýsingar um hvernig á að búa til og velja sína eigin skattaskilgreiningu.

14. Þegar **Útgáfa skilgreiningar** hefur verið valin birtast nokkrir flipar til viðbótar. Fylgdu röðinni sem birtist hér til að ljúka áskilinni uppsetningu flipa.

    **Áskilin uppsetning**

    - **Skattkóðar** – Vinna með aðalgögn fyrir skattkóða. Allir skattkóðar sem eru búnir til í þessum flipa eru sjálfkrafa samstilltir við Finance þegar núverandi útgáfa er virkjuð.
    - **Skattflokkur** – Skilgreindu aðalgögn skattflokks og skattkóða undir flokknum.
    - **Skattflokkur vöru** – Skilgreindu aðalgögn skattflokks fyrir vöru og skattkóða undir flokknum.

    **Valfrjáls uppsetning**

    - **Gildissvið skattflokks** – Skilgreindu fylki sem ákvarðar skattflokkinn. Ef engar gildissviðsreglur í þessu fylki passa við skattskylda skjalið úr Dynamics 365 notar skattaútreikningur sjálfgefið gildi í línu skattskylds skjals.
    - **Gildissvið skattflokks vöru** – Skilgreindu fylki sem ákvarðar skattflokk vöru. Ef engar gildissviðsreglur í þessu fylki passa við skattskylda skjalið úr Dynamics 365 notar skattaútreikningur sjálfgefið gildi í línu skattskylds skjals.
    - **Gildissvið skattskráningarnúmers viðskiptavinar** – Ef þú ert með mörg skattskráningarnúmer fyrir einn viðskiptavin getur skattaútreikningur sjálfkrafa fundið út rétt skattskráningarnúmer. Í fylki þessa flipa eru reglurnar skilgreindar sem ætti að nota til að taka ákvörðunina. Annars munu Finance og Supply Chain Management halda áfram að nota sjálfgefið skattskráningarnúmerí skattskyldum skjölum fyrir sölufærslur.
    - **Gildissvið skattskráningarnúmers lánardrottins** – Ef þú ert með mörg skattskráningarnúmer fyrir einn lánardrottin getur skattaútreikningur sjálfkrafa fundið út rétt skattskráningarnúmer. Í fylki þessa flipa eru reglurnar skilgreindar sem ætti að nota til að taka ákvörðunina. Annars munu Finance og Supply Chain Management halda áfram að nota sjálfgefið skattskráningarnúmerí skattskyldum skjölum fyrir innkaupafærslur.
    - **Gildissvið listakóða** – Finndu sjálfkrafa gildið í reitnum **Listakóði** í gegnum sveigjanlegri og stillanlegri reglur. Í fylki þessa flipa eru reglurnar skilgreindar sem ætti að nota til að taka ákvörðunina. Annars munu Finance og Supply Chain Management halda áfram að nota sjálfgefinn kóða í skattskyldum skjölum.

14. Í flipanum **Skattkóðar** skal velja **Bæta við** og slá inn skattkóðann og lýsingu.
15. Veljið **Skatthluti**. Skatthlutinn er safn af útreikningsaðferðum sem var skilgreint í fyrri útgáfu valdrar skattaskilgreiningar. Eftirfarandi skatthlutar eru í boði:

    - Eftir nettóupphæð
    - Eftir brúttóupphæð
    - Eftir magni
    - Eftir framlegð
    - Skattur á skatt

16. Veljið **Vista**. Fleiri reitir verða tiltækir samkvæmt skatthlutanum sem var valinn.
17. Notið eftirfarandi valkosti til að gera grein fyrir eðli skattkóðans:

    - Er undanskilið
    - Er notkunarskattur
    - Er bakfært gjald
    - Undanskilja úr útreikningi grunnupphæðar

    Fyrir aðstæður neysluskatts skal setja upp einn skattkóða sem er með jákvætt skatthlutfall og merkja hann sem **Er neysluskattur**.

    Fyrir aðstæður bakfærðs gjalds skal setja upp tvo skattkóða, einn sem er með jákvætt skatthlutfall og annan sem er með neikvætt skatthlutfall en sama hlutfallið. Merkið neikvæða skattkóðann sem **Er bakfært gjald**. Frekari upplýsingar um lausn bakfærðs gjalds í Finance er að finna í [Virkni bakfærðs gjalds fyrir skema VSK/VÞS](emea-reverse-charge.md).

    Fyrir sumar skattgerðir sem á að undanskilja frá útreikningnum á skattgrunnupphæð fyrir færslur með verði (t.d. toll í sumum löndum og landsvæðum) skal velja gátreitinn **Undanskilja frá útreikningi grunnupphæðar**. Frekari upplýsingar um þessa færibreytu er að finna í [Reikna skatt ofan á verð þegar „Verð með sköttum“ er virkt](global-exclude-from-tax-base-amount-calculation.md).

    Viðhaldið mörkum skatthlutfalla og skattupphæðar fyrir þennan skattkóða.

18. Endurtakið skref 14 til 17 til að bæta við öllum öðrum nauðsynlegum skattkóðum.
19. Í flipanum **Skattflokkur** skal velja dálkinn **Skattflokkur**, bæta honum við fylkið sem skilyrði innsláttar og síðan bæta við línum til að vinna með aðalgögn skattflokksins.

    Eftirfarandi er dæmi.

    | Skattflokkur    | Skattkóðar           |
    | ------------ | ------------------- |
    | DEU_Domestic | DEU_VAT19; DEU_VAT7 |
    | DEU_EU       | DEU_Exempt          |
    | BEL_Domestic | BEL_VAT21; BEL_VAT6 |
    | BEL_EU       | BEL_Exempt          |

20. Í flipanum **Skattflokkur vöru** skal velja dálkinn **Skattflokkur vöru**, bæta honum við fylkið sem skilyrði innsláttar og síðan bæta við línum til að vinna með aðalgögn skattflokks vöru.

    Eftirfarandi er dæmi.

    | VSK-flokkur | Skattkóðar                                    |
    | -------------- | -------------------------------------------- |
    | Fullt           | DEU_VAT19; BEL_VAT21; DEU_Exempt; BEL_Exempt |
    | Lækkað        | DEU_VAT7; BEL_VAT6; DEU_Exempt; BEL_Exempt   |

21. Í flipanum **Gildissvið skattflokks** skal velja dálkana sem þarf til að finna út réttan skattflokk og síðan velja **Bæta við**. Sláðu inn eða veldu gildi fyrir hvern dálk. Reiturinn **Skattflokkur** verður úttak fylkisins. Ef þessi flipi er ekki stilltur verður VSK-flokkurinn í færslulínunni notaður.

    Eftirfarandi er dæmi.

    | Viðskiptaferli | Sendandi | Viðtakandi | Skattflokkur    |
    | ---------------- | --------- | ------- | ------------ |
    | Sala            | DEU       | DEU     | DEU_Domestic |
    | Sala            | DEU       | FRA     | DEU_EU       |
    | Sala            | BEL       | BEL     | BEL_Domestic |
    | Sala            | BEL       | FRA     | BEL_EU       |

22. Í flipanum **Gildissvið skattkóða vöru** skal velja dálkana sem þarf til að finna út réttan skattkóða og síðan velja **Bæta við**. Sláðu inn eða veldu gildi fyrir hvern dálk. Reiturinn **Skattflokkur vöru** verður úttak fylkisins. Ef þessi flipi er ekki stilltur verður VSK-flokkur vöru í færslulínunni notaður.

    Eftirfarandi er dæmi.

    | Vörukóði | VSK-flokkur |
    | --------- | -------------- |
    | D0001     | Fullt           |
    | D0003     | Lækkað        |

    Frekari upplýsingar um hvernig skattkóðar eru ákvarðaðir í skattaútreikningi er að finna í [Rök fyrir VSK-flokk og VSK-flokk vöru](global-sales-tax-group-determination.md).

23. Settu upp gildissvið skattskráningarnúmera viðskiptavinar, skattskráningarnúmera lánardrottins og listakóða samkvæmt viðskiptaþörfum.
24. Veljið **Vista** og lokið síðan skjámyndinni.
25. Veljið **Breyta stöðu** \> **Ljúka**. Þegar stöðunni er breytt í **Lokið** verður ekki lengur hægt að breyta útgáfunni.
26. Veljið **Breyta stöðu** \> **Birta**. Þessi útgáfa á uppsetningu skattaeiginleikans verður færð í altæku geymsluna og verður sýnileg hverjum lögaðila í Finance.

## <a name="set-up-tax-calculation-in-dynamics-365"></a>Setja upp skattaútreikning í Dynamics 365

Þegar uppsetningu RCS er lokið þarf að vera með útgefna útgáfu af skattaeiginleikanum. Fylgið þessum skrefum til að setja upp skattaútreikning í Finance.

Lögaðili sér um uppsetningu í þessum hluta. Þú verður að skilgreina hana fyrir hvern lögaðila sem á að virkja skattaútreikning fyrir í Finance.

1. Í Finance skal fara í **Skattur** \> **Uppsetning** \> **Skattaskilgreining** \> **Færibreytur skattaútreiknings**.
2. Á flipanum **Almennt** skal stilla eftirfarandi reiti:

    - **Virkja skattaútreikningþjónustu** – Veldu þennan gátreit til að virkja skattaútreikning fyrir lögaðilann. Ef það er ekki virkjað fyrir núverandi lögaðila mun lögaðilinn halda áfram að nota núverandi skattkerfi til að finna út og reikna skatt.
    - **Uppsetning eiginleika** – Veljið uppsetningu og útgáfu útgefins skattaeiginleika fyrir lögaðilann. Frekari upplýsingar um það hvernig á að setja upp og ljúka við útgefinn skattaeiginleika er að finna í fyrri hluta þessa efnisatriðis.
    - **Viðskiptaferli** – Veljið viðskiptaferlana sem á að virkja.

3. Í flipanum **Útreikningar** skal skilgreina fyrirhugaða sléttunarreglu fyrir lögaðilann. Frekari upplýsingar um sléttunarregluna er að finna í [Sléttunarreglur skattaútreiknings](https://go.microsoft.com/fwlink/?linkid=2166988).
4. Í flipanum **Viðbrögð við villum** skal skilgreina fyrirhugaða aðferð við meðhöndlun á villu fyrir lögaðilann. Þrír valkostir eru í boði:

    - Ekkert
    - Viðvörun
    - Villa

    Hægt er að setja upp villumeðhöndlunaraðferð fyrir hvern niðurstöðukóða í hlutanum **Upplýsingar**. Ef sumir niðurstöðukóðar eru ekki samstilltir úr skattaútreikningsþjónustunni er hægt að setja upp sjálfgefna aðferð í hlutanum **Almennt**.

5. Í flipanum **Margar VSK-skráningar** er hægt að kveikja á Vsk-skýrslu, ESB-sölulista og Intrastat aðskilið til að vinna við margar aðstæður VSK-skráningar. Frekari upplýsingar um skattskýrslugerð fyrir margar VSK-skráningar er að finna í [Skýrslugerð fyrir margar VSK-skráningar](emea-reporting-for-multiple-vat-registrations.md).
6. Vistaðu uppsetninguna og endurtaktu fyrri skref fyrir hvern lögaðila sem bætist við. Þegar ný útgáfa er gefin út og þú vilt að hún verði notuð sklatu stilla reitinn **Uppsetning eiginleika** í flipanum **Almennt** á síðunni **Færibreytur skattaútreiknings** (sjá skref 2).

## <a name="transaction-processing"></a>Úrvinnsla á færslu

Þegar öllum uppsetningarferlum er lokið er hægt að nota skattaútreikning til að ákveða og reikna út skatt í Finance. Skrefin til að vinna úr færslum eru þau sömu. Eftirfarandi færslur eru studdar í Finance útgáfu 10.0.21:

- Söluferli

    - Sölutilboð
    - Sölupöntun
    - Staðfesting
    - Tiltektarlisti
    - Fylgiseðill
    - Sölureikningur
    - Kreditnóta
    - Skila pöntun
    - Gjald hauss
    - Línugjald

- Innkaupaferli

    - Innkaupapöntun
    - Staðfesting
    - Komulisti
    - Innhreyfingarskjal afurða
    - Innkaupareikningur
    - Gjald hauss
    - Línugjald
    - Kreditnóta
    - Skila pöntun
    - Innkaupabeiðni
    - Gjald innkaupabeiðnilínu
    - Beiðni um tilboð
    - Síðuhaus gjald við beiðnum um tilboð
    - Lína gjald í beiðni um tilboð

- Birgðavinnsla

    - Flutningspantanir - senda
    - Móttaka flutningspöntunar
