---
title: Aðaláætlanagerð fyrir vörur með takmarkað geymsluþol
description: Þessi grein lýsir því hvernig á að setja upp og nota skipulagsaðgerðir sem taka tillit til geymsluþols á viðkvæmum vörum.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428222"
---
# <a name="master-planning-for-products-with-limited-shelf-life"></a>Aðaláætlanagerð fyrir vörur með takmarkað geymsluþol

[!include [banner](../../includes/banner.md)]

Geymsluþol er sá tími sem hægt er að geyma vöru þar til ekki er lengur hægt að nota eða selja hana. Fyrir vörur sem hafa takmarkaðan geymsluþol muntu líklega nota vöruhúsastefnu fyrst rennur út, fyrst út (FEFO), sem forgangsraðar neyslu og sölu á hlutum miðað við eftirstandandi geymsluþol þeirra. Þessi vöruhúsastefna á við um matvæli, lyf og aðrar vörur sem einkennast af stuttum geymslutíma. Samkvæmt FEFO eru vörur á lagernum geymdar eins og vörur í hillum stórmarkaða: vörur sem hafa langan geymsluþol eru settar djúpt í hillurnar þannig að vörur sem hafa styttri geymsluþol eru sendar fyrst.

## <a name="using-shelf-life-in-master-planning"></a>Notkun geymsluþols í aðalskipulagi

Þessi hluti útskýrir hvernig aðalskipulag leggur til framboð fyrir geymsluþolsvörur.

Þegar þú keyrir aðaláætlun, býr það til fyrirhugaðar pantanir (framboð) sem munu uppfylla eftirspurn þína og einnig lágmarka tafir. Ef áætlun þín inniheldur hluti sem hafa takmarkaðan geymsluþol verða áætlunarútreikningar flóknari, vegna þess að áætlunin verður ekki aðeins að lágmarka tafir heldur einnig nota núverandi framboð áður en það rennur út. Áætlunin verður að reyna að nota framboð sem er næst fyrningardegi áður en framboð sem rennur út síðar. Þess vegna er í aðalskipulagi leitast við að ná eftirfarandi markmiðum, í þessari röð:

1. Lágmarka summu tafa.
1. Hámarka summan af FEFO framboði.
1. Lágmarka áfyllingu á birgðum.

Í sumum tilfellum gæti verið ágreiningur á milli fyrstu tveggja markmiðanna og þá verður að velja: viltu seinka sendingu eða vilt þú nota framboð sem rennur út síðar í stað framboðs sem rennur út fyrr? Til að leysa þennan ágreining við aðalskipulagningu forgangsraðar kerfið að lágmarka tafir fram yfir að nota framboð sem rennur út fljótlega. Almennt séð eiga sér stað átök af þessu tagi þegar það gæti verið tafir og umfjöllun eftir tímabilum. Þess vegna mælum við með að þú notir þekjutíma sem er styttri en geymsluþol vöru. Aðrar tegundir umfjöllunar (eins og kröfu) eru ólíklegar til að lenda í þessari tegund átaka.

## <a name="set-up-shelf-life"></a>Settu upp geymsluþol

### <a name="configure-each-master-plan-to-consider-shelf-life"></a>Stilltu hverja aðaláætlun til að taka tillit til geymsluþols

Sjálfgefið er að aðaláætlanir taka ekki tillit til geymsluþols. Notaðu eftirfarandi aðferð til að virkja geymsluþolsútreikninga fyrir hvert aðalskipulag sem krefst þeirra.

1. Fara til **Aðalskipulag \> uppsetningu \> áætlanir \> Aðaláætlanir**.
1. Veldu annað hvort núverandi áætlun í listaglugganum eða búðu til nýja.
1. Á **Almennt** flýtiflipann, stilltu **Notaðu geymsluþol dagsetningar** valmöguleika til *Já*.

### <a name="configure-tracking-dimension-groups-to-track-the-batch-dimension"></a>Stilla rakningarvíddarhópa til að rekja runuvíddina

