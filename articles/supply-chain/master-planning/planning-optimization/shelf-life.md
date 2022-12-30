---
title: Aðaláætlanagerð fyrir vörur með takmarkaðan endingartíma
description: Í þessari grein er lýst hvernig á að setja upp og nota skipulagseiginleika sem taka tillit til endingartíma forgengilegra vara.
author: t-benebo
ms.date: 08/10/2022
ms.topic: article
ms.search.form: ReqPlanSched, CustTable, EcoResProductDetailsExtended, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 68a1ba2bfe90aaf0462917c405d483fa12bf8126
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428222"
---
# <a name="master-planning-for-products-with-limited-shelf-life"></a>Aðaláætlanagerð fyrir vörur með takmarkaðan endingartíma

[!include [banner](../../includes/banner.md)]

Endingartímier sá tími sem geyma má vöru þar til ekki er lengur hægt að nota hana eða selja. Fyrir vörur sem hafa takmarkaðan endingartíma, munt þú líklega nota fyrst út (FEFO) vöruhúsastefnu, sem forgangsraðar notnun og sölu á vörum byggt á endingartíma þeirra sem eftir eru. Þessi vöruhúsastefna á við um matvæli, lyf og aðrar vörur sem einkennast af stuttum geymslutíma. Samkvæmt FEFO eru vörur í vöruhúsinu geymdir eins og vörur í hillu í verslunum: vörur sem hafa langan endingartíma eru settar djúpt í hillurnar, þannig að vörur sem hafa styttri endingartíma eru sendar fyrst.

## <a name="using-shelf-life-in-master-planning"></a>Notkun endingartíma við áætlanagerð

Þessi hluti útskýrir hvernig aðaláætlanagerð leggur til framboð á geymsluþolnum hlutum.

Þegar aðaláætlun er keyrð býr hún til áætlaðar pantanir (framboð) sem munu fullnægja eftirspurn þinni og einnig lágmarka tafir. Ef áætlunin þín inniheldur vörur með takmarkaðan endingartíma verða útreikningar flóknari þar sem áætlunin verður ekki aðeins að lágmarka tafir heldur einnig að nota fyrirliggjandi framboð áður en það rennur út. Áætlunin verður að reyna að nota framboð sem næst lokadegi þeirra áður en framboð renna út síðar. Í aðaláætlanagerð er því leitast við að ná eftirfarandi markmiðum, í þessari röð:

1. Lágmarkaðu summu tafa.
1. Hámarka samtölu FEFO-birgða.
1. Lágmarka áfyllingu birgða.

Í sumum tilvikum gæti orðið árekstur á milli tveggja fyrstu markmiða og velja verður: Viltu seinka sendingu eða viltu nota framboð sem rennur út síðar í stað framboðs sem rennur út fyrr? Til að leysa úr þessum árekstri á meðan á aðaláætlun stendur forgangsraðar kerfið því að lágmarka tafir á meðan verið er að nýta birgðir sem renna fljótlega út. Slíkur ágreiningur gæti almennt átt sér stað þegar tafir verða á þekju eftir tímabilum. Því mælum við með því að nota þekjutímabil sem er styttra en endingartími vöru. Ólíklegt er að aðrar tegundir þekju (eins og skilyrði) lendi í þessum árekstri.

## <a name="set-up-shelf-life"></a>Setja upp endingartíma

### <a name="configure-each-master-plan-to-consider-shelf-life"></a>Stilla hverja aðaláætlun til að taka mið af endingartíma

Sjálfgefið er að aðaláætlanir taki ekki tillit til endingartíma. Notið eftirfarandi ferli til að gera útreikninga á endingartíma fyrir hvert aðaláætlun sem krefst þeirra.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Veldu núverandi flokk á listasvæðinu eða búa til nýjan.
1. Á flýtiflipanum **Almennt** skal stilla valkostinn **Nota endingartíma** á *Já*.

### <a name="configure-tracking-dimension-groups-to-track-the-batch-dimension"></a>Stilla rakningarvíddaflokka til að fylgjast með runuvíddinni

