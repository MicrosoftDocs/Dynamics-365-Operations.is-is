---
title: Minnkunarlyklar
description: "Þessi grein gefur dæmi um hvernig eigi að setja upp minnkunarlykil. Hún felur í sér upplýsingar um mismunandi stillingar minnkunarlykla og niðurstöður hverrar fyrir sig. Hægt er að nota minnkunarlykil til að skilgreina hvernig á að lækka spárþarfir."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ce3ff2ac0a5bd9bd342baa05425d7d0957ab8a09
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="reduction-keys"></a>Minnkunarlyklar

[!include[banner](../includes/banner.md)]


Þessi grein gefur dæmi um hvernig eigi að setja upp minnkunarlykil. Hún felur í sér upplýsingar um mismunandi stillingar minnkunarlykla og niðurstöður hverrar fyrir sig. Hægt er að nota minnkunarlykil til að skilgreina hvernig á að lækka spárþarfir.

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a>Dæmi 1: Prósenta - minnkunarlykill spá lækkunarregla
---------------------------------------------------------------

Þetta dæmi sýnir hvernig minnkunarlykill minnkar kröfur eftirspurnarspá í samræmi við prósentur og tímabil sem eru skilgreind af minnkunarlykli.

1.  Á **Minnkunarlyklar** síðunni, setjið upp eftirfarandi línur.
    | Skiptimynt | Eining  | Prósent |
    |--------|-------|---------|
    | 1      | Mánuður | 100     |
    | 2      | Mánuður | 75      |
    | 3      | Mánuður | 50      |
    | 4      | Mánuður | 25      |

2.  Tengja þarf minnkunarlykilinn við þekjuflokk vöru.
3.  Á **Aðaláætlanir** síðunni,°í **Lækkunarreglu** svæðinu, veljið **Prósenta - minnkunarlykill**.
4.  Stofnið söluspá fyrir 1.000 stykki á mánuði.

Ef spárröðun er keyrð 1. Janúar, eru spáþarfir eftirspurnar nýttar samkvæmt prósentum sem settar eru upp á **Minnkunarlyklar** síðu. Eftirfarandi þarfamagn er fært í aðaláætlun.

| Mánuður                | Fjöldi eintaka sem óskað er eftir |
|----------------------|---------------------------|
| janúar              | 0                         |
| febrúar             | 250                       |
| mars                | 500                       |
| Apríl                | 750                       |
| Maí til og með desember | 1.000                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a>Dæmi 2: Færslur  minnkunarlykill spá lækkunarreglu
Þetta dæmi sýnir hvernig raunverulegar pantanir sem eiga sér stað á tímabilum sem eru skilgreind af minnkunarlykli minnka kröfur eftirspurnarskrár.

-   Á **Aðaláætlanir** síðunni,°í **Lækkunarreglu** svæðinu, veljið **Færslur - minnkunarlykill**.

Eftirfarandi sölupantanir eru tiltækar 1. janúar.

| Mánuður    | Fjöldi pantaðar stykkja |
|----------|--------------------------|
| janúar  | 956                      |
| febrúar | 1,176                    |
| mars    | 451                      |
| apríl    | 119                      |

Ef sama söluspá fyrir 1.000 stykki á mánuði er notuð er eftirfarandi þarfamagn fært í aðaláætlun.

| Mánuður                | Fjöldi eintaka sem óskað er eftir |
|----------------------|---------------------------|
| janúar              | 44                        |
| febrúar             | 0                         |
| mars                | 549                       |
| Apríl                | 881                       |
| Maí til og með desember | 1.000                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a>Dæmi 3: Færslur breytileg tímabil spá lækkunarreglu
Í flestum tilvikum eru kerfi sett upp þannig að færslur minnka eftirspurnarspár innan tiltekna spátímabila: vikur, mánuðir, og svo framvegis. Þessi tímabil eru skilgreind í minnkunarlyklinum. Hins vegar getur tíminn milli tveggja eftirspurnarspárlína einnig *gefið til kynna* tímabil.

1.  Stofna eftirspurnarspá fyrir eftirfarandi dagsetningar og magn.
    | Dagsetning       | Eftirspurnarspá |
    |------------|-----------------|
    | 1. janúar  | 1.000           |
    | 5. janúar  | 500             |
    | 12. janúar | 1.000           |

    Í þessari spá það er ekki greinilegt tímabil milli spádagsetninganna: Milli fyrstu og annarrar dagsetningar er°fjögurra daga bil og milli annarrar og þriðju dagsetningar er°sjö daga bil. Þessi mismunandi bil eru breytileg tímabil.
2.  Stofna Sölupöntunarlínur á eftirfarandi hátt.
    | Dagsetning                             | Sölupöntunarmagn |
    |----------------------------------|----------------------|
    | 15. Desember á fyrra ári | 500                  |
    | 3. janúar                        | 100                  |
    | 10. janúar                       | 200                  |

Spáin verður lækkuð sem hér segir:

-   Fyrsta sölupöntun er ekki innan neins tímabils svo það ekki að draga úr neinni spá.
-   Önnur sölupöntun er á milli 1. Janúar og 5. Janúar, þannig að hún lækkar spá fyrir 1. Janúar um 100.
-   Þriðja sölupöntun er á milli 5. Janúar og 12. Janúar, þannig að hún lækkar spá fyrir 5. Janúar um 200.

Eftirfarandi áætluð pöntun verður stofnuð til að uppfylla spána.

| Dagsetning eftirspurnarspár | Minnkað magn |
|----------------------|------------------|
| 1. janúar            | 900              |
| 5. janúar            | 300              |
| 12. janúar           | 1.000            |

Hér er samantekt af°**Færslur - breytilegt tímabil** lækkun:

-   Spáþarfir eru minnkaðar við raunverulega pöntunarfærslur sem koma upp við breytilegt tímabil. Breytilegt tímabil nær yfir núgildandi spá dagsetningar og lýkur við upphaf næstu spár.
-   Þessi aðferð notar hvorki né krefst minnkunarlykils.
-   Þegar þessi valkostur er notaður gerist eftirfarandi virkni:
    -   Ef spá er alveg minnkuð verða spárþarfir gildandi spá 0 (núll).
    -   Ef það er engin komandi spá eru spáþarfir frá síðustu spá sem var færð inn minnkaðar.
    -   Tímamörk eru hafðar með í útreikningi á lækkun spár.
    -   Jákvæðir dagar eru hafðir með í útreikningi á lækkun spár.
    -   Ef raunverulegar pöntunarfærslur°fara fram úr spáþörfum, eru eftirstandandi færslur ekki sendar áfram í næsta spátímabil.


<a name="see-also"></a>Sjá einnig
--------

[Aðaláætlanir](master-plans.md)




