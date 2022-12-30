---
title: Aðstæður fyrir viðhald eignar
description: Þessi grein útskýrir aðstæðum eignaviðhalds sem gerir þér kleift að nota skynjaragögn til að stofna talningafærslur sem fylgjast með notkun vélaeignar.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689401"
---
# <a name="the-asset-maintenance-scenario"></a>Aðstæður fyrir viðhald eignar

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Aðstæðurnar fyrir *eignaviðhald* gerir þér kleift að nota skynjaragögn til að stofna talningafærslur. Talningafærslur fylgjast með notkun vélaeignar og eru notaðar sem inntak fyrir að búa til viðhaldsáætlun fyrir vélaeignir.

## <a name="video-instructions"></a>Myndbandsleiðbeiningar

Eftirfarandi myndband sýnir hvernig á að setja upp og prófa aðstæður eignaviðhalds með því að nota stöðluð [sýnigögn](../../fin-ops-core/fin-ops/get-started/demo-data.md). Í hinum köflunum í þessari grein eru sömu leiðbeiningar á textaformi.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58aRW]

## <a name="prepare-demo-data-for-the-asset-maintenance-scenario"></a>Útbúa sýnigögn fyrir aðstæður eignaviðhalds

Ef þú vilt nota sýnikerfi til að prófa aðstæður *eignaviðhald* skaltu nota kerfi þar sem [sýnigögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) eru sett upp, velja lögaðilann (fyrirtæki) *USMF* og útbúa frekari sýnigögn eins og lýst er í þessum hluta. Ef þú notar eigin skynjara og gögn geturðu sleppt þessum hluta.

Í þessum hluta seturðu upp eiginina *AK-101, Air knife* í sýnigögnum sem dæmi. Þá sérðu hvernig hægt er að spá fyrir um væntanlega viðhaldsvinnu samkvæmt skynjaramerkjum sem mæla fjölda klukkustunda sem lofthnífurinn hefur verið í gangi. Þú munt einnig setja upp viðhaldsáætlun þar sem sinna þarf viðhaldi á lofthnífnum á 10.000 klst. fresti.

### <a name="set-up-a-sensor-simulator"></a>Setja upp skynjarahermi

Ef þú vilt prófa þessar aðstæður án þess að nota efnislegan skynjara getur þú sett upp hermi til að búa til nauðsynleg merki. Frekari upplýsingar eru í [Setja upp eftirlíkingarskynjara til prófunar](sdi-set-up-simulated-sensor.md).

### <a name="create-an-asset-counter-to-track-production-hours"></a>Stofna eignateljara til að fylgjast með framleiðslutímum

Fylgdu þessum skrefum til að búa til eignateljara til að fylgjast með framleiðslustundum.

1. Opnaðu **Eignastýringu \> Uppsetningu \> Færibreytur eignastýringar \> Teljarar**.
1. Veldu **Nýtt** á aðgerðasvæðinu til að búa til teljara.
1. Stillið eftirfarandi gildi í hausnum:

    - **Teljari:** *ProductionHr*
    - **Heiti:** *Framleiðslustundir*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Eining:** *hr*
    - **Uppfæra:** *Handvirkt*
    - **Heildarsamtala:** *Summa*

1. Í flýtiflipanum **Eignagerðir** skal velja **Bæta við línu**.
1. Í nýju línunni skal stilla reitinn **Eignagerð** á *Lofthnífur*.

### <a name="create-a-maintenance-plan-for-the-asset"></a>Búðu til viðhaldsáætlun fyrir eignina

Fylgið eftirfarandi skrefum til að útbúa viðhaldsáætlun fyrir eignina.

1. Farið í **Eignastýring \> Uppsetning \> Fyrirbyggjandi viðhald \> Viðhaldsáætlanir**.
1. Veldu **Nýtt** á aðgerðasvæðinu til að búa til viðhaldsáætlun.
1. Stillið eftirfarandi gildi í hausnum:

    - **Viðhaldsáætlun:** *AirKnife*
    - **Heiti:** *Áætlun fyrir lofthnífa*

1. Í flýtiflipanum **Upplýsingar** skal stilla eftirfarandi gildi:

    - **Áætluð dagsetning:** Sláðu inn dagsetninguna í dag.
    - **Virkt:** *Já*

1. Í flýtiflipanum **Línur** skal velja **Bæta við línu eignateljara** til að bæta línu við hnitanetið. Stillið svo eftirfarandi gildi fyrir hana:

    - **Lýsing verkbeiðni:** *Viðhald fyrir lofthníf*
    - **Gerð viðhaldsverks:** *Fyrirbyggjandi*
    - **Gerð millibils:** *Endurtekið frá síðustu verkbeiðni*
    - **Tímabilstíðni:** *10000*
    - **Teljari:** *ProductionHr*

