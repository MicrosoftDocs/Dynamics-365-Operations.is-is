---
title: Atburðarás framleiðslutafir
description: Þessi grein lýsir atburðarás framleiðslutafir, sem býr til tilkynningu ef framleiðsluafköst fer niður fyrir tiltekið viðmiðunargildi.
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
ms.openlocfilehash: 073762581d84646ba12b570e57327b7cab8efd3b
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9429000"
---
# <a name="the-production-delays-scenario"></a>Atburðarás framleiðslutafir

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

The *framleiðslutafir* atburðarás myndar tilkynningu ef framleiðsluafköst fer niður fyrir tiltekið viðmiðunargildi. Í þessari atburðarás, a *hluta út* merki er sent til Microsoft Azure IoT Hub fyrir hvern hlut sem er framleiddur. Í Dynamics 365 Supply Chain Management, pöntunartöfin er reiknuð út frá þeim tíma sem framleiðslupöntunin á að keyra, fjölda vara sem ætti að framleiða, tíma sem verkið hefur verið í gangi og fjölda *hluta út* merki sem hafa borist. Tilkynning um seinkun myndast ef fjöldi *hluta út* merki um starfið fer undir viðmiðunarmörk.

## <a name="scenario-dependencies"></a>Ósjálfstæði sviðsmynda

The *framleiðslutafir* atburðarás hefur eftirfarandi ósjálfstæði:

- Aðeins er hægt að virkja viðvörun ef framleiðslupöntun er keyrð á varpaðri vél.
- Merki sem táknar kortlagða vél *hluta út* merki verður að senda til IoT Hub og einstakt eignarheiti verður að fylgja með.
- UNIX tímastimpils eiginleiki, þar sem gildin eru sýnd í millisekúndum (ms), verður að vera til staðar í skilaboði Azure IoT Hub.

## <a name="prepare-demo-data-for-the-product-delays-scenario"></a>Undirbúa kynningargögn fyrir tafir á vöru

Ef þú vilt nota kynningarkerfi til að prófa *framleiðslutafir* atburðarás, notaðu kerfi þar sem [kynningargögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) er uppsett skaltu velja *USMF* lögaðila (fyrirtæki), og undirbúa viðbótar kynningargögn eins og lýst er í þessum hluta. Ef þú ert að nota þína eigin skynjara og gögn geturðu sleppt þessum hluta.

### <a name="set-up-sensor-simulator"></a>Settu upp skynjarahermi

Ef þú vilt prófa þessa atburðarás án þess að nota líkamlegan skynjara geturðu sett upp hermi til að búa til nauðsynleg merki. Fyrir frekari upplýsingar, sjá [Settu upp herma skynjara til að prófa](sdi-set-up-simulated-sensor.md).

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>Staðfestu að tilföng 3118 sé notuð fyrir vöru P0111

Framleiðslupöntun verður áætluð og gefin út. Þess vegna losnar framleiðsluverk til tilföngs *3118* (*Froðuskurðarvél*). Fylgdu þessum skrefum til að staðfesta það tilfang *3118* er notað fyrir vöru *P0111* í kynningargögnunum þínum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Finndu og veldu vöruna þar sem **Vörunúmer** reiturinn er stilltur á *P0111*.
1. Á aðgerðarrúðunni, á **Verkfræðingur** flipa, í **Útsýni** hópur, veldu **Leið**.
1. Á **Leið** síðu, á **Yfirlit** flipann neðst á síðunni, veldu línuna þar sem **Óper. Nei.** Reiturinn er stilltur á *30*.
1. Á **Auðlindaþörf** flipann neðst á síðunni, vertu viss um að tilföngin *3118* (*Froðuskurðarvél*) tengist aðgerðinni.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Stofna og gefa út framleiðslupöntun fyrir vöru P0111

Fylgdu þessum skrefum til að stofna og gefa út framleiðslupöntun fyrir vöru *P0111*.

1. Fara í **Framleiðslustýringar \> Framleiðslupantanir \> Allar framleiðslupantanir**.
1. Á **Allar framleiðslupantanir** síðu, á aðgerðarrúðunni, veldu **Ný lotupöntun**.
1. Í **Búðu til lotu** valmynd, stilltu eftirfarandi gildi:

    - **Vörunúmer:** *P0111*
    - **Magn:** *10*

1. Veldu **Búa til** til að búa til pöntunina og fara aftur í **Allar framleiðslupantanir** síðu.
1. Nota **Sía** reit til að leita að framleiðslupöntunum þar sem **Vörunúmer** reiturinn er stilltur á *P0111*. Finndu síðan og veldu framleiðslupöntunina sem þú varst að búa til.
1. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Uppsetning**, skal velja **Áætla**.
1. Í **Áætlun** valmynd, veldu **Allt í lagi** til að keyra matið.
1. Á aðgerðarrúðunni, á **Framleiðslupöntun** flipa, í **Ferli** hópur, veldu **Gefa út**.
1. Í **Gefa út** í glugganum skaltu skrifa niður númer lotupöntunarinnar sem þú bjóst til.
1. Veldu **Allt í lagi** að gefa út pöntunina.

### <a name="configure-the-production-floor-execution-interface"></a>Grunnstilla viðmót fyrir framkvæmd á framleiðslugólfi

Ef þú hefur ekki þegar gert það skaltu stilla framkvæmdarviðmót framleiðslugólfs til að sýna verk sem eru úthlutað til tilföngs *3118* (*Froðuskurðarvél*). Fyrir leiðbeiningar, sjá eftirfarandi kafla:

