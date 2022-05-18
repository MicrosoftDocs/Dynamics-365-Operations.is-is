---
title: Uppsetning á aðstæðum fyrir IoT gervigreind
description: Þetta efnisatriði útskýrir hvernig á að skilgreina atburðarásir fyrir IoT-gervigreind í Microsoft Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dddc282ef3e479d524b1dfa0c60091cad1c231e0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675178"
---
# <a name="scenario-setup-for-iot-intelligence"></a>Uppsetning á aðstæðum fyrir IoT gervigreind

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að skilgreina atburðarásir fyrir IoT-gervigreind í Microsoft Dynamics 365 Supply Chain Management. <!-- KFM: Hide setup info for now: Before you can set up the scenarios, you must [set up Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md). -->

Í þessu efnisatriði er hægt að skilgreina aðstæðurnar **Niðurtími búnaðar** þannig að tilkynning er búin til í Supply Chain Management þegar vél verður óvirk. Í efnisatriðinu er einnig sýnt hvernig á að skilgreina aðstæðurnar **Gæði afurðar** þannig að tilkynning er búin til ef eigind vöru er utan tiltekins sviðs og hvernig á að skilgreina aðstæðurnar **Tafir á framleiðslu** þannig að tilkynning er búin til ef gegnumstreymi framleiðslunnar fellur undir þröskuldsgildi.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Skilgreina Niðurtími búnaðar aðstæður í Supply Chain Management

Aðstæðurnar **Niðurtími búnaðar** varpa **PartOut** merki til viðvörunarþröskulds vélar. Aðeins er fylgst með vélinni þegar hún er valin fyrir aðstæðurnar og hún er stillt á **Keyrslu** í Supply Chain Management. Ef tíminn frá því að **PartOut** merki sem síðast var móttekið frá vélinni fer yfir viðvörunarþröskuldinn kviknar á tilkynningunni **Vél niðri**. Ef vél er enn í gangi kviknar á **Vél virk** tilkynningu þegar næsta **PartOut** merki er móttekið. Ef vél er óvirk í 30 mínútur ræsist ný tilkynning um **Vél niðri**.

**Niðurtími búnaðar** aðstæðurnar hafa eftirfarandi tengsl:

+ Aðeins er hægt að virkja viðvörun ef framleiðslupöntun er keyrð á varpaðri vél.
+ Merki sem stendur fyrir **PartOut** merki merktrar vélar, verður að vera send til IoT-miðstöðvarinnar og einkvæmt heiti eiginleika verður að vera innifalið.
+ UNIX **tímastimpils** eiginleiki, þar sem gildin eru sýnd í millisekúndum (ms), verður að vera til staðar í skilaboði Azure IoT Hub.

Til að skilgreina aðstæðurnar skaltu fylgja þessum skrefum.