Aðeins er hægt að rekja geymsluþol vöru ef sú vara er rakin í runuvíddinni. Með öðrum orðum, lotutilvísun og nauðsynlegar dagsetningar verða að vera skráðar við móttöku eða framleiðslu og í gegnum hverja birgðafærslu vörunnar. Til að stjórna þessum valkosti skaltu setja upp einn eða fleiri rakningarvíddarhópa til að gera nauðsynlega rakningu og úthluta síðan viðeigandi hlutum til þessara hópa eftir þörfum.

Notaðu eftirfarandi ferli til að setja upp rakningarvíddarhóp til að rekja runuvíddina.

1. Fara til **Vöruupplýsingastjórnun \> Uppsetning \> Mál og afbrigði hópar \> Rekja víddarhópa**.
1. Fylgið einu af eftirfarandi skrefum:

    - Á aðgerðarrúðunni velurðu **Nýtt** til að búa til nýjan rakningarvíddarhóp. Sláðu inn nafn og lýsingu og veldu síðan **Vista** á aðgerðasvæðinu.
    - Í listarúðunni, veldu núverandi rakningarvíddarhóp sem þú vilt setja upp til að rekja runuvíddina.

1. Á **Rekjavídd** Flýtiflipi, í **Lotunúmer** línu, veldu gátreitina í **Virkur** og **Líkamsbirgðir** dálkar.

### <a name="set-up-shelf-life-for-a-product"></a>Settu upp geymsluþol vöru

Notaðu eftirfarandi aðferð til að setja upp geymsluþol vöru.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Búðu til eða opnaðu vöruna sem þú vilt setja upp.
1. Til að nota geymsluþolsstillingarnar, á **Almennt** Flýtiflipi, stilltu **Rekjavíddarhópur** reit í rakningarvíddarhóp sem er settur upp til að rekja runuvíddina. Þú getur aðeins stillt þennan reit þegar þú ert fyrst að búa til vöru. Þú getur ekki breytt gildinu fyrir núverandi vörur.
1. Á **Stjórna birgðum** Flýtiflipi, stilltu eftirfarandi reiti:

    - **Geymsluráðgjöf í dögum** – Tilgreindu tímabilið (í dögum) sem á að athuga lotu af þessari vöru til að tryggja að hún henti til neyslu eða endursölu. Gildi þessa reits er bætt við lotu *framleiðsludagsetningu* að ákveða það *hilluráðgjöf dags*. Þú getur stillt kerfið til að búa til gæðapantanir þegar lota nálgast dagsetningu hilluráðgjafar.
    - **Geymsluþol í dögum** – Tilgreindu fjölda daga áður en lota af þessari vöru rennur út. Þetta gildi er bætt við *framleiðsludag* að ákvarða *gildistíma*. Lotan er talin ónothæf eftir þessa dagsetningu.
    - **Best fyrir blæðingar í dögum** – Tilgreindu tímabilið (í dögum) eftir að lota af þessari vöru telst enn seljanleg en getur ekki lengur haldið einhverjum upprunalegum eiginleikum sínum. Þetta gildi er bætt við *framleiðsludag* að ákvarða *best fyrir dagsetningu*. Þú getur keyrt skýrslur til að bera kennsl á birgðir sem eru liðnar við best-fyrir dagsetningu. 

### <a name="set-a-sellable-days-rule-for-each-customer"></a>Settu söluhæfa dagareglu fyrir hvern viðskiptavin

*Seljanlegir dagar* virkni tryggir að vörur úr lotu sem rennur út fljótlega séu ekki sendar til viðskiptavina. Ennfremur tryggir það að þegar vörur eru sendar til viðskiptavinar mun nægilegur fjöldi seljanlegra daga enn vera eftir eftir afhendingu.

Til að nota virkni söludaga verður að skilgreina fjölda söludaga sem gildir fyrir hverja vöru (eða vöruflokk) fyrir hvern viðskiptavin. Þú verður að ljúka þessu ferli handvirkt, því það er engin gagnaeining fyrir það.

