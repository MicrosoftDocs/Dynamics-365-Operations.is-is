---
title: Yfirlit yfir þjónustuverk
description: Notið þjónustuverk til að lýsa verkinu sem á að ljúka í þjónustupöntun. Bæði tæknimenn og viðskiptavinir geta séð þessar upplýsingar.
author: ShylaThompson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ebad3a5fdd65155eb822dcd69a1d2624a1891337
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835823"
---
# <a name="service-tasks-overview"></a>Yfirlit yfir þjónustuverk

[!include [banner](../includes/banner.md)]

Notið þjónustuverk til að lýsa verkinu sem á að ljúka í þjónustupöntun.
Bæði tæknimenn og viðskiptavinir geta séð þessar upplýsingar.

Þjónustuverk eru stofnuð í skjámyndinni **Þjónustuverk** og hægt er að tengja þau við tiltekinn þjónustusamning eða þjónustupöntun með því að stofna þjónustuverkatengsl. Í hvert skipti sem þjónustuverkatengsl er stofnað er hægt að stofna eftirfarandi:

-  Innri athugasemdir fyrir verkið, t.d. nákvæmar tæknilegar beiðnir fyrir verkið sem eru nauðsynlegar fyrir tæknimanninn.

-  Ytri athugasemdir sem viðskiptavinurinn getur séð. Þær kunna að innihalda almenna útskýringu á verkinu sem verið er að vinna samkvæmt samningi á milli viðskiptavinar og þjónustufyrirtækis.

Um leið og búið er setja upp þjónustuverkatengsl á milli þjónustuverks og þjónustupöntunar eða þjónustusamnings er hægt að tilgreina þetta þjónustuverk þegar stofnaðar eru þjónustupöntunarlínur eða þjónustusamningslínur fyrir opnu þjónustupöntunina eða þjónustusamninginn.

Þegar þjónustupantanir eru stofnaðar úr þjónustusamningi er hægt að nota þjónustuverk sem tengd eru þjónustusamningslínunum til að flokka þjónustupöntunarlínur í þjónustupantanir.

## <a name="create-a-service-task"></a>Stofna þjónustuverk

1. Smellið á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustuverk**.
2. Stofnið nýja línu.
3. Færið inn kenni þjónustu og lýsingu.

## <a name="example"></a>Dæmi

Tæknimaður verður að ljúka tveimur verkum á gírkassa (þjónustuhluti GB-1234) hjá viðskiptavini. Þjónustusamningur er stofnaður fyrir viðskiptavininn og nokkrar færslur eru tengdar verkunum. Þjónustusamningurinn og þjónustusamningslínurnar fyrir verkin tvö eru eftirfarandi:

### <a name="service-agreement"></a>Þjónustusamningur

| Verkefni | Þjónustusamningur | lýsing                                  | Hópur   |
|---------|-------------------|----------------------------------------------|---------|
| 9012    | 000008\_001       | Skoðun og reglubundin skipti – GB-1234 | Bónusgreiðsla |

### <a name="service-agreement-lines"></a>Þjónustusamningslínur

| lýsing             | Færslugerð | Þjónustuhlutur | Þjónustuverk |
|-------------------------|------------------|----------------|--------------|
| Skoðun og hreinsun | Vinnustund             | GB-1234        | I/C - GB1234 |
| Ferðir                  | Expense          | GB-1234        | I/C - GB1234 |
| Efni               | vara             | GB-1234        | I/C - GB1234 |
| Reglubundin skipti     | Vinnustund             | GB-1234        | RR - GB1234  |
| GR-1                    | vara             | GB-1234        | RR - GB1234  |
| GR-5                    | vara             | GB-1234        | RR - GB1234  |

Tvö þjónustuverk eru tengd þjónustusamningslínunum fyrir verkin tvö. Þjónustuverkin stjórna færslunum sem tilheyra hvoru verki. Í fyrsta lagi auðkennir þjónustuverkið I/C - GB1234 allar þjónustusamningslínur sem tengjast skoðun og hreinsun á hlut GB-1234. Í öðru lagi auðkennir RR - GB1234 allar samningslínur sem tengjast lokum á reglubundnum skiptum.

Þjónustuverkatengslin sem tengja þjónustuverkin við tiltekna samninga eru sem hér segir:

### <a name="service-tasks"></a>Þjónustuverk

| Þjónustuverkliður | Lýsing                             | Innri athugasemd                                                                                                                 | Ytri athugasemd                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| I/C - GB1234 | Skoðun á gírkassa GB-1234           | Sjónræn og vélræn skoðun og hreinsun gírkassa GB-1234                                                              | Reglubundin skoðun á gírkassa |
| RR - GB1234  | Reglubundin skipti á hlutum í GB-1234 | Reglubundin þjónustuskipti á GR-1 og GR-5 íhlutunum (fyrir gírkassa framleidda fyrir 2002, einnig þarf að skipta út GR-2 íhlutnum) | Reglubundin skipti á hlutum  |

## <a name="group-service-orders"></a>Þjónustuflokkapöntun

Þegar þjónustupantanir eru stofnaðar sjálfvirkt er hægt að nota þjónustuverk sem flokkunarskilyrði. Til að flokka þjónustupantanir eftir þjónustuverkum þarf að tilgreina í þjónustusamningnum að þjónustupantanir sem eru byggðar á þjónustusamningnum eigi að flokka eftir þjónustuverkskenni sem fyrsta flokkunarskilyrði.

**Flokka eftir þjónustuverki**

1. Smellið á **Þjónustustjórnun** \> **Almennt** \> **Þjónustusamningar** \> **þjónustusamningar**.
2. Í flipanum **Uppsetning** skal velja **Eftir þjónustuverki** í reitnum **Sameina þjónustupantanir**.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]