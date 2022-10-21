---
title: Aðstæður fyrir viðhald eignar
description: Þessi grein lýsir atburðarás eignaviðhalds, sem gerir þér kleift að nota skynjaragögn til að búa til teljaraskrár sem rekja notkun vélaeignar.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2d103406118be4385177b678de424df12af69c2e
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689401"
---
# <a name="the-asset-maintenance-scenario"></a>Aðstæður fyrir viðhald eignar

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

The *viðhald eigna* atburðarás gerir þér kleift að nota skynjaragögn til að búa til teljaraskrár. Mæliskrár rekja notkun vélaeignar og eru notaðar sem inntak til að búa til viðhaldsáætlun fyrir vélaeignir.

## <a name="video-instructions"></a>Vídeóleiðbeiningar

Eftirfarandi myndband sýnir hvernig á að setja upp og prófa viðhaldssviðsmyndina með því að nota staðal [kynningargögn](../../fin-ops-core/fin-ops/get-started/demo-data.md). Hlutarnir sem eftir eru í þessari grein veita sömu leiðbeiningar í textaformi.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58aRW]

## <a name="prepare-demo-data-for-the-asset-maintenance-scenario"></a>Undirbúa kynningargögn fyrir atburðarás eignaviðhalds

Ef þú vilt nota kynningarkerfi til að prófa *viðhald eigna* atburðarás, notaðu kerfi þar sem [kynningargögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) er uppsett skaltu velja *USMF* lögaðila (fyrirtæki), og undirbúa viðbótar kynningargögn eins og lýst er í þessum hluta. Ef þú ert að nota þína eigin skynjara og gögn geturðu sleppt þessum hluta.

Í þessum hluta muntu setja upp *AK-101, lofthnífur* eign í kynningargögnum sem dæmi. Þú munt þá sjá hvernig hægt er að spá fyrir um komandi viðhaldsvinnu út frá skynjaramerkjum sem mæla fjölda klukkustunda sem lofthnífurinn hefur verið í gangi. Þú munt einnig setja upp viðhaldsáætlun þar sem viðhalda þarf lofthnífnum á 10.000 klukkustunda fresti.

### <a name="set-up-a-sensor-simulator"></a>Settu upp skynjarahermi

Ef þú vilt prófa þessa atburðarás án þess að nota líkamlegan skynjara geturðu sett upp hermi til að búa til nauðsynleg merki. Fyrir frekari upplýsingar, sjá [Settu upp herma skynjara til að prófa](sdi-set-up-simulated-sensor.md).

### <a name="create-an-asset-counter-to-track-production-hours"></a>Búðu til eignateljara til að fylgjast með framleiðslutíma

Fylgdu þessum skrefum til að búa til eignateljara til að rekja framleiðslutíma.

1. Opnaðu **Eignastýringu \> Uppsetningu \> Færibreytur eignastýringar \> Teljarar**.
1. Á aðgerðarrúðunni velurðu **Nýtt** að búa til teljara.
1. Stillið eftirfarandi gildi í hausnum:

    - **Teljari:** *FramleiðslaHr*
    - **Nafn:** *Framleiðslutímar*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Eining:** *hr*
    - **Uppfærsla:** *Handbók*
    - **Heildaruppsöfnun:** *Summa*

1. Á **Tegundir eigna** Flýtiflipi, veldu **Bæta við línu**.
1. Á nýju línunni skaltu stilla **Tegund eigna** sviði til *Lofthnífur*.

### <a name="create-a-maintenance-plan-for-the-asset"></a>Búðu til viðhaldsáætlun fyrir eignina

Fylgdu þessum skrefum til að búa til viðhaldsáætlun fyrir eignina.

1. Fara til **Eignastýring \> Uppsetning \> Fyrirbyggjandi viðhald \> Viðhaldsáætlun**.
1. Á aðgerðarrúðunni velurðu **Nýtt** að búa til viðhaldsáætlun.
1. Stillið eftirfarandi gildi í hausnum:

    - **Viðhaldsáætlun:** *AirKnife*
    - **Nafn:** *Skipuleggðu lofthnífa*

1. Í flýtiflipanum **Upplýsingar** skal stilla eftirfarandi gildi:

    - **Áætlunardagur:** Sláðu inn dagsetningu dagsins.
    - **Virkt:** *Já*

1. Á **Línur** Flýtiflipi, veldu **Bæta við eignateljarlínu** til að bæta línu við ristina. Stilltu síðan eftirfarandi gildi fyrir það:

    - **Lýsing á vinnupöntun:** *Viðhald fyrir lofthníf*
    - **Tegund viðhaldsstarfs:** *Fyrirbyggjandi*
    - **Gerð bils:** *Endurtekið frá síðustu verkbeiðni*
    - **Tíðni tímabils:** *10000*
    - **Teljari:** *FramleiðslaHr*

