---
title: Úrræðaleit fyrir afurðaafbrigðastilli
description: Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með afurðarafbrigðastilli.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dacc7205eaf2084f6fbd3be9d8ac0572f9e1bcde
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516807"
---
# <a name="troubleshoot-the-product-configurator"></a>Úrræðaleit fyrir afurðaafbrigðastilli

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með afurðarafbrigðisstilli.

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a>Skrifað er yfir vörutexta þegar ég skilgreini afurð á sölupöntunarlínu.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þetta vandamál á sér stað þegar sölupöntunarlína er stofnuð fyrir skilgreinanlega vöru og textanum er svo breytt. Þegar varan er grunnstillt og **Í lagi** er svo valið skrifað yfir textann með staðlaða textanum.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Búist er við þessari hegðun. Textasvæðið inniheldur heiti vöruvíddasamsetningar sem er aðeins fyllt út eftir að lína hefur verið skilgreind. Þess vegna verður að breyta textanum eftir að lína hefur verið skilgreind og ekki áður.

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Heiltölueigindir eru rangt sléttaðar þegar afbrigðalíkan afurðar er reiknað út.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þetta vandamál getur komið upp þegar eftirfarandi röð aðgerða er framkvæmd:

1. Setja upp eftirfarandi eigindir í afbrigðalíkani framleiðslu:

    - Innsláttur (heiltala)
    - Prósenta (tugabrot)
    - Niðurstaða (heiltala)

2. Stofna útreikning sem hefur eftirfarandi segð:

    *Niðurstaða* = *Inntak* × *Prósenta* ÷ 100

Í þessu tilvikum er niðurstaðan í heilli tölu ekki alltaf rétt sléttuð. Til dæmis er inntak 1.000 og prósenta er 2,40. Þess vegna er búist við að heiltalan verði 24, þar sem 2,40 prósent af 1.000 er 24 (eða 24,00 á tugabrotssniði). Þess í stað er útkoman sýnd sem 23. Þegar prósentan er hins vegar 2,39 er útreikningurinn sléttaður í 24 í stað 23. Þegar prósenta er 2,50 er útreikningurinn sléttaður í 25, eins og búist er við.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þetta vandamál kemur upp vegna þess hvernig Microsoft Solver Foundation táknar tölur í innra skipulagi með brotum. Fyrir dæmið á undan er niðurstaða útreikningsins þar sem prósentutalan er 2,40 er táknuð sem 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375. Þegar .NET endurgerir þetta gildi sem heiltölu er það aftur 23.

Þessari hegðun verður ekki breytt vegna þess að aðrar aðstæður eru háðar henni. Í dæminu á undan er hægt að lagfæra vandamálið með því að nota aðra aukastafaeigind og útreikning.

Þú getur til dæmis sett upp eftirfarandi eigindir í afbrigðalíkan framleiðslu:

- Innsláttur (heiltala)
- Prósenta (tugabrot)
- ResultDecimal (tugir)
- ResultInteger (heiltala)

Síðan er hægt að bæta við eftirfarandi útreikningum:

- *ResultDecimal* = *Inntak* × *Prósenta* ÷ 100
- *ResultInteger* = *ResultDecimal*
