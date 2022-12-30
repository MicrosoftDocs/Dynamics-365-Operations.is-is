---
title: Aðaláætlanagerð með birgðaspá
description: Í þessari grein er því lýst hvernig birgðaspár eru teknar til skoðunar við aðaláætlanagerð.
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
ms.openlocfilehash: 2bac9355bb1ac00f697ec459f494a64553e0eacc
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740142"
---
# <a name="master-planning-with-supply-forecasts"></a>Aðaláætlanagerð með birgðaspá

[!include [banner](../../includes/banner.md)]

Framboðsspár gera þér kleift að tilgreina framboðið sem þú býst við að þurfa á einhverju tímabili í framtíðinni. Venjulega byggir þú áætlunina á söluferli fyrra árs og notar síðan spána í fjárhagsáætlunargerð. Einnig er hægt að setja upp aðaláætlun til að íhuga spá meðan á áætlunargerð stendur.

## <a name="set-up-a-master-plan-to-consider-supply-forecasts"></a>Setja upp aðaláætlun með tilliti til birgðaspár

Hægt er að tilgreina hvort hvert aðaláætlun eigi að taka mið af spám þegar það er keyrt. Notið eftirfarandi ferli til að stilla spávalkosti fyrir hverja áætlun.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Veldu núverandi aðaláætlun á listasvæðinu eða veldu **Nýtt** á aðgerðasvæðinu til að búa til nýjan.
1. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:

    - **Spárlíkan** – Veldu líkanið sem inniheldur um framboðs- og/eða eftirspurnarspár sem ætti að taka mið af aðaláætluninni.
    - **Hafa með birgðaspá -** Stillið þennan valkost á *Já* ef aðaláætlun ætti að taka mið af birgðaspá.
    - **Hafa með eftirspurnarspá -** Stillið þennan valkost á *Já* ef aðaláætlun ætti að taka mið af eftirspurnarspá. Þrátt fyrir að þessi stilling sé óháð **Hafa með birgðaspá**, þá eiga sumar aðrar stillingar á síðunni bæði við framboðspá og eftirspurnarspá. Frekari upplýsingar um áætlanagerð sem tekur mið af eftirspurnarspám eru í [Aðaláætlanagerð með eftirspurnarspám](demand-forecast.md).
    - **Aðferð sem er notuð til að minnka spárþarfir** - Veljið aðferðina sem á að nota til að minnka spárþarfir við aðaláætlanagerð:

        - *Ekkert* - Ekki verður dregið úr spákröfum við aðaláætlanagerð.
        - *Prósenta - minnkunarlykill* - Dregið er úr spáþörfum í samræmi við prósentur og tímabil sem eru skilgreind af minnkunarlykil.
        - *Færslur - minnkunarlykill* – Dregið er úr spáþörfum í samræmi við færslur sem eiga sér stað á tímabilunum sem eru skilgreind af minnkunarlykil.
        - *Færslur - breytilegt tímabil* - eru spáþarfir minnkaðar við raunverulega pöntunarfærslur sem koma upp við breytilegt tímabil. Breytilegt tímabil nær yfir núgildandi spá dagsetningar og lýkur þegar næsta spá hefst. Aðferðin *Færslur – breytilegt tímabil* notar ekki eða krefst minnkunarlykils og þegar hann er notaður eiga eftirfarandi skilyrði við:

            - Ef spá er alveg minnkuð verða spárþarfir gildandi spár 0 (núll).
            - Ef það er engin komandi spá eru spáþarfir frá síðustu spá sem var færð inn minnkaðar.
            - Tímamörk eru hafðar með í útreikningi á lækkun spár.
            - Jákvæðir dagar eru hafðir með í útreikningi á lækkun spár.
            - Ef raunverulegar pöntunarfærslur°fara fram úr spáþörfum, eru eftirstandandi færslur ekki sendar áfram í næsta spátímabil.

        > [!NOTE]
        > **Aðferðin sem notuð er til að minnka spárkröfur** á einnig við um eftirspurnarspár ef þú hefur virkjað þær fyrir aðaláætlun og það hefur svipuð áhrif. Frekari upplýsingar eru í [Aðaláætlanagerð með eftirspurnarspám](demand-forecast.md).

