---
title: Minnkunarlyklar samkvæmt spá
description: Þetta efnisatriði veitir dæmi sem sýna hvernig á að setja upp minnkunarlykil. Hún felur í sér upplýsingar um mismunandi stillingar minnkunarlykla og niðurstöður hverrar fyrir sig. Hægt er að nota minnkunarlykil til að skilgreina hvernig á að lækka spárþarfir.
author: roxanadiaconu
manager: tfehr
ms.date: 04/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25cdde073878ed090a4d981eff75a337a79b37af
ms.sourcegitcommit: 724f5b400a4e7c385da9d8b22db416ebc3623b93
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/03/2020
ms.locfileid: "3225106"
---
# <a name="forecast-reduction-keys"></a>Minnkunarlyklar samkvæmt spá

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um ólíkar aðferðir sem eru notaðar til að minnka þarfir samkvæmt spá. Það inniheldur dæmi um niðurstöður hverrar aðferðar. Það útskýrir einnig hvernig á að búa til, setja upp og nota minnkunarlykil samkvæmt spá. Hægt er að nota minnkunarlykil samkvæmt spá til að draga úr þörfum samkvæmt spá.

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Aðferðir sem eru notaðar til að draga úr þörfum samkvæmt spá

Þegar þú tekur með spá í aðaláætlun geturðu valið hvernig þarfir samkvæmt spá eru minnkaðar þegar raunveruleg eftirspurn er höfð með. Athugaðu að aðaláætlanagerð útilokar spákröfur úr fortíðinni, sem þýðir allar kröfur um spá fyrir dagsetningu á undan deginum í dag.

Til að hafa spá með í aðaláætlun og velja aðferðina sem er notuð til að draga úr þörfum samkvæmt spá, skal fara í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**. Í reitnum **Spárlíkan** skal velja spárlíkan. Í reitnum **Aðferð notuð til að minnka þörf samkvæmt spá** skal velja aðferð. Eftirtaldir valkostir eru í boði:

- Enginn
- Prósenta - minnkunarlykill
- Færslur - minnkunarlykill
- Færslur - breytilegt tímabil

Eftirfarandi hlutar veita frekari upplýsingar um hvern valmöguleika.

### <a name="none"></a>Enginn

Ef þú velur **Ekkert** verða þarfir samkvæmt spá ekki minnkaðar við aðaláætlanagerð. Í þessu tilfelli stofnar aðaláætlanagerðin áætlaðar pantanir til að mæta kröfum eftirspurnar (spáð eftirspurn). Þessar áætluðu pantanir viðhalda magni sem stungið er upp á, óháð öðrum gerðum af eftirspurn. Til dæmis ef lagðar eru fram sölupantanir, stofnar aðaláætlanagerð fleiri áætlaðar pantanir til að mæta sölupöntunum. Magnið fyrir spáþarfir er ekki minnkað.

### <a name="percent--reduction-key"></a>Prósenta - minnkunarlykill

Ef þú velur **Prósent – minnkunarlykill** er dregið úr spáþörfum í samræmi við prósentur og tímabil sem minnkunarlykillinn skilgreinir. Í þessu tilfelli stofnar aðaláætlanagerðin áætlaðar pantanir þar sem mangið er reiknað sem spáð magn x minnkunarlykill fyrir hvert tímabil. Ef það eru aðrar tegundir eftirspurnar stofnar aðaláætlanagerðin einnig áætlaðar pantanir til að mæta þeirri eftirspurn.

#### <a name="example-percent--reduction-key"></a>Dæmi: Prósenta - minnkunarlykill

Þetta dæmi sýnir hvernig minnkunarlykill minnkar kröfur eftirspurnarspá í samræmi við prósentur og tímabil sem eru skilgreind af minnkunarlykli.

Fyrir þetta dæmi hefurðu með eftirfarandi eftirspurnarspá í aðaláætlun.