## <a name="set-up-the-asset-maintenance-scenario"></a>Setja upp aðstæður eignaviðhalds

Fylgdu þessum skrefum til að setja upp aðstæður *eignaviðhalds* í Supply Chain Management.

1. Farðu í **Eignastýring \> Uppsetning \> Sensor Data Intelligence \> Aðstæður**.
1. Í aðstæðureitnum **Eignaviðhald** skal velja **Skilgreina** til að opna uppsetningarleiðsögnina fyrir þessar aðstæður.
1. Á síðunni **Skynjarar** skal velja **Nýtt** til að bæta skynjara við hnitanetið. Stillið svo eftirfarandi reiti fyrir það:

    - **Auðkenni skynjara** – Sláðu inn kenni skynjarans sem þú ert að nota. (Ef þú notar Raspberry PI Azure IoT Online Simulator og hefur sett það upp eins og lýst er í [Setja upp eftirlíkingarskynjara til prófunar](sdi-set-up-simulated-sensor.md), sláðu inn *AssetMaintenance*.)
    - **Lýsing á skynjara** – Færið inn lýsingu á skynjari.

1. Endurtaka á fyrra skref fyrir hvern skynjara sem þú vilt bæta við. Hægt er að koma aftur og bæta við fleiri skynjurum hvenær sem er.
1. Veljið **Næst**.
1. Á síðunni **Vörpun viðskiptafærslu**, í hlutanum **Skynjarar**, skaltu velja færslu fyrir einn af skynjurunum sem þú varst að bæta við.
1. Í hlutanum **Vörpun viðskiptafærslu** skal velja **Ný** til að bæta línu við hnitanetið.
1. Á nýju línunni ætti reiturinn **Gerð viðskiptafærslu** að vera sjálfkrafa að vera stilltur á *Eignir(EntAssetObjectTable)*. Stilltu reitinn **Viðskiptafærsla** á tilfangið sem þú notar valinn skynjara til að fylgjast með. (Ef þú notar sýnigögnin sem þú bjóst til fyrr í þessari grein skaltu stilla þau á *AK-101, AK-101 Lofthnífur fyrir línu 1*.)
1. Strax og þú hefur valið gerð viðskiptafærslu fyrir línuna sem þú bættir við í fyrra þrepi er annarri línu sjálfkrafa bætt við hnitanetið. Á þessari línu ætti að stilla reitinn **Gerð viðskiptafærslu** á *Teljarar(EntAssetCounterType)*. Stilltu reitinn **Viðskiptafærsla** á eignateljarann sem þú ert að uppfæra samkvæmt merkjum frá völdum skynjara. (Ef þú notar sýnigögnin sem þú bjóst til fyrr í þessari grein skaltu stilla þau á *Framleiðslust., Framleiðslustundir*.)
1. Veljið **Næst**.
1. Á síðunni **Virkja skynjara**, í hnitanetinu, veldu skynjarann sem þú bættir við og veldu síðan **Virkja**. Fyrir hvern virkan skynjara í hnitanetinu birtist gátmerki í dálkinum **Virkur**.
1. Veljið **Ljúka**.

## <a name="work-with-the-asset-maintenance-scenario"></a>Vinna með aðstæður eignaviðhalds

### <a name="view-counter-values"></a>Skoða gildi teljara

Eftir að gögnin hafa verið útbúin og aðstæður *eignaviðhalds* eru skilgreindar og virkjaðar geturðu séð hvernig færslur fyrir eignateljara eru settar inn samkvæmt skynjaragögnum.

1. Farðu í **Eignastýring \> Eignir \> Allar eignir**.
1. Finndu og veldu eignina sem þú vilt skoða. (Ef þú notar sýnigögnin sem þú bjóst til fyrr í þessari grein skaltu stilla þau á *AK-101*.)
1. Á aðgerðasvæðinu, í flipanum **Eign**, í flokknum **Fyrirbyggjandi**, skaltu velja **Teljarar** til að opna síðuan fyrir talningafærslur fyrir eignina *AK-101*.

> [!NOTE]
> Teljarafærslurnar eru sjálfgefið stilltar til að vera settar inn á þriggja klukkustunda fresti, sem þýðir að skynjaragögn verða tekin saman á því bili. Þú getur breytt tímabilinu með því að breyta fyrirspurninni í hlutanum Azure Stream Analytics.

### <a name="generate-maintenance-work-orders"></a>Búa til viðhaldsverkbeiðnir

Eftir að þú virkjar aðstæður *eignaviðhalds* og setur upp viðhaldsáætlunina geturðu keryt viðhaldsáætlunina til að búa til viðhaldsverkbeiðnir. Frekari upplýsingar um hvernig á að vinna með fyrirbyggjandi viðhald er að finna í [Fyrirbyggjandi viðhald](../asset-management/preventive-and-reactive-maintenance/preventive-maintenance-overview.md).
