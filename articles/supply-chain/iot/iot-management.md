---
title: Fylgjast með og stjórna IoT-gervigreind
description: Þetta efnisatriði útskýrir hvernig á að fylgjast með og stjórna IoT-gervigreind.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 15021281b9ec33cd0552bca16e3054d0d3cdd589
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430584"
---
# <a name="monitor-and-manage-iot-intelligence"></a>Fylgjast með og stjórna IoT-gervigreind

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að fylgjast með og stjórna IoT-gervigreind.

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a>Fylgjast með aðstæðum í Microsoft Dynamics 365 Supply Chain Management

Hægt er að fylgjast með vinnslu á IoT-gervigreind frá nokkrum stöðum:

+ **Einingar \> Framleiðslustýring \> Fyrirspurnir og skýrslur \> IoT-gervigreind \> Tilkynningar** – Skoða lista yfir óleystar tilkynningar.
+ **Einingar \> Framleiðslustýring \> Fyrirspurnir og skýrslur \> IoT-gervigreind \> Lokaðar tilkynningar** – Skoða lista yfir tilkynningar sem leyst hefur verið út eða hafa verið hundsaðar.
+ **Einingar \> Framleiðslustýring \> Fyrirspurnir og skýrslur \> IoT-gervigreind \> Mælingalyklar** – Skoða mælingalykla fyrir **Staða tilfanga** á gröfum tímaraða.
+ **Einingar \> Framleiðslustýring \> Framkvæmd framleiðslu \> Tilfangastaða** – Rekja tiltekna mælikvarða með því að nota svargluggann **Skilgreina**. Ef aðstæður skynja undantekningu sýnir tilkynning upplýsingar um undantekningu.
+ **Vinnusvæði \> Stjórnun á framleiðslugólfi \> Tilkynningar** – Skoða lista yfir óleystar tilkynningar.

## <a name="modify-a-running-iot-intelligence-scenario"></a>Breyta aðstæðum IoT-gervigreind í vinnslu

Þegar aðstæður eru í vinnslu er hægt að gera þessar breytingar:

+ Bæta við nýjum skemaskilgreiningum skynjara.
+ Veljið ný gagnagildi merkis.
+ Hætta við val á fyrirliggjandi gagnagildum merkis.
+ Bæta við og varpa nýjum gagnagildum merkis.
+ Uppfæra þröskuldsgildi.

Þegar aðstæður eru í vinnslu eru þessar breytingar bannaðar:

+ Eyða eða breyta skemaskilgreiningum sem verið er að nota í virkjuðum aðstæðum.
+ Breyta völdum skemaleiðum í virkum aðstæðum.

## <a name="simulation-options"></a>Hermivalkostir

Hægt er að líkja eftir merkjum verksmiðjuvélar. Nánari upplýsingar eru í þessum efnisatriðum:

+ [Tengja IoT DevKit AZ3166 við Azure IoT Hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Tengja Raspberry Pi netherbi við Azure IoT Hub (Node.js)](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [Yfirlit yfir hraðal tækjahermis](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