## <a name="set-reduction-options-for-coverage-groups"></a>Veldu minnkunarvalkosti fyrir þekjuflokka

Til að velja valkosti sem stýra því hvernig þekjuflokkur mun draga úr spákröfum sínum fyrir aðaláætlanir sem nota færslubundna minnkun skal fylgja eftirfarandi skrefum.

1. Fara skal í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Þekjuflokkar**.
1. Veldu núverandi þekjuflokk á listasvæðinu eða veldu **Nýtt** á aðgerðasvæðinu til að búa til nýjan.
1. Á flýtiflipanum **Annað** í reitnum **Lækka spá um** skal tilgreina hvernig skuli draga úr þörfum samkvæmt spá fyrir vörur í þekjuflokknum fyrir aðaláætlanir þar sem reiturinn **Aðferð notuð til að minnka þörf samkvæmt spá** er stilltur á *Færslur - minnkunarlykill* eða *Færslur - breytilegt tímabil*. Veljið eitt af eftirfarandi gildum:

    - *Allar færslur* – Allar færslur ættu að lækka spána.
    - *Pantanir* – Aðeins pantanir af sömu gerð ættu að minnka spána.

    Til dæmis gefa sjálfgefnar pantanastillingar fyrir vöru til kynna að það eigi að framleiða. Það er birgðaspárlína fyrir magnið 50, og það er fyrirliggjandi innkaupapöntun fyrir magnið 20. Ef reiturinn **Minnka spá um** er stillt á *Pantanir* verður búin til áætluð framleiðslupöntun fyrir magn 50. Ef það er stillt á *Allar færslur* verður áætluð framleiðslupöntun lækkuð í magn sem nemur 30.

    Þessi stilling gildir einnig um minnkun eftirspurnarspáar. Frekari upplýsingar eru í [Aðaláætlanagerð með eftirspurnarspám](demand-forecast.md).

## <a name="enter-a-supply-forecast-for-a-product"></a>Færa inn birgðaspá fyrir vöru

Til að slá inn birgðaspá fyrir vöru skal fylgja eftirfarandi skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veldu vöru sem þú vilt slá inn spá fyrir.
1. Á aðgerðasvæðinu, í flipanum **Áætlun** skal velja **Birgðaspá**.
1. Á síðunni **Birgðaspá**, á aðgerðasvæðinu, skal velja **Nýtt** til að bæta við spá við hnitanetið.
1. Upplýsingar eru færðar í nýju línuna eins og þörf er á til að tilgreina spá þína.

## <a name="plan-for-an-item-with-supply-forecast-lines"></a>Skipuleggja vöru með birgðaspárlínum

Þegar þú keyrir aðaláætlun sem inniheldur vöru sem birgðaspá er til fyrir mun kerfið stofna innkaupapantanir fyrir birgðalínurnar sem slegnar hafa verið inn. Sjálfgefnar pöntunarstillingar fyrir vöruna eru virtar. Ef þessar sjálfgefnu pöntunarstillingar tilgreina **Sjálfgefnar pöntunargerð** gildi *Innkaupapöntunar* og enginn lánardrottnalykill er tilgreindur í birgðaspálínu mun kerfið nota sjálfgefinn lánardrottinn fyrir vöruna.

## <a name="check-whether-a-planned-order-is-a-supply-forecast-order"></a>Athuga hvort áætluð pöntun sé birgðaspárpöntun

Fylgið eftirfarandi ferli til að fá upplýsingar um hvort áætluð pöntun hafi verið stofnuð vegna birgðaspár.

