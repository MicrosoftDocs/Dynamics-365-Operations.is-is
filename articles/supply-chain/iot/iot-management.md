---
title: Fylgjast með og stjórna IoT-gervigreind
description: Þessi grein útskýrir hvernig á að fylgjast með og stjórna IoT Intelligence.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a640b523adac619377e19d670f932d4d85cfb6a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852419"
---
# <a name="monitor-and-manage-iot-intelligence"></a>Fylgjast með og stjórna IoT-gervigreind

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir hvernig á að fylgjast með og stjórna IoT Intelligence.

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

Hægt er að líkja eftir merkjum verksmiðjuvélar. Fyrir frekari upplýsingar, sjá þessar greinar:

+ [Tengja IoT DevKit AZ3166 við Azure IoT Hub](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Tengja Raspberry Pi netherbi við Azure IoT Hub (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
