--- 
title: "Fara yfir skilgreiningar til að búa til skýrslur á Microsoft Office-sniði með innfelldum myndum fyrir rafræna skýrslugerð (ER)"
description: "Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í verkefnaleiðbeiningar „Rafræn skýrslugerð í MS Office sniði með ívafnar myndir (Hluti 1: Setja upp færibreytur)“."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 21e73f9e7e3fbab4c62786e689f72127598d1961
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="review-configurations-to-make-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er"></a>Fara yfir skilgreiningar til að búa til skýrslur á Microsoft Office-sniði með innfelldum myndum fyrir rafræna skýrslugerð (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í verkefnaleiðbeiningar „Rafræn skýrslugerð í MS Office sniði með ívafnar myndir (Hluti 1: Setja upp færibreytur)“.

Ferlið sýnir hvernig skal hanna Rafræna skýrslugerð (ER) grunnstillingar þannig að þær búi til rafræn skjöl sem innihalda ívafnar myndir í Microsoft Excel og Microsoft Word. Í þessu dæmi muntu yfirfara grunnstillingu Rafræn skýrslugerð fyrir dæmi um fyrirtæki, Litware, Inc. 

Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar. Skrefin er hægt að klára með því að nota USMF gagnasafnið.


## <a name="review-the-imported-data-model"></a>Yfirfara innflutt gagnalíkans
1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
2. Í trénu skal velja „Líkan fyrir ávísanir“.
3. Smellið á Hönnuður.
    * Þetta líkan er sett upp til að standa fyrir færslur lánardrottins frá viðskiptasjónarmiði og vörpun þessa líkans til gagnaveitu forritsins. Yfirfara líkanið með Rafræn skýrslugerð Rekstrar hönnuður. Athugið að eigindir líkaneininga sem eru birtar: skipan, nafn, lýsing, tegund gagna, osfrv.   
4. Stækkið „Rót“ í trénu.
5. Í trénu skal velja „rót\ávísanir“.
6. Í trénu skal víkka út „rót\ávísanir“.
7. Í trénu skal víkka út „rót\ávísanir\eigindir“.
8. Í trénu skal víkka út „rót\greiðandi“.
9. Í trénu skal velja „rót\erprufukeyrsla“.
10. Í trénu skal velja „rót\útlit“.
    * Útlitseiningar líkansins standa fyrir upplýsingar um útlitsform prentun ávísunar fyrir valinn bankareikning. Það inniheldur líka tvo hnúta frá tegund gagna Hólfs til að geyma myndir.   
11. Í trénu skal víkka út „rót\útlit“.
12. Í trénu skal velja „rót\útlit\fyrirtæki lógó“.
13. Í trénu skal víkka út „rót\útlit\fyrirtæki lógó“.
14. Í trénu skal velja „rót\útlit\fyrirtæki lógó\mynd“.
15. Í trénu skal velja „rót\útlit\fyrirtæki lógó\erprentað“.
16. Í trénu skal velja „rót\útlit\undirskrift“.
17. Í trénu skal víkka út „rót\útlit\undirskrift“.
18. Í trénu skal velja „rót\útlit\undirskrift\mynd“.
19. Í trénu skal velja „rót\útlit\undirskrift\erprentað“.
    * Athugið að tvær gagnalíkanseiningar eru bundnar reitum taflanna sem innihalda myndir af lógó fyrirtækisins og undirskrift frá viðurkenndum aðila á tvöföldu formi.  
20. Í trénu skal víkka út „rót\útlit\vatnsmerki“.
21. Smellt er á Varpa líkani á gagnagjafa.
22. Smellið á Hönnuður.
23. Í trénu skal víkka út „valdarávísanir“.
24. Í trénu skal víkka út „Útlit“.
25. Í trénu skal víkka út „útlit\fyrirtækjalógó“.
26. Í trénu skal víkka út „Útlit\Undirskrift“.
27. Í trénu skal víkka út „útlit\vatnsmerki“.
28. Kveikið á „Sýna upplýsingar“.
    * Athugið að gagnalíkanseiningar ávísananna eru bundnar TmpChequePrintout töflunni sem, við keyrslu, mun innihalda skrár fyrir ávísanir sem notandi hefur valið fyrir prentun.   
29. Lokið síðunni.
30. Lokið síðunni.
31. Lokið síðunni.

## <a name="review-the-imported-format"></a>Yfirfara innflutt snið
1. Í trénu skal víkka út „Líkan fyrir ávísanir“.
2. Í trénu skal velja „Líkan fyrir ávísanir\Ávísanir prentsnið“.
3. Smellið á Hönnuður.
4. Smellt er á viðhengi
5. Smellt er á Opin.
    * Opna viðhengt sniðmát skrár í Excel.  
    * Yfirfara viðhengt Ecxel-sniðmát skrárinnar sem verður notuð til að prenta ávísanirnar. Sniðmátið inniheldur tvær ávísanir fyrir hverja síðu og er hannað til að prenta ávísanir til forprentaðs forms. Athugið að tvær auðar myndir eru ívafðar. Þessar auðu myndir eru fyrir lógó fyrirtækisins og undirskrift þess aðila sem heimilar greiðslu. Staðfesta að myndirnar heita CompLogo og SignatureImage í Excel.   
6. Lokið síðunni.
7. Stækkið „skýrsla“ í trénu.
8. Í trénu skal víkka út „Skýrsla\ChequeLines“.
9. Í trénu skal velja 'Report\ChequeLines\CompLogo'.
10. Kveikið á „Sýna upplýsingar“.
    * Athugið að reitaeining „CompLogo“ sniðsins stendur fyrir Excel afurðina sem er notuð til að útfylla myndina af lógó fyrirtækisins í skýrslunni. Þetta sniðseining er bundin við myndgagnalíkanseininguna sem, við keyrslu,  inniheldur mynd af lógó fyrirtækisins í tvöföldu formi.   
11. Smelltu á flipann Vörpun.
12. Smella á virkja Breytingar.
    * Athugið að hægt er að búa til hólfeiningar sniðsins „CompLogo“ þannig að það er ekki lengur virkt. Þannig mun Excel myndeiningin sem þessu tengist fela lógó fyrirtækisins í skýrslunni sem búin er til. Ef segðin sem er virk skilar af sér SATT og skilgreind bindingin birtir enga mynd, mun Excel myndeiningin sem þessu tengist sýna mynd sem hefur verið vistuð í Excel sniðinu.   
13. Lokið síðunni.
14. Stækkið „merkimiða: Hólf“ í trénu.
    * Sumir merkimiðar sem birtast í forprentuðu ávísanaforminu verða með í skýrslunni þegar hún er stofnuð til prófunar. Þessir merkimiðar verða samt sem áður ekki prentaðir þegar raunprentun fer fram, vegna þess að forprentaða formið inniheldur þá nú þegar.  
15. Lokið síðunni.