1. Fara í **Áætlanagerð \> Aðaláætlanagerð \> Áætlaðar pantanir**.
1. Opna skal áætluð pöntun sem á að skoða.
1. Á flýtiflipanum **Almennt** er horft á gildi reitsins **Birgðaspá**. Ef röðin var búin til að þekja birgðaspá verður þessi reitur stilltur á *Já*.

## <a name="examples-of-master-planning-with-supply-forecasts"></a>Dæmi um aðaláætlanagerð með birgðaspá

Í þessum hluta eru nokkur dæmi sem sýna hvernig birgðaspá hafa áhrif á aðaláætlanagerð.

### <a name="example-1-supply-forecast-for-an-item"></a>Dæmi 1: Birgðaspá fyrir vöru

Þú ert með vöru þar sem sjálfgefna pöntunargerðin *er Innkaupapöntun* og sjálfgefni lánardrottinn er *US-002*. Hún eru með eftirfarandi línu eftirspurnarspár.

| Líkan    | Dagsetning     | Lykill lánardrottins | Lánardrottnaflokkur | Magn | Eining | Svæði | Vöruhús |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                |              | 35       | hver   | 1    | 11        |

Þegar aðaláætlunargerð er keyrt verður búið til áætluð innkaupapöntun fyrir *35 ea* frá lánardrottinn *US-002*.

### <a name="example-2-several-supply-forecast-lines-with-and-without-a-vendor"></a>Dæmi 2: Nokkrar birgðaspárlínur, með og án lánardrottins

Þú ert með vöru þar sem sjálfgefna pöntunargerðin *er Innkaupapöntun* og sjálfgefni lánardrottinn er *US-002*. Hún eru með eftirfarandi línur eftirspurnarspár.

| Líkan    | Dagsetning     | Lykill lánardrottins | Lánardrottnaflokkur | Magn | Eining | Svæði | Vöruhús |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                |              | 35       | hver   | 1    | 11        |
| CurrentF | 10/10/22 | US-101         |              | 25       | hver   | 1    | 11        |

Í þessu tilviki meðhöndlar kerfið línuna sem tilgreinir ekki lánardrottinn sem almenna spá, og gerir ráð fyrir að línan sem tilgreinir lánardrottinn eigi að vera dregin frá almennu spánni. Því mun aðaláætlanagerð búa til eftirfarandi áætlaðar innkaupapantanir á vörunni:

- Áætluð innkaupapöntun fyrir magnið *25 ea* frá lánardrottinn *US-101* (Lánardrottinn og magnið sem tilgreint er í spálínunni eru notuð).
- Áætluð innkaupapöntun fyrir magnið *10 ea* frá lánardrottni *US-002* (Þar sem enginn söluaðili var tilgreindur í hinni spálínunni er sjálfgefni lánardrottinn notaður og magnið af þessari spálínu er minnkað um magn spálínu lánardrottins).

### <a name="example-3-plans-that-use-the-transactions---dynamic-period-reduction-method-in-a-single-forecast-period"></a>Dæmi 3: Áætlanir sem nota aðferðina Færslur - breytilegt tímabilsminnkun á einu spátímabili

Fyrir aðaláætlanir sem nota *Færslur - breytilegt tímabil* sem aðferð til að minnka spá, mun aðaláætlanagerð draga úr spámagni ef fyrirliggjandi færslur eru til staðar sem samsvara þessum framboðseiginleikum.

Þú ert t.d. með vöru þar sem sjálfgefna gerð pöntunar er *Innkaupapöntun*. Hún eru með eftirfarandi línu eftirspurnarspár.

| Líkan    | Dagsetning     | Lykill lánardrottins | Lánardrottnaflokkur | Magn | Eining | Svæði | Vöruhús |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | hver   | 1    | 11        |

Vegna þess að aðeins er um eina birgðaspárlínu að ræða er aðeins um eitt spártímabil að ræða.