Aðeins er hægt að fylgjast með endingartími vöru ef hann er rakinn við runuvíddina. Með öðrum orðum verður að skrá runutilvísun og nauðsynlegar dagsetningar við móttöku eða framleiðslu og í gegnum allar birgðafærslur á vörunni. Til að hafa umsjón með þessum valkosti skaltu setja upp einn eða fleiri rakningarvíddarflokka til að gera nauðsynlega rakningu og úthluta síðan viðkomandi vörum til þessara flokka eftir þörfum.

Notið eftirfarandi ferli til að setja upp rakningarvíddarflokk til að fylgjast með runuvíddinni.

1. Farið í **Vöruupplýsingastjórnun \> Uppsetning \> vídd- og afbrigðaflokkar \> Rakningarvíddarflokkar**.
1. Fylgið einu af eftirfarandi skrefum:

    - Á aðgerðasvæðinu skal velja **Nýtt** til að búa til nýjan rakningarvíddarflokk. Sláið inn heiti og lýsingu og síðan velja **Vista** á aðgerðasvæðinu.
    - Í listasvæðinu skal velja þá rakningarvíddarflokk sem á að setja upp til að rekja runuvíddina.

1. Á flýtiflipanum **Rakningarvídd** í línunni **Rununúmer** skal velja gátreitina í dálkunum **Virkt** og **Efnislegar birgðir**.

### <a name="set-up-shelf-life-for-a-product"></a>Setja upp endingartíma fyrir afurð

Notaðu eftirfarandi ferli til að setja upp endingartíma vöru.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Stofna eða opna vöruna sem á að setja upp.
1. Til að nota stillingar fyrir endingartíma, á flýtiflipanum **Almennt**, stillið reitinn **Rakningarvíddarflokkar** á rakningarvíddarflokk sem er settur upp til að fylgjast með runuvíddinni. Þú getur aðeins stillt þennan reit þegar þú ert fyrst að búa til vöru. Ekki er hægt að breyta gildi fyrir núverandi vörur.
1. Á flýtiflipanum **Stjórna birgðum** skal stilla eftirfarandi reiti:

    - **Ráðlagt hillutímabil í dögum** – Tilgreinið tímabilið (í dögum) sem á að athuga runu af þessari vöru til að tryggja að það henti til notkunar eða endursölu. Gildinu í þessum reit er bætt við *framleiðsludagsetningu* runu til að ákvarða *ráðlagðan geymslutíma* hennar. Hægt er að skilgreina kerfið til að búa til gæðapantanir þegar runa nálgast dagsetningu ráðlagður geymslutíma.
    - **Endingartími í dögum** – Tilgreinið fjölda daga áður en runa af þessari vöru rennur út. Þessu gildi er bætt við *framleiðsludagsetningu* til að ákvarða *fyrningardagsetninguna*. Lotan er talin ónothæf eftir þessa dagsetningu.
    - **Tímabil fyrningar í dögum** – Tilgreinið tímabilið (í dögum) þar sem runa af þessari vöru er enn talin seljanleg en getur ekki lengur haldið eftir hluta af upprunalegum eiginleikum hennar. Þessu gildi er bætt við *framleiðsludagsetningu* til að ákvarða *fyrningardagsetninguna*. Hægt er að keyra skýrslur til að auðkenna birgðir sem eru komnar fram yfir fyrningardag. 

### <a name="set-a-sellable-days-rule-for-each-customer"></a>Setja upp reglu um seljanlega daga fyrir hvern viðskiptavin

Eiginleikinn *Seljanlegir dagar* tryggir að vörur úr runu sem brátt rennur út eru ekki sendar til viðskiptavina. Auk þess tryggir það að þegar vörur eru sendar til viðskiptavinar haldist fullnægjandi fjöldi seljanlegra daga eftir afhendingu.

