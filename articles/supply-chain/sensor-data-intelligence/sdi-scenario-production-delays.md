---
title: Aðstæður fyrir framleiðslutöf
description: Þessi grein útskýrir aðstæður framleiðslutafa sem myndar tilkynningu ef gegnumstreymi framleiðslu fellur undir tiltekið þröskuldsgildi.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 25ccbda1628544f14dc32d9bea3f2162ad47d79e
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690022"
---
# <a name="the-production-delays-scenario"></a>Aðstæður fyrir framleiðslutöf

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

*Framleiðslutafir* aðstæður myndar tilkynningu ef gegnumstreymi framleiðslu fellur undir tiltekið þröskuldsgildi. Í þessum aðstæðum er *hluti-út* merki sent til Microsoft Azure IoT-miðstöðvar fyrir hverja vöru sem er framleidd. Í Dynamics 365 Supply Chain Management eru framleiðslutafir reiknaðar út frá tímanum sem áætlað er að framleiðslupöntunin taki, fjölda vara sem á að framleiða, tímanum sem vinnslan hefur verið í gangi og fjölda *hluti-út* merkja sem eru móttekin. Tilkynning um tafir er mynduð ef númerið á *hluti-út* merkjum fyrir vinnsluna fellur undir þröskuldsgildi væntanlegs gildis.

## <a name="scenario-dependencies"></a>Aðstæður tengsl

Aðstæðurnar *Tafir á framleiðslu* eru háðar eftirfarandi:

- Aðeins er hægt að virkja viðvörun ef framleiðslupöntun er keyrð á varpaðri vél.
- Merki sem stendur fyrir merkið *hlutur-út* fyrir vörpuðu vélina verður að vera sent til IoT-Hub og einkvæmt heiti eiginleika verður að vera innifalið.
- UNIX tímastimpils eiginleiki, þar sem gildin eru sýnd í millisekúndum (ms), verður að vera til staðar í skilaboði Azure IoT Hub.

## <a name="prepare-demo-data-for-the-product-delays-scenario"></a>Undirbúa sýnigögn fyrir aðstæður framleiðslutafa

Ef þú vilt nota sýnikerfi til að prófa aðstæður *framleiðslutafir* skaltu nota kerfi þar sem [sýnigögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) eru sett upp, velja lögaðilann (fyrirtæki) *USMF* og útbúa frekari sýnigögn eins og lýst er í þessum hluta. Ef þú notar eigin skynjara og gögn geturðu sleppt þessum hluta.

### <a name="set-up-sensor-simulator"></a>Setja upp skynjarahermi

Ef þú vilt prófa þessar aðstæður án þess að nota efnislegan skynjara getur þú sett upp hermi til að búa til nauðsynleg merki. Frekari upplýsingar eru í [Setja upp eftirlíkingarskynjara til prófunar](sdi-set-up-simulated-sensor.md).

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>Staðfestu að tilfang 3118 sé notað fyrir vöruna P0111

Framleiðslupöntun verður tímasett og losuð. Framleiðsluverk er þar af leiðandi losað til tilfangs *3118* (*Svampskurðarvél*). Fylgdu þessum skrefum til að staðfesta að tilfang *3118* sé notað fyrir framleiðslu *P0111* í sýnigögnunum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Finnið og veljið afurðina þar sem reiturinn **Vörunúmer** er stilltur á *P0111*.
1. Á aðgerðasvæðinu, í flipanum **Hönnuður**, í flokknum **Yfirlit**, skal velja **Leið**.
1. Á síðunni **Leið**, á flipanum **Yfirlit** neðst á síðunni, skaltu velja línuna þar sem **Aðg.nr.** reitur er stilltur á *30*.
1. Á flipanum **Tilfangaþarfir** neðst á síðunni skaltu ganga úr skugga um að tilfang *3118* (*Svampskurðarvél*) sé tengd aðgerðinni.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Stofna og gefa út framleiðslupöntun fyrir vöru P0111

Fylgdu eftirfarandi skrefum til að stofna og losa framleiðslupöntun fyrir vöru *P0111*.

1. Fara í **Framleiðslustýringar \> Framleiðslupantanir \> Allar framleiðslupantanir**.
1. Á síðunni **Allar framleiðslupantanir**, á aðgerðasvæðinu, skal velja **Ný runupöntun**.
1. Í svarglugganum **Stofna runu** skal stilla eftirfarandi gildi:

    - **Vörunúmer:** *P0111*
    - **Magn:** *10*

1. Veldu **Stofna** til að stofna pöntunina og fara aftur á síðuna **Allar framleiðslupantanir**.
1. Notið reitinn **Sía** til að leita að framleiðslupöntunum þar sem reiturinn **Vörunúmer** er stilltur á *P0111*. Leitaðu síðan að og veljið framleiðslupöntun sem var verið að stofna.
1. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Uppsetning**, skal velja **Áætla**.
1. Í svarglugganum **Mat** skal velja Í **lagi** til að keyra matið.
1. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Uppsetning**, skal velja **Losa**.
1. Í svarglugganum **Losa** skaltu skrá niður númer runupöntunar sem var verið að stofna.
1. Veldu **Í lagi** til að losa pöntunina.

### <a name="configure-the-production-floor-execution-interface"></a>Grunnstilla viðmót fyrir framkvæmd á framleiðslugólfi

