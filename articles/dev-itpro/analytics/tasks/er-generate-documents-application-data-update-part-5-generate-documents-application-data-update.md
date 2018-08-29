--- 
title: "Búa til skjöl sem eru með forritsgögnum"
description: "Til að ljúka skrefunum í þessu ferli verður fyrst að ljúka við ferlið, „Rafræn skýrslugerð Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 4: Breyta sniði)“."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 90c6ebc456d3e137e43022fad7d59ce3ca2cdcab
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---
# <a name="generate-documents-that-have-application-data"></a>Búa til skjöl sem eru með forritsgögnum

[!include [task guide banner](../../includes/task-guide-banner.md)]

Til að ljúka skrefunum í þessu ferli verður fyrst að ljúka við ferlið, „Rafræn skýrslugerð Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 4: Breyta sniði)“.



Skrefin í þessu ferli sýna hvernig skal hanna Rafræna skýrslugerð (ER) grunnstillingar þannig að þær búi til rafræn skjöl og uppfæri gögn fyrir forrit. Í þessu ferli er Rafræn skýrslugerð grunnstillingar látnar mynda Intrastat skýrsluna og uppfæra hugbúnaðargögn fyrir safnupplýsingar skýrlugerðarferlisins.



Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar. Skrefin er hægt að klára með því að nota DEMF gagnasafn. Áður en hafist er handa, vertu viss um að land samhengi fyrir DEMF fyrirtæki úr DEU sé BEL (Belgía).


## <a name="set-up-foreign-trade-parameters"></a>Setja upp færibreytur erlendra viðskipta
1. Fara í Skattur > Uppsetning > Erlend viðskipti > Færibreytur erlendra viðskipta.
2. Smellt er á flipann Númeraraðir.
    * Skjala upplýsingar um Intrastat skýrslugerð, við þurfum að bera kennsl á skrár fyrir hvert safn sem við búum til. Fyrir það verður að skilgreina sérstök númeraröð.  
3. Veljið „Intrastat safnkenni“ tilvísunina“.
4. Í reitinn kóði númeraraðar skal slá inn gildi.
    * Í reitnum „Kóði númeraraðar“, skal færa inn eða velja gildið „Fremri_2“.  
5. ÚtkljáBreytingar Kóði númeraraðar. 
6. Smellið á „Vista“.
7. Lokið síðunni.

## <a name="run-modified-er-format"></a>Keryra breytt snið Rafræn skýrslugerð
1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
2. Í trénu skal víkka út „Intrastat (líkan)“.
3. Í trénu skal velja „Intrastat (líkan)\Intrastat (Snið)“.
4. Smellið á „Keyra“.
5. Í reitinn Færið inn skráarheiti skal rita „intrastat2.xml“.
    * intrastat2.xml  
6. Smellið á „Í lagi“.

## <a name="review-er-format-executions-results"></a>Yfirfara snið Rafræn skýrslugerð niðurstöður framkvæmdar
    * Yfirfara myndaða XML-skrá  
1. Lokið síðunni.
2. Fara í Skattur > Yfirlýsingar > Erlend viðskipti > Intrastat.
    * Opnið þessa skjámynd sem inniheldur Intrastat færslur sem hafa verið innifaldar í rafrænt skjal sem er myndað.  
3. Smellið á Intrastat-safn.
    * Þar sem framkvæmt snið Rafræn skýrslugerð inniheldur nú stillingar fyrir gagnauppfærslu fyrir forrit, hafa upplýsingar um Intrastat skýrslugerðina í heild verið skjöluð. Í þessari skjámynd er hægt að sjá skráningarhaus safnsins sem stofnað var.  
4. Smellið á Details.
    * Í þessari skjámynd er hægt að sjá upplýsingar um safnið sem stofnað var.  
5. Lokið síðunni.
6. Lokið síðunni.
7. Lokið síðunni.


