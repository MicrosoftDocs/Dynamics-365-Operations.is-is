---
title: Bóka til gjaldfærslu reikningsskilareglu
description: Þessi grein veitir yfirlit yfir bókhaldsregluna um færslu til gjaldfærslu.
author: rachel-profitt
ms.date: 05/02/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-02
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: c03109baaa341b25af70840b791ddf04f692fb1a
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016566"
---
# <a name="post-to-charge-account-accounting-principle"></a>Bóka til gjaldfærslu reikningsskilareglu

The *pósta til gjaldfærslureiknings* Bókhaldsreglan gerir þér kleift að gera grein fyrir og á auðveldara með að jafna mismun sem verður á einingarverði milli bókunar og fjárhagsbókunar, óbeins kostnaðar á keyptum vörum eða kostnaðar á innkaupapöntun.

Tvær stillingar fyrir kóða viðskiptaskulda á **Gjaldkóði** síða (**Viðskiptaskuldir \> Uppsetning gjalda \> Gjaldkóði**) getur valdið því að innkaupapöntun hefur áhrif á verðmat á birgðaeignum:

- Fyrir gjaldkóða þar sem **Debettegund** reiturinn er stilltur á *Atriði* og **Kredittegund** reiturinn er stilltur á *Fjárhagsreikningur*, fjárhagsreikningurinn sem er valinn sem frásogsreikningur virkar sem birgðabreytingareikningur.
- Fyrir gjaldkóða þar sem **Debettegund** reiturinn er stilltur á *Atriði* og **Kredittegund** reiturinn er stilltur á *Viðskiptavinur/seljandi*, gjaldið verður bókfært sem efniskostnaður og birgðabreytingareikningur vörunnar verður notaður.

## <a name="european-special-accounting-rule"></a>Evrópsk sérbókhaldsregla

Í Evrópu er *pósta til gjaldfærslureiknings* reikningsskilaaðferð er oft notuð til að fella sérstaka reikningsskilareglu. Til dæmis er ein af eftirfarandi aðferðum venjulega notuð til að gera grein fyrir birgðabreytingum:

- **Kostnaðaraðferð við sölu** – Stöðluð uppsetning birgðabókunarsniðs styður þessa aðferð. The *pósta til gjaldfærslureiknings* reikningsskilareglu er ekki krafist.
- **Eðli kostnaðaraðferðar** – Minni stofnanir nota oft þessa aðferð. Það felur venjulega í sér eftirfarandi skref:

    1. Vörur eða þjónusta er gjaldfærð að fullu við móttöku.
    2. Í lok tímabilsins fer fram lotutalning.
    3. Handvirk leiðrétting fyrir magn og gildi er bókað í birgðahald. (Móðureikningurinn er birgðabreytingareikningur sem jafnar kostnaðinn sem var bókaður í skrefi 1. Þess vegna sérðu aðeins breytileika í hlutabréfaverðmæti á þessum reikningi.)

The *pósta til gjaldfærslureiknings* meginreglan gerir þér kleift að gera þessar tvær færslur fullkomlega sjálfvirkar. Á þennan hátt er hægt að útrýma handvirkri leiðréttingarbókun við lok tímabilsloka.

## <a name="enable-the-post-to-charge-account-accounting-principle"></a>Virkja bókhaldsregluna fyrir færslu til að gjaldfæra reikning

Til að virkja *pósta til gjaldfærslureiknings* reikningsskilareglu, fylgdu þessum skrefum.

1. Farðu í **Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**.
2. Á **Reikningur** flipa, á **Reikningur** flýtiflipann, stilltu **Bókaðu á gjaldfærslureikning í höfuðbók** valmöguleika til *Já*.
3. Lokið síðunni.

## <a name="prerequisites-and-recommended-parameters-for-the-post-to-charge-account-accounting-principle"></a>Forsendur og ráðlagðar færibreytur fyrir bókhaldsreglu færslu til gjaldfærslu

Ef þú ætlar að gera grein fyrir innkaupagjöldum og lagerafbrigðum verða eftirfarandi forsendur að vera til staðar:

- Á **Reikningur** flipi á **Færibreytur viðskiptaskulda** síða (**Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**), the **Bókaðu á gjaldfærslureikning í höfuðbók** valkostur verður að vera stilltur á *Já*.
- Á **Hlutamódelhópar** síða (**Kostnaðarstjórnun \> Uppsetning reikningsskilaaðferða birgða \> Hlutamódelhópar**), allir eftirfarandi valkostir verða að vera stilltir á *Já* fyrir hvern viðeigandi tegundarhóp sem inniheldur hluti sem eru innifalin í innkaupapöntun:

    - Bóka raunverulegar birgðir
    - Bóka fjárhagslegar birgðir
    - Safna upp skuld á innhreyfingarskjali afurða

