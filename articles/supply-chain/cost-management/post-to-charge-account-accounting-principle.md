---
title: Reikningsskilaregla bóka á gjaldalykil
description: Þessi grein veitir yfirlit yfir bókhaldsregluna „bóka á gjaldalykil“.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016566"
---
# <a name="post-to-charge-account-accounting-principle"></a>Reikningsskilaregla bóka á gjaldalykil

Bókhaldsreglan *bóka á gjaldalykil* gerir þér kleift að gera grein fyrir og afstemma á auðveldari hátt mismun á einingarverðinu á milli efnislegrar bókunar og fjárhagslegrar bókunar, óbeins kostnaðar og keyptra vara eða gjalda á innkaupapöntun.

Tvær skilgreiningar fyrir gjaldakóða viðskiptaskulda á síðunni **Gjaldakóði** (**Viðskiptaskuldir \> Uppsetning gjalda \> Gjaldakóðar**) geta orðið til þess að innkaupapöntun hafi áhrif á verðmat birgðaeigna:

- Fyrir gjaldakóða þar sem reiturinn **Debetgerð** er stilltur á *Vöru* og reiturinn **Kreditgerð** er stilltur á *Fjárhagslykil* virkar fjárhagslykillinn eins og hagnýtur lykill virkar eins og birgðaafbrigðislykill.
- Fyrir gjaldakóða þar sem reiturinn **Debetgerð** er stilltur á *Vöru* og reiturinn **Kreditgerð** er stilltur á *Viðskiptavinur/Lánardrottinn* verður gerð greint fyrir gjaldinu sem efniskostnað og birgðaafbrigðislykill vörunnar verður notaður.

## <a name="european-special-accounting-rule"></a>Sérstök evrópsk bókhaldsregla

Í Evrópu er bókhaldsreglan *bóka á gjaldalykil* oft notuð til að innleiða sérstaka bókhaldsreglu. Ein af eftirfarandi aðferðum er til dæmis yfirleitt notuð til að reikna birgðabreytingar:

- **Kostnaður við söluaðferð** – Staðlaðar stillingar á birgðabókunarsniði styðja þessa aðferð. Ekki er þörf á bókhaldsreglunni *bóka á gjaldalykil*.
- **Eðli kostnaðaraðferðar** – Minni fyrirtæki nota oft þessa aðferð. Það felur yfirleitt í sér eftirfarandi skref:

    1. Vörur eða þjónusta eru gjaldfærðar að fullu við móttöku.
    2. Við lok tímabils er regluleg talning framkvæmd.
    3. Handvirk leiðrétting fyrir magn og virði er birt í birgðum. (Mótlykill er birgðabreytingareikningur sem jafnar út kostnaðinn sem var birtur í skrefi 1. Þar af leiðandi sérðu aðeins afbrigðið í birgðagildinu í þessum lykli.)

Reglan *bóka á gjaldakóða* gerir þér kleift að sjálfvirknivæða báðar bókanir að fullu. Þannig er hægt að útrýma leiðréttingarbókun við lokun tímabils.

## <a name="enable-the-post-to-charge-account-accounting-principle"></a>Virkja bókunarregluna „bóka á gjaldalykil“

Til að virkja bókhaldsregluna *bóka á gjaldalykil* skal fylgja þessum skrefum.

1. Farðu í **Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**.
2. Í flipanum **Reikningur**, í flýtiflipanum **Reikningur**, skal stilla valkostinn **Bóka á gjaldalykil í fjárhag** á *Já*.
3. Lokið síðunni.

## <a name="prerequisites-and-recommended-parameters-for-the-post-to-charge-account-accounting-principle"></a>Skilyrði og ráðlagðar færibreytur fyrir bókhaldsregluna „bóka á gjaldalykil“

Ef þú hyggst reikna með innkaupagjöldum og brigðaafbrigðum þurfa eftirfarandi skilyrði að vera til staðar:

- Í flipanum **Reikningur** á síðunni **Færibreytur viðskiptaskulda** (**Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**) verður að stilla valkostinn **Bóka á gjaldalykil í fjárhag** á *Já*.
- Á síðunni **Vörulíkanaflokkar** (**Kostnaðarstjórnun \> Uppsetning á birgðabókhaldsreglum \> Vörulíkanaflokkar**) þarf að stilla alla eftirfarandi valkosti á *Já* fyrir alla viðeigandi líkanaflokka sem innihalda vörur sem eru hluti af innkaupapöntun:

    - Bóka raunverulegar birgðir
    - Bóka fjárhagslegar birgðir
    - Safna upp skuld á innhreyfingarskjali afurða

