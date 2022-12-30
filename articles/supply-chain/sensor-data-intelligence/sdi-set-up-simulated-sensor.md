---
title: Setja upp eftirlíkingarskynjara til prófunar
description: Þessi grein lýsir því hvernig á að setja upp hermi sem hægt er að nota til að prófa Sensor Data Intelligence án þess að setja upp efnislega skynjara.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689805"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>Setja upp eftirlíkingarskynjara til prófunar

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Ef þú vilt prófa Sensor Data Intelligence án þess að setja upp neina efnislega skynjara geturðu notað þjónustuna *Netherminn Raspberry PI Azure IoT* til að líkja eftir merkjum skynjara og senda þau til IoT-lausnarinnar á Microsoft Azure. Frekari upplýsingar um herminn eru í [Tengja Raspberry Pi nethermi við Azure IoT Hub (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started).

## <a name="video-instructions"></a>Myndbandsleiðbeiningar

Í eftirfarandi myndskeiði er sýnt hvernig á að setja upp eftirlíkingarskynjar til prófunar. Í hinum köflunum í þessari grein eru sömu leiðbeiningar á textaformi.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE588g6]

## <a name="create-a-device-in-azure-iot-hub"></a>Búa til tæki í Azure IoT Hub

Fyrst þarf að setja upp tæki til að sannvotta merki skynjarans hjá Azure IoT Hub.

1. Í Azure skal fara í lista yfir tilföng fyrir tilfangaflokkinn sem var stofnaður til að nota með Sensor Data Intelligence. (Frekari upplýsingar er að finna í [Setja upp IoT-lausn í Azure](sdi-deploy-iot-solution-on-azure.md).)
1. Í tilfangalistanum skal finna færsluna þar sem reiturinn **Gerð** er stilltur á *IoT Hub*. Í dálkinum **Heiti** skal velja nafnið til að opna upplýsingasíðu tilfangsins.
1. Á yfirlitssvæðinu til vinstri skal velja **Tæki**.
1. Á síðunni **Tæki** skaltu velja **Bæta við tæki**.
1. Á síðunni **Búa til tæki** skal stilla eftirfarandi svæði:

    - **Auðkenni tækis** – Sláðu inn heiti nýja tækisins (t.d. *My-IoT-Device*).
    - **Gerð sannvottunar** – Veldu *Samhverfulykla*.
    - **Búa til lykla sjálfkrafa** – Veldu þennan gátreit.
    - **Tengja þetta tæki við IoT hub** – Veldu *Virkja*.

1. Veldu **Vista** til að fara aftur á síðuna **Tæki**.
1. Finna nýja tækið á listanum. Í dálkinum **Auðkenni tækis** skal velja nafnið til að opna upplýsingasíðu tækisins. Ef þú sérð nýja tækið ekki á listanum skaltu endurhlaða síðuna.
1. Afritaðu gildið **Aðaltengistrengur** (til dæmis með því að velja hnappinn **Afrita á klippiborð**). Þú þarft að nota þetta gildi síðar þegar þú setur upp herminn Raspberry Pi IoT til að líkja eftir merkjum skynjara. Því skaltu íhuga að líma það inn í textaskrá í bili.

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>Bæta Azure tengistreng við Raspberry Pi IoT herminn

Fylgdu þessum skrefum til að bæta tengi strengnum frá tækinu í Azure IoT Hub við skriftuna í Raspberry-þjónustunni.

1. Opnið [Raspberry Pi IoT herminn](https://azure-samples.github.io/raspberry-pi-web-simulator/).
1. Í glugganum fyrir kóðaritli er að finna línuna sem inniheldur eftirfarandi skipun.

    `const connectionString = '[Your IoT hub device connection string]';`

1. Skiptu út hjálpartextanum, þar á meðal festingunum, með gildinu **Aðaltengistrengur** sem þú afritaðir í hlutanum hér á undan. Niðurstaðan ætti að líkjast eftirfarandi dæmi.

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>Bæta við kennum og gildum skynjara við hleðsluna í Raspberry Pi IoT herminum

Nú þarf að setja upp herminn Raspberry Pi IoT með hermiskynjurum og gildunum sem þeir munu senda sem innihald.

- Í kóðaritli hermisins Raspberry Pi IoT skal finna `getMessage` virknina og breyta henni þannig að hún samsvari eftirfarandi kóða. (Skynjararnir eru settir upp í `cb()` línunum.)

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
    > Auðkenni skynjara sem eru skilgreind í kóðaritlinum fyrir herminn Raspberry Pi IoT verða að samsvara skynjarakennum sem þú mun tilgreina síðar fyrir aðstæður í Supply Chain Management. Kóðinn hér á undan notar skynjarakenni sem fólk getur lesið. Hins vegar, í raunverulegum aðstæðum, verða kennimerki skynjara altækt einkvæmt kennimerki (GUID) sem framleiðandi skynjara lætur í té. Læsileg skynjarakenni sem eru notuð í þessum dæmakóða eru einnig notuð í dæmunum í [Aðstæður fyrir vörugæði](sdi-scenario-product-quality.md), [Aðstæður fyrir viðhald eignar](sdi-scenario-asset-maintenance.md), [Aðstæður fyrir framleiðslutöf](sdi-scenario-production-delays.md) og [Aðstæður fyrir vélarstöðu](sdi-scenario-equipment-downtime.md)). Þess vegna skaltu nota þennan kóða ef þú munt vinna í gegnum þessar aðstæður.

## <a name="edit-the-interval-for-sending-sensor-signals"></a>Breyta bili til að senda skynjara merki

Nú þarf að stilla millibilið sem hermirinn Raspberry Pi IoT á að senda hermuð merki skynjara.

1. Í kóðaritlinum fyrir herminn Raspberry Pi IoT skal finna eftirfarandi kall á virkni.

    `setInterval(sendMessage, 2000);`

2. Hermirinn Raspberry Pi IoT sendir sjálfgefið skynjaramerki á 2000 millisekúndna (tveggja sekúndna fresti). Hægt er að breyta gildinu eftir þörfum.

## <a name="run-the-raspberry-pi-iot-simulator"></a>Keyra Raspberry Pi IoT herminn

- Veljið **Keyra** til að ræsa herminn og byrja að senda hermd skynjaragögn.