Til að eiginleikann seljanlegir dagar þarf að skilgreina fjölda seljanlegra daga sem eiga við hverja vöru (eða vöruhóp) fyrir hvern viðskiptavin. Þú verður að ljúka þessu ferli handvirkt vegna þess að það er engin gagnaeining fyrir það.

Notið eftirfarandi ferli til að setja upp seljanlega daga fyrir hverja vöru fyrir hvern viðskiptavin.

1. Opnið **Sölu og markaðssetning \> Viðskiptavinir \> Allir viðskiptavinir**.
1. Leitaðu að og veldu viðskiptavinur sem á að setja upp.
1. Á aðgerðarúðunni á flipanum **Sala** í flokknum **Uppsetning** skal velja **Sala \> Seljanlegir dagar**.
1. Á síðunni **Seljanlegir dagar fyrir viðskiptavini** er listi yfir gildandi reglur um seljanlega daga fyrir hverja vöru eða vöruhóp. Hægt er að nota hnappana á aðgerðasvæði til að bæta við eða breyta línum í hnitanetinu eftir þörfum. **Sía** er til staðar til að hjálpa þér að finna línur sem þegar eru til staðar.
1. Fyrir hverja línu skal stilla eftirfarandi reiti:

    - **Vörukóði** - Velja eitt af eftirfarandi gildum til að tilgreina umfang varanna sem verða fyrir áhrifum:

        - *Tafla* – lína á við um tiltekna vöru.
        - *Flokkur* – Línan gildir fyrir tiltekinn vöruflokk.
        - *Allt* – Línan á við um allar vörur.

    - **Vöruvensl** - Velja skal tiltekna vöru ef reiturinn **Vörukóði** er stilltur á *Tafla*. Ef reiturinn **Vörukóði** er stilltur á *Flokkur* skal velja vöruflokk. Ef þú stillir reitinn **Vörukóði** á *Allt*, þá er þessi reitur ekki tiltækur.
    - **Seljanlegir dagar** – Sláðu inn þann lágmarksfjölda daga sem viðskiptavinurinn verður að hafa til að selja samsvarandi vörur áður en runan rennur út. Gildi seljanlegra daga er byggt á umbeðnum móttökudegi (eða staðfestum móttökudegi, ef hann er skilgreindur) fyrir samsvarandi vörur á sölupöntuninni.
    - *(Aðrar vöruvíddir)* – Til að afmarka umfang línu enn frekar skal tilgreina önnur stærðarvgildi (svo sem **stærð** og **lit**) eftir þörfum. Til að stjórna því hvaða víddir eru sýndar í hnitanetinu skal velja **Birta víddir** á Aðgerðasvæði.

### <a name="set-up-all-relevant-products-so-that-they-are-fefo-date-controlled"></a>Setja upp allar viðeigandi vörur þannig að þeim sé stjórnað með FEFO dagsetningu

Til að seljanlegir dagar virki verður hver vara að tilheyra vörulíkanshópi þar sem **FEFO dagsetningastýrt** gátreiturinn er valinn.

Notið eftirfarandi ferli til að setja upp vörulíkanaflokkur þannig að hann styðji virkni seljanlegra daga.

1. Opnið **Birgðastjórnun \> Uppsetning \> Birgðir \> Vörulíkanaflokkar.**
1. Veldu núverandi flokk á listasvæðinu eða veldu **Nýtt** á aðgerðasvæðinu til að búa til nýjan.
1. Í flýtiflipanum **Birgðareglur** skal velja gátreitinn **Dagsetningarstýrt samkvæmt FEFO**.
1. Setja upp aðra reiti fyrir flokkinn eftir þörfum.

Notið eftirfarandi ferli til að skoða eða stilla vörulíkanaflokkinn sem vara tilheyrir.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Opna vöru sem á að skoða eða breyta.
1. Á flýtiflipanum **Almennt** stillir þú reitinn **Vörulíkanaflokkur** á flokk sem gátreiturinn **FEFO dagsetningastýrt** er valinn.