| Mánuður    | Eftirspurnarspá |
|----------|-----------------|
| Janúar  | 1.000           |
| febrúar | 1.000           |
| Mars    | 1.000           |
| Apríl    | 1.000           |

Á **Minnkunarlyklar** síðunni skal setja upp eftirfarandi línur.

| Skiptimynt | Eining  | Prósent |
|--------|-------|---------|
| 1      | Mánuður | 100     |
| 2      | Mánuður | 75      |
| 3      | Mánuður | 50      |
| 4      | Mánuður | 25      |

Þú úthlutar minnkunarlyklinum á þekjuflokk vöru. Því næst, á síðunni **Aðaláætlanir**, í reitnum **Aðferð notuð til að minnka þörf samkvæmt spá**, skal velja **Prósenta - minnkunarlykill**.

Í þessu tilfelli, ef spárröðun er keyrð 1. Janúar, eru spáþarfir eftirspurnar nýttar samkvæmt prósentum sem settar eru upp á **Minnkunarlyklar** síðu. Eftirfarandi þarfamagn er fært í aðaláætlun.

| Mánuður                | Áætlað pöntunarmagn | Útreikningur    |
|----------------------|------------------------|----------------|
| Janúar              | 0                      | = 0% × 1.000   |
| febrúar             | 250                    | = 25% × 1.000  |
| Mars                | 500                    | = 50% × 1.000  |
| Apríl                | 750                    | = 75% × 1.000  |
| Maí til og með desember | 1.000                  | = 100% × 1.000 |

### <a name="transactions--reduction-key"></a>Færslur - minnkunarlykill

Ef þú velur **Færslur – minnkunarlykill** er dregið úr spáþörfum í samræmi við færslur sem eiga sér stað á tímabilunum sem minnkunarlykillinn skilgreinir.

#### <a name="example-transactions--reduction-key"></a>Dæmi: Færslur - minnkunarlykill

Þetta dæmi sýnir hvernig raunverulegar pantanir sem eiga sér stað á tímabilum sem eru skilgreind af minnkunarlykli minnka kröfur eftirspurnarskrár.

Fyrir þetta dæmi velur þú **Færslur - minnkunarlykill** í reitnum **Aðferð notuð til að minnka þörf samkvæmt spá** á síðunni **Aðaláætlanir**.

Eftirfarandi sölupantanir eru tiltækar 1. janúar.

| Mánuður    | Fjöldi pantaðar stykkja |
|----------|--------------------------|
| janúar  | 956                      |
| febrúar | 1,176                    |
| mars    | 451                      |
| apríl    | 119                      |

Ef sama eftirspurnarspáin fyrir 1.000 stykki á mánuði er notuð, sem var notuð í dæminu á undan, er eftirfarandi magn þarfa fært í aðaláætlun.

| Mánuður                | Fjöldi eintaka sem óskað er eftir |
|----------------------|---------------------------|
| janúar              | 44                        |
| febrúar             | 0                         |
| Mars                | 549                       |
| Apríl                | 881                       |
| Maí til og með desember | 1.000                     |

### <a name="transactions--dynamic-period"></a>Færslur - breytilegt tímabil

Ef þú velur **Færslur - breytilegt tímabil** eru spáþarfir minnkaðar við raunverulega pöntunarfærslur sem koma upp við breytilegt tímabil. Breytilegt tímabil nær yfir núgildandi spá dagsetningar og lýkur við upphaf næstu spár. Í þessu tilfelli stofnar aðaláætlanagerðin áætlaðar pantanir til að mæta kröfum eftirspurnar (spáð eftirspurn). Hins vegar þegar raunverulegar færslur eru færðar inn eru þarfir samkvæmt spá minnkaðar. Raunverulegar færslur nota hluta af spáðum þörfum.

Þegar þessi valkostur er notaður gerist eftirfarandi virkni:

- Minnkunarlyklar eru hvorki nauðsynlegir né notaðir. 
- Ef spá er alveg minnkuð verða spárþarfir gildandi spár 0 (núll).
- Ef það er engin komandi spá eru spáþarfir frá síðustu spá sem var færð inn minnkaðar.
- Tímamörk eru hafðar með í útreikningi á lækkun spár.
- Jákvæðir dagar eru hafðir með í útreikningi á lækkun spár.
- Ef raunverulegar pöntunarfærslur°fara fram úr spáþörfum, eru eftirstandandi færslur ekki sendar áfram í næsta spátímabil.

#### <a name="example-1-transactions--dynamic-period"></a>Dæmi 1: Færslur - breytilegt tímabil

Hér er einfalt dæmi sem sýnir hvernig aðferðin **Færslur - breytilegt tímabil** virkar.

Fyrir þetta dæmi hefurðu með eftirfarandi eftirspurnarspá í aðaláætlun.

| Dagsetning       | Eftirspurnarspá |
|------------|-----------------|
| 1. janúar  | 1.000           |
| 1. febrúar | 1.000             |

Þú býrð einnig til eftirfarandi sölupantanir.

| Dagsetning        | Sölupöntunarmagn |
|-------------|----------------------|
| 15. janúar  | 200                  |
| 15. febrúar | 400                  |

Í þessu tilfelli eru eftirfarandi áætlaðar pantanir búnar til.

| Dagsetning eftirspurnarspár | Magn | Skýring                           |
|--------------------- |----------|---------------------------------------|
| 1. janúar            | 800      | Þarfir samkvæmt spá (= 1.000 - 200) |
| 15. janúar           | 200      | Þarfir sölupantana             |
| 1. febrúar           | 600      | Þarfir samkvæmt spá (= 1.000 - 400) |
| 15. febrúar          | 400      | Þarfir sölupantana             |

#### <a name="example-2-transactions--dynamic-period"></a>Dæmi 2: Færslur - breytilegt tímabil

Í flestum tilvikum eru kerfi sett upp þannig að færslur minnka eftirspurnarspár á tilteknum spártímabilum: vikur, mánuðir, og svo framvegis. Þessi tímabil eru skilgreind í minnkunarlyklinum. Hins vegar getur tíminn milli tveggja eftirspurnarspárlína einnig *gefið til kynna* tímabil.

Fyrir þetta dæmi stofnar þú eftirspurnarspá fyrir eftirfarandi dagsetningar og magn.

| Dagsetning       | Eftirspurnarspá |
|------------|-----------------|
| 1. janúar  | 1.000           |
| 5. janúar  | 500             |
| 12. janúar | 1.000           |

Taktu eftir að í þessari spá er ekkert greinilegt tímabil milli dagsetninga spáa. Milli fyrstu og annarrar dagsetningar er fjögurra daga bil og milli annarrar og þriðju dagsetningar er sjö daga bil. Þessi bil eru breytilegu tímabilin.

Þú býrð einnig til eftirfarandi sölupöntunarlínur.

| Dagsetning                             | Sölupöntunarmagn |
|----------------------------------|----------------------|
| 15. Desember á fyrra ári | 500                  |
| 3. janúar                        | 100                  |
| 10. janúar                       | 200                  |

Í þessu tilfelli er spáin minnkuð á eftirfarandi hátt:

- Af því að fyrsta sölupöntunin er ekki á neinu tímabili, minnkar hún ekki neina spá.
- Af því að önnur sölupöntunin er á milli 1. janúar og 5. janúar, lækkar hún spána fyrir 1. janúar um 100.
- Af því að þriðja sölupöntunin er á milli 5. janúar og 12. janúar, lækkar hún spána fyrir 5. janúar um 200.

Þess vegna eru eftirfarandi áætlaðar pantanir búnar til.