Ef þú hefur ekki þegar gert það, stilltu þá viðmót fyrir framkvæmd á framleiðslugólfi til að sýna verk sem eru úthlutuð tilfangi *3118* (*Svampskurðarvél*). Frekari leiðbeiningar er að finna í eftirfarandi köflum:

- [Grunnstilla viðmót fyrir framkvæmd á framleiðslugólfi](sdi-scenario-equipment-downtime.md#config-pfe)
- [Virkja leitarvalkost á viðmót fyrir framkvæmd á framleiðslugólfi](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>Ræsið fyrsta verk runupöntunina

Fylgið eftirfarandi skrefum til að hefja fyrsta verkið í runupöntuninni.

1. Farið í **Framleiðslustýring \> Framkvæmd framleiðslu \> Framkvæmd á framleiðslugólfi**.
1. Í reitnum **Kortkenni** slærðu inn *123*. Veljið síðan **Innskráning**.
1. Þegar beðið er um ástæðu fjarveru skaltu velja eitt af spjöldunum fyrir fjarveru og velja svo **Í lagi**.
1. Í reitnum **Leita** er slegið inn lotunúmer pöntunar sem þú skrifaðir áður niður hjá þér. Veldu síðan **færslulykilinn**.
1. Smelltu á pöntunar og veldu síðan **Hefja vinnslu**.
1. Í svarglugganum **Hefja vinnslu** velurðu **Ræsa**.

## <a name="set-up-the-production-delays-scenario"></a>Setja upp aðstæður fyrir framleiðslutöf

Fylgdu þessum skrefum til að setja *tafir á framleiðslu* aðstæður í Supply Chain Management.

1. Farðu í **Framleiðslustýring \> Uppsetning \> Gervigreind skynjaragagna \> Aðstæður**.
1. Í aðstæðureitnum **Tafir á framleiðslu** skaltu velja **Stilla** til að opna leið fyrir þessar aðstæður.
1. Á síðunni **Skynjarar** skal velja **Nýtt** til að bæta skynjara við hnitanetið. Stillið svo eftirfarandi reiti fyrir það:

    - **Auðkenni skynjara** – Sláðu inn kenni skynjarans sem þú ert að nota. (Ef þú notar Raspberry PI Azure IoT Online Simulator og hefur sett það upp eins og lýst er í [Setja upp eftirlíkingarskynjara til prófunar](sdi-set-up-simulated-sensor.md), sláðu inn *ProductionDelay*.)
    - **Lýsing á skynjara** – Færið inn lýsingu á skynjari.

1. Endurtaka á fyrra skref fyrir hvern skynjara sem þú vilt bæta við. Hægt er að koma aftur og bæta við fleiri skynjurum hvenær sem er.
1. Veljið **Næst**.
1. Á síðunni **Vörpun viðskiptafærslu**, í hlutanum **Skynjarar**, skaltu velja færslu fyrir einn af skynjurunum sem þú varst að bæta við.
1. Í hlutanum **Vörpun viðskiptafærslu** skal velja **Ný** til að bæta línu við hnitanetið.
1. Á nýju línunni, stilltu **Viðskiptafærsla** á tilfangið sem þú notar valinn skynjara til að fylgjast með. (Ef þú notar sýnigögnin sem þú bjóst til fyrr í þessari grein skaltu stilla þau *á 3118, svampskurðarvél*.)
1. Veljið **Næst**.
1. Á síðunni **Þröskuldur fyrir frávik framleiðslutafa**, ef þú notar sýnigögnin sem voru búin til fyrr í þessari grein, skaltu fylgja þessum skrefum:

    1. Veldu dálkahausinn **Vöruvensl** til að opna fellilistann sem inniheldur leitarsíur fyrir dálkinn. Færið inn *P0111* í leitargluggann og veldu svo **Nota**.
    2. Veldu línuna þar sem reiturinn **Aðgerð** er stilltur á *Klippa*. Stilltu reitinn **Tilkynningarþröskuldur fyrir töf (%)** á þröskuldinn (sem prósenta) sem senda á tilkynningu við.

1. Veljið **Næst**.
1. Á síðunni **Virkja skynjara**, í hnitanetinu, veldu skynjarann sem þú bættir við og veldu síðan **Virkja**. Fyrir hvern virkan skynjara í hnitanetinu birtist gátmerki í dálkinum **Virkur**.
1. Veljið **Ljúka**.

## <a name="work-with-the-production-delays-scenario"></a>Vinna með aðstæður framleiðslutafa

### <a name="view-production-delay-data-on-the-resource-status-page"></a>Skoða gögn um framleiðslutafir á síðu tilfangastöðu

Á síðunni **Staða tilfanga** geta eftirlitsaðilar fylgst með merkjum sem tekið er við frá skynjurunum sem er varpað á hvert tilfang vélarinnar. Fylgja skal þessum skrefum til að skilgreina tímalínu.

1. Farið í **Framleiðslustýring \> Framkvæmd framleiðslu \> Staða tilfanga**.
1. Í svarglugganum **Skilgreina** skal stilla eftirfarandi reiti:

    - **Tilfang** – Veldu tilföngin sem á að fylgjast með. (Ef þú ert að vinna með sýnigögnin skaltu velja *3118*).
    - **Tímaröð 1** – Veldu færslu (mælieiningarlykil) sem hefur eftirfarandi snið fyrir heiti sitt: *ProductionJobDelayed:ActualQuantity:&lt;JobId&gt;*
    - **Birtingarheiti** – Færðu inn *Merki um hluti út*.
