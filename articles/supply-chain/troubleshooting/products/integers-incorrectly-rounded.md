---
title: Heilar tölur eru sléttaðar á rangan hátt í útreikningum afbrigðalíkans afurðar
description: Niðurstöður heiltalna eru ekki alltaf sléttaðar rétt þegar afbrigðalíkön afurðar eru reiknuð. Laga skal vandamálið með eigind viðbættra aukastafa og útreikning.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b17145d7d17cb784fe11b3fbf65ddf5aa5530f27
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476679"
---
# <a name="integers-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Heiltölur eru rangt sléttaðar þegar afbrigðalíkan afurðar er reiknað út

## <a name="symptoms"></a>Einkenni

Þetta vandamál getur komið upp þegar eftirfarandi röð aðgerða er framkvæmd:

1. Settu upp þessar eigindir í afbrigðalíkani framleiðslu:

    - Innsláttur (heiltala)
    - Prósenta (tugabrot)
    - Niðurstaða (heiltala)

2. Stofna útreikning sem hefur eftirfarandi segð:

    *Niðurstaða* = *Inntak* × *Prósenta* ÷ 100

Í þessu tilvikum er niðurstaðan í heilli tölu ekki alltaf rétt sléttuð. Til dæmis ef innslátturinn er 1000 og prósentan er 2,40 er búist við að niðurstaða heiltölunnar verði 24 þar sem 2,40 prósent af 1000 er 24 (eða 24,00 á tugabrotssniði). Þess í stað er útkoman sýnd sem 23. Þegar prósentan er hins vegar 2,39 er útreikningurinn sléttaður í 24 í stað 23. Þegar prósenta er 2,50 er útreikningurinn sléttaður í 25, eins og búist er við.

## <a name="cause"></a>Orsök

Þetta vandamál kemur upp vegna þess hvernig Microsoft Solver Foundation táknar tölur í innra skipulagi með brotum. Fyrir dæmið á undan er niðurstaða útreikningsins þar sem prósentutalan er 2,40 er táknuð sem 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375. Þegar .NET endurgerir þetta gildi sem heiltölu er það aftur 23.

## <a name="resolution"></a>Lausn

Þessari hegðun verður ekki breytt vegna þess að aðrar aðstæður eru háðar henni. Í dæminu á undan er hægt að lagfæra vandamálið með því að nota aðra aukastafaeigind og útreikninga.

Til dæmis, setja upp eftirfarandi eigindir í afbrigðalíkani framleiðslu:

- Innsláttur (heiltala)
- Prósenta (tugabrot)
- ResultDecimal (tugir)
- ResultInteger (heiltala)

Síðan er hægt að bæta við eftirfarandi útreikningum:

- *ResultDecimal* = *Inntak* × *Prósenta* ÷ 100
- *ResultInteger* = *ResultDecimal*
