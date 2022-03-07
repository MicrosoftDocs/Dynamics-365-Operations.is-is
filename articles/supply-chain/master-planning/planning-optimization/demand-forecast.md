---
title: Aðaláætlanagerð með eftirspurnarspám
description: Þetta efnisatriði útskýrir hvernig á að bæta við eftirspurnarspár við aðaláætlanagerð með fínstillingu skipulagningar.
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup, ReqReduceKey, ForecastModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: cbac68b79b2a10f05e0e442d4f0aa716e5a04634
ms.sourcegitcommit: ac23a0a1f0cc16409aab629fba97dac281cdfafb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/29/2021
ms.locfileid: "7867248"
---
# <a name="master-planning-with-demand-forecasts"></a>Aðaláætlanagerð með eftirspurnarspám

[!include [banner](../../includes/banner.md)]

Hægt er að nota eftirspurnarspá ásamt fínstillingu áætlanagerðar til að gera grein fyrir væntanlegri eftirspurn í aðaláætlanagerð. Hægt er að stofna eftirspurnarspá handvirkt, flytja hana inn eða mynda hana með því að nota virkni eftirspurnarspár í Microsoft Dynamics 365 Supply Chain Management. Frekari upplýsingar um eftirspurnarspár er að finna í [Yfirlit eftirspurnarspár](../introduction-demand-forecasting.md).

> [!NOTE]
> Aðskilin spáráætlun er ekki studd í fínstillingu skipulagningar. Þess vegna hefur stillingin **Núgildandi spáráætlun** á síðunni **Færibreytur áætlanagerðar** engin áhrif þegar verið er að nota fínstillingu skipulagningar.

## <a name="set-up-a-master-plan-to-include-a-demand-forecast"></a>Setja upp aðaláætlun með eftirspurnarspá