- Á **Afhending** flipi á **Innkaupa- og innkaupabreytur** síða (**Innkaup og innkaup \> Uppsetning \> Innkaupa- og innkaupabreytur**), the **Búðu til gjöld á vörumóttöku** valkostur verður að vera stilltur á *Já*.
- Á **Birgðabókhald** flipi á **Birgða- og vöruhúsastjórnunarfæribreytur** síða (**Vörustjórnun \> Uppsetning \> Birgða- og vöruhúsastjórnunarfæribreytur**), the **Bókaðu fylgiseðil í höfuðbók** valkostur verður að vera stilltur á *Já*.
- Á **Pöntun** flipi á **Birting** síða (**Vörustjórnun \> Uppsetning \> Birting \> Birting**), verður að tilgreina aðalreikninga sem eiga við um hvern viðkomandi lið fyrir hverja af eftirfarandi bókunartegundum:

    - Útgjöld innkaupa, óreikningsfærð
    - Innkaupaútgjöld afurðar
    - Birgðaafbrigði

## <a name="example-scenario-1-change-in-unit-cost-price"></a>Dæmi sviðsmynd 1: Breyting á kostnaðarverði eininga

Þetta dæmi atburðarás hefur eftirfarandi forsendur:

- Fyrst inn, fyrst út (FIFO) kostnaðarlíkan

Eftirfarandi ferli gefur dæmi sem sýnir hvað gerist þegar kostnaðarverði eininga er breytt í innkaupapöntun.

1. Stofna innkaupapöntun fyrir 1 magn af vöru sem hefur einingarverðið 100,00.
2. Staðfesta innkaupapöntun.
3. Bókaðu vörukvittun fyrir innkaupapöntunina.
4. Staðfestu skírteinið á vörukvittuninni. Eftirfarandi tafla sýnir sýnishorn af skírteini.

    | Bókunargerð | Aðallykill | Heiti aðallykils | Lykilgerð | Debet/kredit? | Millireikningur | Líkamlegt/fjárhagslegt? | Upphæð |
    |---|---|---|---|---|---|---|---|
    | Innkaup, birgðaafbrigði | 600170 | Lagerafbrigði efni | Kostnaður | Kredit | Nr. | Efnislegt | -100,00 |
    | Kostnaður vegna keypts efnis sem er móttekið | 140100 | Efnisskrá | Eign | Debet | Já | Efnislegt | 100.00 |
    | Útgjöld innkaupa, óreikningsfærð | 600180 | Efniskvittanir | Kostnaður | Debet | Já | Efnislegt | 100.00 |
    | Innkaup, uppsöfnun | 200140 | Uppsöfnuð kaup | Bótaábyrgð | Kredit | Já | Efnislegt | -100,00 |

5. Bókaðu reikninginn fyrir innkaupapöntunina sem hefur uppfært einingarverð 110,00.
6. Staðfestu skírteinið á reikningnum. Eftirfarandi tafla sýnir sýnishorn af skírteini.

    | Bókunargerð | Aðallykill | Heiti aðallykils | Lykilgerð | Debet/kredit? | Millireikningur | Líkamlegt/fjárhagslegt? | Upphæð |
    |---|---|---|---|---|---|---|---|
    | Innkaup, birgðaafbrigði | 600170 | Lagerafbrigði efni | Kostnaður | Kredit | Nr. | Fjármál | -10,00 |
    | Kostnaður vegna keypts efnis sem er móttekið | 140100 | Efnisskrá | Eign | Debet | Já | Fjármál | -100,00 |
    | Útgjöld innkaupa, óreikningsfærð | 600180 | Efniskvittanir | Kostnaður | Debet | Já | Fjármál | -100,00 |
    | Innkaup, uppsöfnun | 200140 | Uppsöfnuð kaup | Bótaábyrgð | Kredit | Já | Fjármál | 100.00 |
    | Kostnaður vegna keypts reikningsfærðs efnis | 140100 | Efnisskrá | Eign | Debet | Nr. | Fjármál | 110,00 |
    | Innkaupaútgjöld afurðar | 600180 | Efniskvittun | Kostnaður | Kredit | Nr. | Fjármál | 110,00 |
    | Staða lánardrottins | 211000 | Viðskiptaskuldir | Bótaábyrgð | Kredit | Nr. | Fjármál | -110.00 |