Notaðu eftirfarandi aðferð til að setja upp söludaga fyrir hverja vöru fyrir hvern viðskiptavin.

1. Opnið **Sölu og markaðssetning \> Viðskiptavinir \> Allir viðskiptavinir**.
1. Finndu og veldu viðskiptavininn sem þú vilt setja upp.
1. Á aðgerðarrúðunni, á **Selja** flipa, í **Settu upp** hópur, veldu **Selja \> Seljanlegir dagar**.
1. Á **Seljanlegir dagar fyrir viðskiptavini** síðu, töfluna listar núverandi reglur um söludaga fyrir hverja vöru eða vöruflokk. Notaðu hnappa á aðgerðarrúðunni til að bæta við eða breyta línum í hnitanetinu eftir þörfum. A **Sía** er veitt til að hjálpa þér að finna núverandi línur.
1. Fyrir hverja línu skal stilla eftirfarandi reiti:

    - **Vörukóði** – Veldu eitt af eftirfarandi gildum til að tilgreina umfang hlutanna sem verða fyrir áhrifum:

        - *Tafla* – Línan á við tiltekinn hlut.
        - *Hópur* – Línan á við tiltekinn vöruflokk.
        - *Allt* – Röðin á við um alla hluti.

    - **Atriðatengsl** – Ef þú stillir á **Vörukóði** sviði til *Tafla*, veldu tiltekið atriði. Ef þú stillir **Vörukóði** sviði til *Hópur*, veldu vöruflokk. Ef þú stillir **Vörukóði** sviði til *Allt*, þessi reitur er ekki tiltækur.
    - **Seljanlegir dagar** – Færið inn lágmarksfjölda daga sem viðskiptavinurinn þarf að hafa til að selja samsvarandi vörur áður en lotan rennur út. Gildi söludaga er byggt á umbeðinni móttökudagsetningu (eða staðfestri móttökudagsetningu, ef hún er skilgreind) fyrir samsvarandi vörur í sölupöntuninni.
    - *(Aðrar vörustærðir)* – Til að takmarka enn frekar umfang línu, tilgreindu önnur víddargildi (ss **Stærð** og **Litur**) eftir þörfum. Til að stjórna hvaða stærðir eru sýndar í hnitanetinu skaltu velja **Sýna stærðir** á aðgerðasvæðinu.

### <a name="set-up-all-relevant-products-so-that-they-are-fefo-date-controlled"></a>Settu allar viðeigandi vörur upp þannig að þær séu FEFO dagsetningarstýrðar

Til þess að seljanlegir dagar virki verður hver viðkomandi vara að tilheyra vörulíkanahópi þar sem **FEFO dagsetningarstýrt** gátreiturinn er valinn.

Notaðu eftirfarandi aðferð til að setja upp vörulíkanaflokk þannig að hann styðji virkni seljanlegra daga.

1. Opnið **Birgðastjórnun \> Uppsetning \> Birgðir \> Vörulíkanaflokkar.**
1. Veldu annað hvort núverandi hóp í listaglugganum eða búðu til nýjan með því að velja **Nýtt** á aðgerðasvæðinu.
1. Á **Birgðareglur** flýtiflipann, veldu **FEFO dagsetningarstýrt** gátreit.
1. Stilltu aðra reiti fyrir hópinn eftir þörfum.

Notaðu eftirfarandi aðferð til að skoða eða stilla vörulíkanahópinn sem vara tilheyrir.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Opnaðu vöruna sem þú vilt skoða eða breyta.
1. Á **Almennt** flýtiflipann, stilltu **Vörulíkanahópur** reit til hóps þar sem **FEFO dagsetningarstýrt** gátreiturinn er valinn.

## <a name="example-1-simple-fefo-10-day-period-zero-days-of-lead-time"></a>Dæmi 1: Einfalt FEFO, 10 daga tímabil, núll dagar af afgreiðslutími

