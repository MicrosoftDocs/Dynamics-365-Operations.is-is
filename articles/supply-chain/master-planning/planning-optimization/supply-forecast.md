---
title: Aðalskipulag með framboðsspám
description: Þessi grein lýsir því hvernig tillit er tekið til framboðsspár við aðalskipulagningu.
author: t-benebo
ms.date: 09/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-21
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: dc83d10851958ec67166cb7e40cfd84dceae6651
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690162"
---
# <a name="master-planning-with-supply-forecasts"></a>Aðalskipulag með framboðsspám

[!include [banner](../../includes/banner.md)]

Framboðsspár gera þér kleift að tilgreina framboðið sem þú býst við að þurfi á einhverju framtíðartímabili. Venjulega byggir þú matið á sölusögu fyrra árs og notar síðan spána í fjárhagsáætlunargerð. Þú getur líka sett upp aðaláætlanir þínar til að taka tillit til spár við skipulagningu.

## <a name="set-up-a-master-plan-to-consider-supply-forecasts"></a>Settu upp aðaláætlun til að huga að framboðsspám

Hægt er að tilgreina hvort hvert aðalskipulag eigi að taka tillit til spár þegar það keyrir. Notaðu eftirfarandi aðferð til að stilla spámöguleika fyrir hverja áætlun.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Veldu annað hvort núverandi aðalskipulag í listaglugganum eða veldu **Nýtt** á aðgerðarrúðunni til að búa til nýjan.
1. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:

    - **Spálíkan** – Veldu líkanið sem inniheldur þær framboðs- og/eða eftirspurnarspár sem aðalskipulagið ætti að hafa í huga.
    - **Látið framboðsspá fylgja með** – Stilltu þennan valkost á *Já* ef rammaáætlun ætti að huga að framboðsspám.
    - **Látið eftirspurnarspá fylgja með** – Stilltu þennan valkost á *Já* ef rammaáætlun ætti að huga að eftirspurnarspám. Þó að þessi stilling sé óháð **Látið framboðsspá fylgja með** stilling, sumar af öðrum stillingum á síðunni eiga við um bæði framboðsspár og eftirspurnarspár. Fyrir frekari upplýsingar um áætlanagerð sem tekur tillit til eftirspurnarspár, sjá [Aðalskipulag með eftirspurnarspám](demand-forecast.md).
    - **Aðferð notuð til að draga úr spákröfum** – Veldu aðferðina sem á að nota til að draga úr spákröfum við aðalskipulagningu:

        - *Enginn* – Kröfur um spár munu ekki minnka við aðalskipulagningu.
        - *Prósenta - lækkunarlykill* – Spákröfur verða lækkaðar í samræmi við prósentutölur og tímabil sem eru skilgreind í lækkunarlyklinum.
        - *Viðskipti – lækkunarlykill* – Spáþörf verður minnkuð með þeim viðskiptum sem eiga sér stað á þeim tímabilum sem eru skilgreind í lækkunarlyklinum.
        - *Viðskipti – kraftmikið tímabil* – Spákröfur verða minnkaðar með pöntunarfærslum sem eiga sér stað á kraftmiklu tímabilinu. Tímabilið nær yfir núverandi spádagsetningar og því lýkur þegar næsta spá hefst. The *Viðskipti – kraftmikið tímabil* aðferðin notar ekki eða þarfnast minnkunarlykils og þegar þú notar hana gilda eftirfarandi skilyrði:

            - Ef spá er alveg minnkuð verða spárþarfir gildandi spár 0 (núll).
            - Ef það er engin komandi spá eru spáþarfir frá síðustu spá sem var færð inn minnkaðar.
            - Tímamörk eru hafðar með í útreikningi á lækkun spár.
            - Jákvæðir dagar eru hafðir með í útreikningi á lækkun spár.
            - Ef raunverulegar pöntunarfærslur°fara fram úr spáþörfum, eru eftirstandandi færslur ekki sendar áfram í næsta spátímabil.

        > [!NOTE]
        > The **Aðferð notuð til að draga úr spákröfum** stillingin á einnig við um eftirspurnarspár ef þú hefur virkjað þær fyrir aðalskipulagið og það hefur áhrif á þær á svipaðan hátt. Fyrir frekari upplýsingar, sjá [Aðalskipulag með eftirspurnarspám](demand-forecast.md).