## <a name="set-up-the-asset-maintenance-scenario"></a>Settu upp atburðarás eignaviðhalds

Fylgdu þessum skrefum til að setja upp *viðhald eigna* atburðarás í Supply Chain Management.

1. Fara til **Eignastýring \> Uppsetning \> Sensor Data Intelligence \> Sviðsmyndir**.
1. Í **Viðhald eigna** atburðarás kassi, veldu **Stilla** til að opna uppsetningarhjálpina fyrir þessa atburðarás.
1. Á **Skynjarar** síðu, veldu **Nýtt** til að bæta skynjara við ristina. Stilltu síðan eftirfarandi reiti fyrir það:

    - **Auðkenni skynjara** – Sláðu inn auðkenni skynjarans sem þú ert að nota. (Ef þú ert að nota Raspberry PI Azure IoT Online Simulator og hefur sett hann upp eins og lýst er í [Settu upp herma skynjara til að prófa](sdi-set-up-simulated-sensor.md), koma inn *Eignaviðhald* .)
    - **Lýsing á skynjara** – Sláðu inn lýsingu á skynjaranum.

1. Endurtaktu fyrra skref fyrir hvern viðbótarskynjara sem þú vilt bæta við núna. Þú getur komið aftur og bætt við fleiri skynjurum hvenær sem er.
1. Veljið **Næst**.
1. Á **Kortlagning viðskiptaskráa** síðu, í **Skynjarar** kafla, veldu skrána fyrir einn af skynjurunum sem þú varst að bæta við.
1. Í **Kortlagning viðskiptaskráa** kafla, veldu **Nýtt** til að bæta línu við ristina.
1. Á nýju röðinni er **Tegund viðskiptaskrár** reiturinn ætti sjálfkrafa að vera stilltur á *Eignir(EntAssetObjectTable)*. Stilltu **Viðskiptaskrá** reitnum við auðlindina sem þú notar valinn skynjara til að fylgjast með. (Ef þú ert að nota kynningargögnin sem þú bjóst til fyrr í þessari grein, stilltu þau á *AK-101, AK-101 Lofthnífur fyrir línu 1* .)
1. Strax eftir að þú hefur valið tegund viðskiptaskrár fyrir línuna sem þú bættir við í fyrra skrefi er annarri línu sjálfkrafa bætt við hnitanetið. Á þessari röð er **Tegund viðskiptaskrár** reit ætti að vera stillt á *Teljarar (EntAssetCounterType)*. Stilltu **Viðskiptaskrá** reit í eignateljarann sem þú ert að uppfæra á grundvelli merkja frá völdum skynjara. (Ef þú ert að nota kynningargögnin sem þú bjóst til fyrr í þessari grein, stilltu þau á *FramleiðsluHr, Framleiðslutími* .)
1. Veljið **Næst**.
1. Á **Virkjaðu skynjara** síðu, í hnitanetinu, veldu skynjarann sem þú bættir við og veldu síðan **Virkjaðu**. Fyrir hvern virkan skynjara í ristinni birtist gátmerki í **Virkur** dálki.
1. Veljið **Ljúka**.

## <a name="work-with-the-asset-maintenance-scenario"></a>Vinna með eignaviðhaldssviðsmyndina

### <a name="view-counter-values"></a>Skoða teljaragildi

Eftir að gögnin eru útbúin, og *viðhald eigna* atburðarás er stillt og virkjuð geturðu séð hvernig færslur fyrir eignateljara eru settar inn á grundvelli skynjaragagna.

1. Fara til **Eignastýring \> Eignir \> Allar eignir**.
1. Finndu og veldu eignina sem þú vilt skoða. (Ef þú ert að nota kynningargögnin sem þú bjóst til fyrr í þessari grein skaltu velja *AK-101* .)
1. Á aðgerðarrúðunni, á **Eign** flipa, í **Fyrirbyggjandi** hópur, veldu **Teljarar** til að opna síðuna fyrir teljaraskrár fyrir eign *AK-101*.

> [!NOTE]
> Teljaskrárnar eru sjálfgefnar stilltar til að vera settar inn á þriggja klukkustunda fresti, sem þýðir að skynjaragögn verða tekin saman á því millibili. Þú getur breytt bilinu með því að breyta fyrirspurninni í Azure Stream Analytics íhlutnum.

### <a name="generate-maintenance-work-orders"></a>Búðu til viðhaldsvinnupantanir

Eftir að þú hefur virkjað *viðhald eigna* atburðarás og setja upp viðhaldsáætlunina geturðu keyrt viðhaldsáætlunina til að búa til viðhaldsvinnupantanir. Fyrir frekari upplýsingar um hvernig á að vinna með fyrirbyggjandi viðhald, sjá [Yfirlit yfir fyrirbyggjandi viðhald](../asset-management/preventive-and-reactive-maintenance/preventive-maintenance-overview.md).