Þetta dæmi sýnir grundvallardæmi um geymsluþol, þar sem tenging á milli birgðapantana og eftirspurnar er gerð til að uppfylla eftirfarandi markmið kerfisins:

- Lágmarka summu tafa.
- Hámarka summan af FEFO framboði.
- Lágmarka áfyllingu á birgðum.

Kerfið hefur eftirfarandi atriði og aðalskipulagsstillingar:

- **Þekkjakóði (áfyllingaraðferð):** Tímabil 
- **Gildistími:** 10 dagar (jafnt geymsluþoli)
- **Geymsluþol:** 10 dagar
- **Seljanlegir dagar:** 0 dagar
- **Leiðslutími:** 0 dagar
- **Neikvæð dagar:** 0 dagar
- **Tegund áætlaðrar pöntunar (sjálfgefnar pöntunarstillingar vörunnar):** Pöntun

Eftirfarandi sölupantanir fyrir vöruna eru til í kerfinu:

- **SO1:** Magn (magn) = 2, umbeðinn afhendingardagur = í dag + 1 dagur
- **SO2:** Magn = 1, umbeðinn afhendingardagur = í dag + 4 dagar
- **SO3:** Magn = 1, umbeðinn afhendingardagur = í dag + 5 dagar

Allar þessar sölupantanir skapa eftirspurn eftir vörunni.

Eftirfarandi framboð er til fyrir hlutinn:

- **Á lager:** Magn = 1, gildistími = í dag + 5 dagar
- **Innkaupapöntun 1 (PO1):** Kvittunardagsetning = í dag + 2 dagar, magn = 1, fyrningardagsetning = í dag + 4 dagar

Kerfið býr til lista yfir framboð sem getur staðið undir þessari eftirspurn og það flokkar listann eftir gildistíma (með því að nota FEFO).

Aðalskipulag skapar nauðsynlega tengingu milli framboðs og eftirspurnar. Það skapar einnig nauðsynlega eftirspurn byggt á framboðslistanum (með því að nota FEFO) og tekur tiltæka dagsetningu.

- SO1 er hægt að fullnægja með magni á lager, en það er ekki hægt að uppfylla með PO1, vegna þess að framboðsdagsetning fyrir PO1 er einum degi síðar en SO1 krefst. Þess vegna skapar SO1 eftirspurn eftir einni vörueiningu.
- SO2 getur fallið undir PO1, vegna þess að PO1 kemur fyrir umbeðinn tíma og gildistíminn mun enn gilda. Þess vegna er SO2 krafan að fullu undir PO1.
- SO3 er ekki fjallað um, vegna þess að úrræði eru ekki tiltæk. Þess vegna skapar SO3 eftirspurn eftir einni vörueiningu.

Til að mæta öllum þörfum sem eftir eru verður kerfið að búa til eftirfarandi fyrirhugaða innkaupapöntun:

- **PPO1:** Kvittunardagsetning = í dag, magn = 2, gildistími = í dag + 10 dagar

Eftirfarandi tafla dregur saman niðurstöðuna.

| Eftirspurn | Þarfarakning |
|---|---|
| **SO1:** Afhendingardagur = í dag + 1 dagur, magn = 2 | <p>**Á hendi:** Magn = 1, gildistími = í dag + 5 dagar</p><p>**PPO1:** Kvittunardagsetning = í dag, magn = 1, fyrningardagur = í dag + 10 dagar</p> |
| **SO2:** Afhendingardagur = í dag + 4 dagar, magn = 1 | **PO1:** Kvittunardagsetning = í dag + 2 dagar, 1 magn, fyrningardagur = í dag + 4 dagar |
| **SO3:** Afhendingardagur = í dag + 5 dagar, magn = 1 | **PPO1:** Kvittunardagsetning = í dag, magn = 2, gildistími = í dag + 10 dagar |

Eftirfarandi mynd sýnir tímalínuna fyrir þetta dæmi.

