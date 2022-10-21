---
title: Setja upp eftirlíkingarskynjara til prófunar
description: Þessi grein lýsir því hvernig á að setja upp hermi sem þú getur notað til að prófa skynjaragagnagreind án þess að setja upp líkamlega skynjara.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: f12d6e1d417a260477b1eb4e027b850d1862f51f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689805"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>Setja upp eftirlíkingarskynjara til prófunar

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Ef þú vilt prófa Sensor Data Intelligence án þess að setja upp neina líkamlega skynjara geturðu notað *Raspberry PI Azure IoT Online Simulator* þjónustu til að líkja eftir skynjaramerkjum og senda þau á Internet of Things (IoT) lausnina þína á Microsoft Azure. Fyrir frekari upplýsingar um hermir, sjá [Tengdu Raspberry Pi nethermir við Azure IoT Hub (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started).

## <a name="video-instructions"></a>Vídeóleiðbeiningar

Eftirfarandi myndband sýnir hvernig á að setja upp hermaskynjara til að prófa. Hlutarnir sem eftir eru í þessari grein veita sömu leiðbeiningar í textaformi.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE588g6]

## <a name="create-a-device-in-azure-iot-hub"></a>Búðu til tæki í Azure IoT Hub

Þú verður fyrst að setja upp tæki til að auðkenna skynjaramerkin til Azure IoT Hub.

1. Í Azure, farðu í lista yfir tilföng fyrir tilfangahópinn sem þú bjóst til til notkunar með Sensor Data Intelligence. (Fyrir frekari upplýsingar, sjá [Settu upp IoT lausn á Azure](sdi-deploy-iot-solution-on-azure.md) .)
1. Í auðlindalistanum, finndu skrána þar sem **Tegund** reiturinn er stilltur á *IoT miðstöð*. Í **Nafn** dálk, veldu nafnið til að opna upplýsingasíðuna fyrir tilfangið.
1. Í vinstri yfirlitsrúðunni, veldu **Tæki**.
1. Á **Tæki** síðu, veldu **Bæta við tæki**.
1. Á **Búðu til tæki** síðu, stilltu eftirfarandi reiti:

    - **Auðkenni tækis** – Sláðu inn nafn fyrir nýja tækið (til dæmis, *My-IoT-Tækið*).
    - **Auðkenningartegund** – Veldu *Samhverfar lyklar*.
    - **Búa til lykla sjálfkrafa** – Veldu þennan gátreit.
    - **Tengdu þetta tæki við IoT miðstöð** – Veldu *Virkja*.

1. Veldu **Vista** að fara aftur til **Tæki** síðu.
1. Finndu nýja tækið á listanum. Í **Auðkenni tækis** dálki, veldu nafnið til að opna upplýsingasíðu tækisins. Ef þú sérð ekki nýja tækið á listanum skaltu endurnýja síðuna.
1. Afritaðu **Aðaltengingarstrengur** gildi (til dæmis með því að velja **Afritaðu á klemmuspjald** takki). Þú þarft þetta gildi síðar þegar þú setur upp Raspberry Pi IoT hermir til að líkja eftir skynjaramerkjum. Þess vegna skaltu íhuga að líma það inn í textaskrá í bili.

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>Bættu Azure tengistrengnum við Raspberry Pi IoT hermirinn

Fylgdu þessum skrefum til að bæta tengistrengnum úr tækinu í Azure IoT Hub við handritið í Raspberry þjónustunni.

1. Opnaðu [Raspberry Pi IoT hermir](https://azure-samples.github.io/raspberry-pi-web-simulator/).
1. Finndu línuna sem inniheldur eftirfarandi skipun í kóðaritara glugganum.

    `const connectionString = '[Your IoT hub device connection string]';`

1. Skiptu út hjálpartextanum, þar á meðal sviga, fyrir **Aðal tengistrengur** gildi sem þú afritaðir í fyrri hlutanum. Niðurstaðan ætti að líkjast eftirfarandi dæmi.

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>Bættu skynjaraauðkennum og gildum við hleðsluna í Raspberry Pi IoT hermirnum

Þú verður nú að setja upp Raspberry Pi IoT hermir með herma skynjurum og gildunum sem þeir munu senda sem hleðslu.

- Í kóðaritlinum Raspberry Pi IoT hermir, finndu`getMessage` fall, og breyttu því þannig að það passi við eftirfarandi kóða. (Nemjararnir eru settir upp í`cb()` línur.)

    ```cpp
    function getMessage(cb) {
        messageId++;
        sensor.readSensorData()
        .then(function (data) {
            cb(JSON.stringify({ value: 1, sensorId: 'MachineStatus' }), false);
            cb(JSON.stringify({ value: 70, sensorId: 'Quality' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'AssetMaintenance' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'ProductionDelay' }), false);
            cb(JSON.stringify({ value: 20, sensorId: 'AssetDowntime' }), false);
        })
        .catch(function (err) {
            console.error('Failed to read out sensor data: ' + err);
        });
    }
    ```

    > [!IMPORTANT]
    > Auðkenni skynjara sem eru skilgreind í kóðaritlinum fyrir Raspberry Pi IoT hermir verða að vera eins og skynjaraauðkennin sem þú munt tilgreina síðar fyrir aðstæður í Supply Chain Management. Kóðinn á undan dæmi notar auðkenni skynjara sem hægt er að lesa af mönnum. Hins vegar, í raunverulegri atburðarás, verða skynjaraauðkennin alþjóðlegt einstakt auðkenni (GUID) gildi sem eru veitt af framleiðanda skynjarans. Mannlesanleg skynjaraauðkenni sem eru notuð í þessum dæmikóða eru einnig notuð í dæmunum í [Atburðarás vörugæða](sdi-scenario-product-quality.md),[Atburðarás eignaviðhalds](sdi-scenario-asset-maintenance.md),[Atburðarás framleiðslutafir](sdi-scenario-production-delays.md), og [Atburðarás vélarstöðu](sdi-scenario-equipment-downtime.md)). Þess vegna skaltu nota þennan kóða ef þú ætlar að vinna í gegnum þessar aðstæður.

## <a name="edit-the-interval-for-sending-sensor-signals"></a>Breyttu bilinu til að senda skynjaramerki

Þú verður nú að stilla bilið sem Raspberry Pi IoT hermirinn á að senda eftirlíkingu skynjaramerkin á.

1. Í kóðaritlinum Raspberry Pi IoT hermir, finndu eftirfarandi aðgerðakall.

    `setInterval(sendMessage, 2000);`

2. Sjálfgefið er að Raspberry Pi IoT hermir sendir skynjaramerki á 2.000 millisekúndna fresti (tveggja sekúndur). Þú getur stillt gildið eftir þörfum.

## <a name="run-the-raspberry-pi-iot-simulator"></a>Keyrðu Raspberry Pi IoT hermirinn

- Veldu **Hlaupa** til að ræsa herminn og byrja að senda herma skynjaragögn.
