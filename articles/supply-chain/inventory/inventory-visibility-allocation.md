---
title: Inventory Visibility birgðaúthlutun
description: Þessi grein útskýrir hvernig á að setja upp og nota birgðaúthlutunareiginleikann, sem gerir þér kleift að leggja til hliðar sérstakar birgðir til að tryggja að þú getir uppfyllt arðbærustu rásirnar þínar eða viðskiptavini.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 449ca0616405ba589b92fba1ef078a4350d1e3b1
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762673"
---
# <a name="inventory-visibility-inventory-allocation"></a>Inventory Visibility birgðaúthlutun

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Viðskiptabakgrunnur og tilgangur

Stofnanir þurfa oft að forúthluta birgðum sínum til þeirra mikilvægustu sölurása, viðskiptavinahópa, svæða og kynningarviðburða til að tryggja að forúthlutaða lagerinn sé varinn gegn allri annarri notkun og sé einungis hægt að neyta í gegnum söluviðskipti sem skipta máli fyrir úthlutun. Birgðaúthlutun í Birgðasýnileika er hluti af rekstraráætlunarferli sölu og er gert áður en raunveruleg sölustarfsemi á sér stað eða sölupöntun er stofnuð.

Til dæmis framleiðir fyrirtæki sem heitir Contoso vinsælt hjól. Því miður, vegna þess að nýleg truflun á birgðakeðjunni hefur haft áhrif á alla vöruflutninga á því hjóli, hefur Contoso aðeins takmarkað lager á lager og verður að nýta það sem best. Contoso rekur bæði sölu á netinu og í verslun. Í hverri sölurás hefur fyrirtækið nokkra mikilvæga fyrirtækjasamstarfsaðila (markaðstaðir og stórir smásalar) sem krefjast þess að tiltekinn hluti af tiltækum birgðum hjólsins verði vistaður fyrir þá. Þess vegna verður reiðhjólafyrirtækið að geta jafnað dreifingu hlutabréfa á milli rása og einnig stjórnað væntingum VIP samstarfsaðila sinna. Besta leiðin til að ná báðum markmiðum er að nota birgðaúthlutun, þannig að hver rás og smásali geti fengið ákveðið úthlutað magn sem hægt er að selja neytendum síðar.

Birgðaúthlutun hefur tvö grundvallarviðskiptatilgang:

- **Birgðavörn (hringgirðingar)** – Stofnanir vilja fyrirframúthluta takmörkuðum eða takmörkuðum birgðum til forgangsraða rása, svæða, VIP-viðskiptavina og dótturfyrirtækja. Úthlutunareiginleikinn Birgðasýnileiki miðar að því að vernda úthlutaðar birgðir, þannig að aðrar úthlutanir, frátekningar eða aðrar sölukröfur hafi ekki áhrif á áður úthlutaðar birgðir.
- **Yfirsölustýring** – Úthlutunareiginleikinn Birgðasýnileiki miðar að því að setja takmörkun á áður úthlutað magni, svo að móttökuaðilinn (til dæmis rás eða viðskiptavinahópur) muni ekki ofneyta það þegar raunveruleg sölufærsla sem er byggð á mjúkum fyrirvari tekur gildi.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Úthlutunarskilgreining í birgðasýnileikaþjónustu

### <a name="allocation-virtual-pool"></a>Úthlutunar sýndarlaug

Þó að úthlutunareiginleikinn í Birgðasýnileika leggi ekki efnislegt birgðamagn til hliðar, vísar það til tiltæks efnislegrar birgðamagns til að skilgreina upphaflegt birgðamagn þess.*laus til úthlutunar* magn sýndarlaugar. Birgðaúthlutun í Birgðasýnileika er mjúk úthlutun. Það er gert áður en raunverulegar sölufærslur eiga sér stað og er ekki háð sölupöntunum. Til dæmis geturðu úthlutað lager til mikilvægustu sölurásanna þinna eða stórra fyrirtækjasala áður en einhverjir endir viðskiptavinir heimsækja sölurásina eða smásöluna til að kaupa hana.

### <a name="difference-between-inventory-allocation-and-soft-reservation"></a>Mismunur á birgðaúthlutun og mjúkri frátekningu