![Dæmi 1: Einfalt FEFO, 10 daga tímabil, núll dagar af afgreiðslutími.](media/fefo-example-1.png "Dæmi 1: Einfalt FEFO, 10 daga tímabil, núll dagar af afgreiðslutími")

## <a name="example-2-simple-fefo-requirement-three-days-of-lead-time"></a>Dæmi 2: Einfalt FEFO, krafa, þriggja daga afgreiðslutími

Þetta dæmi sýnir hvernig tilraun kerfisins til að lágmarka tafir getur stundum valdið ofpöntun.

Kerfið hefur eftirfarandi atriði og aðalskipulagsstillingar:

- **Þekkjakóði (áfyllingaraðferð):** Krafa
- **Geymsluþol:** 10 dagar
- **Seljanlegir dagar:** 0 dagar
- **Leiðslutími:** Stofnað með eftirfarandi viðskiptasamningum söluaðila:

    - **Viðskiptasamningur 1:** Ef magn = 1, afgreiðslutími = 4
    - **Viðskiptasamningur 2:** Ef magn = 2, afgreiðslutími = 3

- **Neikvæð dagar:** 0 dagar
- **Tegund áætlaðrar pöntunar (sjálfgefnar pöntunarstillingar vörunnar):** Pöntun

Eftirfarandi sölupöntun er til í kerfinu:

- **SO1:** Magn = 2, umbeðinn afhendingardagur = í dag + 3 dagar

Þessi eftirspurn er tryggð af núverandi framboði og staðfestri innkaupapöntun:

- **Á lager:** Í boði = í dag, magn = 1, gildistími = í dag + 2 dagar
- **PO1:** Kvittunardagsetning = í dag + 3 dagar, magn = 1, fyrningardagsetning = í dag + 4 dagar

Ekki er hægt að uppfylla SO1 með tiltækum birgðum vegna þess að lokadagsetning birgða er fyrir sendingardagsetningu. PO1 getur staðið undir SO1 kröfunni með magni sem er aðeins 1. Þess vegna skapar SO1 eftirspurn eftir einni vörueiningu. Til að mæta þessari kröfu býr kerfið til fyrirhugaða innkaupapöntun (PPO1).

Kerfið hefur tvo viðskiptasamninga (einn fyrir magn = 1, afgreiðslutími = 4 dagar og einn fyrir magn = 2, afgreiðslutími = 3 dagar). Þess vegna reynir kerfið að lágmarka tafir með því að búa til fyrirhugaða innkaupapöntun (PPO1) sem stenst seinni viðskiptasamninginn. Niðurstaðan er offramboð (magn = 2, fyrningardagur = í dag + 10 dagar).

Eftirfarandi tafla dregur saman niðurstöðuna.

| Eftirspurn | Þarfarakning |
|---|---|
| **SO1:** Afhendingardagur = í dag + 3 dagar, magn = 2 | <p>**PO1:** Kvittunardagsetning = í dag + 3 dagar, magn = 1, fyrningardagsetning = í dag + 4 dagar</p><p>**PPO1:** Kvittunardagsetning = í dag + 3 dagar, magn = 1, fyrningardagur = í dag + 10 dagar</p> |

Eftirfarandi mynd sýnir tímalínuna fyrir þetta dæmi.

![Dæmi 2: Einfalt FEFO, krafa, þriggja daga afgreiðslutími.](media/fefo-example-2.png "Dæmi 2: Einfalt FEFO, krafa, þriggja daga afgreiðslutími")

## <a name="example-3-simple-fefo-requirement-three-days-of-lead-time-five-sellable-days"></a>Dæmi 3: Einfalt FEFO, krafa, þriggja daga afgreiðslutími, fimm seljanlegir dagar

Þetta dæmi sýnir hvernig geymsluþol virkar þegar söludögum er bætt við fyrir vöru.

Kerfið hefur eftirfarandi atriði og aðalskipulagsstillingar:

- **Þekkjakóði (áfyllingaraðferð):** Krafa
- **Geymsluþol:** 10 dagar
- **Seljanlegir dagar:** 5 dagar
- **Leiðslutími:** 5 dagar
- **Neikvæð dagar:** 0 dagar
- **Tegund áætlaðrar pöntunar (sjálfgefnar pöntunarstillingar vörunnar):** Pöntun

Eftirfarandi sölupantanir eru til í kerfinu:

- **SO1:** Magn = 2, umbeðinn afhendingardagur = í dag + 2 dagar
- **SO2:** Magn = 1, umbeðinn afhendingardagur = í dag + 3 dagar
- **SO3:** Magn = 1, umbeðinn afhendingardagur = í dag + 5 dagar

Hægt er að mæta þessari eftirspurn með núverandi framboði og staðfestri innkaupapöntun:

- **Á lager:** Í boði = í dag, magn = 1, gildistími = Í dag + 6 dagar
- **PO1:** Kvittunardagsetning = í dag + 2 dagar, magn = 3, fyrningardagsetning = í dag + 10 dagar

Kerfið býr til lista yfir tengingar umsækjendur, byggt á framboðslistanum (FEFO) og framboðsdögum. Þess vegna er ekki hægt að uppfylla SO1 með birgðum á lager, vegna þess að þær birgðir rennur út fyrir lok söludaganna sem viðskiptavinurinn krefst (umbeðin móttökudagsetning + 5 dagar). PO1 getur staðið undir SO1 kröfunni með tveimur einingum og SO2 kröfunni með einni einingu. Þess vegna hefur aðeins SO3 enn afhjúpað eftirspurn eftir einni vörueiningu. Til að mæta þessari kröfu býr kerfið til eftirfarandi fyrirhugaða innkaupapöntun:

- **PP01:** Kvittunardagsetning = í dag + 5 dagar, magn = 1, fyrningardagur = í dag + 10 dagar

Eftirfarandi tafla dregur saman niðurstöðuna.

| Eftirspurn | Þarfarakning |
|---|---|
| **SO1:** Afhendingardagur = í dag + 2 dagar, magn = 2 | **PO1:** Kvittunardagsetning = í dag + 2 dagar, magn = 2, fyrningardagsetning = í dag + 10 dagar |
| **SO2:** Afhendingardagur = í dag + 3 dagar, magn = 1 | **PO1:** Kvittunardagsetning = í dag + 2 dagar, magn = 1, fyrningardagur = í dag + 10 dagar |
| **SO3:** Afhendingardagur = í dag + 5 dagar, magn = 1 | **PPO1:** Kvittunardagsetning = í dag + 5 dagar, magn = 1, fyrningardagur = í dag + 10 dagar |

Eftirfarandi mynd sýnir tímalínuna fyrir þetta dæmi.

![Dæmi 3: Einfalt FEFO, krafa, þriggja daga afgreiðslutími, fimm seljanlegir dagar.](media/fefo-example-3.png "Dæmi 3: Einfalt FEFO, krafa, þriggja daga afgreiðslutími, fimm seljanlegir dagar")

## <a name="example-4-simple-fefo-period-lead-time-depends-on-the-quantity"></a>Dæmi 4: Einfalt FEFO, tímabil, leiðtími fer eftir magni

Þetta dæmi sýnir hvernig tilraun kerfisins til að lágmarka tafir getur stundum valdið ofpöntun.

Kerfið hefur eftirfarandi atriði og aðalskipulagsstillingar:

- **Þekkjakóði (áfyllingaraðferð):** Tímabil
- **Gildistími:** 10 dagar (jafnt geymsluþoli)
- **Geymsluþol:** 10 dagar
- **Seljanlegir dagar:** 0 dagar
- **Leiðslutími:** Stofnað með eftirfarandi viðskiptasamningum söluaðila:

    - **Viðskiptasamningur 1:** Ef magn = 1, afgreiðslutími = 5
    - **Viðskiptasamningur 2:** Ef magn = 2, afgreiðslutími = 0