| Dagsetning eftirspurnarspár             | Magn | Skýring                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| 15. Desember á fyrra ári | 500      | Þarfir sölupöntunar                                            |
| 1. janúar                        | 900      | Tímabilið 1. janúar til 5. janúar fyrir spárþarfir (= 1.000 - 100) |
| 3. janúar                        | 100      | Þarfir sölupöntunar                                            |
| 5. janúar                        | 300      | Tímabilið 5. janúar til 10. janúar fyrir spárþarfir (= 500 - 200)  |
| 12. janúar                       | 1.000    | Spárþarfir tímabilið 12. janúar til loka                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a>Stofna og setja upp minnkunarlykil samkvæmt spá

Minnkunarlykill samkvæmt spá er notaður í aðferðunum **Færslur - minnkunarlykill** og **Prósenta - minnkunarlykill** til að lækka þarfir samkvæmt spá. Fylgdu eftirfarandi skrefum til að búa til og setja upp minnkunarlykil.

1. Fara skal í **Aðaláætlanagerð \> Uppsetning \> Þekja \> Minnkunarlyklar**.
2. Velja skal **Nýtt** eða ýta á **Ctrl+N** til að stofna minnkunarlykil.
3. Í reitinn **Minnkunarlykill** skal færa inn einkvæmt kennimerki fyrir minnkunarlykil samkvæmt spá. Því næst, í reitinn **Heiti** skal færa inn heiti. 
4. Skilgreindu tímabilin og prósentu minnkunarlykils fyrir hvert tímabil:

    - Reiturinn **Gildistökudagur** birtir daginn sem stofnun á tímabili byrjaði. Þegar valkosturinn **Nota gildisdagsetningu** er stilltur á **Já** byrja tímabilin á gildistökudeginum. Þegar hann er stilltur á **Nei** byrja tímabilin á deginum þegar aðaláætlanagerð er keyrð.
    - Skilgreindu tímabilin sem lækkun spár ætti að eiga sér stað.
    - Fyrir tiltekið tímabil skal tilgreina prósenturnar sem spárþarfir ættu að minnka um. Þú getur slegið inn jákvæð gildi til að minnka kröfur, eða neikvæð gildi til að auka kröfur.

## <a name="use-a-reduction-key"></a>Nota minnkunarlykil

Úthluta verður minnkunarlykli samkvæmt spá á þekjuflokk vörunnar. Fylgdu eftirfarandi skrefum til að úthluta minnkunarlykli á þekjuflokk vöru.

1. Fara skal í **Aðaláætlanagerð \> Uppsetning \> Þekja \> þekjuflokkar**.
2. Í flýtiflipanum **Annað**, í reitnum **Minnkunarlykill**, skal velja minnkunarlykilinn sem á að úthluta á þekjuflokkinn. Minnkunarlykillinn á þá við um allar vörur sem tilheyra þekjuflokknum.
3. Til að nota minnkunarlykil til að reikna út spárlækkun við aðaláætlanagerð er nauðsynlegt að skilgreina þessa stillingu í uppsetningu spáráætlunar eða aðaláætlunar. Farðu í eina af eftirfarandi staðsetningum:

    - Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Spáráætlanir
    - Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir

4. Á síðunni **Spáráætlanir** eða **Aðaláætlanir**, í flýtiflipanum **Almennt**, í reitnum **Aðferð notuð til að minnka þörf samkvæmt spá**, skal velja annaðhvort **Prósenta - minnkunarlykill** eða **Færslur - minnkunarlykill**.

## <a name="reduce-a-forecast-by-transactions"></a>Lækka spá með færslum

Þegar valið er **Færslur - minnkunarlykill** eða **Færslur - breytilegt tímabil** sem aðferð til að lækka spárþarfir, er hægt að tilgreina hvaða færslur lækka spána. Á síðunni **Útgefnar afurðir**, í flýtiflipanum **Annað**, í reitnum **Lækka spá um**, skal velja **Allar færslur** ef allar færslur eiga að lækka spána eða **Pantanir** ef sölupantanir ættu eingöngu að lækka spána.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit aðaláætlana](master-plans.md)
