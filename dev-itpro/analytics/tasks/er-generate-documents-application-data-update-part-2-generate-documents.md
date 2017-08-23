--- 
title: "Mynda skjöl með uppfærslu forritsgagna fyrir rafræna skýrslugerð (ER)"
description: "Til að ljúka þessum skrefum í ferlinu verður fyrst að ljúka við ferlið, Rafræn skýrslugerð Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 1: Flytja inn grunnstillingar)."
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f10faaaffeb7df5be0b37a9b8dbfa5db5c24d2a2
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a>Mynda skjöl með uppfærslu forritsgagna fyrir rafræna skýrslugerð (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Til að ljúka þessum skrefum í ferlinu verður fyrst að ljúka við ferlið, Rafræn skýrslugerð Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 1: Flytja inn grunnstillingar).



Skrefin í þessu ferli sýna hvernig skal hanna Rafræna skýrslugerð (ER) grunnstillingar þannig að þær búi til rafræn skjöl. Í þessu ferli keyrirðu innfluttar grunnstillingar sniðs fyrir Rafræn skýrslugerð, sem hafa verið stofnaðar fyrir sýnifyrirtækið, Litware, Inc. til að mynda rafræn skjöl.



Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar. Skrefin er hægt að klára með því að nota DEMF gagnasafn. 



Áður en hafist er handa, skal breyta löndum samhengi fyrir DEMF fyrirtæki úr DEU (Þýskaland) yfir í BEL (Belgía). Smellið á Fyrirtækjastjórnun > Fyrirtæki > Lögaðilar til að uppfæra landskóðann á aðalaðsetri lögaðilans DEMF. Endurræsið umsókn


## <a name="run-imported-er-format"></a>Keyra innflutt Rafræn skýrslugerð snið
1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
2. Í trénu skal víkka út „Intrastat (líkan)“.
3. Í trénu skal velja „Intrastat (líkan)\Intrastat (Snið)“.
4. Smellið á „Keyra“.
    * Keyrið drög að útgáfu Rafræn skýrslugerð grunnstillingar til að mynda Intrastat skýrsluna.  
5. Í reitinn Færið inn skráarheiti, skal rita „intrastat.xml“.
    * Tilgreinið heiti skrárinnar.  
6. Smellið á „Í lagi“.
    * Yfirfara myndaða XML-skrá  
7. Lokið síðunni.
8. Fara í Skattur > Yfirlýsingar > Erlend viðskipti > Intrastat.
    * Opnið þessa skjámynd til að skoða Intrastat færslur sem eru innifaldar í rafrænt skjalið sem er myndað.  
9. Smellið á Intrastat-safn.
    * Þar sem keyrt snið Rafræn skýrslugerð inniheldur engar stillingar fyrir uppfærslu gagna forrits, hafa upplýsingar tilbúinnar Instrastat skýrslu ekki verið skjöluð.  
10. Lokið síðunni.
11. Lokið síðunni.