- **Neikvæð dagar:** 0 dagar
- **Tegund áætlaðrar pöntunar (sjálfgefnar pöntunarstillingar vörunnar):** Pöntun

Eftirfarandi sölupantanir eru til í kerfinu:

- **SO1:** Magn = 1, umbeðinn afhendingardagur = í dag
- **SO2:** Magn = 1, umbeðinn afhendingardagur = í dag + 6 dagar

Hægt er að mæta þessari eftirspurn að hluta með núverandi framboði frá eftirfarandi staðfestum innkaupapantunum:

- **PO1:** Kvittunardagsetning = í dag + 1 dagur, magn = 1, gildistími = í dag + 2 dagar
- **PO2:** Kvittunardagsetning = í dag + 3 dagar, magn = 1, fyrningardagur = í dag + 7 dagar

Kerfið hefur tvo viðskiptasamninga (einn fyrir magn = 1, afgreiðslutími = 5 dagar, og einn fyrir magn = 2, afgreiðslutími = 0 dagar). Þess vegna reynir kerfið að lágmarka töf með því að búa til eftirfarandi fyrirhugaða innkaupapöntun sem uppfyllir seinni viðskiptasamninginn:

- **PP01:** Kvittunardagsetning = í dag, magn = 2, gildistími = í dag + 10 dagar

SO1 mun falla undir eina einingu frá PPO1. SO2 mun falla undir PO2, vegna þess að PO2 rennur út fyrr en PPO1.

Eftirfarandi tafla dregur saman niðurstöðuna.

| Eftirspurn | Þarfarakning |
|---|---|
| **SO1:** Afhendingardagur = í dag, magn = 1 | **PPO1:** Kvittunardagsetning = í dag, magn = 1, fyrningardagur = í dag + 10 dagar |
| **SO2:** Afhendingardagur = í dag + 6 dagar, magn = 1 | **PO2:** Kvittunardagsetning = í dag + 3 dagar, magn = 1, fyrningardagur = í dag + 7 dagar |

> [!NOTE]
> PO1 er ekki notað, því það kemur of seint fyrir S01 og rennur út áður en S02 er afhent. PPO1 hefur ofpantað um eina einingu til að gera afgreiðslutíma kleift að vera 0 (núll), fyrir hvern viðskiptasamning 2.

Eftirfarandi mynd sýnir tímalínuna fyrir þetta dæmi.

![Dæmi 4: Einfalt FEFO, tímabil, leiðtími fer eftir magni.](media/fefo-example-4.png "Dæmi 4: Einfalt FEFO, tímabil, leiðtími fer eftir magni")

## <a name="example-5-simple-fefo-requirement-10-negative-days"></a>Dæmi 5: Einfalt FEFO, krafa, 10 neikvæðir dagar

Þetta dæmi sýnir hvernig geymsluþol virkar þegar mörgum neikvæðum dögum er bætt við fyrir vöru. Neikvæð dagar eru fjöldi daga sem þú ert tilbúinn að bíða áður en þú pantar áfyllingu á vöru sem er með neikvæðar birgðir. Kerfið skapar ekki framboð nema farið sé yfir fjölda neikvæðra daga.

Kerfið hefur eftirfarandi atriði og aðalskipulagsstillingar:

- **Þekkjakóði (áfyllingaraðferð):** Krafa
- **Leiðslutími:** 0 dagar
- **Neikvæð dagar:** 10 dagar
- **Tegund áætlaðrar pöntunar (sjálfgefnar pöntunarstillingar vörunnar):** Pöntun

Eftirfarandi sölupöntun er til í kerfinu:

- **SO1:** Magn = 1, umbeðinn afhendingardagur = í dag

Hægt er að mæta þessari eftirspurn með núverandi framboði úr eftirfarandi staðfestu innkaupapöntun:

- **PO1:** Kvittunardagsetning = í dag + 3 dagar, magn = 1, fyrningardagur = í dag + 5 dagar

