---
title: "Taka frá birgðamagn"
description: "Þessi efnisliður útskýrir aðra valkosti sem eru tiltækar fyrir að taka frá birgðir."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 207264
ms.assetid: 47537e4f-cdf6-4813-96fd-c945b2dfe9d4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 7361b2e04376284238c8c9b1f91d03d18b121d24
ms.lasthandoff: 03/31/2017


---

# <a name="reserve-inventory-quantities"></a>Taka frá birgðamagn

Þessi efnisliður útskýrir aðra valkosti sem eru tiltækar fyrir að taka frá birgðir.

Hægt er að taka birgðir sjálfkrafa frá fyrir tiltekna sölupöntun. Það þýðir að ekki er hægt að taka fráteknar birgðir út úr vöruhúsi fyrir aðra pöntun nema birgðafrátektin eða hluti hennar er afturkölluð.

Margar ástæður eru til að taka frá birgðir:
-   Pantað fyrst, afhent fyrst sem þýðir að viðskiptavinir fá tiltækar vörur í sömu röð og þeir panta þær.
-   Skortur á vörum vegna langs eða óþekkts afhendingartíma lánardrottins. Hægt er að tryggja að tilteknir viðskiptavinir eða pantanir fá fyrstu tiltækar vörur afhentar.
-   Tilteknir viðskiptavinir og tilteknar gerðir pantana hafa forgang um afhendingu.
-   Vörur með rað- eða rununúmer. Hægt er að merkja tilteknar vörur sem hafa verið eða verða afhentar í tilteknum pöntunum.
-   Sérpantaðar vörur sem eru fráteknar fyrir tilteknar pantanir.
-   Framleiðslupantanir. Til dæmis er hægt að merkja vörur sem eru framleiddar fyrir og lagaðar að tilteknum pöntunum.

Hægt er að taka birgðir sjálfkrafa frá þegar ný pöntunarlína er stofnuð eða taka birgðir handvirkt frá í einstökum pöntunum. Einnig er hægt að taka frá birgðir á mismunandi sviðum í framleiðsluferli. Aðeins er hægt að taka frá vörur í birgðum. Ekki er hægt að taka frá þjónustu vegna þess að engar birgðir eru á lager. Hægt er að taka frá bæði efnislegar birgðir og birgðir sem eru pantaðar en ekki mótteknar. Ef meira magn er tekið frá en tiltækt er á lager birtist skilaboð um að ekki sé hægt að taka frá svo mikið magn. Síðan er hægt að taka magnið frá samt, frá eða breyta magninu sem er pantað. Hægt er að taka magnið frá eða breyta því. Ef fleiri vörur eru teknar frá en eru til á lager er mismunurinn afgreiddur næst þegar vörurnar eru tiltækar til afhendingar.

## <a name="inventory-reservation-policies"></a>Reglur um birgðafrátekningu
Reglur um birgðafrátekningu eru stillt á **vörulíkanaflokkur **síðunni á **Færibreytur birgða- og vöruhúsakerfis** síðunni og **framleiðslufæribreytur** síðuna.
### <a name="policies-on-the-item-model-groups-page"></a>Reglur á síðunni vörulíkanaflokkur

**Birgðareglur** kafla inniheldur eftirfarandi reglur um frátekningu.
|                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Frátekningarregla**  | **Lýsing**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Dagsetningarstýrt samkvæmt FIFO    | Ef valið er **dagsetningarstýrt með FIFO (fyrst inn - fyrst út)** valkostur er birgðafrátekning stjórnað af röðunardagsetningu samkvæmt FIFO meginreglunni. Runur eru teknar frá samkvæmt fyrstu dagsetningu innhreyfingar afurðar, samkvæmt meginreglu um fyrst inn, fyrst út (FIFO).                                                                                                                                                                                                                                                                       |
| Afturábak frá sendingardagsetningu | Þessi valmöguleiki verður tiltækt ef valkosturinn **dagsetningarstýrt með FIFO (fyrst inn - fyrst út)** hefur verið valinn. Ef **Afturábak frá sendingardagsetningu** er valið, eru birgðir teknar frá afturábak frá umbeðinni sendingardagsetningin samkvæmt reglunni um síðast inn, fyrst út (LIFO). Ef engar innhreyfingar eru tiltækar fyrir sendingardagsetningm, er FIFO frátekning notuð.                                                                                                                                                                                                           |
| Frátekning vörusölu  | Ákvarðar hvort frátekning á vöru sé sjálfvirk eða handvirk. Ef frátekning er Sjálfvirk, eru birgðir teknar frá þegar pantanalínur eru stofnaðar. Hægt er að gera frátekningar á stigi vörunúmers fyrir Uppskriftir (**Sjálfvirka** valkost), eða fyrir einstakar einingar uppskriftar (**Niðurbrot** valkost). Sjálfgefið gildi fyrir **Vöru frátekning vörusölu** gæti erfast frá **Færibreytur viðskiptakrafna.** Á þeirri síðu er gildið sett í svæðið Frátekning á **sjálfgildi Sölu****hluta** á á **Almennt** flipa. |
| Val á sömu runu    | Frátekning í sömu runu gerir kleift að taka frá birgðir fyrir sölupöntunarlínu gagnvart einni runu birgða. Ef óskað er að nota þennan valkost verður einnig að stilla **Sameina kröfu** valkostinn á **Já**. Frekari stillingar eru nauðsynleg til að rekja rakningarvíddarflokk og geymsluvíddaflokk. Frekari upplýsingar eru í [Taka frá sömu runu fyrir sölupöntun](../sales-marketing/reserve-same-batch-sales-order.md).                                                          |
| Sameina kröfu | Þessi valkostur er svipuð og í **Sama runuval** valkostur og það sameinar birgðir sem eru teknar frá fyrir sölupöntunarlínur í eina kröfu.                                                                                                                                                                                                                                                                                                                                                                                      |
| Dagsetningarstýrt samkvæmt FEFO    | Þessi valkostur gerir mögulegt að taka frá runur sem er nálægt þeirra lokadagur eða fyrningardagsetning. Einnig þarf að stilla **Tiltektarskilyrði** svæðið til að velja annað hvort **lokadagur** eða **fyrningardagsetning**.                                                                                                                                                                                                                                                                                                                              |