## <a name="example-1-simple-fefo-10-day-period-zero-days-of-lead-time"></a>Dæmi 1: Einfaldur FEFO, 10 daga tímabil, núll dagar af afhendingartíma

Þetta dæmi sýnir grunndæmi um endingartími, þar sem þarfarakning pantana milli framboðs og eftirspurnar er gerð til að uppfylla eftirfarandi markmiðum kerfisins:

- Lágmarkaðu summu tafa.
- Hámarka samtölu FEFO-birgða.
- Lágmarka áfyllingu birgða.

Í kerfinu eru eftirfarandi stillingar fyrir vöru og aðaláætlun:

- **Þekjukóði (áfyllingaráætlun):** Tímabil 
- **Bótatímabil:** 10 dagar (jafnt endingartíma)
- **Endingartími:** 10 dagar
- **Seljanlegir dagar:** 0 days
- **Afhendingartími:** 0 dagar
- **Neikvæður dagafjöldi:** 0 dagar
- **Tegund áætlaðrar pöntunar (sjálfgefnar pöntunarstillingar vörunnar):** Innkaupapöntun

Eftirfarandi sölupantanir fyrir vöruna eru til í kerfinu:

- **SO1:** Magn (mgn) = 2, umbeðinn afhendingardagur = í dag + 1 dagur
- **SO2:** Magn = 1, umbeðinn afhendingardagur = í dag + 4 dagar
- **SO3:** Magn = 1, umbeðinn afhendingardagur = í dag + 5 dagar

Allar þessar sölupantanir skapa eftirspurn eftir vörunni.

Eftirfarandi framboð eru til fyrir vöruna:

- **Lagerbirgðir:** Magn = 1, lokadagur = í dag + 5 dagar
- **Innkaupapöntun 1 (PO1):** Móttökudagsetning = í dag + 2 dagar, magn = 1, lokadagur = í dag + 4 dagar

Kerfið býr til lista yfir framboð sem getur mætt þessari eftirspurn og hann raðar listanum eftir endingartíma (með því að nota FEFO).

Aðaláætlanagerð skapar áskilda þarfarakningu milli framboðs og eftirspurnar. Það skapar einnig alla nauðsynlega eftirspurn á grundvelli framboðslistans (með því að nota FEFO) og tekur tillit til tiltækilega á dagsetningu.

- Hægt er að uppfylla SO1 með lagerbirgðum, en ekki er hægt að uppfylla það með PO1, þar sem framboðsdagur fyrir PO1 er einum degi síðar en SO1 krefst. Þess vegna myndar SO1 eftirspurn eftir einni vörueiningu.
- Hægt er að þekja SO2 með PO1 þar sem PO1 kemur á umsömdum tíma og lokadagsetning gildir enn. Þar af leiðandi er skilyrði SO2 þakið af öllu leyti af PO1.
- SO3 er ekki þakið, vegna þess að tilföng eru ekki tiltæk. Þess vegna myndar SO3 eftirspurn eftir einni vörueiningu.

Kerfið þarf að búa til eftirfarandi áætlaða innkaupapöntun til að þekja allar eftirstandandi kröfur:

- **PPO1:** Móttökudagsetning = í dag, magn = 2, lokadagur = í dag + 10 dagar

Eftirfarandi tafla sýnir samantekt niðurstaðna.

| Eftirspurn | Þarfarakning |
|---|---|
| **SO1:** Afhendingardagur = í dag + 1 dagur, magn = 2 | <p>**Á lager:** Magn = 1, lokadagur = í dag + 5 dagar</p><p>**PPO1:** Móttökudagsetning = í dag, magn = 1, lokadagur = í dag + 10 dagar</p> |
| **SO2:** Afhendingardagur = í dag + 4 dagar, magn = 1 | **PO1:** Móttökudagsetning = í dag + 2 dagar, 1 magn, lokadagur = í dag + 4 dagar |
| **SO3:** Afhendingardagur = í dag + 5 dagar, magn = 1 | **PPO1:** Móttökudagsetning = í dag, magn = 2, lokadagur = í dag + 10 dagar |