Vegna þess að kerfið er stillt til að leyfa 10 neikvæða daga, dekkir það eftirspurn eftir SO1 með því að nota PO1, jafnvel þó að niðurstaðan verði þriggja daga töf vegna þess að SO1 skapar neikvæðar birgðir þar til PO1 kemur. Engin áætluð innkaupapöntun er stofnuð, jafnvel þó að afgreiðslutími sé 0 (núll) og stofnun áætlaðrar innkaupapöntunar myndi draga úr töfum.

Eftirfarandi tafla dregur saman niðurstöðuna.

| Eftirspurn | Þarfarakning |
|---|---|
| **SO1:** Afhendingardagur = í dag, magn = 1 | **PO1:** Kvittunardagsetning = í dag + 3 dagar, magn = 1, fyrningardagur = í dag + 5 dagar |

Eftirfarandi mynd sýnir tímalínuna fyrir þetta dæmi.

![Dæmi 5: Einfalt FEFO, krafa, 10 neikvæðir dagar.](media/fefo-example-5.png "Dæmi 5: Einfalt FEFO, krafa, 10 neikvæðir dagar")

## <a name="example-6-simple-fefo-requirement-five-negative-days"></a>Dæmi 6: Einfalt FEFO, krafa, fimm neikvæðir dagar

Þetta dæmi sýnir hvernig geymsluþol virkar þegar fjöldi neikvæðra daga fyrir vöru er minni en geymsluþolstími hennar.

Kerfið hefur eftirfarandi atriði og aðalskipulagsstillingar:

- **Þekkjakóði (áfyllingaraðferð):** Krafa
- **Seljanlegir dagar:** 0 dagar
- **Leiðslutími:** 0 dagar
- **Neikvæð dagar:** 5 dagar
- **Tegund áætlaðrar pöntunar (sjálfgefnar pöntunarstillingar vörunnar):** Pöntun

Eftirfarandi sölupöntun er til í kerfinu:

- **SO1:** Magn = 2, umbeðinn afhendingardagur = í dag

Hægt er að mæta þessari eftirspurn með núverandi framboði frá eftirfarandi staðfestum innkaupapantunum:

- **PO1:** Kvittunardagsetning = í dag, magn = 1, fyrningardagur = í dag + 1 dagur
- **PO2:** Kvittunardagsetning = í dag + 2 dagar, magn = 1, fyrningardagsetning = í dag + 3 dagar

Hins vegar verður kerfið að virða takmörkunina um að sendar vörur megi ekki renna út við sendingu. Þess vegna er ekki hægt að nota bæði PO2 og PO1 fyrir SO1, vegna þess að PO1 rennur út áður en PO2 kemur. Kerfið býr til eftirfarandi fyrirhugaða innkaupapöntun til að klára eftirspurn eftir SO1:

- **PPO1:** Kvittunardagsetning = í dag, magn = 1, fyrningardagur = í dag + 10 dagar

Kerfið getur nýtt sér fimm neikvæðu dagana og notað PO2 og PPO1 til að ná yfir SO1. Hins vegar mun þessi nálgun valda því að afhending verður seinkuð þar til PO2 kemur og PO1 rennur út á meðan. Þess vegna nær kerfið yfir SO1 með því að nota PPO1 og PO1.

Eftirfarandi tafla dregur saman niðurstöðuna.

| Eftirspurn | Þarfarakning |
|---|---|
| **SO1:** Afhendingardagur = í dag, magn = 2 | <p>**PO1:** Kvittunardagsetning = í dag, magn = 1, fyrningardagur = í dag + 1 dagur</p><p>**PPO1:** Kvittunardagsetning = í dag, magn = 1, fyrningardagur = í dag + 10 dagar</p> |

Eftirfarandi mynd sýnir tímalínuna fyrir þetta dæmi.

![Dæmi 6: Einfalt FEFO, krafa, fimm neikvæðir dagar.](media/fefo-example-6.png "Dæmi 6: Einfalt FEFO, krafa, fimm neikvæðir dagar")
