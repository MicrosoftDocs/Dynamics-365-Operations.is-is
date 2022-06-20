---
title: Inventory Visibility birgðaúthlutun
description: Þessi grein útskýrir hvernig á að setja upp og nota birgðaúthlutunareiginleikann, sem gerir þér kleift að leggja til hliðar sérstakar birgðir til að tryggja að þú getir uppfyllt arðbærustu rásirnar þínar eða viðskiptavini.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: ccc3a8c4b3d0649397b1d1f9139f7feebf39b02f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852506"
---
# <a name="inventory-visibility-inventory-allocation"></a>Inventory Visibility birgðaúthlutun

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Viðskiptabakgrunnur og tilgangur

Í mörgum tilfellum verða framleiðendur, smásalar og aðrir eigendur birgðakeðjufyrirtækja að úthluta birgðum fyrirfram fyrir mikilvægar söluleiðir, staðsetningar eða viðskiptavini eða fyrir sérstaka söluviðburði. Birgðaúthlutun er dæmigerð venja í rekstraráætlunarferli sölu og er gerð áður en raunveruleg sölustarfsemi á sér stað og sölupöntun er stofnuð.

Til dæmis hefur reiðhjólafyrirtæki takmarkaðan lager í boði fyrir mjög vinsælt hjól. Þetta fyrirtæki stundar bæði sölu á netinu og í verslun. Í hverri sölurás hefur fyrirtækið nokkra mikilvæga fyrirtækjasamstarfsaðila (markaðstaðir og stórir smásalar) sem krefjast þess að tiltekinn hluti af tiltækum birgðum hjólsins sé vistaður fyrir þá. Þess vegna verður reiðhjólafyrirtækið að geta jafnað dreifingu hlutabréfa á milli rása og einnig stjórnað væntingum VIP samstarfsaðila sinna. Besta leiðin til að ná báðum markmiðum er að nota birgðaúthlutun, þannig að hver rás og smásali geti fengið ákveðið úthlutað magn sem hægt er að selja neytendum síðar.

Birgðaúthlutun hefur tvo grundvallarviðskiptatilgang:

- **Birgðavörn (hringgirðingar)** – Stofnanir vilja fyrirframúthluta takmörkuðum eða takmörkuðum birgðum til forgangsraða rása, svæða, VIP-viðskiptavina og dótturfyrirtækja. Úthlutunareiginleikinn Birgðasýnileiki miðar að því að vernda úthlutaðar birgðir, þannig að aðrar úthlutanir, frátekningar eða aðrar sölukröfur hafi ekki áhrif á áður úthlutaðar birgðir.
- **Yfirsölustýring** – Úthlutunareiginleikinn Birgðasýnileiki miðar að því að setja takmörkun á áður úthlutað magni, þannig að móttökuaðilinn (til dæmis rás eða viðskiptavinahópur) muni ekki ofneyta það þegar raunveruleg sölufærsla sem er byggð á mjúkri fyrirvari tekur gildi.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Úthlutunarskilgreining í birgðasýnileikaþjónustu

Þó að úthlutunareiginleikinn í birgðasýnileikaþjónustunni leggi ekki efnislegt birgðamagn til hliðar, vísar það til tiltæks efnislegrar birgðamagns til að skilgreina upphaflegt birgðamagn.*laus til úthlutunar* magn sýndarlaugar. Birgðaúthlutun í Birgðasýnileika er mjúk úthlutun. Það er gert áður en raunverulegar sölufærslur eiga sér stað og er ekki háð sölupöntunum. Til dæmis geturðu úthlutað lager til mikilvægustu sölurásanna þinna eða stórra fyrirtækjasala áður en einhverjir endir viðskiptavinir heimsækja sölurásina eða smásöluna til að kaupa það.

