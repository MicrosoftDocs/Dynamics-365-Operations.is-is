---
title: IoT gervigreind – heimasíða
description: Í þessu efnisatriði er að finna tengla á upplýsingar um IoT-gervigreind.
author: robinarh
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: intro-internal
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f32cb5578f3c15a10f863980491a687f64312cd
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652017"
---
# <a name="iot-intelligence-home-page"></a>IoT gervigreind – heimasíða

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

+ **Seinkun á framleiðslu** – Þessi atburðarás ber saman raunverulegan tíma ferlis við áætlaðan tíma ferlis. Supply Chain Management tilkynnir þér þegar framleiðsla er ekki á áætlun þannig að þú getir brugðist við til að hámarka rekstrarhagkvæmni og komið í veg fyrir seinkun á pöntunum.
+ **Niðurtími búnaðar** – Í þessari atburðarás er borinn saman mældur uppitími við notandaskilgreindar færibreytur. Supply Chain Management tilkynnir þér þegar farið er yfir mörk stöðvunar þannig að þú getir gripið til aðgerða á borð við enduráætlun á verkbeiðni framleiðslu eða stofnun viðhaldsverkbeiðni.
+ **Gæði vöru** – Í þessari atburðarás eru skynjunarlestrar bornir saman, t.d. raki og hitastig, við gæðamælingar skilgreindar af notanda. Supply Chain Management tilkynnir þér þegar frávik kemur upp þannig að þú getir brugðist við til að halda uppi gæðum og lágmarkað eyðslu.

Eftirfarandi mynd sýnir samspil Azure IoT Hub, IoT-gervigreind og Supply Chain Management.

![IoT Hub, IoT-gervigreind og Supply Chain Management.](media/iot_intelligence.png)

## <a name="setup"></a>Uppsetning

Hægt er að setja upp og stilla IoT-gervigreind án þess að skrifa kóða. Hér eru grunnskrefin.

1. [Setja upp Azure-tilföng](iot-azure-setup.md) – Búðu til IoT-miðstöð, Redis-skyndiminni og lyklageymslu sem hægt er að fara í úr Supply Chain Management.
2. [Snið skilaboðaskema fyrir IoT-miðstöð](iot-schema-format.md) – Stilltu tækin þín á að senda skilaboð til IoT Hub og skilgreindu skilaboðasnið JavaScript Object Notation (JSON).
3. Í eiginleikastjórnun skal virkja eiginleikaflagg IoT-gervigreindar. 
4. [Setja upp viðbót IoT-gervigreindar í Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Settu upp innbótina í LCS og stilltu Azure-leynilyklana.
5. [Setja upp mælieiningar](iot-metrics-setup.md) – Settu upp mælieiningar í Supply Chain Management.
6. [Uppsetning atburðarásar](iot-scenario-setup.md) – Settu upp atburðarásirnar í Supply Chain Management.

## <a name="tracking-and-maintenance"></a>Rakning og viðhald

+ [Fylgjast með aðstæðum í Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
+ [Gera aðstæður óvirkar](iot-scenario-setup.md#disable-a-scenario)
+ [Fjarlægja innbótina](iot-lcs-setup.md#uninstall-addin)
+ [Breyta aðstæðum IoT-gervigreind í vinnslu](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [Hermivalkostir](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]