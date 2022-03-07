---
title: Hanna skilgreiningar til að búa til skjöl sem eru með forritsgögnum
description: Þetta efni útskýrir hvernig skal hanna skilgreiningar rafrænnar skýrslugerðar þannig að þær búi til rafrænt skjal. (Hluti 1 - Flytja inn skilgreiningar).
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f335721ee97919af20e73fc9da6c9bf07dcae50aca8f8904d144d75c2f4d7b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726262"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>Hanna skilgreiningar til að búa til skjöl sem eru með forritsgögnum

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]