Þegar þú keyrir aðaláætlun sem er sett upp til að nota *Færslur – breytilegt tímabil* sem minnkunaraðferð, skilar slíkt einni af eftirfarandi niðurstöðum:

- Ef innkaupapöntun er til fyrir lánardrottinn *US-101* og magnið er *10 ea* og reiturinn **Birgðaspá** er stillt á *Já*, býr aðaláætlanagerð til nýja áætlaða innkaupapöntun fyrir það magn sem eftir er af *10 ea*. Spárlínan er lækkuð, vegna þess að lánardrottinn passar við núverandi innkaupapöntun.
- Ef innkaupapöntun er til fyrir lánardrottinn *US-102* svæði *1*, vöruhús *11* og magnið er *10 ea* og reiturinn **Birgðaspá** er stillt á *Já*, býr aðaláætlanagerð til nýja áætlaða innkaupapöntun fyrir það magn sem eftir er af *25 ea*. Ekki er hægt að lækka spárlínuna, því hún er með annan lánardrottin en núverandi innkaupapöntun.

> [!NOTE]
> Þessi staða getur komið upp fyrir áætlaðar innkaupapantanir, vegna þess að lánardrottinn er tengdur þeim. Hins vegar, fyrir flutningspantanir og framleiðslupantanir, mun magn birgðaspáin alltaf lækka með fyrirliggjandi pöntunum, vegna þess að enginn lánardrottinn er tilgreindur fyrir þessar tegundir pantana.

### <a name="example-4-plans-that-use-the-transactions---dynamic-period-reduction-method-over-several-forecast-periods"></a>Dæmi 4: Áætlanir sem nota aðferðina Færslur - breytilegt tímabilsminnkunaraðferð á nokkrum spátímabilum

Þú ert með vöru þar sem sjálfgefna gerð pöntunar er *Innkaupapöntun*. Hún eru með eftirfarandi línur eftirspurnarspár.

| Líkan    | Dagsetning     | Lykill lánardrottins | Lánardrottnaflokkur | Magn | Eining | Svæði | Vöruhús |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | hver   | 1    | 11        |
| CurrentF | 15/10/22 | US-101         |              | 25       | hver   | 1    | 11        |

Í þessu dæmi eru tvær spárlínur sem hvor um sig hefur aðra dagsetningu. Þar af leiðandi stilla dagsetningarnar mörk spátímabilanna. Fyrsta tímabil er frá 10. október til og með 14. október 2022 (10/10/22–10/14/22). Sú seinni er frá 15. október 2022 (10/15/22) og seinna.

Fyrir liggur innkaupapöntun fyrir lánardrottinn *US-101* magnið er *10 ea* og dagsetningin er *10/12/22* (12. október 2022). Þegar þú keyrir aðaláætlun sem er sett upp til að nota *Færslur – breytilegt tímabil* sem lækkunaraðferð, mun það búa til eftirfarandi pantanir:

- Fyrirhuguð pöntun fyrir magnið *15 ea* og dagsetninguna *10/10/22* (magnið er lækkað með fyrirliggjandi innkaupapöntun sem er dagsett á sama spátímabili).
- Fyrirhuguð pöntun fyrir magnið *25 ea* og dagsetninguna *10/15/22* (magnið er allt magn spárinnar).

### <a name="example-5-plans-that-use-no-reduction"></a>Dæmi 5: Áætlanir sem nota enga minnkun

Þegar keyrð er áætlun þar sem spáminnkunaraðferðin er *Engin*, mun aðaláætlun alltaf búa til áætlað framboð fyrir allar birgðaspárlínur. Eftir að áætlað framboð hefur verið samþykkt mun það draga úr áætluðum pöntunum í framtíðinni. Hins vegar munu innkaupapantanir ekki draga úr birgðaspárlínunum.

Þú ert t.d. með vöru þar sem sjálfgefna gerð pöntunar er *Innkaupapöntun*. Hún eru með eftirfarandi línu eftirspurnarspár.