1. Skráðu þig inn í Supply Chain Management.
2. Virkja eiginleikaflaggið IoT-gervigreind. Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Skilgreinið mælingarnar. Frekari upplýsingar eru í [Hvernig skal skilgreina mælingar](iot-metrics-setup.md#configure-metrics).
4. Farðu í **Framleiðslustýring \> Uppsetning \> IoT-gervigreind \> Stjórnun aðstæðna**.
6. Í reitnum **Niðurtími búnaðar** skal velja **Skilgreina** til að opna leiðsagnarforrit skilgreiningarinnar.

   Fyrsta síða í leiðsagnarforritinu er síðan **Skilgreining á skema fyrir skynjunarbúnað**. Á þessari síðu er markmið þitt að setja upp skema í Supply Chain Management þannig að það passi við JavaScript Object Notation-snið (JSON) í skilaboðum IoT Hub. Hægt er að skilgreina mörg skilaboðaskema. Frekari upplýsingar er að finna í [Snið skemu fyrir skilaboð IoT Hub](iot-schema-format.md). Í þessu dæmi felur innihald skilaboðanna í sér runu af skilaboðum sem eru á eftirfarandi sniði.

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

7. Bætið línu við töfluna og stillið eftirfarandi gildi:

    1. Stillið reitinn **Heiti skema** á **Kenni**.
    2. Stillið reitinn **Slóð skema** á **/innihald\[\*\]/kenni**.
    3. Stillið reitinn **Lýsing** á **Skilaboðakenni**.

8. Bæta annarri línu við töfluna og stilla eftirfarandi gildi:

    1. Stillið reitinn **Heiti skema** á **Tímastimpill**.
    2. Stillið **Slóð skema** á **/innihald\[\*\]/tímastimpill**.
    3. Stillið reitinn **Lýsing** á **Tímastimpill skilaboða**.

9. Bæta annarri línu við töfluna og stilla eftirfarandi gildi:

    1. Stillið reitinn **Heiti skema** á **Gildi**.
    2. Stillið reitinn **Slóð skema** á **/innihald\[\*\]/gildi**.
    3. Stillið reitinn **Lýsing** á **Gildi skilaboða**.

    > [!NOTE]
    > Ekki þarf að skilgreina alla eiginleikana í skilaboðunum. Skilgreina aðeins eiginleikana sem eru nauðsynlegir. Í skrefunum á undan var ekki stofnuð lína fyrir **Tímastimpil rótar**. Slóðin fyrir **Tímastimpil rótar** væri **/tímastimpill**.

10. Veljið **Áfram** til að fara á síðuna **Skemavörpun á skynjunarbúnaði**.
11. Í línunni fyrir **Tilfangakenni búnaðar**, í reitnum **Heiti skema**, skal velja **Kenni**.
12. Í línunni fyrir **UTC-tími**, í reitnum **Heiti skema**, skal velja **Tímastimpill**.
13. Í línunni fyrir **Framleiðslumerki hlutar** skal stilla **Heiti skema** á **Gildi**.
14. Veljið **Næst** til að fara á síðuna **Skilgreining á tilfangakenni búnaðar**.
15. Fylgið eftirfarandi skrefum til að varpa gildunum úr skilaboðum IoT Hub yfir í tilföng Supply Chain Management:

    1. Í töflunni **Gagnagildi merkis** skal bæta við nýrri línu. Í reitinn **Gildi** skal færa inn **IoTInt.Machine1225.PartOut**. Þetta gildi kemur frá JSON-eiginleikanum **kenni** í skilaboðum IoT-miðstöðvar.
    2. Veljið **Vista**.
    3. Í töflunni **Vörpun viðskiptafærslu** skal velja **Nýtt**. Sjálfgefið gildi fyrir **Gerð viðskiptafærslu** er sjálfkrafa fyllt út og ekki þarf að breyta því.
    4. Í dálkinum **Viðskiptafærsla** skal velja tilfang vélar Supply Chain Management sem þetta merkjagildi er sent frá.
    5. Veljið **Vista**.
    6. Endurtekið þessi skref til að bæta við nýrri viðskiptafærsluvörpun fyrir **Machine1226**. Hægt er að varpa mörgum gagnagildum merkis í eina færslu í Supply Chain Management.

16. Notið dálkinn **Valið** til að velja hvaða vélar á að vinna með. Ekki þarf að skilgreina öll merkjagildi og ekki þarf að velja allar vélar.
17. Veljið **Áfram** til að fara á síðuna **Grunnstilling framleiðslumerkis hlutar**.
18. Í töflunni **Gagnagildi merkis** skal bæta við línu og stilla reitinn **Gildi** á **Satt**. Þetta gildi kemur frá JSON-eiginleikanum **gildi** í skilaboðum IoT-miðstöðvar. Hægt er að bæta við eins mörgum gildum og nauðsynlegt er fyrir aðstæðurnar.
19. Veljið **Vista**.
20. Veljið **Áfram** til að opna síðuna **Niðurtímaþröskuldur búnaðar**. Vélarnar sem taldar eru upp eru vélarnar sem var varpað áður á merkjagildi. Á þessari síðu eru mörk skilgreind til að ákvarða hvort vél er niðri. Til dæmis ef þröskuldur er stilltur á **10** býr Supply Chain Management til tilkynningu ef ekkert **PartOut** merki er móttekið frá vél í 10 mínútur.
21. Veljið **Áfram** til að fara á síðuna **Virkja aðstæður**. Stillið valkostinn til að virkja aðsmengitæðurnar.
22. Veljið **Ljúka**.

Uppsetning aðstæðna er nú lokið. IoT-gervigreind hefst sjálfkrafa handa við að vinna úr skilaboðum IoT Hub.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Skilgreina Gæði afurðar aðstæður í Supply Chain Management

**Gæði afurðar** aðstæður myndar tilkynningu ef eigind vöru er utan tiltekins sviðs. Til dæmis sendir skynjari þyngd hverrar vöru til IoT-miðstöðvar. Ef vara er of þung eða of létt er tilkynning búin til í Supply Chain Management.

Aðstæðurnar **Gæði afurðar** eru háðar eftirfarandi:

+ Viðvörun getur aðeins verið ræst ef framleiðslupöntun er keyrð á varpaðri vél og framleiðir afurð sem er með varpaða runueigind.
+ Merki sem stendur fyrir runueigindina verður að vera send til IoT-miðstöðvar og einkvæmt heiti eiginleika verður að fylgja.
+ UNIX **tímastimpils** eiginleiki, þar sem gildið er sýnt í millisekúndum, verður að vera til staðar í skilaboði Azure IoT Hub.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Skilgreina Framleiðslutafir aðstæður í Supply Chain Management

**Framleiðslutafir** aðstæður myndar tilkynningu ef gegnumstreymi framleiðslu fellur undir þröskuldsgildi. Í þessum aðstæðum er **PartOut** merki sent til IoT-miðstöðvar fyrir hverja vöru sem er framleidd. Í Supply Chain Management eru framleiðslutafir reiknaðar út frá tímanum sem áætlað er að framleiðslupöntunin taki, fjölda vara sem á að framleiða, tímanum sem vinnslan hefur verið í gangi og fjölda **PartOut** merkja sem eru móttekin. Tilkynning um tafir er mynduð ef númerið á **PartOut** merkjum fyrir vinnsluna fellur undir þröskuldsgildi væntanlegs gildis.

Aðstæðurnar **Tafir á framleiðslu** eru háðar eftirfarandi:

+ Aðeins er hægt að virkja viðvörun ef framleiðslupöntun er keyrð á varpaðri vél.
+ Merki sem stendur fyrir **PartOut** merki merktrar vélar, verður að vera send til Azure IoT-miðstöðvarinnar og einkvæmt heiti eiginleika verður að vera innifalið.
+ UNIX **tímastimpils** eiginleiki, þar sem gildið er sýnt í millisekúndum, verður að vera til staðar í skilaboði Azure IoT Hub.

## <a name="disable-a-scenario"></a>Gera aðstæður óvirkar

Til að gera aðstæður óvirkar skal fylgja eftirfarandi skrefum.

1. Í Supply Chain Management er farið í **Framleiðslustýring \> Uppsetning \> IoT-gervigreind \> Stjórnun aðstæðna**.
2. Á svæðinu fyrir aðstæðurnar skal velja **Skilgreina**.
3. Veljið **Næst** til að fara á síðustu leiðsagnarsíðuna.
4. Stillið valkostinn til að slökkva á aðstæðunum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]