## <a name="set-reduction-options-for-coverage-groups"></a>Stilltu minnkunarmöguleika fyrir umfjöllunarhópa

Fylgdu þessum skrefum til að stilla valkosti sem stjórna því hvernig þekjuhópur mun draga úr spákröfum sínum fyrir aðaláætlanir sem nota færslumiðaða lækkun.

1. Fara skal í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Þekjuflokkar**.
1. Veldu annað hvort fyrirliggjandi þekjuhóp í listaglugganum eða veldu **Nýtt** á aðgerðarrúðunni til að búa til nýjan.
1. Á **Annað** Flýtiflipi, í **Draga úr spá um** reit, tilgreinið hvernig draga skuli úr kröfum um framboðsspá fyrir atriði í þekjuhópnum, fyrir aðaláætlanir þar sem **Aðferð notuð til að draga úr spákröfum** reiturinn er stilltur á *Færslur - lækkunarlykill* eða *Viðskipti - kraftmikið tímabil*. Veljið eitt af eftirfarandi gildum:

    - *Allar færslur* – Allar færslur ættu að lækka spána.
    - *Pantanir* – Aðeins pantanir af sömu gerð ættu að draga úr spánni.

    Til dæmis gefa sjálfgefnar pöntunarstillingar fyrir vöru til kynna að það eigi að framleiða hana. Það er framboðsspálína fyrir magnið 50 og það er fyrirliggjandi innkaupapöntun fyrir magnið 20. Ef **Draga úr spá um** reiturinn er stilltur á *Pantanir*, verður fyrirhuguð framleiðslupöntun búin til fyrir magnið 50. Ef það er stillt á *Öll viðskipti*, verður fyrirhuguð framleiðslupöntun lækkuð í 30 magn.

    Þessi stilling á einnig við um lækkun eftirspurnarspár. Fyrir frekari upplýsingar, sjá [Aðalskipulag með eftirspurnarspám](demand-forecast.md).

## <a name="enter-a-supply-forecast-for-a-product"></a>Færðu inn framboðsspá fyrir vöru

Til að slá inn framboðsspá fyrir vöru skaltu fylgja þessum skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veldu vöruna sem þú vilt slá inn spá fyrir.
1. Á aðgerðarrúðunni, á **Áætlun** flipa, veldu **Framboðsspá**.
1. Á **Framboðsspá** síðu, á aðgerðarrúðunni, veldu **Nýtt** til að bæta spá við töfluna.
1. Sláðu inn upplýsingar á nýju línunni eftir þörfum til að tilgreina spá þína.

## <a name="plan-for-an-item-with-supply-forecast-lines"></a>Áætlun fyrir vöru með framboðsspálínum

Þegar þú keyrir aðaláætlun sem inniheldur vöru sem framboðsspá er til fyrir, mun kerfið stofna innkaupapöntun fyrir framboðslínurnar sem hafa verið færðar inn. Sjálfgefnar pöntunarstillingar fyrir hlutinn eru virtar. Ef þessar sjálfgefnu pöntunarstillingar tilgreina a **Sjálfgefin pöntunartegund** verðmæti á *Pöntun*, og enginn lánardrottinsreikningur er tilgreindur á framboðsspálínunni, mun kerfið nota sjálfgefinn lánardrottinn fyrir vöruna.

## <a name="check-whether-a-planned-order-is-a-supply-forecast-order"></a>Athugaðu hvort áætluð pöntun sé framboðsspápöntun

Notaðu eftirfarandi ferli til að læra hvort áætlað pöntun hafi verið stofnuð vegna framboðsspár.