| Líkan    | Dagsetning     | Lykill lánardrottins | Lánardrottnaflokkur | Magn | Eining | Svæði | Vöruhús |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | hver   | 1    | 11        |

Fyrir liggur innkaupapöntun fyrir lánardrottinn *US-101*, svæði *1*, vöruhús *11* magnið er *25 ea* og dagsetningin er *10/10/22*. 

Þegar þú rekur aðaláætlun sem er sett upp til að nota *Ekkert* sem minnkunaraðferð mun það búa til áætlaða innkaupapöntun fyrir lánardrottinn *US-101*, svæði *1*, vöruhús *11*, magn sem nemur *25 ea* og dagsetninguna *10/10/22*. Með öðrum orðum, núverandi innkaupapöntun verður ekki lækkuð, vegna þess aðferð við lækkun spár er *Engin*.

Þú getur nú breytt áætlaðri innkaupapöntun sem var stofnuð eftir síðustu áætlunarkeyrslu og breytt magninu í *15 ea*. Síðan samþykkir þú pöntunina. Næst þegar þú keyrir aðaláætlun mun það búa til áætlaða innkaupapöntun fyrir lánardrottinn *US-101*, svæði *1*, vöruhús *11*, magn sem nemur *10 ea* og dagsetninguna *10/10/22*. Í þetta sinn verður magnið lækkað í samræmi við magn núverandi samþykkts pöntunar frá fyrri áætlanakeyrslu.

## <a name="differences-between-planning-optimization-and-the-deprecated-master-planning-engine"></a>Munur á fínstillingu skipuluagningar og úreltri aðaláætlunarvél

Birgðaspár virka aðeins öðruvísi, eftir því hvaða aðaláætlunarvél þú notar (Fínstilling áætlanagerðar eða úreltu aðaláætlunarvélina). Í þessum hluta er mismuninum lýst.

### <a name="vendor-groups"></a>Lánardrottnaflokkar

Þegar áætlaðri línu er bætt við er hægt að tilgreina lánardrottinn eða lánardrottnaflokk. Í aðaláætlunarvélinni eru áætlaðar pantanir sem eru búnar til flokkaðar eftir samsettum gildum lánardrottins og lánardrottnaflokks. Í fínstillingu skipulagningar eru áætlaðar pantanir flokkaðar eftir lánardrottni.

Eftirfarandi tafla sýnir nokkur dæmi um birgðaspárlínur fyrir vöru.

| Líkan    | Dagsetning     | Lykill lánardrottins | Lánardrottnaflokkur | Magn | Eining | Svæði | Vöruhús |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                | VendorGroupA | 5        | hver   | 1    | 11        |
| CurrentF | 10/10/22 |                | VendorGroupA | 6        | hver   | 1    | 11        |
| CurrentF | 10/10/22 |                |              | 7        | hver   | 1    | 11        |

Lánardrottinn *VendorA* er sjálfgefni lánardrottinn fyrir lánardrottnaflokkinn *VendorGroupA*. Hann er einnig sjálfgefinn lánardrottinn vörunnar.

Úrelt aðaláætlunarvél býr til eftirfarandi pantanir:

- Áætluð innkaupapöntun fyrir lánardrottinn *VendorA*, lánardrottnaflokk *VendorGroupA* og magn sem nemur *11*
- Áætluð innkaupapöntun fyrir lánardrottinn *VendorA* og magn sem nemur *7*

Fínstilling skipulagningar mun búa til bara eina pöntun:

- Áætluð innkaupapöntun fyrir lánardrottinn *VendorA*, lánardrottnaflokk *VendorGroupA* og magn sem nemur *18*

### <a name="reduction-of-general-forecasts-by-more-specific-forecasts"></a>Lækkun almennra spáa með því að nota sértækari spár

