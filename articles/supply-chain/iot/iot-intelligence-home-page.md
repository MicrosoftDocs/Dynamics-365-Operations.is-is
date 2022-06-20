---
title: IoT-gervigreind – heimasíða
description: Þessi grein veitir tengla á upplýsingar um IoT Intelligence.
author: johanhoffmann
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b43681b036379a6f95103d4bb17cbde018724552
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877625"
---
# <a name="iot-intelligence-home-page"></a>IoT-gervigreind – heimasíða

[!include [banner](../../includes/banner.md)]

> [!IMPORTANT]
> Þessi eiginleiki er sem stendur aðeins í boði í eftirfarandi löndum/svæðum:
>
> - US (Bandaríkin)
> - ESB (Evrópusambandið)
> - AU (Ástralía)
> - CA (Kanada)
> - UK (Bretland)

IoT-gervigreind er viðbót fyrir Microsoft Dynamics 365 Supply Chain Management. Hún samþættir Internet of Things (IoT) merki með gögnum í Supply Chain Management til að búa til innsýn sem hægt er að bregðast við.

IoT gervigreind styður eftirfarandi atburðarásir:

- **Seinkun á framleiðslu** – Þessi atburðarás ber saman raunverulegan tíma ferlis við áætlaðan tíma ferlis. Supply Chain Management tilkynnir þér þegar framleiðsla er ekki á áætlun þannig að þú getir brugðist við til að hámarka rekstrarhagkvæmni og komið í veg fyrir seinkun á pöntunum.
- **Niðurtími búnaðar** – Í þessari atburðarás er borinn saman mældur uppitími við notandaskilgreindar færibreytur. Supply Chain Management tilkynnir þér þegar farið er yfir mörk stöðvunar þannig að þú getir gripið til aðgerða á borð við enduráætlun á verkbeiðni framleiðslu eða stofnun viðhaldsverkbeiðni.
- **Gæði vöru** – Í þessari atburðarás eru skynjunarlestrar bornir saman, t.d. raki og hitastig, við gæðamælingar skilgreindar af notanda. Supply Chain Management tilkynnir þér þegar frávik kemur upp þannig að þú getir brugðist við til að halda uppi gæðum og lágmarkað eyðslu.

Eftirfarandi mynd sýnir samspil Azure IoT Hub, IoT-gervigreind og Supply Chain Management.

![IoT Hub, IoT-gervigreind og Supply Chain Management.](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>Rakning og viðhald

- [Fylgjast með aðstæðum í Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
- [Gera aðstæður óvirkar](iot-scenario-setup.md#disable-a-scenario)
- [Breyta aðstæðum IoT-gervigreind í vinnslu](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [Hermivalkostir](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]