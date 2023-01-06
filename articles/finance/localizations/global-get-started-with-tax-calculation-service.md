---
title: Hafist handa með skattaútreikning
description: Í þessari grein er útskýrt hvernig á að setja upp skattaútreikning.
author: EricWangChen
ms.date: 10/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.custom: intro-internal
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: 42898823ffc366351c6f58f1fe9b924678ab4b49
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690384"
---
# <a name="get-started-with-tax-calculation"></a>Hafist handa með skattaútreikning

[!include [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um hvernig hafist er handa við skattaútreikning. Hlutarnir í þessari grein leiða þig í gegnum ítarlega hönnuð og skilgreind skref í Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS), Dynamics 365 Finance og Dynamics 365 Supply Chain Management. 

Þessi uppsetning samanstendur af þremur meginskrefum.

1. Í LCS skal setja upp innbót skattaútreiknings.
2. Í RCS skal setja upp eiginleika skattaútreiknings. Þessi uppsetning á ekki við um neinn sérstakan lögaðila. Hægt er að nota hana í öllum lögaðilum í Finance og Supply Chain Management.
3. Í Finance og Supply Chain Management skal setja upp færibreytur skattaútreiknings eftir lögaðila.

## <a name="high-level-design"></a>Ítarleg hönnun

### <a name="runtime-design"></a><a name="runtime"></a>Hönnun keyrslu

Eftirfarandi skýringarmynd sýnir ítarlega keyrsluhönnun skattaútreiknings. Þar sem hægt er að samþætta skattaútreikning með mörgum Dynamics 365-forritum notar myndin samþættinguna við Finance sem dæmi.

1. Færsla eins og sölupöntun eða innkaupapöntun er stofnuð í Finance.
2. Finance notar sjálfkrafa sjálfgefin gildi VSK-flokks og VSK-flokks vöru.
3. Þegar hnappurinn **Virðisaukaskattur** er valinn í færslunni fer skattaútreikningurinn í gang. Finance sendir þá innihaldið til skattaútreikningsþjónustuna.
4. Skattaútreikningsþjónustan stemmir innihaldið við fyrirfram skilgreindar reglur í skattaeiginleikanum til að finna nákvæmari VSK-flokk og VSK-flokk vöru samtímis.

    - Ef hægt er að stemma innihaldið við fylkið **Gildissvið skattflokks** hnekkir það gildi VSK-flokks með samsvöruðu gildi VSK-flokks í gildissviðsreglunni. Annars heldur hún áfram að nota gildi VSK-flokks úr Finance.
    - Ef hægt er að stemma innihaldið við fylkið **Gildissvið VSK-flokks vöru** hnekkir það gildi VSK-flokks vöru með samsvöruðu gildi VSK-flokks í gildissviðsreglunni. Annars vegar heldur það áfram að nota gildi VSK-flokkur vöru úr Finance.

5. Skattaútreikningsþjónustan ákvarðar endanlega skattkóða með því að nota skurðpunkt VSK-flokks og VSK-flokks vöru.
6. Skattaútreikningsþjónustan reiknar skatt, byggðan á endanlegum skattkóðum sem hún hefur ákvarðað.
7. Skattaútreikningsþjónustan skilar niðurstöðum skattaútreikningsins til Finance.

![Keyrsluhönnun skattaútreiknings.](media/tax-calculation-runtime-logic.png)

### <a name="high-level-configuration"></a>Ítarleg skilgreining

Eftirfarandi skref gefa ítarlegt yfirlit yfir skilgreiningarferlið fyrir skattaútreikningsþjónustuna.

1. Í LCS skal setja upp innbótina **Skattaútreikningur** í LCS-verkið.
2. Í RCS skal setja upp eiginleikann **Skattaútreikningur**.
3. Í RCS skal setja upp eiginleika **Skattaútreiknings**.

    1. Veldu útgáfu skattaskilgreiningar.
    2. Stofnaðu skattkóða.
    3. Búa til skattflokk
    4. Stofnaðu skattflokk vöru.
    5. Valfrjálst: Búðu til gildissvið skattflokks ef ætlunin er að hnekkja sjálfgefnum VSK-flokki sem færður er inn úr aðalgögnum viðskiptavinar eða lánardrottins.
    6. Valfrjálst: Búðu til gildissvið vöruflokks ef ætlunin er að hnekkja sjálfgefnum VSK-flokki vöru sem færður er inn úr aðalgögnum vörunnar.

4. Í RCS skal ljúka við og birta eiginleikann **Skattaútreikningur**.
5. Í Finance skal velja útgefna eiginleikann **Skattaútreikningur**.

Eftir að þessum skrefum er lokið eru eftirfarandi uppsetningar sjálfkrafa samstilltar úr RCS við Finance.

- VSK-kóðar
- VSK-flokkar
- VSK-flokkar vöru

Eftirstandandi hlutar þessarar greinar veita ítarlegri stillingarskref.

## <a name="prerequisites"></a>Forkröfur

Áður en hægt er að klára eftirstandandi ferli í þessari grein þarf að uppfylla eftirfarandi skilyrði:<!--TO HERE-->

- Þú verður að hafa aðgang að LCS-reikningnum þínum og þú verður að hafa virkjað LCS-verk með umhverfi í lagi 2 (eða ofar) sem keyrir Dynamics 365 útgáfu 10.0.21 eða nýrri.
- Þú verður að búa til RCS umhverfi fyrir fyrirtækið og þú verður að hafa aðgang að reikningnum þínum. Nánari upplýsingar um hvernig á að stofna RCS-umhverfi er að finna í [Yfirlit Regulatory configuration service](rcs-overview.md).
- Kveikja þarf á eftirfarandi eiginleikum á vinnusvæðinu **Eiginleikastjórnun** ef þú settir upp umhverfi Finance eða Supply Chain Management eftir því hverjar rekstrarþarfir þínar eru:

    - Skattaútreikningsþjónusta
    - Styðja mörg VSK-skráningarnúmer
    - Skattar í flutningspöntun

- Kveikja þarf á eftirfarandi eiginleikum á vinnusvæðinu **Eiginleikastjórnun** fyrir uppsett RCS-umhverfi.

    - Altækir eiginleikar

- Eftirfarandi hlutverkum skal úthlutað eftir því sem hentar notendum í RCS-umhverfinu:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Þróunaraðili altæks eiginleika
    - Framkvæmdaraðili skattkerfis
    - Hagnýtur ráðgjafi skattkerfis
    - Þróunaraðili skattþjónusta

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
8. Veldu rétta [Skilgreiningarútgáfur skatta](global-tax-calcuation-service-overview.md#versions) útgáfu skattaskilgreiningar samkvæmt útgáfu þinni af Finance og veldu svo **Flytja inn**.
9. Á vinnusvæðinu **Altækir eiginleikar** skal velja **Eiginleikar**, velja reitinn **Skattaútreikningur** og veljið því næst **Bæta við**.

    > [!NOTE]
    > Í útgáfu 10.0.26 og nýrri er hægt að flytja inn prufueiginleika fyrir prufulögaðilann **DEMF**. Frekari upplýsingar er að finna í [Sýnigögn innflutningseiginleika](tax-calculation-import-export-feature.md).

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

15. Í flipanum **Skattkóðar** skal velja **Bæta við** og slá inn skattkóðann og lýsingu.
16. Veljið **Skatthluti**. Skatthlutinn er safn af útreikningsaðferðum sem var skilgreint í fyrri útgáfu valdrar skattaskilgreiningar. Eftirfarandi skatthlutar eru í boði:

    - Eftir nettóupphæð
    - Eftir brúttóupphæð
    - Eftir magni
    - Eftir framlegð
    - Skattur á skatt

17. Veljið **Vista**. Fleiri reitir verða tiltækir samkvæmt skatthlutanum sem var valinn.
18. Notið eftirfarandi valkosti til að gera grein fyrir eðli skattkóðans:

    - Er undanskilið
    - Er notkunarskattur
    - Er bakfært gjald
    - Undanskilja úr útreikningi grunnupphæðar

    Fyrir aðstæður neysluskatts skal setja upp einn skattkóða sem er með jákvætt skatthlutfall og merkja hann sem **Er neysluskattur**.

    Fyrir aðstæður bakfærðs gjalds skal setja upp tvo skattkóða, einn sem er með jákvætt skatthlutfall og annan sem er með neikvætt skatthlutfall en sama hlutfallið. Merkið neikvæða skattkóðann sem **Er bakfært gjald**. Frekari upplýsingar um lausn bakfærðs gjalds í Finance er að finna í [Virkni bakfærðs gjalds fyrir skema VSK/VÞS](emea-reverse-charge.md).

    Fyrir sumar skattgerðir sem á að undanskilja frá útreikningnum á skattgrunnupphæð fyrir færslur með verði (t.d. toll í sumum löndum og landsvæðum) skal velja gátreitinn **Undanskilja frá útreikningi grunnupphæðar**. Frekari upplýsingar um þessa færibreytu er að finna í [Reikna skatt ofan á verð þegar „Verð með sköttum“ er virkt](global-exclude-from-tax-base-amount-calculation.md).

    Viðhaldið mörkum skatthlutfalla og skattupphæðar fyrir þennan skattkóða.

19. Endurtakið skref 15 til 18 til að bæta við öllum öðrum nauðsynlegum skattkóðum.
20. Í flipanum **Skattflokkur** skal velja dálkinn **Skattflokkur**, bæta honum við fylkið sem skilyrði innsláttar og síðan bæta við línum til að vinna með aðalgögn skattflokksins.

    Eftirfarandi er dæmi.

    | Skattflokkur    | Skattkóðar           |
    | ------------ | ------------------- |
    | DEU_Dom | DEU_VAT19; DEU_VAT7 |
    | DEU_EU       | DEU_Exempt          |
    | BEL_Dom | BEL_VAT21; BEL_VAT6 |
    | BEL_EU       | BEL_Exempt          |

21. Í flipanum **Skattflokkur vöru** skal velja dálkinn **Skattflokkur vöru**, bæta honum við fylkið sem skilyrði innsláttar og síðan bæta við línum til að vinna með aðalgögn skattflokks vöru.

    Eftirfarandi er dæmi.

    | VSK-flokkur | Skattkóðar                                    |
    | -------------- | -------------------------------------------- |
    | Fullt           | DEU_VAT19; BEL_VAT21; DEU_Exempt; BEL_Exempt |
    | Lækkað        | DEU_VAT7; BEL_VAT6; DEU_Exempt; BEL_Exempt   |

22. Í flipanum **Gildissvið skattflokks** skal velja dálkana sem þarf til að finna út réttan skattflokk og síðan velja **Bæta við**. Sláðu inn eða veldu gildi fyrir hvern dálk. Reiturinn **Skattflokkur** verður úttak fylkisins. Ef þessi flipi er ekki stilltur verður VSK-flokkurinn í færslulínunni notaður.

    Eftirfarandi er dæmi.

    | Viðskiptaferli | Sendandi | Viðtakandi | Skattflokkur    |
    | ---------------- | --------- | ------- | ------------ |
    | Sala            | DEU       | DEU     | DEU_Dom |
    | Sala            | DEU       | FRA     | DEU_EU       |
    | Sala            | BEL       | BEL     | BEL_Dom |
    | Sala            | BEL       | FRA     | BEL_EU       |
    
    > [!NOTE]
    > Ef sjálfgefinn VSK-flokkur í línum skattskylds skjals er réttur skal skilja þetta fylki eftir autt. Frekari upplýsingar er að finna í hlutanum [Hönnun keyrslu](#runtime) í þessari grein.

23. Í flipanum **Gildissvið skattkóða vöru** skal velja dálkana sem þarf til að finna út réttan skattkóða og síðan velja **Bæta við**. Sláðu inn eða veldu gildi fyrir hvern dálk. Reiturinn **Skattflokkur vöru** verður úttak fylkisins. Ef þessi flipi er ekki stilltur verður VSK-flokkur vöru í færslulínunni notaður.

    Eftirfarandi er dæmi.

    | Vörukóði | VSK-flokkur |
    | --------- | -------------- |
    | D0001     | Fullt           |
    | D0003     | Lækkað        |

    > [!NOTE]
    > Ef sjálfgefinn VSK-flokkur vöru í línum skattskylds skjals er réttur skal skilja þetta fylki eftir autt. Frekari upplýsingar er að finna í hlutanum [Hönnun keyrslu](#runtime) í þessari grein.

    Frekari upplýsingar um hvernig skattkóðar eru ákvarðaðir í skattaútreikningi er að finna í [Rök fyrir VSK-flokk og VSK-flokk vöru](global-sales-tax-group-determination.md).

24. Settu upp gildissvið skattskráningarnúmera viðskiptavinar, skattskráningarnúmera lánardrottins og listakóða samkvæmt viðskiptaþörfum.
25. Veljið **Vista** og lokið síðan skjámyndinni.
26. Veljið **Breyta stöðu** \> **Ljúka**. Þegar stöðunni er breytt í **Lokið** verður ekki lengur hægt að breyta útgáfunni.
27. Veljið **Breyta stöðu** \> **Birta**. Þessi útgáfa á uppsetningu skattaeiginleikans verður færð í altæku geymsluna og verður sýnileg hverjum lögaðila í Finance.

## <a name="set-up-tax-calculation-in-dynamics-365"></a>Setja upp skattaútreikning í Dynamics 365

Þegar uppsetningu RCS er lokið þarf að vera með útgefna útgáfu af skattaeiginleikanum. Fylgið þessum skrefum til að setja upp skattaútreikning í Finance.

Lögaðili sér um uppsetningu í þessum hluta. Þú verður að skilgreina hana fyrir hvern lögaðila sem á að virkja skattaútreikning fyrir í Finance.

1. Í Finance skal fara í **Skattur** \> **Uppsetning** \> **Skattaskilgreining** \> **Færibreytur skattaútreiknings**.
2. Á flipanum **Almennt** skal stilla eftirfarandi reiti:

    - **Virkja skattaútreikningþjónustu** – Veldu þennan gátreit til að virkja skattaútreikning fyrir lögaðilann. Ef það er ekki virkjað fyrir núverandi lögaðila mun lögaðilinn halda áfram að nota núverandi skattkerfi til að finna út og reikna skatt.
    - **Uppsetning eiginleika** – Veljið uppsetningu og útgáfu útgefins skattaeiginleika fyrir lögaðilann. Frekari upplýsingar um það hvernig á að setja upp og ljúka við útgefinn skattaeiginleika er að finna í fyrri hluta þessarar greinar.
    - **Viðskiptaferli** – Veljið viðskiptaferlana sem á að virkja.

3. Í flipanum **Útreikningar** skal skilgreina fyrirhugaða sléttunarreglu fyrir lögaðilann. Frekari upplýsingar um sléttunarregluna er að finna í [Sléttunarreglur skattaútreiknings](https://go.microsoft.com/fwlink/?linkid=2166988).
4. Í flipanum **Viðbrögð við villum** skal skilgreina fyrirhugaða aðferð við meðhöndlun á villu fyrir lögaðilann. Þrír valkostir eru í boði:

    - Nei
    - Viðvörun
    - Villa

    Hægt er að setja upp villumeðhöndlunaraðferð fyrir hvern niðurstöðukóða í hlutanum **Upplýsingar**. Ef sumir niðurstöðukóðar eru ekki samstilltir úr skattaútreikningsþjónustunni er hægt að setja upp sjálfgefna aðferð í hlutanum **Almennt**.

5. Í flipanum **Margar VSK-skráningar** er hægt að kveikja á Vsk-skýrslu, ESB-sölulista og Intrastat aðskilið til að vinna við margar aðstæður VSK-skráningar. Frekari upplýsingar um skattskýrslugerð fyrir margar VSK-skráningar er að finna í [Skýrslugerð fyrir margar VSK-skráningar](emea-reporting-for-multiple-vat-registrations.md).
6. Vistaðu uppsetninguna og endurtaktu fyrri skref fyrir hvern lögaðila sem bætist við. Þegar ný útgáfa er gefin út og þú vilt að hún verði notuð sklatu stilla reitinn **Uppsetning eiginleika** í flipanum **Almennt** á síðunni **Færibreytur skattaútreiknings** (sjá skref 2).