Eftirfarandi skýringarmynd sýnir tímalína fyrir þetta dæmi.

![Dæmi 1: Einfaldur FEFO, 10 daga tímabil, núll dagar af afhendingartíma.](media/fefo-example-1.png "Dæmi 1: Einfaldur FEFO, 10 daga tímabil, núll dagar af afhendingartíma")

## <a name="example-2-simple-fefo-requirement-three-days-of-lead-time"></a>Dæmi 2: Einfalt FEFO, skilyrði, þriggja daga afhendingartími

Þetta dæmi sýnir hvernig tilraun kerfisins til að lágmarka tafir getur stundum valdið því að ofpantanir eigi sér stað.

Í kerfinu eru eftirfarandi stillingar fyrir vöru og aðaláætlun:

- **Þekjukóði (áfyllingaráætlun):** Krafa
- **Endingartími:** 10 dagar
- **Seljanlegir dagar:** 0 days
- **Afhendingartími:** Stofnað með eftirfarandi viðskiptasamningum lánardrottins:

    - **Verðsamningur 1:** Ef magn = 1, afhendingartími = 4
    - **Verðsamningur 2:** Ef magn = 2, afhendingartími = 3

- **Neikvæður dagafjöldi:** 0 dagar
- **Tegund áætlaðrar pöntunar (sjálfgefnar pöntunarstillingar vörunnar):** Innkaupapöntun

Eftirfarandi sölupöntun er til í kerfinu:

- **SO1:** Magn = 2, umbeðinn afhendingardagur = í dag + 3 dagar

Þessi eftirspurn fellur undir fyrirliggjandi framboð og staðfesta innkaupapöntun:

- **Lagerbirgðir:** Tiltækt = í dag, magn = 1, lokadagur = í dag + 2 dagar
- **PO1:** Móttökudagsetning = í dag + 3 dagar, magn = 1, lokadagur = í dag + 4 dagar

SO1 er ekki hægt að uppfylla með lagerbirgðum þar sem lokadagur birgða er á undan afhendingardegi. PO1 getur uppfyllt SO1 kröfu með magni sem er aðeins 1. Þess vegna myndar SO1 eftirspurn eftir einni vörueiningu. Til að uppfylla kröfu býr kerfið til innkaupatillögu (PPO1).

Kerfið er með tvo verðsamninga (einn fyrir magn = 1, afhendingartími = 4 dagar og einn fyrir magn = 2, afhendingartími = 3 dagar). Því reynir kerfið að lágmarka tafir með því að búa til áætlaða innkaupapöntun (PPO1) sem uppfyllir annan verðsamninginn. Niðurstaðan er ofafhending (magn = 2, lokadagur = í dag + 10 dagar).

Eftirfarandi tafla sýnir samantekt niðurstaðna.

| Eftirspurn | Þarfarakning |
|---|---|
| **SO1:** Afhendingardagur = í dag + 3 dagar, magn = 2 | <p>**PO1:** Móttökudagsetning = í dag + 3 dagar, magn = 1, lokadagur = í dag + 4 dagar</p><p>**PPO1:** Móttökudagsetning = í dag + 3 dagar, magn = 1, lokadagur = í dag + 10 dagar</p> |

Eftirfarandi skýringarmynd sýnir tímalína fyrir þetta dæmi.

![Dæmi 2: Einfalt FEFO, skilyrði, þriggja daga afhendingartími.](media/fefo-example-2.png "Dæmi 2: Einfalt FEFO, skilyrði, þriggja daga afhendingartími")

## <a name="example-3-simple-fefo-requirement-three-days-of-lead-time-five-sellable-days"></a>Dæmi 3: Einfalt FEFO, skilyrði, þriggja daga afhendingartími, fimm seljanlegir dagar

Þetta dæmi sýnir hvernig geymsluþolið virkar þegar seljanlegum dögum er bætt við fyrir vöru.

