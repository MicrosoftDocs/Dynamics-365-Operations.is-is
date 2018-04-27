---
title: "Skilgreina skilyrta ákvörðun í verkflæði"
description: "Notið eftirfarandi ferli til að stilla eiginleika fyrir skilyrt ákvörðun."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 597a6a254dcd623f9e7c59a0309eeedee1b5adee
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>Skilgreina skilyrta ákvörðun í verkflæði

[!INCLUDE [banner](../includes/banner.md)]

Notið eftirfarandi ferli til að stilla eiginleika fyrir skilyrt ákvörðun.

Skilyrt ákvörðun er punktur þar sem verkflæði skiptist í tvær greinar. Til að skilgreina skilyrta ákvörðun í verkflæðisritlinum, hægrismellt er á skilyrt ákvörðun og smellið síðan á **Eiginleika** til að opna **Eiginleika** skjámynd.

## <a name="name-a-decision"></a>Nefndu ákvörðun.
Fylgið þessum skrefum til að færa inn heiti á skilyrta ákvörðun.
1.  Í vinstri glugganum, smelltu á **grunnstillingar**.
2.  Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir skilyrtu ákvörðunina.

## <a name="set-conditions"></a>Stilla skilyrði
Kerfið ákveður sjálfkrafa hvaða grein á að nota með því að meta sent fylgiskjal til að ákvarða hvort það fullnægi ákveðnum skilyrðum.
1.  Í vinstri glugganum, smelltu á **grunnstillingar**.
2.  Smelltu á **Bæta við Aðgerð**.
3.  Færið inn skilyrði.
4.  Færa inn viðbótarskilyrði ef þess gerist þörf:
5.  Til að sannreyna að skilyrðin sem voru færð hafi verið sett upp rétt, skal ljúka eftirfarandi skrefum:
    1.  Smellið á **Prófun** til að opna **Kanna verkflæðisskilyrði** skjámyndinni.
    2.  Veljið færslu í svæðinu **Villuleita skilyrði** á skjámyndinni.
    3.  Smellið á **Prófun**. Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú tiltókst.
    4.  Smelltu á **Í lagi** eða **Hætta við** til að fara aftur síðuna **Eiginleikar**.