1. Fara í **Áætlanagerð \> Aðaláætlanagerð \> Áætlaðar pantanir**.
1. Opnaðu fyrirhugaða pöntun sem þú vilt skoða.
1. Á **Almennt** Flýtiflipi, skoðaðu verðmæti **Framboðsspá** sviði. Ef pöntunin var stofnuð til að ná yfir framboðsspá verður þessi reitur stilltur á *Já*.

## <a name="examples-of-master-planning-with-supply-forecasts"></a>Dæmi um aðalskipulag með framboðsspám

Þessi hluti gefur nokkur dæmi sem sýna hvernig framboðsspá hefur áhrif á aðalskipulagningu.

### <a name="example-1-supply-forecast-for-an-item"></a>Dæmi 1: Framboðsspá fyrir vöru

Þú ert með hlut þar sem sjálfgefin pöntunartegund er *Pöntun* og sjálfgefinn söluaðili er *US-002*. Það hefur eftirfarandi framboðsspálínu.

| Líkan    | Dagsetning     | Lykill lánardrottins | Lánardrottnaflokkur | Magn | Eining | Svæði | Vöruhús |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| NúverandiF | 10/10/22 |                |              | 35       | hver   | 1    | 11        |

Þegar þú keyrir aðalskipulagningu verður áætluð innkaupapöntun stofnuð fyrir *35 ea* frá seljanda *US-002*.

### <a name="example-2-several-supply-forecast-lines-with-and-without-a-vendor"></a>Dæmi 2: Nokkrar framboðspálínur, með og án söluaðila

Þú ert með hlut þar sem sjálfgefin pöntunartegund er *Pöntun* og sjálfgefinn söluaðili er *US-002*. Það hefur eftirfarandi framboðsspálínur.

| Líkan    | Dagsetning     | Lykill lánardrottins | Lánardrottnaflokkur | Magn | Eining | Svæði | Vöruhús |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| NúverandiF | 10/10/22 |                |              | 35       | hver   | 1    | 11        |
| NúverandiF | 10/10/22 | US-101         |              | 25       | hver   | 1    | 11        |

Í þessu tilviki meðhöndlar kerfið línuna sem tilgreinir ekki lánardrottinn sem almenna spá og gerir ráð fyrir að línuna sem tilgreinir lánardrottinn ætti að draga frá almennu spánni. Þess vegna mun aðalskipulag stofna eftirfarandi fyrirhugaðar innkaupapantanir fyrir vöruna:

- Fyrirhuguð innkaupapöntun fyrir magn af *25 ea* frá seljanda *US-101* (Lánardrottinn og magnið sem tilgreint er á spálínunni er notað.)
- Fyrirhuguð innkaupapöntun fyrir magn af *10 ea* frá seljanda *US-002* (Vegna þess að enginn lánardrottinn var tilgreindur á hinni spálínunni er sjálfgefinn lánardrottinn notaður og magn þessarar spálínu er minnkað um magn lánardrottinssértæku spálínunnar.)

### <a name="example-3-plans-that-use-the-transactions---dynamic-period-reduction-method-in-a-single-forecast-period"></a>Dæmi 3: Áætlanir sem nota Færslur - breytilegt tímabilslækkunaraðferð á einu spátímabili

Fyrir aðaláætlanir sem nota *Viðskipti - kraftmikið tímabil* sem spálækkunaraðferð mun aðalskipulag minnka spármagn ef það eru fyrirliggjandi færslur sem passa við þá framboðseiginleika.

Til dæmis ertu með vöru þar sem sjálfgefin pöntunartegund er *Pöntun*. Það hefur eftirfarandi framboðsspálínu.

| Líkan    | Dagsetning     | Lykill lánardrottins | Lánardrottnaflokkur | Magn | Eining | Svæði | Vöruhús |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| NúverandiF | 10/10/22 | US-101         |              | 25       | hver   | 1    | 11        |