- [Grunnstilla viðmót fyrir framkvæmd á framleiðslugólfi](sdi-scenario-equipment-downtime.md#config-pfe)
- [Virkjaðu leitarmöguleika á framkvæmdarviðmóti framleiðslugólfs](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>Byrjaðu fyrsta verkið í runupöntuninni

Fylgdu þessum skrefum til að hefja fyrsta verkið í runupöntuninni.

1. Farið í **Framleiðslustýring \> Framkvæmd framleiðslu \> Framkvæmd á framleiðslugólfi**.
1. Í **Merki auðkenni** reit, slá inn *123*. Veldu síðan **skrá inn**.
1. Ef þú ert beðinn um fjarvistarástæðu skaltu velja eitt af kortunum fyrir fjarveru og síðan velja **Allt í lagi**.
1. Í **Leita** reit, sláðu inn lotupöntunarnúmerið sem þú skráðir áður. Veldu síðan **Til baka** lykill.
1. Veldu pöntunina og veldu síðan **Byrja starf**.
1. Í **Byrja starf** valmynd, veldu **Byrjaðu**.

## <a name="set-up-the-production-delays-scenario"></a>Settu upp atburðarás framleiðslutafa

Fylgdu þessum skrefum til að setja upp *framleiðslutafir* atburðarás í Supply Chain Management.

1. Fara til **Framleiðslueftirlit \> Uppsetning \> Sensor Data Intelligence \> Sviðsmyndir**.
1. Í **Framleiðslutafir** atburðarás kassi, veldu **Stilla** til að opna uppsetningarhjálpina fyrir þessa atburðarás.
1. Á **Skynjarar** síðu, veldu **Nýtt** til að bæta skynjara við ristina. Stilltu síðan eftirfarandi reiti fyrir það:

    - **Auðkenni skynjara** – Sláðu inn auðkenni skynjarans sem þú ert að nota. (Ef þú ert að nota Raspberry PI Azure IoT Online Simulator og hefur sett hann upp eins og lýst er í [Settu upp herma skynjara til að prófa](sdi-set-up-simulated-sensor.md), koma inn *FramleiðsluTöf* .)
    - **Lýsing á skynjara** – Sláðu inn lýsingu á skynjaranum.

1. Endurtaktu fyrra skref fyrir hvern viðbótarskynjara sem þú vilt bæta við núna. Þú getur komið aftur og bætt við fleiri skynjurum hvenær sem er.
1. Veljið **Næst**.
1. Á **Kortlagning viðskiptaskráa** síðu, í **Skynjarar** kafla, veldu skrána fyrir einn af skynjurunum sem þú varst að bæta við.
1. Í **Kortlagning viðskiptaskráa** kafla, veldu **Nýtt** til að bæta línu við ristina.
1. Á nýju röðinni, stilltu **Viðskiptaskrá** til auðlindarinnar sem þú notar valinn skynjara til að fylgjast með. (Ef þú ert að nota kynningargögnin sem þú bjóst til fyrr í þessari grein, stilltu þau á *3118, Froðuskurðarvél* .)
1. Veljið **Næst**.
1. Á **Fráviksþröskuldur framleiðslutöf** síðu, ef þú ert að nota kynningargögnin sem þú bjóst til fyrr í þessari grein, fylgdu þessum skrefum:

    1. Veldu **Atriðatengsl** dálkfyrirsögn til að opna fellivalglugga sem inniheldur leitarsíur fyrir dálkinn. Koma inn *P0111* í leitarreitnum og veldu síðan **Sækja um**.
    2. Veldu línuna þar sem **Aðgerð** reiturinn er stilltur á *Klippa/klippa*. Stilltu **Tilkynningaþröskuldur fyrir seinkun (%)** reit að þröskuldinum (sem hlutfall) sem tilkynning ætti að senda á.

1. Veljið **Næst**.
1. Á **Virkjaðu skynjara** síðu, í hnitanetinu, veldu skynjarann sem þú bættir við og veldu síðan **Virkjaðu**. Fyrir hvern virkan skynjara í ristinni birtist gátmerki í **Virkur** dálki.
1. Veljið **Ljúka**.

## <a name="work-with-the-production-delays-scenario"></a>Vinna með framleiðslutafir atburðarás

### <a name="view-production-delay-data-on-the-resource-status-page"></a>Skoðaðu gögn um framleiðslutafir á síðunni Tilfangsstaða

Á **Auðlindastaða** síðu geta umsjónarmenn fylgst með tímalínu merkja sem berast frá skynjurum sem eru kortlagðar á hverja vélaauðlind. Fylgdu þessum skrefum til að stilla tímalínuna.

1. Fara til **Framleiðslueftirlit \> Framleiðsluframkvæmd \> Auðlindastaða**.
1. Í **Stilla** valmynd, stilltu eftirfarandi reiti:

    - **Auðlind** - Veldu úrræði sem þú vilt fylgjast með. (Ef þú ert að vinna með kynningargögnin skaltu velja *3118* .)
    - **Tímaröð 1** – Veldu færsluna (mælingarlykill) sem hefur eftirfarandi snið fyrir nafnið: *Framleiðslustarf seinkað: Raunverulegt magn:&lt; JobId&gt;*
    - **Birta nafn** - Koma inn *Hlutar út merki*.