- Í flipanum **Afhenda** á síðunni **Færibreytur innkaupa og aðfanga** (**Innkaup og aðföng \> Uppsetning \> Færibreytur innkaupa og aðfanga**) verður að stilla valkostinn **Mynda gjöld á innhreyfingarskjali afurða** á *Já*.
- Í flipanum **Birgðabókhald** á síðunni **Færibreytur birgða- og vöruhúsakerfis** (**Birgðastjórnun \> Uppsetning \> Færibreytur birgða- og vöruhúsakerfis**) verður að stilla valkostinn **Bóka fylgiseðil í fjárhag** á *Já*.
- Í flipanum **Innkaupapöntun** á síðunni **Bókun** (**Birgðastjórnun \> Uppsetning \> Bókun \> Bókun**) verður að tilgreina aðallykla sem gilda um allar viðeigandi vörur fyrir hverja af eftirfarandi bókunargerðum:

    - Útgjöld innkaupa, óreikningsfærð
    - Innkaupaútgjöld afurðar
    - Birgðaafbrigði

## <a name="example-scenario-1-change-in-unit-cost-price"></a>Dæmi 1: Breyting á kostnaðarverði einingar

Þessar dæmiaðstæður hafa eftirfarandi skilyrði:

- FIFO (first in, first out) kostnaðarlíkan

Eftirfarandi ferli sýnir hvað gerist þegar einingarkostnaði er breytt í innkaupapöntun.

1. Stofna innkaupapöntun fyrir magnið 1 á vöru sem er með einingarverðið 100,00.
2. Staðfesta innkaupapöntun.
3. Bóka innhreyfingarskjal afurða fyrir innkaupapöntunina.
4. Staðfesta fylgiskjal á innhreyfingarskjali. Eftirfarandi tafla sýnir dæmi um fylgiskjal.

    | Bókunargerð | Aðallykill | Heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | Efnislegt/fjárhagslegt? | Upphæð |
    |---|---|---|---|---|---|---|---|
    | Innkaup, birgðaafbrigði | 600170 | Efni birgðaafbrigðis | Kostnaður | Kredit | Nr. | Efnislegt | -100,00 |
    | Kostnaður vegna keypts efnis sem er móttekið | 140100 | Efnisbirgðir | Eign | Debet | Já | Efnislegt | 100.00 |
    | Útgjöld innkaupa, óreikningsfærð | 600180 | Efnisinnhreyfingar | Kostnaður | Debet | Já | Efnislegt | 100.00 |
    | Innkaup, uppsöfnun | 200140 | Uppsöfnuð innkaup | Bótaábyrgð | Kredit | Já | Efnislegt | -100,00 |

5. Bókaðu reikninginn fyrir innkaupapöntunina sem er með uppfært einingarverð upp á 110,00.
6. Staðfestu fylgiskjalið á reikningnum. Eftirfarandi tafla sýnir dæmi um fylgiskjal.

    | Bókunargerð | Aðallykill | Heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | Efnislegt/fjárhagslegt? | Upphæð |
    |---|---|---|---|---|---|---|---|
    | Innkaup, birgðaafbrigði | 600170 | Efni birgðaafbrigðis | Kostnaður | Kredit | Nr. | Fjármál | -10,00 |
    | Kostnaður vegna keypts efnis sem er móttekið | 140100 | Efnisbirgðir | Eign | Debet | Já | Fjármál | -100,00 |
    | Útgjöld innkaupa, óreikningsfærð | 600180 | Efnisinnhreyfingar | Kostnaður | Debet | Já | Fjármál | -100,00 |
    | Innkaup, uppsöfnun | 200140 | Uppsöfnuð innkaup | Bótaábyrgð | Kredit | Já | Fjármál | 100.00 |
    | Kostnaður vegna keypts reikningsfærðs efnis | 140100 | Efnisbirgðir | Eign | Debet | Nr. | Fjármál | 110,00 |
    | Innkaupaútgjöld afurðar | 600180 | Efnisinnhreyfing | Kostnaður | Kredit | Nr. | Fjármál | 110,00 |
    | Staða lánardrottins | 211000 | Viðskiptalykill viðskiptaskulda | Bótaábyrgð | Kredit | Nr. | Fjármál | -110,00 |

## <a name="example-2-charges-and-indirect-costs-on-the-purchase-order"></a>Dæmi 2: Gjöld og óbeinn kostnaður á innkaupapöntunina