Í úreltu aðaláætlunarvélinni er niðurstaðan ófyrirsjáanleg ef sumar spár eru með lánardrottinn en aðrar ekki.

Í fínstilling skipulagningar eru almennar spár alltaf lækkaðar með sértækari spám, eins og eftirfarandi dæmi sýnir.

Eftirfarandi tafla sýnir nokkur dæmi um birgðaspárlínur fyrir vöru.

| Dagsetning       | Magn | Lánardrottinn   | Lánardrottnaflokkur  |
|------------|----------|----------|---------------|
| 11/02/2022 | 5.00     | Lánardrottinn-A | VendorGroup-A |
| 11/02/2022 | 6,00     | Lánardrottinn-A | VendorGroup-A |
| 11/02/2022 | 15.00    |          |               |

Almenn spá (fyrir 15,00 stykki) er lækkuð með sértækari spám (fyrir 5,00 + 6,00 = 11,00 stykki). Afganginum er úthlutað til sjálfgefins lánardrottins. Eftirfarandi tafla sýnir áætlaðar pantanir.

| Dagsetning       | Magn | Lánardrottinn   | Lánardrottnaflokkur  |
|------------|----------|----------|---------------|
| 11/02/2022 | 11,00    | Lánardrottinn-A | VendorGroup-A |
| 11/02/2022 | 4.00     | Lánardrottinn-A | VendorGroup-A |

### <a name="respect-for-default-order-settings-when-planned-orders-are-generated"></a>Vinnsla á sjálfgefnum pöntunarstillingum þegar áætlaðar pantanir eru stofnaðar

Hver vara getur haft sjálfgefnar pöntunarstillingar, eins og til dæmis lágmarksmagn innkaupapöntunar. Úrelt aðaláætlunarvél hunsar þessar stillingar og breytir því áætluðum spám í áætlaðar pantanir sem hafa sama magn. Fínstilling áætlanagerðar tekur mið af þessar stillingar þegar áætlaðar pantanir eru búnar til úr birgðaspám. 

### <a name="aggregation-of-planned-orders-as-a-result-of-reduction-by-approved-orders"></a>Uppsöfnun áætlaðra pantana vegna lækkunar af samþykktum pöntunum

Úrelt aðaláætlunarvél gerir ráð fyrir að aðeins ein pöntun dragi úr fyrirliggjandi afgreiðsluspá. Þess vegna, ef nokkrar pantanir passa við birgðaspálína, mun aðeins fyrsta pöntunin lækka hana. Í fínstillingu skipulagningar munu allar pantanir sem passa við birgðaspálínuna lækka hana.

### <a name="reduction-of-forecasts-by-matching-vendors-only"></a>Aðeins fækka spám samkvæmt samsvarandi lánardrottnum

Þegar úrelta aðaláætlunarvélin lækkar spá með því að gefa út fyrirliggjandi innkaupapantanir, tryggir það ekki að lánardrottinn á innkaupapöntuninni passi við lánardrottinn í spánni. Fínstilling áætlanagerðar dregur aðeins úr spám með innkaupapöntunum sem hafa samsvarandi gildi í reit lánardrottins.

Fyrir flutnings- og framleiðslupantanir er reiturinn fyrir lánardrottinn alltaf hunsaður, því það skiptir ekki máli fyrir þær pöntunartegundir.

### <a name="reduction-of-forecasts-by-transfer-orders"></a>Lækkun spáar vegna flutningspantana

Ef sjálfgefna pöntunargerðin fyrir vöru er *Flutningur* er aðeins hægt að lækka spár með fyrirliggjandi áætluðum flutningspöntunum. Hins vegar, fyrir framleiðslupantanir og innkaupapantanir, aðeins losaðar pantanir lækka birgðaspá.

Úrelt aðaláætlunarvél lækkar stöðu allra flutningspantana, en fínstilling skipulagningar lækkar aðeins spár með flutningspöntunum í stöðunni *Losað*.
