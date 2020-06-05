---
title: Uppsetning á aðstæðum fyrir IoT gervigreind
description: Þetta efnisatriði lýsir því hvernig skilgreina á aðstæður í Supply Chain Management fyrir IoT-gervigreind.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b87a9b73f49e73fe13b98fb11da939c9b30e0f6e
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386526"
---
# <a name="scenario-setup-for-iot-intelligence"></a>Uppsetning á aðstæðum fyrir IoT gervigreind

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig skilgreina á aðstæður í Supply Chain Management fyrir IoT-gervigreind. Áður en hægt er að setja upp aðstæðurnar þarf að [setja upp LCS](iot-lcs-setup.md).

Í þessu efnisatriði er hægt að skilgreina aðstæðurnar **Niðurtími búnaðar** til að mynda tilkynningu í Supply Chain Management þegar vél verður óvirk.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Skilgreina **Niðurtími búnaðar** aðstæður í Supply Chain Management

**Niðurtími búnaðar** aðstæður varpar merki fyrir hlut út í viðvörunarþröskuldi vélar. Aðeins er fylgst með vélum þegar vél er valin fyrir aðstæðurnar og hún er stillt á að keyra í Supply Chain Management. Ef tíminn frá því að vélin síðast tók við merki fyrir hlut út er meiri en viðvörunarþröskuldurinn, þá er **Vél óvirk** tilkynning ræst. Ef vél er enn í gangi, þegar næsta **hlutur út** merki hefur borist er **Vél virk** tilkynning ræst. Ef vél er óvirk í 30 mín er ný **Vél óvirk** tilkynning ræst.

**Niðurtími búnaðar** aðstæðurnar hafa þessi tengsl:

+ Framleiðslupöntun verður að vera í vinnslu á varpaðri vél til að viðvörun sé ræst.
+ Merki sem stendur fyrir merki varpaðrar vélar fyrir hlut út verður að senda á IoT-miðstöð með einkvæmu heiti eiginleika.
+ Unix-millisekúndutímastimpill verður að vera til staðar í skilaboðum IoT miðstöðvar.

Til að skilgreina aðstæðurnar skaltu fylgja þessum skrefum:

1. Skrá inn á Supply Chain Management.
2. Virkja eiginleikaflaggið IoT-gervigreind. Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Skilgreinið mælingarnar. Frekari upplýsingar eru í [Hvernig skal skilgreina mælingar](iot-metrics-setup.md#configure-metrics).
4. Farið í **Framleiðslustýring**.
5. Farið í **Uppsetning \> IoT-gervigreind \> Stjórnun aðstæðna**.
6. Smellið á **Grunnstilla** á reitnum **Niðurtími búnaðar**. Skilgreiningarforritið byrjar á síðunni **Skilgreining á skema fyrir skynjunarbúnað**. Markmiðið hér er að setja upp skema í Supply Chain Management til að samsvara JSON-sniði IoT skilaboða. Hægt er að skilgreina mörg skilaboðaskema. Frekari upplýsingar er að finna í [Snið skilaboðaskema fyrir IoT-miðstöð](iot-schema-format.md). Í þessu dæmi er inniheldur innihald skilaboða runu skilaboða með þessu sniði:

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. Bæta línu við töfluna.

    1. Stillið **Heiti skema** á **Kenni**.
    2. Stillið **Slóð skema** á **/innihald[\*]/kenni**.
    3. Stillið **Lýsing** á **Skilaboðakenni**.

8. Bæta línu við töfluna.

    1. Stillið **Heiti skema** á **Tímastimpill**.
    2. Stillið **Slóð skema** á **/innihald[\*]/tímastimpill**.
    3. Stillið **Lýsing** á **Tímastimpill skilaboða**.

9. Bæta línu við töfluna.

    1. Stillið **Heiti skema** á **Gildi**.
    2. Stillið **Slóð skema** á **/innihald[\*]/gildi**.
    3. Stillið **Lýsing** á **Gildi skilaboða**.

    Ekki þarf að skilgreina alla eiginleikana í skilaboðunum, aðeins þær sem þörf er á. Í þessu dæmi var ekki stofnuð lína fyrir **Tímastimpill rótar**. Slóðin fyrir **Tímastimpill rótar** væri **/tímastimpill**.
  
10. Smellið á **Áfram** til að fara á síðuna **Skemavörpun á skynjunarbúnaði**.
11. Í línu fyrir **Tilfangakenni búnaðar** skal stilla **Heiti skema** á **Kenni**. Gild gildi eru birt í fellitöflu.
12. Í línunni fyrir **UTC-tími** skal stilla **Heiti skema** á **Tímastimpill**. Gild gildi eru birt í fellitöflu.
13. Í línunni fyrir **Framleiðslumerki hlutar** skal stilla **Heiti skema** á **Gildi**. Gild gildi eru birt í fellitöflu.
14. Smellið á **Áfram** fyrir síðuna **Grunnstilling tilfangakennis búnaðar**.
15. Í þessu skrefi er skeytagildunum á IoT-miðstöð varpað í tilföng Supply Chain Management.

    1. Í töflunni **Gagnagildi merkis** skal bæta við nýrri línu og færa inn **IoTInt.Machine1225.PartOut** í dálknum **Gildi**. Gildið **IoTInt.Machine1225.PartOut** kemur frá eiginleikanum JSON **kenni** í skilaboðum IoT-miðstöðvar.
    2. Smellt er á **Vista**.
    3. Í töflunni **Vörpun viðskiptafærslu** er smellt á **Nýtt**. Sjálfgildi fyrir **Gerð viðskiptafærslu** er útfyllt sjálfkrafa, og óþarfi er að breyta því.
    4. Í dálkinum **Viðskiptafærsla** skal velja aðfangakeðjustjórnun tilfanga vélar sem þetta merkisgildi er sent frá.
    5. Smellt er á **Vista**.
    6. Endurtekið þessi skref og bætið við nýrri viðskiptafærsluvörpun fyrir **Machine1226**. Hægt er að varpa mörgum gagnagildum merkis í eina færslu í Supply Chain Management.

16. Notaðu dálkinn **Valið** til að velja hvaða vélar á að vinna með. Ekki þarf að skilgreina öll merkigildi og ekki þarf að velja allar vélar.
17. Smellið á **Áfram** til að fara á síðuna **Grunnstilling framleiðslumerkis hlutar**.
18. Í töflunni **Gagnagildi merkis** skal bæta við línu og stilla **Gildi** á **Satt**. Gildið **Satt** kemur frá eiginleikanum JSON **gildi** í skilaboðum IoT-miðstöðvar. Hægt er að bæta við eins mörgum gildum og nauðsynlegt er fyrir aðstæðurnar.
19. Smellt er á **Vista**.
20. Smellið á **Áfram** til að opna síðuna **Niðurtímaþröskuldur búnaðar**. Vélarnar sem taldar eru upp eru vélarnar sem áður hafa verið varpað á merki gilda. Í þessu skrefi er þröskuldur skilgreindur til að ákvarða hvort vél er óvirk. Til dæmis ef þröskuldur er stilltur á 10 skal Supply Chain Management mynda tilkynningu ef engin skilaboð um hlut út frá vél hafa verið send í 10 mínútur.
21. Smellið á **Áfram** til að fara á síðuna **Virkja aðstæður**. Víxlið sleðanum til að virkja aðstæðurnar.
22. Smellt er á **Ljúka**.

Uppsetningu aðstæðnanna er lokið. IoT gervigreind ræsir sjálfkrafa vinnslu á skilaboðum IoT-miðstöðvar.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Skilgreina **Gæði afurðar** aðstæður í Supply Chain Management

**Gæði afurðar** aðstæður myndar tilkynningu ef eigind vöru er utan tiltekins sviðs. Til dæmis gæti skynjari sent þyngd hverrar vöru í IoT-miðstöð. Í Supply Chain Management væri mynduð tilkynning ef varan væri of þung eða of létt.

Aðstæðurnar eru með þessi tengsl:

+ Framleiðslupöntun verður að vera í keyrslu á varpaðri vél og framleiða afurð með varpaðri runueigind til að viðvörun verður ræst.
+ Merki sem stendur fyrir runueigind verður að senda á IoT-miðstöð með einkvæmu heiti eiginleika.
+ Unix-millisekúndutímastimpill verður að vera til staðar í skilaboðum IoT miðstöðvar.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Skilgreina **Framleiðslutafir** aðstæður í Supply Chain Management

**Framleiðslutafir** aðstæður myndar tilkynningu ef gegnumstreymi framleiðslu fellur undir þröskuldsgildi. Í þessum aðstæðum er **Hlutur út** merki sent í IoT miðstöð fyrir hverja vöru sem er framleidd. Í Supply Chain Management er pöntunarfrestur reiknaður út frá því hversu lengi framleiðslupöntunin á að keyra, hversu margar vörur á að framleiða, hversu lengi vinnslan hefur verið í gangi og hversu mörg **Hlutur út** merki eru móttekin. Tilkynning um tafir yrði mynduð ef númerið á **Hlutur út** merki fyrir vinnsluna fellur undir þröskuldsgildi væntanlegs gildis.

Aðstæðurnar eru með þessi tengsl:

+ Framleiðslupöntun verður að vera í vinnslu á varpaðri vél til að viðvörun sé ræst.
+ Merki sem stendur fyrir merki varpaðrar vélar fyrir hlut út verður að senda á IoT-miðstöð með einkvæmu heiti eiginleika.
+ Unix-millisekúndutímastimpill verður að vera til staðar í skilaboðum IoT miðstöðvar.

## <a name="how-to-disable-a-scenario"></a>Hvernig á að gera aðstæður óvirkar

Til að gera aðstæður óvirkar skal fylgja eftirfarandi skrefum:

1. Í Supply Chain Management er farið í **Framleiðslustýring \> Uppsetning \> IoT-gervigreind \> Stjórnun aðstæðna**.
2. Smellið á **Grunnstilla** á aðstæðunum.
3. Smellið á **Áfram** til að komast á flipann fyrir síðustu leiðsögn.
4. Víxlið sleðanum til að gera aðstæðurnar óvirkar.