Þessar dæmiaðstæður hafa eftirfarandi skilyrði:

- FIFO kostnaðarmódel
- **Gjaldakóði 1:** Debetvara og kreditfjárhagslykill fyrir 10%
- **Gjaldakóði 2:** Debetvara og kreditviðskiptavinur/lánardrottinn fyrir 10,00 hlutfallslega
- **Óbeinn kostnaður:** 2,00% bætt við innkaupsverð

Eftirfarandi ferli gefur dæmi sem sýnir hvað gerist þegar gjöld og óbeinn kostnaður eru innifalin í innkaupapöntun.

1. Stofna innkaupapöntun fyrir magnið 1 á vöru sem er með einingarverðið 100,00.
2. Bæta við einum gjaldakóða fyrir 10 prósent sem skuldfærir hlutinn og inneignir í fjárhaginn.
3. Bæta við einum kóða fyrir 10,00 sem skuldfærir hlutinn og kreditfærir viðskiptavina/lánardrottinn.
4. Úthluta gjöldunum á innkaupapöntunarlínurnar.
5. Staðfesta innkaupapöntun.
6. Bóka innhreyfingarskjal afurða fyrir innkaupapöntunina.
7. Staðfesta fylgiskjal á innhreyfingarskjali. Eftirfarandi tafla sýnir dæmi um fylgiskjal.

    | Bókunargerð | Aðallykill | Heiti aðallykils | Lykilgerð | Debet/kredit? | Millireikningur | Efnislegt eða fjárhagslegt | Upphæð |
    |---|---|---|---|---|---|---|---|
    | Innkaup, birgðaafbrigði | 600170 | Efni birgðaafbrigðis | Kostnaður | Kredit | Nr. | Efnislegt | -110,00 |
    | Áætlaður óbeinn kostnaður notaður | 600520 | Notaður óbeinn kostnaður | Kostnaður | Kredit | Já | Efnislegt | -2,40 |
    | Farmur í innkaupum | 600120 | Farm-/flutningskostnaður | Kostnaður | Kredit | Nr. | Efnislegt | -10,00 |
    | Kostnaður vegna keypts efnis sem er móttekið | 140100 | Efnisbirgðir | Eign | Debet | Já | Efnislegt | 122,40 |
    | Útgjöld innkaupa, óreikningsfærð | 600180 | Efnisinnhreyfingar | Kostnaður | Debet | Já | Efnislegt | 110,00 |
    | Innkaup, uppsöfnun | 200140 | Uppsöfnuð innkaup | Bótaábyrgð | Kredit | Já | Efnislegt | -110,00 |

8. Bóka reikninginn fyrir innkaupapöntunina.
9. Staðfestu fylgiskjalið á reikningnum. Eftirfarandi tafla sýnir dæmi um fylgiskjal.

    | Bókunargerð | Aðallykill | Heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | Efnislegt/fjárhagslegt? | Upphæð |
    |---|---|---|---|---|---|---|---|
    | Innkaup, birgðaafbrigði | 600170 | Efni birgðaafbrigðis | Kostnaður | Kredit | Nr. | Fjármál | 0,00 |
    | Áætlaður óbeinn kostnaður notaður | 600520 | Notaður óbeinn kostnaður | Kostnaður | Debet | Já | Fjármál | 2,40 |
    | Óbeinn kostnaður notaður | 600520 | Notaður óbeinn kostnaður | Kostnaður | Debet | Nr. | Fjármál | -2,40 |
    | Kostnaður vegna keypts efnis sem er móttekið | 140100 | Efnisbirgðir | Eign | Kredit | Já | Fjármál | -110,00 |
    | Útgjöld innkaupa, óreikningsfærð | 600180 | Efnisinnhreyfingar | Kostnaður | Kredit | Já | Fjármál | -110,00 |
    | Innkaup, uppsöfnun | 200140 | Uppsöfnuð innkaup | Bótaábyrgð | Debet | Já | Fjármál | 110,00 |
    | Kostnaður vegna keypts reikningsfærðs efnis | 140100 | Efnisbirgðir | Eign | Debet | Nr. | Fjármál | 110,00 |
    | Innkaupaútgjöld afurðar | 600180 | Efnisinnhreyfing | Kostnaður | Kredit | Nr. | Fjármál | 110,00 |
    | Staða lánardrottins | 211000 | Viðskiptalykill viðskiptaskulda | Bótaábyrgð | Kredit | Nr. | Fjármál | -110,00 |