Munurinn á birgðaúthlutun og [birgðamjúkur fyrirvari](inventory-visibility-reservations.md) er að mjúkur fyrirvari er venjulega tengdur raunverulegum sölufærslum (sölupöntunarlínum). Þess vegna, ef þú vilt nota eiginleika úthlutunar og mjúkrar frátekningar saman, mælum við með því að þú gerir birgðaúthlutun fyrst og síðan mjúka forða á móti úthlutuðu magni. Fyrir frekari upplýsingar, sjá [Neyta sem mjúkur fyrirvari](#consume-to-soft-reserved).

Birgðaúthlutunareiginleikinn gerir okkur kleift að skipuleggja sölu eða lykilreikninga stjórna og fyrirframúthluta mikilvægum birgðum yfir úthlutunarhópa (eins og rásir, svæði og viðskiptavinahópa). Það styður einnig rauntíma mælingu, aðlögun og greiningu á neyslu miðað við úthlutað magn, svo að hægt sé að endurnýja eða endurúthluta á réttum tíma. Þessi hæfileiki til að hafa rauntíma sýnileika í úthlutun, neyslu og úthlutunarjöfnuði er sérstaklega mikilvægur við hraðsölu eða kynningarviðburði.

## <a name="terminology"></a>Orðalisti

Eftirfarandi hugtök og hugtök eru gagnleg í umræðum um birgðaúthlutun:

- **Úthlutunarhópur** – Hópurinn sem á úthlutunina, svo sem sölurás, viðskiptavinahóp eða pöntunartegund.
- **Gildi úthlutunarhóps** – Verðmæti hvers úthlutunarhóps. Til dæmis, *vefur* eða *verslun* gæti verið verðmæti sölurásarúthlutunarhópsins, en *VIP* eða *eðlilegt* gæti verið verðmæti viðskiptavinaúthlutunarhópsins.
- **Úthlutunarstigveldi** – Aðferð til að sameina úthlutunarhópa á stigveldislegan hátt. Til dæmis er hægt að skilgreina *rás* sem stigveldisstig 1, *svæði* sem stig 2, og *viðskiptavinahópur* sem stig 3. Við birgðaúthlutun verður að fylgja úthlutunarstigveldisröðinni þegar þú tilgreinir gildi úthlutunarhópsins. Til dæmis gætirðu úthlutað 200 rauðum hjólum til *vefur* rás, the *London* svæði, og *VIP* viðskiptavinahópur.
- **Hægt að úthluta** — Hið *sýndar sameiginleg laug* sem gefur til kynna magnið sem er til ráðstöfunar til frekari úthlutunar. Það er útreiknaður mælikvarði sem þú getur frjálst skilgreint með því að nota þína eigin formúlu. Ef þú ert líka að nota mjúka bókunareiginleikann, mælum við með að þú notir sömu formúlu til að reikna út tiltækt til úthlutunar og tiltækt til að panta.
- **Úthlutað** – Líkamleg mælikvarði sem sýnir úthlutaðan kvóta sem úthlutunarhóparnir geta neytt.
- **Neytt** – Eðlisfræðilegur mælikvarði sem gefur til kynna að magn sem hefur verið neytt á móti upprunalegu úthlutuðu magni. Þegar tölum er bætt við þessa efnislegu mælingu, minnkar úthlutað líkamleg mál sjálfkrafa.

Eftirfarandi mynd sýnir verkflæði fyrirtækja fyrir birgðaúthlutun.

![Viðskiptavinnuflæði fyrir úthlutun birgðasýnileika.](media/inventory-visibility-allocation-flow.png "Viðskiptavinnuflæði fyrir úthlutun birgðasýnileika.")

## <a name="set-up-inventory-allocation"></a>Settu upp birgðaúthlutun

Birgðaúthlutunareiginleikinn samanstendur af eftirfarandi hlutum:

- Forskilgreindur, úthlutunartengdur gagnagjafi, líkamlegar mælingar og reiknaðar mælikvarðar.
- Sérhannaðar úthlutunarhópar sem hafa að hámarki átta stig.
- Safn af úthlutunarforritunarviðmótum (API):

    - Úthluta
    - endurúthluta
    - óúthlutað
    - neyta
    - fyrirspurn

Ferlið við að stilla úthlutunareiginleikann hefur tvö skref:

- Settu upp [gagnagjafa](inventory-visibility-configuration.md#data-source-configuration) og þess [ráðstafanir](inventory-visibility-configuration.md#data-source-configuration-physical-measures).
- Settu upp heiti úthlutunarhóps og stigveldi.

### <a name="predefined-data-source"></a>Forskilgreind gagnagjafi

Þegar þú virkjar úthlutunareiginleikann og kallar uppstillingaruppfærsluforritaskil, býr birgðasýnileiki til einn fyrirfram skilgreindan gagnagjafa og nokkrar upphafsmælingar.

Gagnagjafinn er nefndur `@iv`.

Hér eru fyrstu líkamlegu ráðstafanir:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

Hér eru fyrstu reiknaðar mælingar:

- `@iv`

    - `@iv.@available_to_allocate` = `??`–`??` –`@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Bættu öðrum líkamlegum mælingum við reiknaða mælikvarða sem tiltækt er að úthluta

Til að nota úthlutun verður þú að setja upp reiknaða mælikvarða sem hægt er að úthluta (`@iv.@available_to_allocate`). Til dæmis, þú hefur`fno` gagnagjafa og`onordered` mæla, the`pos` gagnagjafa og`inbound` mæla, og þú vilt gera úthlutun á hendi fyrir summan af`fno.onordered` og `pos.inbound`. Í þessu tilfelli,`@iv.@available_to_allocate` ætti að innihalda`pos.inbound` og`fno.onordered` í formúlunni. Hér er dæmi:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound`–`@iv.@allocated`

### <a name="change-the-allocation-group-name"></a>Breyttu heiti úthlutunarhóps

Að hámarki er hægt að stilla átta nöfn úthlutunarhópa. Hóparnir hafa stigveldi.

Þú stillir hópnöfnin á **Birgðasýnileiki Power App Stilling** síðu. Til að opna þessa síðu, í þínu Microsoft Dataverse umhverfi, opnaðu Inventory Visibility appið og veldu **Stillingar \> Úthlutun**.

Til dæmis, ef þú notar fjögur hópnöfn og stillir þau á\[`channel`,`customerGroup`,`region`,`orderType`\], þessi nöfn munu gilda fyrir úthlutunartengdar beiðnir þegar þú hringir í uppfærsluuppfærsluforritaskil stillinga.

### <a name="allocation-using-tips"></a>Úthlutun með ábendingum

- Fyrir hverja vöru ætti úthlutunaraðgerðin að nota það sama *víddarstig* í samræmi við vöruvísitölustigveldið sem þú stillir í [uppsetningu vöruvísitölu stigveldis](inventory-visibility-configuration.md#index-configuration). Segjum til dæmis að vísitölustigveldið þitt sé það\[`Site`,`Location`,`Color`,`Size`\]. Ef þú úthlutar einhverju magni fyrir eina vöru á víddarstigi\[`Site`,`Location`,`Color`\], næst þegar þú vilt úthluta þessari vöru, ættirðu líka að úthluta á sama stigi,\[`Site`,`Location`,`Color`\]. Ef þú notar borðið\[`Site`,`Location`,`Color`,`Size`\] eða\[`Site`,`Location`\], gögnin verða ósamræmi.
- Breyting á nafni úthlutunarhóps mun ekki hafa áhrif á gögn sem eru vistuð í þjónustunni.
- Úthlutun ætti að gerast eftir að varan hefur jákvætt magn við höndina.
- Að úthluta vörum frá háum *úthlutunarstig* hópur í undirhóp, notaðu`Reallocate` API. Til dæmis ertu með stigveldi úthlutunarhópa\[`channel`,`customerGroup`,`region`,`orderType`\], og þú vilt úthluta einhverri vöru úr úthlutunarhópi\[ Á netinu, VIP\] til undirúthlutunarhópsins\[ Á netinu, VIP, ESB\], nota`Reallocate` API til að færa magnið. Ef þú notar`Allocate` API, það mun úthluta magninu úr sýndar sameiginlegu lauginni.

### <a name="using-the-allocation-api"></a><a name="using-allocation-api"></a> Notkun úthlutunar API

Sem stendur eru fimm úthlutunarforritaskil opnuð:

- POST /api/umhverfi/{environmentId} /úthlutun/úthluta
- POST /api/umhverfi/{environmentId} /úthlutun/afúthluta
- POST /api/umhverfi/{environmentId} /úthlutun/endurúthluta
- POST /api/umhverfi/{environmentId} /úthlutun/neyta
- POST /api/umhverfi/{environmentId} /úthlutun/fyrirspurn

#### <a name="allocate"></a>Úthluta

Hringdu í`Allocate` API til að úthluta vöru sem hefur sérstakar stærðir. Hér er skema fyrir meginmál beiðninnar.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "targetGroups": {
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
    "id": "???",
    "productId": "Bike",
    "targetGroups": {
        "channel": "Online",
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

#### <a name="unallocate"></a>Afúthlutun

Nota`Unallocate` API til að snúa við`Allocate` aðgerð. Neikvætt magn er ekki leyfilegt í`Allocate` aðgerð. Líkaminn á`Unallocate` er samhljóða meginmáli `Allocate`.

#### <a name="reallocate"></a>Endurúthluta

Nota`Reallocate` API til að færa eitthvað úthlutað magn í aðra hópsamsetningu. Hér er skema fyrir meginmál beiðninnar.

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
    "targetGroups": {
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
    "id": "???",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "targetGroups": {
        "channel": "Online",
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

#### <a name="consume"></a>Nota

Nota`Consume` API til að bóka neyslumagnið á móti úthlutun. Til dæmis gætirðu notað þetta API til að færa úthlutað magn til nokkurra raunverulegra mælikvarða. Hér er skema fyrir meginmál beiðninnar.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "targetGroups": {
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

Nú eru þrjú hjól seld og þau tekin úr úthlutunarpottinum. Til að skrá þessa hreyfingu geturðu hringt símtal sem hefur eftirfarandi beiðni.

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
    "targetGroups": {
        "channel": "Online",
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

Í þessari beiðni skaltu taka eftir því að líkamlega mælikvarðinn sem þú notar í meginmáli neyslubeiðnarinnar ætti að nota gagnstæða breytingagerð (samlagning eða frádráttur), samanborið við breytingagerðina sem notuð er í útreiknuðu mælingu. Svo í þessum neyta líkama,`iv.inbound` hefur gildi`Subtraction`, ekki `Addition`.

The`fno` gagnagjafa er ekki hægt að nota í neysluhlutanum þar sem við héldum alltaf fram að birgðasýnileiki geti ekki breytt neinum gögnum fyrir`fno` gagnagjafa. Gagnaflæðið er einstefnu, sem þýðir að allt magn breytist fyrir`fno` gagnagjafi verður að koma frá Supply Chain Management umhverfi þínu.

#### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a> Neyta sem mjúkur fyrirvari

The`Consume` API getur einnig notað úthlutað magn sem mjúkan fyrirvara. Í þessu tilviki er`Consume` rekstur mun minnka úthlutað magn og gera síðan mjúkan fyrirvara fyrir það magn. Til að nota þessa aðferð verður þú líka að nota [mjúkur fyrirvari](inventory-visibility-reservations.md) eiginleiki birgðasýnileika.

Til dæmis hefur þú stillt mjúkan frátekningarbreyti (mæling) sem `iv.softreserved`. Eftirfarandi formúla er notuð fyrir tiltæka forða reiknaða mælingu:

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
    "targetGroups": {
        "channel": "Online",
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

#### <a name="query"></a>Fyrirspurn

Nota`Query` API til að sækja úthlutunartengdar upplýsingar fyrir sumar vörur. Þú getur notað víddarsíur og úthlutunarhópasíur til að þrengja niðurstöðurnar. Málin verða að passa nákvæmlega við þá sem þú vilt sækja, td.\[ síða=1, staðsetning=11\] mun hafa ótengdar niðurstöður miðað við\[ síða=1, staðsetning=11, litur=rauður \].

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
        "channel": "Online",
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
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```