Til að skilgreina aðaláætlun þannig að hún feli í sér eftirspurnarspá skal fylgja þessum skrefum.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Veljið fyrirliggjandi áætlun eða stofna nýja áætlun.
1. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:

    - **Spárlíkan** – Veljið spálíkanið sem á að nota. Þetta líkan verður tekið með þegar framboðstillögur eru myndaðar fyrir núverandi aðaláætlun.
    - **Taka með eftirspurnarspá** – Stillið þennan valkost á *Já* til að taka með eftirspurnarspá í gildandi aðaláætlun. Ef það er stillt á *Nei* eru eftirspurnarspárfærslur ekki teknar með í aðaláætluninni.
    - **Aðferð sem er notuð til að minnka spárþarfir** -Veljið aðferðina sem á að nota til að minnka spárþarfir. Nánari upplýsingar eru í efnisþættinum [Minnkunarlyklar samkvæmt spá](#reduction-keys) síðar í þessum kafla.

1. Á flipanum **Tímamörk í dögum** er hægt að stilla eftirfarandi reiti til að tilgreina tímabilið sem eftirspurnarspáin er höfð með í:

    - **Spáráætlun** – Stillið þennan valkost á *Já* til að hnekkja tímamörkum spáráætlunarinnar sem eiga uppruna sinn í einstökum þekjuflokkum. Stillið þetta á *Nei* til að nota gildin úr einstökum þekjuflokkum fyrir núverandi aðaláætlun.
    - **Spátímatímabil** – Ef **Spáráætlun** valkosturinn er stilltur á *Já* skal tilgreina dagafjöldann (frá deginum í dag) sem á að nota eftirspurnarspá fyrir.

    > [!IMPORTANT]
    > **Spáráætlunin** stillingin er ekki enn studd í fínstillingu skipulagningar.

## <a name="set-up-a-coverage-group-to-include-a-demand-forecast"></a>Setja upp þekjuflokk með eftirspurnarspá

Til að skilgreina þekjuhóp þannig að hann feli í sér eftirspurnarspá skal fylgja þessum skrefum.

1. Fara skal í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Þekjuflokkar**.
1. Veljið fyrirliggjandi þekjuflokk eða búið til nýjan flokk.
1. Á flipanum **Annað** skal stilla eftirfarandi reiti.

    - **Tímamörk spáráætlunar** – Sláið inn dagafjöldann (frá deginum í dag) sem á að nota eftirspurnarspá fyrir. Hægt er að hnekkja þessu gildi með því að nota valkostinn **Spáráætlun** í aðaláætluninni, eins og lýst er í fyrri hluta.
    - **Minnkunarlykill** – Veljið minnkunarlykilinn sem á að nota. Frekari upplýsingar er að finna í skjámyndinni [Stofna og setja upp minnkunarlykil samkvæmt spá](#create-reduction-key) og [Nota minnkunarlykil](#use-reduction-key) hlutunum síðar í þessu efnisatriði.
    - **Lækka spá um** – Fyrir aðaláætlanir þar sem reiturinn **Aðferð notuð til að minnka þörf samkvæmt spá** er stilltur á *færslur - minnkunarlykill* eða *Færslur - breytilegt tímabil* skal tilgreina hvaða færslur eiga að draga úr spánni. Veljið eitt af eftirfarandi gildum:

        - **Allar færslur** – Allar færslur ættu að lækka spána.
        - **Pantanir** – Aðeins sölupantanir ættu að draga úr spánni.

        > [!NOTE]
        > Ef *Allar færslur* er valið verða færslur sem hafa bæði eftirspurn og framboð í sömu birgðavíddum taldar hlutlausar og eru hunsaðar við lækkun spár. Ef áætlunarvíddin er til dæmis aðeins stillt á svæði, ekki vöruhús, verður flutningspöntun á svæði 1, vöruhúsi 11 og svæði 1, vöruhúsi 13 hunsað og það mun ekki minnka eftirstandandi eftirspurnarspá.

    - **Taka með samstæðupantanir** – Stillið þennan valkost á *Já* til að taka með samstæðupantanir þegar spáin er lækkuð. Að öðrum kosti skal stilla þetta á *Nei*.
    - **Taka spá fyrir viðskiptamann með í eftirspurnarspá** – Tilgreina hvort taka skuli með spá viðskiptavinar í heildarspánni. Þessi valkostur ákvarðar hvernig raunveruleg eftirspurn minnkar spáeftirspurn. Nota má þetta til að tryggja að aðaláætlanagerð fjallar um framboð vara sem eru keyptar af tilteknum viðskiptavinum.

        - Stillið þennan valkost á *Já* til að taka með spá viðskiptavinar í heildarspánni. Í þessu tilfelli dregur raunveruleg eftirspurn viðskiptavina bæði úr spá viðskiptavinarins og heildarspánni. Aðaláætlanagerð býr til áætlaðar pantanir til að ná yfir aðeins heildar spármagn.
        - Stillið þennan valkost á *Nei* ef ekki á að taka spá viðskiptavinar með í heildarspánni. Í þessu tilfelli dregur raunveruleg eftirspurn viðskiptavina aðeins úr spá viðskiptavinarins. Aðaláætlanagerð býr til áætlaðar pantanir til að ná yfir bæði heildar spármagn og spá fyrir hvert magn viðskiptavinar.

## <a name="forecast-reduction-keys"></a><a name="reduction-keys"></a>Minnkunarlyklar samkvæmt spá

Þessi hluti veitir upplýsingar um ólíkar aðferðir sem eru notaðar til að minnka þarfir samkvæmt spá. Það inniheldur dæmi um niðurstöður hverrar aðferðar. Það útskýrir einnig hvernig á að búa til, setja upp og nota minnkunarlykil samkvæmt spá. Hægt er að nota minnkunarlykil samkvæmt spá til að draga úr þörfum samkvæmt spá.

### <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Aðferðir sem eru notaðar til að draga úr þörfum samkvæmt spá

Þegar þú tekur með spá í aðaláætlun geturðu valið hvernig þarfir samkvæmt spá eru minnkaðar þegar raunveruleg eftirspurn er höfð með. Athugaðu að aðaláætlanagerð útilokar spákröfur úr fortíðinni, sem þýðir allar kröfur um spá fyrir dagsetningu á undan deginum í dag.

Til að hafa spá með í aðaláætlun og velja aðferðina sem er notuð til að draga úr þörfum samkvæmt spá, skal fara í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**. Í reitnum **Spárlíkan** skal velja spárlíkan. Í reitnum **Aðferð notuð til að minnka þörf samkvæmt spá** skal velja aðferð. Eftirtaldir valkostir eru í boði:

- Enginn
- Prósenta - minnkunarlykill
- Færslur - minnkunarlykill
- Færslur - breytilegt tímabil

Eftirfarandi hlutar veita frekari upplýsingar um hvern valmöguleika.

#### <a name="none"></a>Enginn

Ef þú velur **Ekkert** verða þarfir samkvæmt spá ekki minnkaðar við aðaláætlanagerð. Í þessu tilfelli stofnar aðaláætlanagerðin áætlaðar pantanir til að mæta kröfum eftirspurnar (spáð eftirspurn). Þessar áætluðu pantanir viðhalda magni sem stungið er upp á, óháð öðrum gerðum af eftirspurn. Til dæmis ef lagðar eru fram sölupantanir, stofnar aðaláætlanagerð fleiri áætlaðar pantanir til að mæta sölupöntunum. Magnið fyrir spáþarfir er ekki minnkað.

#### <a name="percent--reduction-key"></a>Prósenta - minnkunarlykill

Ef þú velur **Prósent – minnkunarlykill** er dregið úr spáþörfum í samræmi við prósentur og tímabil sem minnkunarlykillinn skilgreinir. Í þessu tilfelli stofnar aðaláætlanagerðin áætlaðar pantanir þar sem mangið er reiknað sem spáð magn x minnkunarlykill fyrir hvert tímabil. Ef það eru aðrar tegundir eftirspurnar stofnar aðaláætlanagerðin einnig áætlaðar pantanir til að mæta þeirri eftirspurn.

##### <a name="example-percent--reduction-key"></a>Dæmi: Prósenta - minnkunarlykill

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

#### <a name="transactions--reduction-key"></a>Færslur - minnkunarlykill

Ef þú stillir reitinn **Aðferð notuð til að minnka þörf samkvæmt spá** á *Færslur - minnkunarlykill* er þörf samkvæmt spá minnkuð samkvæmt viðurkenndum eftirspurnarfærslum sem gerast á tímabilinu sem er skilgreint af minnkunarlyklinum.

Viðurkennd eftirspurn er skilgreind af reitnum **Lækka spá eftir** á síðunni **Þekjuflokkar**. Ef þú stillir reitinn **Lækka spá eftir** á *Pantanir* eru aðeins færslur sölupöntunar teknar sem viðurkennd eftirspurn. Ef þú stilltir hann á *Allar færslur* eru allar birgðafærslur vegna úthreyfingar sem er ekki innan samstæðu teknar sem viðurkennd eftirspurn. Ef einnig á að líta á samstæðusölupantanir sem viðurkennd eftirspurn skal stilla valkostinn **Taka með samstæðupantanir** á *Já*.

Lækkun spár hefst á fyrstu (elstu) færslu eftirspurnarspár á tímabili minnkunarlykils. Ef magn viðurkenndra birgðafærslna er meira en magnið í línum eftirspurnarspár á sama tímabili minnkunarlykils verður staða á magni birgðafærslna notað til að minnka magn eftirspurnarspár á fyrra tímabili (ef er ónotuð spá).

Ef engin ónotuð spá er eftir á fyrra tímabili minnkunarlykils verður staðan á magni birgðafærslna notað til að minnka spármagnið í næsta mánuði (ef til er ónotuð spá).

Gildið í reitnum **Prósenta** í línum minnkunarlykilsins er ekki notað þegar reiturinn **Aðferð notuð til að minnka þörf samkvæmt spá** er stilltur á *Færslur - minnkunarlykill*. Aðeins dagsetningarnar eru notaðar til að skilgreina tímabil minnkunarlykils.

> [!NOTE]
> Allar spár sem eru birtar á eða á undan deginum í dag verða hunsaðar og ekki notaðar til að stofna áætlaðar pantanir. Ef til dæmis eftirspurnarspáin þín fyrir mánuðinn er mynduð 1. janúar og þú keyrir aðaláætlanagerð sem inniheldur eftirspurnarspá þann 2. janúar mun útreikningurinn hunsa línu eftirspurnarspár sem er dagsett 1. janúar.

##### <a name="example-transactions--reduction-key"></a>Dæmi: Færslur - minnkunarlykill

Þetta dæmi sýnir hvernig raunverulegar pantanir sem eiga sér stað á tímabilum sem eru skilgreind af minnkunarlykli minnka kröfur eftirspurnarskrár.

[![Raunverulegar pantanir og spá áður en aðaláætlanagerð er keyrð.](media/forecast-reduction-keys-1-small.png)](media/forecast-reduction-keys-1.png)

Fyrir þetta dæmi velur þú *Færslur - minnkunarlykill* í reitnum **Aðferð notuð til að minnka þörf samkvæmt spá** á síðunni **Aðaláætlanir**.

Eftirfarandi línur eftirspurnarspár eru til 1. apríl.

| Dagsetning     | Fjöldi stykkja sem spáð er fyrir |
|----------|-----------------------------|
| 5. apríl  | 100                         |
| 12. apríl | 100                         |
| 19. apríl | 100                         |
| 26. apríl | 100                         |
| 3. maí    | 100                         |
| 10. maí   | 100                         |
| 17. maí   | 100                         |

Eftirfarandi sölupöntunarlínur eru til í apríl.

| Dagsetning     | Fjöldi eintaka sem óskað er eftir |
|----------|----------------------------|
| 27. apríl | 240                        |

[![Áætlað framboð myndað byggt á pöntunum í apríl.](media/forecast-reduction-keys-2-small.png)](media/forecast-reduction-keys-2.png)

Eftirfarandi þarfamagn er fært í aðaláætlun þegar aðaláætlanagerð er keyrð 1. apríl. Eins og sjá má voru færslur aprílspár minnkaðar samkvæmt eftirspurnarmagninu 240 í röð, sem byrjar á fyrstu færslunum.

| Dagsetning     | Fjöldi eintaka sem óskað er eftir |
|----------|---------------------------|
| 5. apríl  | 0                         |
| 12. apríl | 0                         |
| 19. apríl | 60                        |
| 26. apríl | 100                       |
| 27. apríl | 240                       |
| 3. maí    | 100                       |
| 10. maí   | 100                       |
| 17. maí   | 100                       |

Gerum nú ráð fyrir að nýju pantanirnar hafi verið fluttar inn fyrir maí.

Eftirfarandi sölupöntunarlínur eru til í maí.

| Dagsetning   | Fjöldi eintaka sem óskað er eftir |
|--------|----------------------------|
| 4. maí  | 80                         |
| 11. maí | 130                        |

[![Áætlað framboð myndað byggt á pöntunum í apríl og maí.](media/forecast-reduction-keys-3-small.png)](media/forecast-reduction-keys-3.png)

Eftirfarandi þarfamagn er fært í aðaláætlun þegar aðaláætlanagerð er keyrð 1. apríl. Eins og sjá má voru færslur aprílspár minnkaðar samkvæmt eftirspurnarmagninu 240 í röð, sem byrjar á fyrstu færslunum. Hinsvegar voru spárfærslur fyrir maí minnkaðar um samtals 210 frá og með fyrstu færslu eftirspurnarspár í maí. Samtölur hvers tímabils eru hinsvegar geymdar (400 í apríl og 300 í maí).

| Dagsetning     | Fjöldi eintaka sem óskað er eftir |
|----------|---------------------------|
| 5. apríl  | 0                         |
| 12. apríl | 0                         |
| 19. apríl | 60                        |
| 26. apríl | 100                       |
| 27. apríl | 240                       |
| 3. maí    | 0                         |
| 4. maí    | 80                        |
| 10. maí   | 0                         |
| 11. maí   | 130                       |
| 17. maí   | 90                        |

#### <a name="transactions--dynamic-period"></a>Færslur - breytilegt tímabil

Ef þú velur **Færslur - breytilegt tímabil** eru spáþarfir minnkaðar við raunverulega pöntunarfærslur sem koma upp við breytilegt tímabil. Breytilegt tímabil nær yfir núgildandi spá dagsetningar og lýkur við upphaf næstu spár. Í þessu tilfelli stofnar aðaláætlanagerðin áætlaðar pantanir til að mæta kröfum eftirspurnar (spáð eftirspurn). Hins vegar þegar raunverulegar færslur eru færðar inn eru þarfir samkvæmt spá minnkaðar. Raunverulegar færslur nota hluta af spáðum þörfum.

Þegar þessi valkostur er notaður gerist eftirfarandi virkni:

- Minnkunarlyklar eru hvorki nauðsynlegir né notaðir. 
- Ef spá er alveg minnkuð verða spárþarfir gildandi spár 0 (núll).
- Ef það er engin komandi spá eru spáþarfir frá síðustu spá sem var færð inn minnkaðar.
- Tímamörk eru hafðar með í útreikningi á lækkun spár.
- Jákvæðir dagar eru hafðir með í útreikningi á lækkun spár.
- Ef raunverulegar pöntunarfærslur°fara fram úr spáþörfum, eru eftirstandandi færslur ekki sendar áfram í næsta spátímabil.

##### <a name="example-1-transactions--dynamic-period"></a>Dæmi 1: Færslur - breytilegt tímabil

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

##### <a name="example-2-transactions--dynamic-period"></a>Dæmi 2: Færslur - breytilegt tímabil

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

### <a name="create-and-set-up-a-forecast-reduction-key"></a><a name="create-reduction-key"></a>Stofna og setja upp minnkunarlykil samkvæmt spá

Minnkunarlykill samkvæmt spá er notaður í aðferðunum **Færslur - minnkunarlykill** og **Prósenta - minnkunarlykill** til að lækka þarfir samkvæmt spá. Fylgdu eftirfarandi skrefum til að búa til og setja upp minnkunarlykil.

1. Fara skal í **Aðaláætlanagerð \> Uppsetning \> Þekja \> Minnkunarlyklar**.
2. Veldu **Nýtt** til að búa til minnkunarlykil.
3. Í reitinn **Minnkunarlykill** skal færa inn einkvæmt kennimerki fyrir minnkunarlykil samkvæmt spá. Því næst, í reitinn **Heiti** skal færa inn heiti. 
4. Skilgreindu tímabilin og prósentu minnkunarlykils fyrir hvert tímabil:

    - Reiturinn **Gildistökudagur** birtir daginn sem stofnun á tímabili byrjaði. Þegar valkosturinn **Nota gildisdagsetningu** er stilltur á **Já** byrja tímabilin á gildistökudeginum. Þegar hann er stilltur á **Nei** byrja tímabilin á deginum þegar aðaláætlanagerð er keyrð.
    - Skilgreindu tímabilin sem lækkun spár ætti að eiga sér stað.
    - Fyrir tiltekið tímabil skal tilgreina prósenturnar sem spárþarfir ættu að minnka um. Þú getur slegið inn jákvæð gildi til að minnka kröfur, eða neikvæð gildi til að auka kröfur.

### <a name="use-a-reduction-key"></a><a name="use-reduction-key"></a>Nota minnkunarlykil

Úthluta verður minnkunarlykli samkvæmt spá á þekjuflokk vörunnar. Fylgdu eftirfarandi skrefum til að úthluta minnkunarlykli á þekjuflokk vöru.

1. Fara skal í **Aðaláætlanagerð \> Uppsetning \> Þekja \> þekjuflokkar**.
2. Í flýtiflipanum **Annað**, í reitnum **Minnkunarlykill**, skal velja minnkunarlykilinn sem á að úthluta á þekjuflokkinn. Minnkunarlykillinn á þá við um allar vörur sem tilheyra þekjuflokknum.
3. Til að nota minnkunarlykil til að reikna út spárlækkun við aðaláætlanagerð er nauðsynlegt að skilgreina þessa stillingu í uppsetningu spáráætlunar eða aðaláætlunar. Farðu í eina af eftirfarandi staðsetningum:

    - **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Spáráætlanir**
    - **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**

4. Á síðunni **Spáráætlanir** eða **Aðaláætlanir**, í flýtiflipanum **Almennt**, í reitnum **Aðferð notuð til að minnka þörf samkvæmt spá**, skal velja annaðhvort **Prósenta - minnkunarlykill** eða **Færslur - minnkunarlykill**.

### <a name="reduce-a-forecast-by-transactions"></a>Lækka spá með færslum

Þegar valið er **Færslur - minnkunarlykill** eða **Færslur - breytilegt tímabil** sem aðferð til að lækka spárþarfir, er hægt að tilgreina hvaða færslur lækka spána. Á síðunni **Þekjuflokkar**, í flýtiflipanum **Annað**, í reitnum **Lækka spá um**, skal velja **Allar færslur** ef allar færslur eiga að lækka spána eða **Pantanir** ef sölupantanir ættu eingöngu að lækka spána.

## <a name="forecast-models-and-submodels"></a>Spárlíkön og undirlíkön

Þessi hluti lýsir því hvernig á að búa til spárlíkön og hvernig á að sameina mörg spárlíkön með því að setja upp undirlíkön.

*Spálíkan* nefnir og auðkennir tiltekna spá. Eftir að búið er að stofna spárlíkanið er hægt að bæta spárlínum við það. Til að bæta við spárlínum fyrir margar vörur skal nota **Eftirspurnarspárlínur** síðuna. Til að bæta við spárlínum fyrir tiltekna valda vöru skal nota síðuna **Útgefnar afurðir**.

Spárlíkan getur innihaldið spár úr öðrum spárlíkönum. Til að ná fram þessari niðurstöðu er öðrum spárlíkönum bætt við sem *undirlíkön* yfirspárlíkans. Stofna þarf hvert viðeigandi líkan áður en hægt er að bæta því við sem undirlíkan yfirspárlíkans.

Skipulagið sem verður til býður upp á öfluga leið til að stjórna spám vegna þess að það gerir kleift að sameina (safna saman) inntak margra spárlíkana. Séð út frá áætlanagerð er því auðvelt að sameina spár fyrir hermanir. Til dæmis væri hægt að setja upp hermun sem byggir á samsetningu reglulegra spár með spánni fyrir kynningu á vortilboðum.

### <a name="submodel-levels"></a>Stig undirlíkana

Engin takmörk eru á fjölda undirlíkana sem hægt er að bæta við yfirspárlíkan. Hins vegar getur skipulagið aðeins verið einslaga stig. Þ.e.a.s. spárlíkan sem er undirlíkan annars spárlíkans getur ekki haft eigin undirlíkön. Þegar undirlíkönum er bætt við spárlíkan athugar kerfið hvort spárlíkanið sé nú þegar undirlíkan annars spárlíkans.

Ef aðaláætlanagerð finnur undirlíkan sem er með sín eigin undirlíkön koma upp villuboð.

#### <a name="submodel-levels-example"></a>Dæmi um stig undirlíkana

Spárlíkan A er með spárlíkan B sem undirlíkan. Þar af leiðandi getur spárlíkan B ekki verið með sín eigin undirlíkön. Ef reynt er að bæta undirlíkani við spárlíkan B koma upp eftirfarandi villuboð: „Spárlíkan B er undirlíkan fyrir líkan A.“

### <a name="aggregating-forecasts-across-forecast-models"></a>Spám safnað saman yfir spárlíkön

Spárlínur sem gerast á sama degi verður safnað saman þvert yfir spárlíkan þeirra og undirlíkana.

#### <a name="aggregation-example"></a>Uppsöfnunardæmi

Spárlíkan A er með spárlíkön B og C sem undirlíkön.

- Spárlíkan A inniheldur eftirspurnarspá fyrir 2 stykki (stk) þann 15. júní.
- Spárlíkan B inniheldur eftirspurnarspá fyrir 3 stk þann 15. júní.
- Spárlíkan C inniheldur eftirspurnarspá fyrir 4 stk þann 15. júní.

Eftirspurnarspáin í kjölfarið verður ein eftirspurn eftir 9 stk (2 + 3 + 4) þann 15. júní.

> [!NOTE]
> Hvert undirlíkan notar eigin færibreytur, ekki færibreytur yfirspárlíkansins.

### <a name="create-a-forecast-model"></a>Stofna spálíkan

Til að búa til spárlíkan skal fylgja þessum skrefum.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Eftirspurnarspá \> Spárlíkön**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stillið eftirfarandi reiti fyrir nýja spárlíkanið:

    - **Líkan** – Færið inn einkvæmt kenni fyrir líkanið.
    - **Heiti** - Færið inn lýsandi heiti á líkaninu.
    - **Stöðvað** – Venjulega á að stilla þennan valkost á *Nei*. Stillið hann á *Já* ef á að koma í veg fyrir breytingar á öllum spárlínum sem er úthlutað á líkanið.

    > [!NOTE]
    > Reiturinn **Telja með í sjóðsstreymisspár** og reitirnir í flýtiflipanum **Verk** eru ekki tengdir aðaláætlanagerð. Þess vegna er hægt að hunsa þá í þessu samhengi. Aðeins þarf að taka þá til greina þegar unnið er með spár fyrir **Verkefnastjórnun og bókhaldskerfi**.

### <a name="assign-submodels-to-a-forecast-model"></a>Úthluta undirlíkönum á spárlíkan

Til að úthluta undirlíkönum á spárlíkan skal fylgja þessum skrefum.

1. Opnið **Birgðastjórnun \> Uppsetning \> Spá \> Spárlíkön**.
1. Á listasvæðinu er spárlíkanið valið til að setja upp undirlíkan fyrir.
1. Í flýtiflipanum **Undirlíkan** skal velja **Bæta við** til að bæta línu við hnitanetið.
1. Í nýju línunni skal stilla eftirfarandi reiti:

    - **Undirlíkan** – Veljið spárlíkanið sem á að bæta við sem undirlíkan. Þetta spárlíkan verður að vera til staðar og það má ekki hafa sín eigin undirlíkön.
    - **Heiti** - Færið inn lýsandi heiti á undirlíkaninu. Til dæmis gæti þetta heiti gefið til kynna tengsl undirlíkans við yfirspárlíkanið.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

