---
title: Skemasnið fyrir IoT-skilaboð
description: Þetta efnisatriði útskýrir hvernig á að hanna skilaboðaskema sem hægt er að nota í IoT-gervigreind.
author: robinarh
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ecf4a70d69d24ea75f5448339057e7017cb93af
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652018"
---
# <a name="schema-formats-for-iot-hub-messages"></a>Skemasnið fyrir IoT-skilaboð

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að hanna skilaboðaskema sem hægt er að nota í IoT-gervigreind.

## <a name="message-requirements"></a>Skilyrði skilaboða

Eftirfarandi reglur gilda um eftirlit með skilaboðum í IoT-gervigreind:

+ Skilaboðaskema verða að vera á JSON-sniði.
+ UNIX **tímastimpils** eiginleiki, þar sem gildið er sýnt í millisekúndum (ms), verður að vera til staðar í skilaboðum Microsoft Azure IoT Hub.
+ Skilaboð er aðeins rakið ef það inniheldur alla eiginleika sem eru skilgreindir í uppsetningu aðstæðna. Ef þú skilgreinir til dæmis eiginleikana **auðkenni**, **tímastimpill** og **gildi** er fylgst með eftirfarandi skilaboðum.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    Ekki er fylgst með þessum skilaboðum þar sem vantar eiginleikann **gildi**.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ IoT-gervigreind hunsar eiginleika í skilaboðunum sem eru ekki skilgreind í stillingu aðstæðna. Ef þú skilgreinir til dæmis eiginleikana **auðkenni**, **tímastimpill** og **gildi** mun IoT-gervigreind fylgjast með öllum eftirfarandi skilaboðum.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ IoT-gervigreind hunsar hljóðlaust skilaboð sem passa ekki við stillingarskilyrði aðstæðna.
+ Hægt er að skilgreina og nota margar gerðir af skilaboðaskema.
+ Ekki verður að skilgreina allar gerðir skilaboðaskema. Aðeins þarf að skilgreina skema sem verða notuð fyrir aðstæður IoT-gervigreindar.

## <a name="id-value-pair-schema"></a>Skema fyrir par auðkennisgildis

Par auðkennisgildis er algengt mynstur fyrir skilaboðaskema IoT-gervigreindar. Með því að nota par auðkennisgildis tryggir þú að skilaboðaskemað sé það sama í öllum aðstæðum. Hér eru t.d. skilaboð vegna aðstæðnanna **Niðurtími búnaðar** eða **Tafir á framleiðslu**.

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

Hér eru skilaboð fyrir aðstæðurnar **Gæði vörunnar**.

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

Bæði skilaboðin á undan innihalda eiginleikana **auðkenni** og **gildi**. Hægt er að varpa **auðkennisgildum** í töfluna **Gagnagildi merkis** við uppsetningu aðstæðna. Fyrir aðstæðurnar **Niðurtími búnaðar** varpar þú gildinu **IoTInt.Machine1225.PartOut**. Fyrir aðstæðurnar **Gæði vörunnar** varpar þú gildinu **IoTInt.Machine1225.Temperature**.

Frekari upplýsingar er að finna í [Fylgigögn Azure IoT Hub](/azure/iot-hub/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]