#### <a name="example-for-fifo-date-controlled-and-backward-from-ship-date"></a>Dæmi um FIFO dagsetningarstýrt og Afturábak frá sendingardagsetningu

Í þessu dæmis eru lagerbirgðir fyrir vörunúmer A til staðar fyrir þrjár mismunandi rununúmer.
| Vörunúmer | Rununúmer | Magn | Dagsetning             |
|-------------|--------------|----------|------------------|
| Lista fyrir           | 1000         | 5        | 2. febrúar 2016 |
| Lista fyrir           | 1001         | 3        | 1. janúar 2016  |
| Lista fyrir           | 1002         | 7        | 3. mars, 2016    |

Sölupöntun sem á að vera tekin frá sjálfkrafa og afhent 4. aprí 2016, tekur eftirfarandi runu frá:
-   Ef bæði **dagsetningarstýrt FIFO** og **Afturábak frá sendingardagsetningu** gátreitir eru hreinsaðir, er runa 1000 tekin frá þar sem það er runan með lægstu töluna.
-   Ef **dagsetningarstýrt FIFO** gátreitur og **Afturábak frá sendingardagsetningu** gátreitiur eru hreinsaðir, er runa 1001 tekin frá þar sem það er runan með fyrstu viðtökudagur (FIFO).
-   Ef bæði **dagsetningarstýrt FIFO** og **Afturábak frá sendingardagsetningu** gátreitir eru valdir, er runa 1002 tekin frá þar sem það er runan með viðtöku sem er hvað næst sendingardagsetningu sölupöntunar.

### <a name="policies-on-the-inventory-and-warehouse-management-parameter-page"></a>Reglur á síðunni færibreytur birgða- og vöruhúsakerfis

Það eru tveir valmöguleikar tengdir frátekningar á **færibreytur birgða- og vöruhúsakerfis** síðuna:
-   Valkosturinn **taka frá pantaðar vörur** á flipanum **almennt** gerir þér kleift að taka frá vöruinnhreyfingar sem eru pantaðar á móti vöruúthreyfingum í Viðskiptakröfum, Verkefnastjórnun og bókhald og Framleiðslustýringu. Ef þessi valkostur er hreinsaður verður aðeins hægt að taka frá vörur sem hafa verið efnislega mótteknar. Ef tiltekin vara hefur verið sett þannig upp að hún samþykki neikvæðar birgðir skiptir þessi reitur ekki máli.
-   **Taka vörur frá sjálfkrafa** valkostinn á **Flutningi** flipanum ákvarðar sjálfgefnar stillingar ef vörum er tekið sjálfvirkt frá fyrir flutningspöntun. Sjálfgefin stilling er hægt að hnekkja í einstökum flutningspantanir.

### <a name="inventory-reservation-policies-on-the-production-parameters-page"></a>Reglur um birgðafrátekningu á síðunni færibreytur framleiðslu

Gildi reitsins **Frátekning** á **Almennar** flipanum á **framleiðslufæribreytur** síðuna ákvarðar sjálfgefið stað í framleiðsluferlinu þar sem á að taka frá birgðir. Til dæmis, mætti taka frá birgðir þegar vinnu er áætluð, eða þegar vinna er byrjuð.