Í kerfinu eru eftirfarandi stillingar fyrir vöru og aðaláætlun:

- **Þekjukóði (áfyllingaráætlun):** Krafa
- **Endingartími:** 10 dagar
- **Seljanlegir dagar:** 5 days
- **Afhendingartími:** 5 dagar
- **Neikvæður dagafjöldi:** 0 dagar
- **Tegund áætlaðrar pöntunar (sjálfgefnar pöntunarstillingar vörunnar):** Innkaupapöntun

Eftirfarandi sölupantanir eru til staðar í kerfinu:

- **SO1:** Magn = 2, umbeðinn afhendingardagur = í dag + 2 dagar
- **SO2:** Magn = 1, umbeðinn afhendingardagur = í dag + 3 dagar
- **SO3:** Magn = 1, umbeðinn afhendingardagur = í dag + 5 dagar

Hægt er að mæta þessari eftirspurn með fyrirliggjandi framboði og staðfestri innkaupapöntun:

- **Lagerbirgðir:** Tiltækt = í dag, magn = 1, lokadagur = í dag + 6 dagar
- **PO1:** Móttökudagsetning = í dag + 2 dagar, magn = 3, lokadagur = í dag + 10 dagar

Kerfið býr til lista yfir umsækjendur þarfarakningar, byggt á framboðslista (FEFO) og framboðsdögum. Þess vegna er ekki hægt að uppfylla SO1 með lagerbirgðim, vegna þess að birgðirnar renna út fyrir lok seljanlegra daga sem viðskiptavinurinn krefst (umbeðin móttökudagsetning + 5 dagar). PO1 getur þakið SO1 skilyrðið með tveimur einingum og SO2 kröfuna með einni einingu. Því hefur aðeins SO3 enn fundið eftirspurn eftir einni vörueiningu. Til að uppfylla þetta skilyrði býr kerfið til eftirfarandi innkaupatillögu:

- **PP01:** Móttökudagsetning = í dag + 5 dagar, magn = 1, lokadagur = í dag + 10 dagar

Eftirfarandi tafla sýnir samantekt niðurstaðna.

| Eftirspurn | Þarfarakning |
|---|---|
| **SO1:** Afhendingardagur = í dag + 2 dagar, magn = 2 | **PO1:** Móttökudagsetning = í dag + 2 dagar, magn = 2, lokadagur = í dag + 10 dagar |
| **SO2:** Afhendingardagur = í dag + 3 dagar, magn = 1 | **PO1:** Móttökudagsetning = í dag + 2 dagar, magn = 1, lokadagur = í dag + 10 dagar |
| **SO3:** Afhendingardagur = í dag + 5 dagar, magn = 1 | **PPO1:** Móttökudagsetning = í dag + 5 dagar, magn = 1, lokadagur = í dag + 10 dagar |

Eftirfarandi skýringarmynd sýnir tímalína fyrir þetta dæmi.

![Dæmi 3: Einföld FEFO, skilyrði, þriggja daga afhendingartími, fimm seljanlegir dagar.](media/fefo-example-3.png "Dæmi 3: Einfalt FEFO, skilyrði, þriggja daga afhendingartími, fimm seljanlegir dagar")

## <a name="example-4-simple-fefo-period-lead-time-depends-on-the-quantity"></a>Dæmi 4: Einfalt FEFO, tímabil, afhendingartími fer eftir magni

Þetta dæmi sýnir hvernig tilraun kerfisins til að lágmarka tafir getur stundum valdið því að ofpantanir eigi sér stað.

Í kerfinu eru eftirfarandi stillingar fyrir vöru og aðaláætlun:

- **Þekjukóði (áfyllingaráætlun):** Tímabil
- **Bótatímabil:** 10 dagar (jafnt endingartíma)
- **Endingartími:** 10 dagar
- **Seljanlegir dagar:** 0 days
- **Afhendingartími:** Stofnað með eftirfarandi viðskiptasamningum lánardrottins:

    - **Verðsamningur 1:** Ef magn = 1, afhendingartími = 5
    - **Verðsamningur 2:** Ef magn = 2, afhendingartími = 0