Vegna þess að það er aðeins ein framboðsspálína er aðeins eitt spátímabil.

Þegar þú keyrir aðaláætlun sem er sett upp til að nota *Viðskipti – kraftmikið tímabil* sem minnkunaraðferðin getur ein af eftirfarandi niðurstöðum komið fram:

- Ef innkaupapöntun er til fyrir lánardrottinn *US-101* og magn af *10 ea*, og **Framboðsspá** reiturinn er stilltur á *Já*, aðalskipulag stofnar nýja áætlaða innkaupapöntun fyrir eftirstandandi magn af *10 ea*. Spálínan minnkar, vegna þess að lánardrottinn passar við núverandi innkaupapöntun.
- Ef innkaupapöntun er til fyrir lánardrottinn *US-102*, síða *1*, vöruhús *11*, og magn af *10 ea*, og **Framboðsspá** reiturinn er stilltur á *Já*, stofnar aðalskipulag nýja áætlaða innkaupapöntun fyrir allt magn af *25 ea*. Ekki er hægt að minnka spálínuna, vegna þess að hún er með annan lánardrottinn en núverandi innkaupapöntun.

> [!NOTE]
> Þetta ástand getur komið upp fyrir áætlaðar innkaupapantanir, vegna þess að lánardrottinn er tengdur þeim. Hins vegar, fyrir flutningspantanir og framleiðslupantanir, verða framboðspáupphæðir alltaf lækkaðar um fyrirliggjandi pantanir, vegna þess að enginn lánardrottinn er tilgreindur fyrir þessar tegundir pantana.

### <a name="example-4-plans-that-use-the-transactions---dynamic-period-reduction-method-over-several-forecast-periods"></a>Dæmi 4: Áætlanir sem nota Færslur - breytilegt tímabilslækkunaraðferð yfir nokkur spátímabil

Þú ert með hlut þar sem sjálfgefin pöntunartegund er *Pöntun*. Það hefur eftirfarandi framboðsspálínur.

| Líkan    | Dagsetning     | Lykill lánardrottins | Lánardrottnaflokkur | Magn | Eining | Svæði | Vöruhús |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| NúverandiF | 10/10/22 | US-101         |              | 25       | hver   | 1    | 11        |
| NúverandiF | 10/15/22 | US-101         |              | 25       | hver   | 1    | 11        |

Í þessu dæmi eru tvær spálínur sem hver um sig hefur mismunandi dagsetningu. Þess vegna setja dagsetningar mörk spátímabilanna. Fyrsta tímabilið er frá 10. október til og með 14. október 2022 (10/10/22–10/14/22). Annað er frá 15. október 2022 (10/15/22) og áfram.

Það er fyrirliggjandi innkaupapöntun fyrir lánardrottinn *US-101*, magn af *10 ea*, og dagsetninguna *10/12/22* (12. október 2022). Þegar þú keyrir aðaláætlun sem er sett upp til að nota *Viðskipti – kraftmikið tímabil* sem lækkunaraðferðin mun það búa til eftirfarandi pantanir:

- Fyrirhuguð pöntun fyrir magn af *15 ea* og dagsetninguna *10/10/22* (Magnið er minnkað með núverandi innkaupapöntun sem er dagsett á sama spátímabili.)
- Fyrirhuguð pöntun fyrir magn af *25 ea* og dagsetninguna *15.10.22* (Magnið er allt magn spáarinnar.)

### <a name="example-5-plans-that-use-no-reduction"></a>Dæmi 5: Áætlanir sem nota enga lækkun

Þegar þú keyrir áætlun þar sem spálækkunaraðferðin er *Enginn*, aðalskipulag mun alltaf búa til áætlað framboð fyrir allar framboðsspárlínur. Eftir að fyrirhugað framboð hefur verið samþykkt mun það draga úr pöntunum í framtíðinni. Hins vegar munu innkaupapantanir ekki draga úr framboðsspálínum.

