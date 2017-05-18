---
title: "Setja upp viðvaranir vegna svika"
description: "Í þessu efnisatriði er útskýrt hvernig á að setja upp reglur viðvörun viðskiptavinar þjónustu biðlaraþjónustu hugsanlega sviksamleg upplýsinga þegar pantanir eru unnar. Hægt er að skilgreina ákveðna kóða sem nota á til að sjálfvirkt eða handvirkt setja grunsamlegar pantanir í bið."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: ddcf68b9d9d35d63cb092225d468dd4a6a3d4446
ms.contentlocale: is-is
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-fraud-alerts"></a>Setja upp viðvaranir vegna svika

[!include[banner](includes/banner.md)]


Í þessu efnisatriði er útskýrt hvernig á að setja upp reglur viðvörun viðskiptavinar þjónustu biðlaraþjónustu hugsanlega sviksamleg upplýsinga þegar pantanir eru unnar. Hægt er að skilgreina ákveðna kóða sem nota á til að sjálfvirkt eða handvirkt setja grunsamlegar pantanir í bið. 

Áður en hægt er að setja upp og nota reglum um eftirlit með svikum verður að virkja eftirlit með svikum og skilgreina grunnupplýsingar um eftirlit með svikum í færibreytum símavers. Til eru tvær gerðir af reglum gegn svikum:

-   **Fastar reglur** nota tiltekið gildi, eins og símanúmer sem hefur verið sett á svartan lista.
-   **Breytilegar reglur** geta samanstaðið af breytum og skilyrðum.

Áður en breytilega regla er stofnuð verður að stofna breytur og skilyrði sem skilgreina hverja reglan á við og hvenær á að nota regluna. Til dæmis viltu stofna reglu til að krefjast þess að þegar viðskiptavinur 1202 setur pöntun sem er að andvirði 1.000,00 eða hærra, verður að setja sölupöntun í bið áður en hægt er að staðfesta greiðslu viðskiptavinar.. Í þessu dæmi eru breyturnar viðskiptavinur 1202 og pöntunarsamtalan 1.000,00. Skilyrðin tilgreina að ef viðskiptavinur 1202 setur pöntun, og heildarupphæð pöntunarinnar er jafnt eða meira en 1.000,00 verður sölupöntunin að fara í bið þar til það er hægt að staðfesta greiðslu viðskiptavinar.




