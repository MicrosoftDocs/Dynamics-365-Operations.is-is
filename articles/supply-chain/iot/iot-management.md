---
title: Fylgjast með og stjórna IoT-gervigreind
description: Þetta efnisatriði útskýrir hvernig á að fylgjast með og stjórna IoT-gervigreind.
author: tonyafehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8fbd750aa4a316f5e04f3c8622d0847ad9318360
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782658"
---
# <a name="monitor-and-manage-iot-intelligence"></a>Fylgjast með og stjórna IoT-gervigreind

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að fylgjast með og stjórna IoT-gervigreind.

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a> Fylgjast með aðstæðum í Microsoft Dynamics 365 Supply Chain Management

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

+ [Tengja IoT DevKit AZ3166 við Azure IoT Hub](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Tengja Raspberry Pi netherbi við Azure IoT Hub (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [Yfirlit yfir hraðal tækjahermis](/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]