Til dæmis ertu með vöru þar sem sjálfgefin pöntunartegund er *Pöntun*. Það hefur eftirfarandi framboðsspálínu.

| Líkan    | Dagsetning     | Lykill lánardrottins | Lánardrottnaflokkur | Magn | Eining | Svæði | Vöruhús |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| NúverandiF | 10/10/22 | US-101         |              | 25       | hver   | 1    | 11        |

Það er fyrirliggjandi innkaupapöntun fyrir lánardrottinn *US-101*, síða *1*, vöruhús *11*, magn af *25 ea*, og dagsetninguna *10/10/22*. 

Þegar þú keyrir aðaláætlun sem er sett upp til að nota *Enginn* sem lækkunaraðferð mun það búa til fyrirhugaða innkaupapöntun fyrir lánardrottinn *US-101*, síða *1*, vöruhús *11*, magn af *25 ea*, og dagsetninguna *10/10/22*. Með öðrum orðum, núverandi innkaupapöntun verður ekki lækkuð, vegna þess að spálækkunaraðferðin er *Enginn*.

Þú breytir nú áætlaðri innkaupapöntun sem var stofnuð eftir síðustu áætlunarkeyrslu og breytir magninu í *15 ea*. Þú samþykkir síðan pöntunina. Næst þegar þú keyrir aðaláætlunina mun hún stofna fyrirhugaða innkaupapöntun fyrir lánardrottinn *US-101*, síða *1*, vöruhús *11*, magn af *10 ea*, og dagsetninguna *10/10/22*. Að þessu sinni verður magnið minnkað til að endurspegla magn núverandi samþykktrar pöntunar frá fyrri áætlunargerð.

## <a name="differences-between-planning-optimization-and-the-built-in-planning-engine"></a>Mismunur á skipulagshagræðingu og innbyggðu skipulagsvélinni

Framboðsspár virka aðeins öðruvísi, allt eftir skipulagsvélinni sem þú ert að nota (innbyggð aðaláætlanagerð eða áætlanagerð fínstilling). Þessi hluti lýsir muninum.

### <a name="vendor-groups"></a>Lánardrottnaflokkar

Þegar þú bætir við spálínu er hægt að tilgreina lánardrottinn og lánardrottnahóp. Í innbyggðu áætlunarvélinni eru áætlaðar pantanir sem eru stofnaðar flokkaðar eftir samsetningu gildi lánardrottins og lánardrottinshóps. Í Hagræðingu áætlanagerðar eru áætlaðar pantanir flokkaðar eftir lánardrottni.

Eftirfarandi tafla gefur nokkur dæmi um framboðsspálínur fyrir vöru.

| Líkan    | Dagsetning     | Lykill lánardrottins | Lánardrottnaflokkur | Magn | Eining | Svæði | Vöruhús |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| NúverandiF | 10/10/22 |                | Seljandi GroupA | 5        | hver   | 1    | 11        |
| NúverandiF | 10/10/22 |                | Seljandi GroupA | 6        | hver   | 1    | 11        |
| NúverandiF | 10/10/22 |                |              | 7        | hver   | 1    | 11        |

Seljandi *Seljandi A* er sjálfgefinn lánardrottinn fyrir lánardrottnahóp *Seljandi GroupA*. Það er líka sjálfgefinn söluaðili vörunnar.

Innbyggða skipulagsvélin mun búa til eftirfarandi pantanir:

- Fyrirhuguð innkaupapöntun fyrir seljanda *Seljandi A*, söluaðila hópur *Seljandi GroupA*, og magn af *11*
- Fyrirhuguð innkaupapöntun fyrir seljanda *Seljandi A* og magn af *7*

Hagræðing áætlanagerðar mun aðeins búa til eina pöntun:

- Fyrirhuguð innkaupapöntun fyrir seljanda *Seljandi A*, söluaðila hópur *Seljandi GroupA*, og magn af *18*

### <a name="reduction-of-general-forecasts-by-more-specific-forecasts"></a>Fækkun almennra spáa með sértækari spám

