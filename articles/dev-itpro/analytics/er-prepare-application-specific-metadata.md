---
title: Undirbúa forritasértæk lýsigögn fyrir RCS og ER
description: Þetta efni útskýrir hvernig á að undirbúa forritasértæk lýsigögn fyrir Regulatory Configuration Service (RCS) og Rafræna skýrslugerð (ER).
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 289f901501a68319c9d85e993d8dfbfc3838a8eb
ms.sourcegitcommit: d940c7892b6caa6141b3bda8abf1c56e9df4687a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726433"
---
# <a name="prepare-application-specific-metadata-for-rcs"></a>Undirbúa forritasértæk lýsigögn fyrir RCS

[!include[banner](../includes/banner.md)]

Þetta efni fer með þig í gegnum dæmi um eftirfarandi verk:

- [Undirbúa lýsigögn forrits sem hægt er að nota í RCS](#prepare-application-metadata-that-can-be-used-in-rcs)
- [Aðgangur að lýsigögnum forrits með ER-skilgreiningu](#access-application-metadata-by-using-an-er-configuration)
- [Aðgangur að lýsigögnum forrits með tengdum forritum](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a>Undirbúa lýsigögn forrits sem hægt er að nota í RCS

Eftirfarandi ferli sýnir hvernig notandi á Finance and Operations sem er með hlutverkið **Kerfisstjóri** eða **Þróunaraðili rafrænnar skýrslulausnar** getur búið til skilgreiningar rafrænnar skýrslugerðar (ER) sem innihalda lýsigögn fyrir forritið Microsoft Dynamics 365 for Finance and Operations og sem eru notuð til að setja upp skilgreiningar ER-líkanavörpunar í Regulatory Configuration Service (RCS). Sýnisskilgreining ER-líkanavörpunar sem er búið til í þessu dæmi verður notað til að fá aðgang að utanríkisviðskiptum.

Í þessu dæmi viltu nota RCS til að setja upp ER-lausn fyrir Finance and Operations, sem verður notuð til að búa til rafræn skjöl sem innihalda upplýsingar úr umdæmi utanríkisviðskipta. Til að tilgreina vörpun milli ER-gagnalíkans og uppruna nauðsynlegra gagna, verður þú að hafa aðgang að forritslýsigögnum fyrir Finance and Operations í RCS. Þess vegna verður þú að skilgreina nýja ER lýsigagnaskilgreiningu sem inniheldur öll lýsigögnin sem þarf eins og stendur til að mynda ER-skýrslur fyrir valið viðskiptalén sem hluta af ferlinu við að setja upp ER-lausnina.

> [!NOTE]
> Í þessu dæmi muntu stofna skilgreiningu fyrir sýnifyrirtækið, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er.

1. Fara í **Fyrirtækisstjórnun \> Vinnusvæði \> Rafræn skýrslugerð**.
2. Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**. Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í ferlinu [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Veldu **Skilgreiningar lýsigagna**.
4. Veljið **Stofna skilgreiningu**.
5. Í fellilistanum, í reitnum **Heiti** slærðu inn heiti. Fyrir þetta dæmi skaltu slá inn **Lýsigögn utanríkisviðskipta**.
6. Veljið **Stofna skilgreiningu**.
7. Veljið **Hönnuður**.
8. Veljið **Bæta við**.

    > [!NOTE]
    > Þú getur valið öll lýsigögn annaðhvort fyrir allt forritið eða fyrir valdin líkön eða einingar. Í báðum dæmum skaltu hafa í huga að eftirfarandi lýsigögnum verður sjálfkrafa bætt við: töflum yfir skrám, talningum og lengd gagnategunda (EDT). Þegar fleiri tegundir lýsigagna eru nauðsynlegar verður að bæta þeim handvirkt við.

Þú verður að bæta við lýsigögnum sem tengjast utanríkisviðskiptadæealum og velja lýsigögn á handvirkan hátt.

9. Veldu **Bæta við gagnasafni \> Töflufærslur**.
10. Sía á gildi **Intrastat** í reitnum **Heiti**.
11. Veldu **Intrastat**-töflu.
12. Veljið **Í lagi**.

Þú verður að bæta við lýsigögnum um Intrastat-skráatöfluna.

13. Í trénu skaltu velja **Töflufærslur Intrastat \> \>Vensl \> IntrastatCommodity (Töflufærslur EcoResCategory)**.
14. Veldu **Bæta við lýsigögnum**.

    > [!NOTE]
    > Lýsigögn um nauðsynleg vensl fyrir valda skráatöflu verður að bæta við á handvirkan hátt.

15. Veldu **Bæta við gagnagjafa**.
16. Veldu **Upptalningu**.
17. Sía á gildi **IntrastatDirection** í reitnum **Heiti**.
18. Veldu upptalningarskrána **IntrastatDirection**.
19. Veljið **Í lagi**.
20. Veljið **Vista**.
21. Lokið síðunni.
22. Ljúktu drögunum að útgáfu skilgreiningar lýsigagnanna:

    1. Velduð **Breyta stöðu \> Ljúka**.
    2. Veljið **Í lagi**.
    3. Veldu fullgerða útgáfu 1.

23. Flyttu út fullgerða útgáfu lýsigagnauppsetningar úr forritinu sem XML-skrá:

    1. Veldu **Gengi \> Flytja út sem XML-skrá**.
    2. Veljið **Í lagi**.

ER-lýsigagnasskilgreiningin sem þú bjóst til er vistuð sem skráin **Foreign trade metadata.xml**. Núna geturðu flutt þær inn í RCS, þannig að hægt sé að nota þær sem uppruna lýsigagna fyrir utanríkisviðskiptalén í Finance and Operations. Samkvæmt þessum upplýsingum er hægt að tilgreina vörpun á milli lýsigagna forritsins og ER-gagnalíkansins.

## <a name="access-application-metadata-by-using-an-er-configuration"></a>Aðgangur að lýsigögnum forrits með ER-skilgreiningu

Eftirfarandi ferli sýnir hvernig RCS-notandi sem er með hlutverkið **Kerfisstjóri** eða **Þróunaraðili rafrænnar skýrsluhönnunar** getur sett upp nýja ER-líkanavörpun með því að nota lýsigögn úr forritinu Finance and Operations. Farið verður í lýsigögn forrits með því að nota skilgreiningar ER-lýsigagna sem innihalda sýnishorn af lýsigögnum til að fá aðgang að utanríkisviðskiptum.

Áður en hægt er að ljúka þessu verður fyrst að ljúka eftirfarandi ferlum:

- [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [Undirbúa lýsigögn forrits sem hægt er að nota í RCS](#prepare-application-metadata-that-can-be-used-in-rcs)

1. Farðu í **Öll vinnusvæði \> Rafræn skýrslugerð**.
2. Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**. Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í ferlinu [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Flyttu inn lýsigögn rafrænnar skýrslugerðar sem inniheldur lýsigögn fyrir forritið Finance and Operations og sem eru stillt til að búa til rafræn skjöl fyrir lén utanríkisviðskipta. Þú stofnaðir þessa skilgreiningu ER-lýsigagna og fluttir það sem XML-skrá í [Undirbúa lýsigögn forrits sem hægt er að nota í RCS-ferlinu](#prepare-application-metadata-that-can-be-used-in-rcs) fyrr í þessu efnisatriði.

    1. Veldu **Skilgreiningar lýsigagna**.
    2. Veldu **Gengi**.
    3. Veldu **Hlaða úr XML-skrá**.
    4. Flettu til að velja skrána **Foreign trade metadata.xml**.
    5. Veljið **Í lagi**.
    6. Lokið síðunni.

4. Stofnaðu nýja skilgreiningu gagnalíkans:

    1. Veldu **Skilgreiningar skýrslugerðar**.
    2. Veljið **Stofna skilgreiningu**.
    3. Í fellilistanum, í reitnum **Heiti** slærðu inn **Líkan utanríkisverslunar**.
    4. Veljið **Stofna skilgreiningu**.
    5. Veljið **Hönnuður**.
    6. Veldu **Nýtt** til að opna felligluggann.

        1. Í reitnum **Heiti** skaltu færa inn **Rót**.
        2. Veljið **Bæta við**.
    
    7. Veldu **Nýtt** til að opna felligluggann.

        1. Í reitinn **Heiti** slærðu inn **Færsla**.
        2. Í reitnum **Gerð vöru** velurðu **Skráalisti**.
        3. Veljið **Bæta við**.
 
    8. Veldu **Nýtt** til að opna felligluggann.

        1. Í reitinn **Heiti** slærðu inn **Grunnvörukóði**.
        2. Í reitnum **Gerð vöru** velurðu **Strengur**.
        3. Veljið **Bæta við**.

    9. Veldu **Nýtt** til að opna felligluggann.

        1. Í reitinn Heiti slærðu inn **Reikningsfærð upphæð**.
        2. Í reitnum **Gerð vöru** velurðu **Rauntala**.
        3. Veljið **Bæta við**.

    10. Veldu **Nýtt** til að opna felligluggann.

        1. Í reitinn **Heiti** slærðu inn **Dags.**.
        2. Í reitnum **Gerð vöru** velurðu **Dags.**.
        3. Veljið **Bæta við**.
 
    11. Veldu **Bæta við \> Rótartilvísun**.
    12. Veljið **Í lagi**.
    13. Veljið **Vista**.
    14. Lokið síðunni.
    15. Velduð **Breyta stöðu \> Ljúka**.
    16. Veljið **Í lagi**.

5. Stofna skilgreiningu líkanavörpunar:

    1. Veljið **Stofna skilgreiningu**.
    2. Í fellilistanum, í reitnum **Nýtt**, slærðu inn **Vörpun líkans byggir á gagnalíkani utanríkisverslunarlíkans**.
    3. Í reitnum **Heiti** slærðu inn **Vörpun utanríkisverslunar**.
    4. Veljið **Stofna skilgreiningu**.
    5. Á flýtiflipanum **Forkröfur** velurðu **Breyta**.
    6. Veljið **Nýtt**.
    7. Í reitnum **Gerð forkröfuíhlutar** velurðu **Skilgreining**.
    8. Veldu skilgreininguna **Lýsigögn utanríkisviðskipta**.
    9. Veljið **Vista**. Athugaðu að tilvísuninni er bætt við í útgáfu 1 af skilgreiningunni **Lýsigögn utanríkisviðskipta**. Lýsigögn forrits úr þessari skilgreiningu verða boðin á meðan líkanavörpunin er sett upp.
    10. Lokið síðunni.
    11. Veljið **Hönnuður**.
    12. Veljið **Hönnuður**.
    13. Í trénu velurðu **Dynamics 365 for Operations \> Töflufærslur**.
    14. Veljið **Bæta við rót**.
    15. Í reitinn **Heiti** skal færa inn **Intrastat**.
    16. Veldu **Intrastat**-töflufærslur.
    17. Veljið **Í lagi**.

        > [!NOTE]
        > Einu 2 töflurnar eru boðnar, þar sem aðeins tveimur töflum var bætt við í sett af lýsigögnum sem eru í notkun.

    18. Veldu **Binda**.
    19. Í trénu velurðu **Intrastat \> AmountMST**.
    20. Í trénu velurðu **Færsla = Intrastat \> Reikningsfærð upphæð**.
    21. Veldu **Binda**.
    22. Í trénu velurðu **Intrastat \> TransDate**.
    23. Í trénu velurðu **Færsla = Intrastat \> Dags.**.
    24. Veldu **Binda**.
    25. Í trénu víkkarðu út **Intrastat \> \>Vensl \> IntrastatCommodity \> Kóði**.
    26. Í trénu velurðu **Færsla = Intrastat \> Grunnvörukóði**.
    27. Veldu **Binda**.
    28. Veldu **Staðfesta**.

        > [!NOTE]
        > Eftir að staðfestingu er lokið hefur þér tekist að binda þætti gagnalíkans við atriði gagnagjafa sem er lýst með því að nota upplýsingar um lýsigögn forrits tilvísaðri skilgreiningu ER-lýsigagna.

    29. Veljið **Vista**.

Þegar þú þarft þess geturðu framlengt núverandi safn lýsigagna í Finance and Operations. Síðan geturðu flutt út nýlokna útgáfu af skilgreiningu ER-lýsigagna úr Finance and Operations, flutt hana inn í RCS og uppfært forkröfur þess að skilgreind líkanavörpun vísi í nýja útgáfu af innfluttri skilgreiningu lýsigagna.

> [!NOTE]
> Þessi aðferð til að sækja upplýsingar um lýsigögn hugbúnaðar er eina tiltæka aðferðin fyrir forrit sem eru notuð staðbundið (það er að segja, þegar uppsetningarlíkan staðbundinna eða innanhúss viðskiptagagna \[LBD\] er notað fyrir Finance and Operations).

## <a name="access-application-metadata-by-using-connected-applications"></a>Aðgangur að lýsigögnum forrits með tengdum forritum

Eftirfarandi ferli sýnir hvernig RCS-notandi sem er með hlutverkið **Kerfisstjóri** eða **Þróunaraðili rafrænnar skýrsluhönnunar** getur sett upp nýja ER-líkanavörpun með því að nota lýsigögn úr forritinu Finance and Operations. Lýsigögn hugbúnaðar verða skoðuð á netinu með því að nota RCS -tengda forritið. Dæmi um ER-líkanavörpun verður skilgreint til að fá aðgang að utanríkisviðskiptafærslum.

Til að ljúka þessu ferli verður fyrst að ljúka ferlinu [Stofna skilgreiningarveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md) í RCS. Ef þú hefur ekki þegar lokið við ferlið [Aðgangur að lýsigögnum forrits með ER-skilgreiningu](#access-application-metadata-by-using-an-er-configuration) fyrri í þessu efnisatriði, skaltu fara á síðuna [Verkefnaleiðbeiningar rafrænnar skýrslugerðar fyrir Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) til að sækja eftirfarandi ER-skilgreiningarskrár fyrirfram og vista þær staðbundið: **Foreign trade metadata.xml**, **Foreign trade model.xml** og **Foreign trade mapping.xml**.


### <a name="get-required-er-configurations"></a>Sækja umbeðnar ER-skilgreiningar

Ef þú hefur þegar lokið við í ferlið [Fá aðgang að lýsigögnum hugbúnaðar með notkun á ER-skilgreiningum](#access-application-metadata-by-using-an-er-configuration) fyrr í þessu efnisatriði, hefurðu nú þegar allar umbeðnar ER-skilgreiningar (skilgreiningar lýsigagna utanríkisviðskipta, líkans og vörpunar) í gildandi RCS-tilviki. Í því tilfelli getur þú sleppt þessu ferli.

1. Farðu í **Öll vinnusvæði \> Rafræn skýrslugerð**.
2. Veldu **Skilgreiningar skýrslugerðar**.
3. Hladdu inn skilgreiningarskránum **Foreign trade metadata.xml**, **Foreign trade model.xml**, og **Foreign trade mapping.xml** sem endurtaka eftirfarandi keðju skrefa fyrir hverja þeirra:

    1. Veldu **Gengi**.
    2. Veldu **Hlaða úr XML-skrá**.
    3. Veldu **Fletta** og veldu skrá.
    4. Veljið **Í lagi**.

### <a name="register-the-connection-with-finance-and-operations"></a>Skráðu tenginguna hjá Finance and Operations

1. Farðu í **Öll vinnusvæði \> Rafræn skýrslugerð**.
2. Veldu **Tengd forrit**.
3. Gakktu úr skugga um að skilgreint forrit sé byggt á Microsoft Azure og að það sé almennt aðgengilegt RCS-notendum. Núverandi notandi RCS verður að hafa aðgang að skilgreindu forriti og vera skráður sem notandi þessa forrits í hlutverki sem gefur honum eða henni réttindi til að fá aðgang að lýsigögnum forritsins.
4. Veljið **Nýtt**.
5. Í reitnum **Heiti** slærðu inn **MyConnectedApp** sem heiti tengds forrits.
6. Í reitnum **Forrit** skaltu tilgreina slóð forritsins.
7. Í reitnum **Leigjandi** skaltu tilgreina forritaveituna.
8. Veljið **Vista**. 
9. Þegar þú skoðar tengingu við skilgreint forrit skaltu á síðunni **Tengja við ytra forrit** velja tengilinn **Velja hér til að tengja við valið ytra forrit**. 
10. Veldu **Athuga tengingu** til að sannreyna aðgang að skilgreindu forriti.
11. Veljið **Loka**.

Þegar þú hefur lokið þessu ferli og tengingarvottun tekist verða upplýsingar um útgáfu og leigjendur uppfærðar fyrir skilgreint forrit í núverandi hnitaneti.

### <a name="review-the-existing-model-mapping-configuration"></a>Yfirfara fyrirliggjandi skilgreiningu fyrir líkanavörpun

1. Farðu í **Öll vinnusvæði \> Rafræn skýrslugerð**.
2. Veldu **Skilgreiningar skýrslugerðar**.
3. Í trénu skaltu velja **Líkan utanríkisviðskipta \> Vörpun utanríkisviðskipta**.
4. Veldu flýtiflipann **Forkröfur**.

    > [!NOTE]
    > Eins og er vísar þessi vörpun í skilgreiningu lýsigagna. Lýsigögn forrits úr þessari skilgreiningu verða boðin á meðan þessi líkanavörpunin er sett upp.

4. Veljið **Hönnuður**.
5. Veljið **Hönnuður**.
6. Í trénu velurðu **Dynamics 365 for Operations \> Töflufærslur**.
7. Veljið **Bæta við rót**.
8. Sláið inn eða veldu gildi í reitnum **Tafla**.

    > [!NOTE]
    > Eins og er vísar þessi vörpun í skilgreiningu lýsigagna. Lýsigögn forrits úr þessari skilgreiningu verða boðin á meðan þessi líkanavörpunin er sett upp.

9. Veldu **Hætta við**.

### <a name="assign-the-connected-application-to-a-model-mapping"></a>Úthluta tengdu forriti á líkanavörpun

1. Veljið **Breyta**.
2. Í reitnum **Tengt forritasvæði** velurðu forritið **MyConnectedApp**.

    > [!NOTE]
    > Þessi vörpun í lýsigögn valins tengds forrits. Ef vöpun vísar í lýsigagnaskilgreininguna um leið og tengt forrit verða lýsigögn tengds forrits notuð.

3. Veljið **Hönnuður**.
4. Veljið **Hönnuður**.
5. Í trénu velurðu **Dynamics 365 for Operations \> Töflufærslur**.
6. Veljið **Bæta við rót**.
7. Sláið inn eða veldu gildi í reitnum **Tafla**.

    > [!NOTE]
    > Á þessum tímapunkti eru fleiri en tvær forritstöflur boðnar þar sem þessi vörpun notar öll lýsigögn tengds forrits sem hefur verið úthlutað á það.

8. Veldu **Hætta við**.
9. Veldu **Staðfesta**.

Núna hefur þú bundið þætti gagnalíkansins við atriði gagnagjafa sem er lýst með því að nota upplýsingar um lýsigögn forrits úr tengdu forriti sem hefue verið úthlutað á þessa vörpun.

Þegar þú verður að meta þessa líkanavörpun með því að nota lýsigögn annarrar útgáfu forrits skaltu skrá annað tengt forrit, úthluta því á þessa líkanavörpun og sannprófa það gegn nýjum lýsigögnunum.

## <a name="additional-resources"></a>Frekari upplýsingar

Að öðrum kosti getur þú spilað verkleiðbeiningarnar **Undirbúa lýsigögn forrits sem hægt er að nota í RCS** í Finance and Operations ásamt **Fá aðgang að lýsigögnum forrits með því að nota ER-stillingu** og **Fá aðgang að lýsigögnum forrits með því að nota tengd forrit** í RCS. Hægt er að sækja þessar verkleiðbeiningar af síðunni [Verkleiðbeiningar fyrir rafræna skýrslugerð Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).
