--- 
title: "Flytja inn skilgreiningar til að búa til skjöl sem eru með forritsgögnum"
description: "Til að ljúka þessum skrefum í ferlinu verður fyrst að ljúka við ferlið „Rafræn skýrslugerð Stofna skilgreiningarveitu og merkja hana sem virka“."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.openlocfilehash: 1637ba59525f5f8bd9fe41a00c34eca90f7a2751
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---
# <a name="import-configurations-to-generate-documents-that-have-application-data"></a>Flytja inn skilgreiningar til að búa til skjöl sem eru með forritsgögnum

[!include [task guide banner](../../includes/task-guide-banner.md)]

Til að ljúka þessum skrefum í ferlinu verður fyrst að ljúka við ferlið „Rafræn skýrslugerð Stofna skilgreiningarveitu og merkja hana sem virka“.

Skrefin í þessu ferli sýna hvernig skal hanna Rafræna skýrslugerð (ER) grunnstillingar þannig að þær búi til rafræn skjöl. Í þessu ferli muntu flytja inn þær grunnstillingar Rafræn skýrslugerð (ER) sem krafist er, sem hafa verið stofnaðar fyrir sýnifyrirtækið, Litware, Inc. og nota þær til að búa til rafræn skjöl. Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar. Skrefin er hægt að klára með því að nota DEMF gagnasafn. Áður en þú byrjar, skal hlaða niður og vista skrárnar sem eru á listanum í Hjálp efnisatriði, „Mynda rafræn skjöl og uppfæra gögn forrits með Rafræn skýrslugerð verkfæri“ (generate-electronic-documents-update-application-data/). Skrárnar eru Intrastat (líkan).xml, Intrastat (vörpun).xml, og Intrastat (snið).xml.

1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
    * Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt Virk. Ef þú sérð skilgreiningarveituna ekki, skal klára skrefin í ferlinu, Stofna skilgreiningarveitu og merkja hana sem virka.  
    * Skrefin í þessu ferli sýna hvernig skal nota getu Rafræn skýrslugerð til að ljúka við uppfærslu á gögnum forrits og hvernig á að búa til Intrastat-skýrslu Upplýsingar um skýrslugerðarferlið eru skjalaðar í töflum forritsins. Þegar Intrastat-skýrslugerðarferlið er virkjað úr Intrastat skjámyndinni, er skjölun framkvæmd og byggð á rökfræðinni sem var forrituð í fyrirliggjandi frumkóða. Í þessu ferli muntu grunnstilla sambærilega en einfaldaða rökfræði fyrir gögn forritsins með því að nota eingöngu umgjörð Rafræn skýrslugerð. Frumkóðanum verður ekki breytt.   

## <a name="import-er-configurations"></a>Flytja inn rafræn skýrslugerð grunnstillingar
1. Smelltu á Grunnstillingar skýrslugerðar
2. Smellt er á Skipta út.
3. Smellt er á Hlaða úr XML-skrá.
    * Flytja inn grunnstillingu líkans Rafræn Skýrslugerð sem inniheldur gagnalíkan sem er hannað til notkunar sem gagnaveita fyrir tilbúning Intrastat-skýrslunnar. Seinna, muntu útvíkka þessa skilgreiningu gagnalíkans til að nota það fyrir uppfærslu gagna forrits til að skjala upplýsingar Intrastat skýrslugerðaferlisins.   
    * Flettið og veljið  Intrastat (líkan).xml skrána.  
4. Smellið á „Í lagi“.
5. Í trénu skal velja „Intrastat (líkan)“.
6. Smellið á Hönnuður.
7. Í trénu skal víkka út „Fyrir skjöl á útleið“.
8. Í trénu skal víkka út „Fyrir skjöl á útleið\Færslur“.
    * Yfirfara skipan innflutt gagnalíkans. Athugið að rótaratriði „Fyrir skjal á útleið“ er skilgreint til að tilgreina gagnaflæði sem er notað til að sækja gögn frá forritinu og nota þau sem gagnaveitu til að búa til Intrastat skýrsluna. „Færslurnar (Skráaralisti)“ er notaður til að sýna listann yfir Intrastat færslur sem verður að skrá. Þar sem þú munt skjala skráða vörukóða, er þörf á einkvæmu kennimerki eins vörukóða „Vara skrá kenni (Int64)“ í þessu gagnaflæði.   
9. Lokið síðunni.
10. Smellt er á Skipta út.
11. Smellt er á Hlaða úr XML-skrá.
    * Flytja inn grunnstillingu vörpunar Rafræn skýrslugerð sem tilgreinir gagnaflæðið til að sækja gögn frá forritinu og síðan nota það til að bút til Intrastat skýrsluna. Seinna, muntu útvíkka þessa skilgreiningu vörpunar líkans til að sækja gögn úr Intrastat skýrslunni og nota þau fyrir uppfærslu gagna forrits til að skjala upplýsingar Intrastat skýrslugerðaferlisins.   
    * Flettið og veljið  Intrastat (vörpun).xml skrána.  
12. Smellið á „Í lagi“.
13. Í trénu skal víkka út „Intrastat (líkan)“.
14. Í trénu skal velja „Intrastat (líkan)\Intrastat (vörpun)“.
15. Smellið á Hönnuður.
    * Athugið að núverandi vörpun líkans inniheldur gildið „Til líkans“ í reitnum Stefna. Þetta þýðir að þessi vörpun líkans hefur verið hönnuð til þess að sækja gögn frá forritinu og geyma það í gagnalíkaninu.  
16. Smellið á Hönnuður.
17. Stækkið „Listi“ í trénu.
18. Í trénu skal víkka út „Færslur= Listi“.
    * Yfirfara skipan vörpunar líkans sem notar gagnalíkanið sem inniheldur afmörkun byggða á rótaratriðinu, „Fyrir skjal á útleið.“ Athugið að viðbætt gagnaveita „Listi“ veitir aðgang að þeim gögnum forrits sem er krafist, sem er listi skráa úr Intrastat töflunni.  
19. Lokið síðunni.
20. Lokið síðunni.
21. Smellt er á Skipta út.
22. Smellt er á Hlaða úr XML-skrá.
    * Flytja inn Rafræn skýrslugerð grunnstilling sem tilgreinir útlit Intrastat skýrslunnar og ferlið að fylla út gögn til skýrslunnar. Seinna, muntu útvíkka þessa sniðsskilgreiningu til að setja gögn úr Intrastat skýrslunni inn í gagnalíkanið og nota það síðan fyrir uppfærslu gagna forrits til að skjala upplýsingar Intrastat skýrslugerðaferlisins.   
    * Flettið og veljið  Intrastat .xml skrána.  
23. Smellið á „Í lagi“.
24. Í trénu skal velja „Intrastat (líkan)\Intrastat (Snið)“.
25. Smellið á Hönnuður.
26. Smellt er á Víkka/draga saman.
27. Í trénu skal velja „Skrá\Framtal“.
28. Smelltu á flipann Vörpun.
29. Í trénu skal velja „Skrá“.
    * Fara yfir skipan sniðsins sem er notað til að búa til Intrastat skýrlsuna. Athugið að það er hannað til að búa til XML skrá með því að fylla út í gögn frá gagnalíkaninu, sem er byggt á rótaratriðinu „Fyrir skjöl á útleið“. Staðfesta að heiti skrárinnar sem búin er til sé skilgreint á svargluggaskjámynd notanda („fn“ gagnaveita er notuð til þess).   
30. Lokið síðunni.