[Mjúkir fyrirvarar](inventory-visibility-reservations.md) eru venjulega tengd raunverulegum sölufærslum (sölupöntunarlínur). Hægt er að nota bæði úthlutun og mjúkan fyrirvara sjálfstætt, en ef þú vilt nota þau saman ætti að gera mjúka fyrirvara eftir úthlutun. Við mælum með því að þú gerir birgðaúthlutun fyrst og síðan mjúkan varasjóð á móti úthlutuðu magni til að ná næstum rauntímanotkun gegn úthlutun. Fyrir frekari upplýsingar, sjá [Neyta sem mjúkur fyrirvari](#consume-to-soft-reserved).

Birgðaúthlutunareiginleikinn gerir söluskipuleggjendum eða lykilreikningsstjóra kleift að stjórna og úthluta mikilvægum birgðum á milli úthlutunarhópa (svo sem rásir, svæði og viðskiptavinahópa). Það styður einnig rauntíma mælingu, aðlögun og greiningu á neyslu miðað við úthlutað magn, til að tryggja að hægt sé að endurnýja eða endurúthluta á réttum tíma. Þessi hæfileiki til að hafa rauntíma sýnileika í úthlutun, neyslu og úthlutunarjöfnuði er sérstaklega mikilvægur við hraðsölu eða kynningarviðburði.

## <a name="terminology"></a>Orðalisti

Eftirfarandi hugtök og hugtök eru gagnleg í umræðum um birgðaúthlutun:

- **Úthlutunarhópur** – Hópurinn sem á úthlutunina, svo sem sölurás, viðskiptavinahóp eða pöntunartegund.
- **Gildi úthlutunarhóps** – Verðmæti hvers úthlutunarhóps. Til dæmis, *vefur* eða *verslun* gæti verið verðmæti sölurásarúthlutunarhópsins, en *VIP* eða *eðlilegt* gæti verið verðmæti viðskiptavinaúthlutunarhópsins.
- **Úthlutunarstigveldi** – Aðferð til að sameina úthlutunarhópa á stigveldislegan hátt. Til dæmis er hægt að skilgreina *rás* sem stigveldisstig 1, *svæði* sem stig 2, og *viðskiptavinahópur* sem stig 3. Við birgðaúthlutun verður þú að fylgja úthlutunarstigveldisröðinni þegar þú tilgreinir gildi úthlutunarhópsins. Til dæmis gætirðu úthlutað 200 rauðum hjólum til *vefur* rás, the *London* svæði, og *VIP* viðskiptavinahópur.
- **Hægt að úthluta** — Hið *sýndar sameiginleg laug* sem gefur til kynna magnið sem er til ráðstöfunar til frekari úthlutunar. Það er reiknaður mælikvarði sem þú getur skilgreint frjálslega með því að nota þína eigin formúlu. Ef þú ert líka að nota mjúka bókunareiginleikann mælum við með því að þú notir sömu formúlu til að reikna út tiltækt til úthlutunar og tiltækt til að panta.
- **Úthlutað** – Efnislegur mælikvarði sem sýnir úthlutaðan kvóta sem úthlutunarhóparnir geta neytt. Það er dregið frá á sama tíma og neytt magn er bætt við.
- **Neytt** – Eðlisfræðilegur mælikvarði sem gefur til kynna að magn sem hefur verið neytt á móti upprunalegu úthlutuðu magni. Þegar tölum er bætt við þessa efnislegu mælingu, minnkar úthlutað líkamleg mál sjálfkrafa.

Eftirfarandi mynd sýnir verkflæði fyrirtækja fyrir birgðaúthlutun.

![Viðskiptavinnuflæði fyrir úthlutun birgðasýnileika.](media/inventory-visibility-allocation-flow.png "Viðskiptavinnuflæði fyrir úthlutun birgðasýnileika.")

Eftirfarandi mynd sýnir úthlutunarstigveldið og úthlutunarhópa. The *sýndar sameiginleg laug* sem er sýnt hér er magn sem er tiltækt til að úthluta.

[<img src="media/inventory-visibility-allocation-hierarchy.png" alt="Inventory Visibility allocation hierarchy." title=" Úthlutunarstigveldi birgðasýnileika" width="720" />](media/inventory-visibility-allocation-hierarchy.png)

## <a name="set-up-inventory-allocation"></a>Settu upp birgðaúthlutun

Birgðaúthlutunareiginleikinn samanstendur af eftirfarandi hlutum:

- Forskilgreindur, úthlutunartengdur gagnagjafi, efnislegar mælingar og reiknaðar mælikvarðar.
- Sérhannaðar úthlutunarhópar sem hafa að hámarki átta stig.
- Safn af úthlutunarforritunarviðmótum (API):

    - Úthluta
    - endurúthluta
    - óúthlutað
    - neyta
    - fyrirspurn

Ferlið við að stilla úthlutunareiginleikann hefur þrjú skref:

- Virkjaðu eiginleikann í Inventory Visibility appinu með því að fara á **Stillingar \> Eiginleikastjórnun og stillingar \> Úthlutun**.
- Settu upp [gagnagjafa](inventory-visibility-configuration.md#data-source-configuration) og þess [ráðstafanir](inventory-visibility-configuration.md#data-source-configuration-physical-measures).
- Settu upp heiti og stigveldi úthlutunarhóps.

### <a name="predefined-data-source"></a>Forskilgreindur gagnagjafi

Þegar þú virkjar úthlutunareiginleikann og kallar uppstillingaruppfærsluforritaskil, býr birgðasýnileiki til einn fyrirfram skilgreindan gagnagjafa og nokkrar upphafsmælingar.

Gagnagjafinn er nefndur `@iv`. Það inniheldur sett af sjálfgefnum líkamlegum ráðstöfunum. Þú getur skoðað þær í Inventory Visibility appinu með því að fara á **Stillingar \> Uppruni gagna**. Þú ættir að sjá **Gagnaheimild - @IV**. Stækkaðu`@iv` gagnagjafi til að skoða lista yfir fyrstu líkamlegar ráðstafanir:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

Veldu **Reiknaðar mælikvarðar** flipa til að skoða upphaflega reiknaða mælikvarða, sem er nefndur `@iv.@available_to_allocate`:

- `@iv`

    - `@iv.@available_to_allocate` = `??`–`??` –`@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Bættu öðrum líkamlegum mælingum við reiknaða mælikvarða sem tiltækt er að úthluta

Til að nota úthlutun verður þú að setja upp formúluna rétt fyrir útreikninga mælikvarða sem er tiltækur til úthlutunar (`@iv.@available_to_allocate`). Til dæmis, þú hefur`fno` gagnagjafa og`onordered` mæla, og`pos` gagnagjafa og`inbound` mæla, og þú vilt gera úthlutun á lager á lager fyrir summan af`fno.onordered` og `pos.inbound`. Í þessu tilfelli,`@iv.@available_to_allocate` ætti að innihalda`pos.inbound` og`fno.onordered` í formúlunni. Hér er dæmi:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound`–`@iv.@allocated`

> [!NOTE]
> Uppruni gagna`@iv` er fyrirfram skilgreindur gagnagjafi og líkamlegar mælingar skilgreindar í`@iv` með forskeyti`@` eru fyrirfram skilgreindar ráðstafanir. Þessar ráðstafanir eru fyrirfram skilgreindar stillingar fyrir úthlutunareiginleikann, svo ekki breyta eða eyða þeim eða þú ert líklegri til að lenda í óvæntum villum þegar þú notar úthlutunareiginleikann.
>
> Þú getur bætt nýjum líkamlegum mælingum við fyrirfram skilgreinda reiknaða mælingu`@iv.@available_to_allocate`, en þú mátt ekki breyta nafni þess.

### <a name="manage-allocation-groups"></a>Stjórna úthlutunarhópum

Að hámarki er hægt að stilla átta nöfn úthlutunarhópa. Hóparnir hafa stigveldi. Fylgdu þessum skrefum til að skoða og uppfæra úthlutunarhópa.

1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu **Stillingar** síðu og síðan á **Úthlutun** flipa, veldu **Breyta stillingum**. Sjálfgefið er úthlutunarstigveldi sem hefur fjögur lög:`Channel` (efsta lag),`customerGroup` (annað lag),`Region` (þriðja lag), og`OrderType` (fjórða lag).
1. Þú getur fjarlægt núverandi úthlutunarhóp með því að velja **X** við hliðina á því. Einnig er hægt að bæta nýjum úthlutunarhópum við stigveldið með því að slá inn nafn hvers nýs hóps beint í reitinn.

    > [!IMPORTANT]
    > Vertu varkár þegar þú eyðir eða breytir úthlutunarstigveldisvörpuninni. Til leiðbeiningar, sjá [Ráð til að nota úthlutun](#allocation-tips).

1. Þegar þú hefur lokið við að stilla úthlutunarhópinn og stigveldisstillingarnar skaltu vista breytingarnar og velja síðan **Uppfærðu stillingar** efst til hægri. Gildi stilltu úthlutunarhópanna verða uppfærð þegar þú býrð til úthlutun með því að nota annað hvort notendaviðmótið eða API POST (/api<wbr> /umhverfi<wbr>/\{ umhverfisauðkenni\}<wbr> /úthlutun<wbr> /úthluta). Upplýsingar um báðar aðferðir eru veittar síðar í þessari grein.

Ef þú notar fjögur hópnöfn og stillir þau á\[`channel`,`customerGroup`,`region`,`orderType`\], munu þessi nöfn gilda fyrir úthlutunartengdar beiðnir þegar þú hringir í forritaskil uppfærsluuppfærslu.

### <a name="tips-for-using-allocation"></a><a name="allocation-tips"></a> Ráð til að nota úthlutun

- Fyrir hverja vöru ætti úthlutunaraðgerðin að nota í það sama *víddarstig* í samræmi við vöruvísitölustigveldið sem þú stillir í [uppsetningu vöruvísitölu stigveldis](inventory-visibility-configuration.md#index-configuration). Segjum til dæmis að vísitölustigveldið þitt sé það\[`Site`,`Location`,`Color`,`Size`\]. Ef þú úthlutar einhverju magni fyrir eina vöru á víddarstigi\[`Site`,`Location`,`Color`\], næst þegar þú vilt úthluta þessari vöru, ættirðu líka að úthluta á sama stigi,\[`Site`,`Location`,`Color`\]. Ef þú notar borðið\[`Site`,`Location`,`Color`,`Size`\] eða\[`Site`,`Location`\], gögnin verða ósamræmi.
- **Breyting á úthlutunarhópum og stigveldi:** Ef úthlutunargögn eru þegar til í kerfinu mun eyðing núverandi úthlutunarhópa eða breyting á stigveldi úthlutunarhópa skemma núverandi kortlagningu milli úthlutunarhópanna. Vertu því viss um að hreinsa öll gömlu gögnin handvirkt áður en þú uppfærir nýju stillingarnar þínar. Hins vegar, vegna þess að það að bæta nýjum úthlutunarhópum við lægsta stigveldið hefur ekki áhrif á núverandi kortanir, þarftu ekki að hreinsa gögnin.
- Úthlutun mun aðeins heppnast ef varan er jákvæð`available_to_allocate` magni.
- Að úthluta vörum frá háum *úthlutunarstig* hópur í undirhóp, notaðu`Reallocate` API. Til dæmis, þú ert með stigveldi úthlutunarhópa\[`channel`,`customerGroup`,`region`,`orderType`\], og þú vilt úthluta einhverri vöru úr úthlutunarhópi\[ Á netinu, VIP\] til undirúthlutunarhópsins\[ Á netinu, VIP, ESB\], nota`Reallocate` API til að færa magnið. Ef þú notar`Allocate` API, það mun úthluta magninu úr sýndar sameiginlegu lauginni.
- Til að skoða heildarframboð vöru (sameiginlegu sundlaugina), notaðu [fyrirspurn á hendi](inventory-visibility-api.md#query-on-hand) API til að biðja um birgðaupphæð sem er *laus til úthlutunar*. Þú getur síðan tekið úthlutunarákvarðanir byggðar á þessum upplýsingum.

## <a name="use-the-allocation-api"></a><a name="using-allocation-api"></a> Notaðu úthlutunar-API

Eins og er eru fimm úthlutunar API opnuð:

- **POST /api<wbr> /umhverfi<wbr>/\{ umhverfisauðkenni\}<wbr> /úthlutun<wbr> /úthluta** – Þetta API er notað til að búa til upphaflegu úthlutunina.
- **POST /api<wbr> /umhverfi<wbr>/\{ umhverfisauðkenni\}<wbr> /úthlutun<wbr> /afúthluta** – Þetta API er notað til að afturkalla eða fjarlægja úthlutað magn.
- **POST /api<wbr> /umhverfi<wbr>/\{ umhverfisauðkenni\}<wbr> /úthlutun<wbr> /endurúthluta** – Þetta API er notað til að færa úthlutað magn úr núverandi úthlutun yfir í aðra úthlutunarhópa.
- **POST /api<wbr> /umhverfi<wbr>/\{ umhverfisauðkenni\}<wbr> /úthlutun<wbr> /neyta** – Þetta API er notað til að draga (nota) úthlutað magn.
- **POST /api<wbr> /umhverfi<wbr>/\{ umhverfisauðkenni\}<wbr> /úthlutun<wbr> /fyrirspurn** – Þetta API er notað til að athuga núverandi úthlutunarskrár á móti úthlutunarhópum og stigveldi.

### <a name="allocate"></a>Úthluta

Hringdu í`Allocate` API til að úthluta vöru sem hefur sérstakar stærðir. Hér er skema fyrir meginmál beiðninnar.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Til dæmis viltu úthluta 10 magni fyrir vöru *Hjól*, síða *1*, staðsetning *11*, litur *rauður*, rás *Á netinu*, viðskiptavinahópur *VIP*, og svæði *BNA*. Til að gera þessa úthlutun geturðu hringt símtal sem hefur eftirfarandi meginmál.

```json
{
    "id": "test101",
    "productId": "Bike",
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 10,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

Magnið verður alltaf að vera meira en 0 (núll).

### <a name="unallocate"></a>Afúthlutun

Nota`Unallocate` API til að snúa við`Allocate` aðgerð. Neikvætt magn er ekki leyfilegt í`Allocate` aðgerð. Líkaminn á`Unallocate` er eins og meginmál `Allocate`.

### <a name="reallocate"></a>Endurúthluta

Nota`Reallocate` API til að færa úthlutað magn í aðra hópsamsetningu. Hér er skema fyrir meginmál beiðninnar.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "sourceGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "groups": {
        "groupD": "string",
        "groupE": "string",
        "groupF": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Til dæmis er hægt að færa tvö hjól sem hafa stærðirnar\[ síða=1, staðsetning=11, litur=rauður\] úr úthlutunarhópi\[ Á netinu, VIP, Bandaríkjunum\] til úthlutunarhóps\[ Á netinu, VIP, ESB\] með því að hringja í`Reallocate` API og gefa upp eftirfarandi megintexta.

```json
{
    "id": "test102",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "EU"
    },
    "quantity": 2,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

### <a name="consume"></a>Nota

Nota`Consume` API til að bóka neyslumagnið á móti úthlutun. Til dæmis gætirðu notað þetta forritaskil til að færa úthlutað magn til nokkurra raunverulegra mælikvarða. Hér er skema fyrir meginmál beiðninnar.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "physicalMeasures": {
        "datasource1": {
            "measure": "string" // Addition or Subtraction
        }
    }
}
```

Til dæmis eru átta úthlutað hjól sem hafa stærðirnar\[ síða=1, staðsetning=11, litur=rauður\] fyrir úthlutunarhóp\[ Á netinu, VIP, Bandaríkjunum \]. Eftirfarandi formúla sem hægt er að úthluta er notuð:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound`–`@iv.@allocated`

Hjólin átta eru úthlutað frá`pos.inbound` mæla.

Nú eru þrjú hjól seld og þau tekin úr úthlutunarpottinum. Til að skrá þessa hreyfingu geturðu hringt sem hefur eftirfarandi beiðni.

```json
{
    "id": "test103",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "pos": {
            "inbound": "Subtraction"
        }
    }
}
```

Eftir þetta símtal mun úthlutað magn fyrir vöruna minnka um 3. Að auki mun birgðasýnileiki búa til breytingaviðburð á staðnum þar sem`pos.inbound` = *-3*. Að öðrum kosti geturðu haldið`pos.inbound` verðmæti eins og það er og neyta bara úthlutaðs magns. Hins vegar, í þessu tilviki, verður þú annað hvort að búa til aðra líkamlega mælingu til að halda neytt magni eða nota fyrirfram skilgreinda mælingu `@iv.@consumed`.

Í þessari beiðni skaltu taka eftir því að líkamlega mælikvarðinn sem þú notar í meginmáli neyslubeiðnarinnar ætti að nota gagnstæða breytingagerð (samlagning eða frádráttur), samanborið við breytingagerðina sem notuð er í útreiknuðu mælingu. Svo í þessum neyslu líkama,`iv.inbound` hefur gildi`Subtraction`, ekki `Addition`.

The`fno` gagnagjafa er ekki hægt að nota í neysluhlutanum þar sem við héldum alltaf fram að birgðasýnileiki geti ekki breytt neinum gögnum fyrir`fno` gagnagjafa. Gagnaflæðið er einstefnu, sem þýðir að allt magn breytist fyrir`fno` gagnagjafi verður að koma frá Supply Chain Management umhverfi þínu.

### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a> Neyta sem mjúkur fyrirvari

The`Consume` API getur einnig notað úthlutað magn sem mjúkan fyrirvara. Í þessu tilviki er`Consume` aðgerð mun minnka úthlutað magn og gera síðan mjúkan fyrirvara fyrir það magn. Til að nota þessa aðferð verður þú líka að nota [mjúkur fyrirvari](inventory-visibility-reservations.md) eiginleiki birgðasýnileika.

Til dæmis, þú hefur stillt mjúka bókun líkamlega mælingu sem `iv.softreserved`. Eftirfarandi formúla er notuð fyrir tiltæka forða reiknaða mælingu:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound`–`iv.softreserved`

Til að nota þessa uppsetningu með úthlutunareiginleikanum skaltu bæta við`@iv.@allocated` til`iv.available_to_reserve` til að búa til eftirfarandi formúlu:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound`–`iv.softreserved` –`@iv.@allocated`

Uppfærðu síðan`@iv.@available_to_allocate` að sama virði.

Þegar þú vilt neyta 3 magns og panta þetta magn beint geturðu hringt sem hefur eftirfarandi beiðni.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "iv": {
            "softreserved": "Addition"
        }
    }
}
```

Taktu eftir því í þessari beiðni`iv.softreserved` hefur gildi`Addition`, ekki `Subtraction`.

### <a name="query"></a>Fyrirspurn

Nota`Query` API til að sækja úthlutunartengdar upplýsingar fyrir sumar vörur. Þú getur notað víddarsíur og úthlutunarhópasíur til að þrengja niðurstöðurnar. Stærðirnar verða að passa nákvæmlega við þá sem þú vilt sækja, td.\[ síða=1, staðsetning=11\] mun hafa ótengdar niðurstöður miðað við\[ síða=1, staðsetning=11, litur=rauður \].

```json
{
    "productId": "string",
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "groups": {
        "additionalProp1": "string",
        "additionalProp2": "string",
        "additionalProp3": "string"
    },
}
```

Til dæmis, notaðu\[ síða=1, staðsetning=11, litur=rauður\] og tómur hópareitur til að fá allar úthlutunarfærslur:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

Notaðu\[ síða=1, staðsetning=11, litur=rauður\] og hópa\[ channel=Online, customerGroup=VIP, region=US\] til að fá úthlutunarskrár fyrir þennan hóp:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

## <a name="use-the-allocation-user-interface"></a>Notaðu úthlutunarnotendaviðmótið

Þú getur handvirkt stjórnað úthlutunum í gegnum notendaviðmótið með því að opna Inventory Visibility appið og fara á **Sýnileiki í rekstri \> Úthlutun**. Þaðan geturðu framkvæmt allar aðgerðir sem lýst er í eftirfarandi undirköflum.

### <a name="create-an-allocation"></a>Búðu til úthlutun

Fylgdu þessum skrefum til að búa til úthlutun úr **Úthlutun** síðu birgðasýnileika appsins.

1. Veldu **Úthluta**.
1. Stilltu grunnreiti, víddir og gildi úthlutunarhópa. (Þegar þú velur gagnaöflunina í **Mál** hluta, notaðu fyrst fellilistann til að tilgreina stærðirnar (td,`siteId`). Sláðu síðan inn víddargildi í reitina sem birtast.)
1. Veldu **leggja fram**.

### <a name="consume-an-allocation"></a>Neyta úthlutun

Veldu **Neyta** að neyta úthlutunar. Til að tryggja að þú eyðir innan rétts úthlutunarhóps og stigveldis skaltu slá inn sömu sett af skipulagi og víddarupplýsingum og þú færðir inn þegar þú stofnaðir úthlutunina.

### <a name="reallocate-an-allocation"></a>Endurúthluta úthlutun

Veldu **Endurúthluta** til að færa fyrirliggjandi úthlutað magn frá einum hópi úthlutunarhópa til annars.

### <a name="query-existing-allocations"></a>Spurðu fyrirliggjandi úthlutun

Veldu **Fyrirspurn**, og sláðu síðan inn vöru-, skipulags-, víddar- og úthlutunarhópsgildi til að fá fyrirspurnarniðurstöður af núverandi úthlutunum.