Í innbyggðu aðalskipulagsvélinni er niðurstaðan ófyrirsjáanleg ef sumar spár hafa söluaðila en aðrar ekki.

Í Hagræðingu áætlanagerðar eru almennar spár alltaf minnkaðar með nákvæmari spám, eins og eftirfarandi dæmi sýnir.

Eftirfarandi tafla gefur nokkur dæmi um framboðsspálínur fyrir vöru.

| Dagsetning       | Magn | Lánardrottinn   | Lánardrottnaflokkur  |
|------------|----------|----------|---------------|
| 02/11/2022 | 5.00     | Seljandi-A | Seljandi Group-A |
| 02/11/2022 | 6,00     | Seljandi-A | Seljandi Group-A |
| 02/11/2022 | 15.00    |          |               |

Almenna spáin (fyrir 15.00 stykki) minnkar með nákvæmari spám (fyrir 5.00 + 6.00 = 11.00 stykki). Afgangurinn er úthlutað til sjálfgefna lánardrottins. Eftirfarandi tafla sýnir fyrirhugaðar pantanir.

| Dagsetning       | Magn | Lánardrottinn   | Lánardrottnaflokkur  |
|------------|----------|----------|---------------|
| 02/11/2022 | 11,00    | Seljandi-A | Seljandi Group-A |
| 02/11/2022 | 4.00     | Seljandi-A | Seljandi Group-A |

### <a name="respect-for-default-order-settings-when-planned-orders-are-generated"></a>Virðing fyrir sjálfgefnum pöntunarstillingum þegar áætlaðar pantanir eru búnar til

Hver vara getur haft sjálfgefnar pöntunarstillingar, svo sem lágmarks innkaupapöntunarmagn. Innbyggða áætlunarvélin hunsar þessar stillingar og þýðir því spár í áætlaðar pantanir sem hafa sama magn. Hagræðing áætlanagerðar virðir þessar stillingar þegar áætlaðar pantanir eru búnar til úr framboðsspám. 

### <a name="aggregation-of-planned-orders-as-a-result-of-reduction-by-approved-orders"></a>Söfnun áætluðum pöntunum vegna lækkunar með samþykktum pöntunum

Innbyggða aðalskipulagsvélin gerir ráð fyrir að aðeins ein pöntun dragi úr núverandi framboðsspá. Þess vegna, ef nokkrar pantanir passa við framboðsspálínu, mun aðeins fyrsta pöntunin draga úr henni. Í Hagræðingu áætlanagerðar munu allar pantanir sem passa við framboðsspálínuna draga úr henni.

### <a name="reduction-of-forecasts-by-matching-vendors-only"></a>Minnkun á spám með því að passa við söluaðila eingöngu

Þegar innbyggða aðalskipulagsvélin dregur úr spá með fyrirliggjandi útgefnum innkaupapöntunum, tryggir það ekki að lánardrottinn á innkaupapöntuninni passi við lánardrottinn úr spánni. Hagræðing áætlanagerðar dregur aðeins úr spám með innkaupapöntunum sem hafa samsvarandi gildi í reitnum lánardrottins.

Fyrir flutnings- og framleiðslupantanir er reiturinn lánardrottinn alltaf hunsaður, vegna þess að hann á ekki við um þessar pöntunargerðir.

### <a name="reduction-of-forecasts-by-transfer-orders"></a>Fækkun spár með millifærslupöntunum

Ef sjálfgefin pöntunartegund fyrir vöru er *Flytja*, aðeins er hægt að minnka spár með fyrirliggjandi fyrirhuguðum flutningspöntunum. Hins vegar, fyrir framleiðslupantanir og innkaupapantanir, draga aðeins út pantanir úr framboðsspánni.

Innbyggða áætlunarvélin minnkar fyrir öll flutningspöntunarstöður, en áætlanagerð fínstilling dregur aðeins úr spám með flutningspöntunum sem eru í *Gefin út* ríki.