- **Neikvæður dagafjöldi:** 0 dagar
- **Tegund áætlaðrar pöntunar (sjálfgefnar pöntunarstillingar vörunnar):** Innkaupapöntun

Eftirfarandi sölupantanir eru til staðar í kerfinu:

- **SO1:** Magn = 1, umbeðinn afhendingardagur = í dag
- **SO2:** Magn = 1, umbeðinn afhendingardagur = í dag + 6 dagar

Hægt er að tryggja þessa eftirspurn að hluta með fyrirliggjandi framboði frá eftirfarandi staðfestum innkaupapöntunum:

- **PO1:** Móttökudagsetning = í dag + 1 dagur, magn = 1, lokadagur = í dag + 2 dagar
- **PO2:** Móttökudagsetning = í dag + 3 dagar, magn = 1, lokadagur = í dag + 7 dagar

Kerfið er með tvo verðsamninga (einn fyrir magn = 1, afhendingartími = 5 dagar og einn fyrir magn = 2, afhendingartími = 0 dagar). Því reynir kerfið að lágmarka tafir með því að búa til eftirfarandi áætlaða innkaupapöntun sem uppfyllir annan verðsamninginn:

- **PP01:** Móttökudagsetning = í dag, magn = 2, lokadagur = í dag + 10 dagar

SO1 verður þakið einni einingu úr PPO1. SO2 er þakið af PO2, vegna þess að PO2 rennur fyrr út en PPO1.

Eftirfarandi tafla sýnir samantekt niðurstaðna.

| Eftirspurn | Þarfarakning |
|---|---|
| **SO1:** afhendingardagur = í dag, magn = 1 | **PPO1:** Móttökudagsetning = í dag, magn = 1, lokadagur = í dag + 10 dagar |
| **SO2:** Afhendingardagur = í dag + 6 dagar, magn = 1 | **PO2:** Móttökudagsetning = í dag + 3 dagar, magn = 1, lokadagur = í dag + 7 dagar |

> [!NOTE]
> PO1 er ekki notað því það kemur of seint fyrir S01 og rennur út áður en S02 er afhent. PPO1 hefur verið yfirpantað af einni vöru til að afhendingartími verði 0 (núll), samkvæmt verðsamningi 2.

Eftirfarandi skýringarmynd sýnir tímalína fyrir þetta dæmi.

![Dæmi 4: Einfalt FEFO, tímabil, afhendingartími fer eftir magni.](media/fefo-example-4.png "Dæmi 4: Einfalt FEFO, tímabil, afhendingartími fer eftir magni")

## <a name="example-5-simple-fefo-requirement-10-negative-days"></a>Dæmi 5: Einföld FEFO, skilyrði, 10 neikvæðir dagar

Þetta dæmi sýnir hvernig endingartími virkar þegar mörgum neikvæðum dögum er bætt við fyrir vöru. Neikvæðir dagar eru sá fjöldi daga sem þú vilt bíða áður en þú pantar áfyllingu á hlut sem er með neikvæðar birgðir. Kerfið býr ekki til framboð nema farið sé yfir fjölda neikvæðra daga.

Í kerfinu eru eftirfarandi stillingar fyrir vöru og aðaláætlun:

- **Þekjukóði (áfyllingaráætlun):** Krafa
- **Afhendingartími:** 0 dagar
- **Neikvæður dagafjöldi:** 10
- **Tegund áætlaðrar pöntunar (sjálfgefnar pöntunarstillingar vörunnar):** Innkaupapöntun

Eftirfarandi sölupöntun er til í kerfinu:

- **SO1:** Magn = 1, umbeðinn afhendingardagur = í dag

Hægt er að tryggja þessa eftirspurn með núverandi framboði í eftirfarandi staðfestri innkaupapöntun:

- **PO1:** Móttökudagsetning = í dag + 3 dagar, magn = 1, lokadagur = í dag + 5 dagar