## <a name="example-2-charges-and-indirect-costs-on-the-purchase-order"></a>Dæmi 2: Gjöld og óbeinn kostnaður á innkaupapöntun

Þetta dæmi atburðarás hefur eftirfarandi forsendur:

- FIFO kostnaðarlíkan
- **Gjaldkóði 1:** Debetatriði og kreditbók eru 10%
- **Gjaldkóði 2:** Debethlutur og kreditviðskiptavinur/seljandi fyrir 10.00 hlutfallslega
- **Óbeinn kostnaður:** 2,00% bætt við kaupverð

Eftirfarandi ferli gefur dæmi sem sýnir hvað gerist þegar gjöld og óbeinn kostnaður eru teknir með í innkaupapöntun.

1. Stofna innkaupapöntun fyrir 1 magn af vöru sem hefur einingarverðið 100,00.
2. Bættu við einum gjaldakóða fyrir 10 prósent sem skuldfæra vöruna og skuldfæra höfuðbókina.
3. Bættu við einum gjaldakóða fyrir 10.00 sem skuldfærir vöruna og skuldfærir viðskiptavininn/söluaðilann.
4. Úthluta gjöldum á innkaupapöntunarlínur.
5. Staðfesta innkaupapöntun.
6. Bókaðu vörukvittun fyrir innkaupapöntunina.
7. Staðfestu skírteinið á vörukvittuninni. Eftirfarandi tafla sýnir sýnishorn af skírteini.

    | Bókunargerð | Aðallykill | Heiti aðallykils | Lykilgerð | Debet/kredit? | Millireikningur | Líkamlegt eða fjárhagslegt | Upphæð |
    |---|---|---|---|---|---|---|---|
    | Innkaup, birgðaafbrigði | 600170 | Lagerafbrigði efni | Kostnaður | Kredit | Nr. | Efnislegt | -110.00 |
    | Áætlaður óbeinn kostnaður notaður | 600520 | Upptekinn óbeinn kostnaður | Kostnaður | Kredit | Já | Efnislegt | -2.40 |
    | Farmur í innkaupum | 600120 | Frakt/flutningskostnaður | Kostnaður | Kredit | Nr. | Efnislegt | -10,00 |
    | Kostnaður vegna keypts efnis sem er móttekið | 140100 | Efnisskrá | Eign | Debet | Já | Efnislegt | 122,40 |
    | Útgjöld innkaupa, óreikningsfærð | 600180 | Efniskvittanir | Kostnaður | Debet | Já | Efnislegt | 110,00 |
    | Innkaup, uppsöfnun | 200140 | Uppsöfnuð kaup | Bótaábyrgð | Kredit | Já | Efnislegt | -110.00 |

8. Bókaðu reikninginn fyrir innkaupapöntunina.
9. Staðfestu skírteinið á reikningnum. Eftirfarandi tafla sýnir sýnishorn af skírteini.

    | Bókunargerð | Aðallykill | Heiti aðallykils | Lykilgerð | Debet/kredit? | Millireikningur | Líkamlegt/fjárhagslegt? | Upphæð |
    |---|---|---|---|---|---|---|---|
    | Innkaup, birgðaafbrigði | 600170 | Lagerafbrigði efni | Kostnaður | Kredit | Nr. | Fjármál | 0,00 |
    | Áætlaður óbeinn kostnaður notaður | 600520 | Upptekinn óbeinn kostnaður | Kostnaður | Debet | Já | Fjármál | 2,40 |
    | Óbeinn kostnaður notaður | 600520 | Upptekinn óbeinn kostnaður | Kostnaður | Debet | Nr. | Fjármál | -2.40 |
    | Kostnaður vegna keypts efnis sem er móttekið | 140100 | Efnisskrá | Eign | Kredit | Já | Fjármál | -110.00 |
    | Útgjöld innkaupa, óreikningsfærð | 600180 | Efniskvittanir | Kostnaður | Kredit | Já | Fjármál | -110.00 |
    | Innkaup, uppsöfnun | 200140 | Uppsöfnuð kaup | Bótaábyrgð | Debet | Já | Fjármál | 110,00 |
    | Kostnaður vegna keypts reikningsfærðs efnis | 140100 | Efnisskrá | Eign | Debet | Nr. | Fjármál | 110,00 |
    | Innkaupaútgjöld afurðar | 600180 | Efniskvittun | Kostnaður | Kredit | Nr. | Fjármál | 110,00 |
    | Staða lánardrottins | 211000 | Viðskiptaskuldir | Bótaábyrgð | Kredit | Nr. | Fjármál | -110.00 |