Þar sem kerfið er stillt til að leyfa 10 neikvæða daga, þekur það eftirspurn eftir SO1 með því að nota PO1, jafnvel þó að seinkun verði í þrjá daga vegna þess að SO1 býr til neikvæðar birgðir þar til PO1 kemur. Engin áætluð innkaupapöntun er stofnuð þrátt fyrir að afhendingartíminn sé 0 (núll) og að áætluð innkaupapöntun myndi draga úr töfum.

Eftirfarandi tafla sýnir samantekt niðurstaðna.

| Eftirspurn | Þarfarakning |
|---|---|
| **SO1:** afhendingardagur = í dag, magn = 1 | **PO1:** Móttökudagsetning = í dag + 3 dagar, magn = 1, lokadagur = í dag + 5 dagar |

Eftirfarandi skýringarmynd sýnir tímalína fyrir þetta dæmi.

![Dæmi 5: Einföld FEFO, skilyrði, 10 neikvæðir dagar.](media/fefo-example-5.png "Dæmi 5: Einföld FEFO, skilyrði, 10 neikvæðir dagar")

## <a name="example-6-simple-fefo-requirement-five-negative-days"></a>Dæmi 6: Einföld FEFO, skilyrði, fimm neikvæðir dagar

Þetta dæmi sýnir hvernig endingartími virkar þegar fjöldi neikvæðra daga fyrir vöru eru færri en endingartími hennar.

Í kerfinu eru eftirfarandi stillingar fyrir vöru og aðaláætlun:

- **Þekjukóði (áfyllingaráætlun):** Krafa
- **Seljanlegir dagar:** 0 days
- **Afhendingartími:** 0 dagar
- **Neikvæður dagafjöldi:** 5 dagar
- **Tegund áætlaðrar pöntunar (sjálfgefnar pöntunarstillingar vörunnar):** Innkaupapöntun

Eftirfarandi sölupöntun er til í kerfinu:

- **SO1:** Magn = 2, umbeðinn afhendingardagur = í dag

Hægt er að tryggja þessa eftirspurn með núverandi framboði í eftirfarandi staðfestri innkaupapöntun:

- **PO1:** Móttökudagsetning = í dag, magn = 1, lokadagur = í dag + 1 dagur
- **PO2:** Móttökudagsetning = í dag + 2 dagar, magn = 1, lokadagur = í dag + 3 dagar

Kerfið verður þó að virða þá takmörkun að sendar vörur mega ekki vera útrunnar þegar sending á sér stað. Þess vegna er ekki hægt að nota bæði PO2 og PO1 fyrir SO1, vegna þess að PO1 rennur út áður en PO2 berst. Kerfið býr til eftirfarandi áætlaða innkaupapöntun til að klára að þekja eftirspurn eftir SO1:

- **PPO1:** Móttökudagsetning = í dag, magn = 1, lokadagur = í dag + 10 dagar

Kerfið getur nýtt sér neikvæðu dagana fimm og notað PO2 og PPO1 til að þekja SO1. Þessi aðferð mun þó valda því að afhendingu seinkar þar til PO2 kemur og PO1 rennur út í millitíðinni. Þess vegna þekur kerfið SO1 með því að nota PPO1 og PO1.

Eftirfarandi tafla sýnir samantekt niðurstaðna.

| Eftirspurn | Þarfarakning |
|---|---|
| **SO1:** afhendingardagur = í dag, magn = 2 | <p>**PO1:** Móttökudagsetning = í dag, magn = 1, lokadagur = í dag + 1 dagur</p><p>**PPO1:** Móttökudagsetning = í dag, magn = 1, lokadagur = í dag + 10 dagar</p> |

Eftirfarandi skýringarmynd sýnir tímalína fyrir þetta dæmi.

![Dæmi 6: Einföld FEFO, krafa, fimm neikvæðir dagar.](media/fefo-example-6.png "Dæmi 6: Einföld FEFO, skilyrði, fimm neikvæðir dagar")
