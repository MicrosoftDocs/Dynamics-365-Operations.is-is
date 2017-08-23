--- 
title: "Setja upp greiðslumáta fyrir ISO20022-beingreiðslur"
description: "Þessi verklýsing sýnir hvernig á að setja upp greiðsluhátt viðskiptavinar fyrir ISO20022 beingreiðsla eða hvers kyns aðra greiðslugerð sem notar rafræn skýrslugerð."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 16ff0cc28b272add80b08ae43b9fe5b8e7370b70
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a>Setja upp greiðslumáta fyrir ISO20022-beingreiðslur

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að setja upp greiðsluhátt viðskiptavinar fyrir ISO20022 beingreiðsla eða hvers kyns aðra greiðslugerð sem notar rafræn skýrslugerð. 



Áður en lokið er við þetta verkefni verður að hafa skilgreiningu útflutningssniðs og greiðslulyklar sett upp.



Þetta ferli var stofnuð með því að nota sýnigögn fyrirtækisins DEMF.



Þetta er þriðja af fimm ferlum sem lýsa greiðsluferlinu viðskiptavinar með grunnstillingar fyrir rafræna skýrslugerð.

1. Farðu í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.
2. Nota flýtiafmörkun til að finna færslur Til dæmis síu á í Greiðsluaðferðarsvæðinu með gildið 'RAFRÆNA'.
3. Smella á Breyta.
4. Tilgreindu gildi 'DEMF OPER' í svæði greiðslulykils.
5. Útvíkka hlutann Skráarsnið.
6. Velja skal Já í Almennan rafræna skýrslugerð svæði.
7. Færa inn eða velja gildi í reitnum skilgreiningu útflutningssniðs.
    * Á listanum, veljið ISO20022 beingreiðsla (DE).  Ef listi er auður er skilgreining greiðsluútflutnings viðskiptavinar ekki innfluttu og virkt.  
8. Velja skal Já í svæðinu krefjast umboðs.
    * Veljið færibreyturna krefjarst umboðs fyrir greiðslusnið viðskiptavinar, sem krefjast þess að innifela upplýsingar um umboð í greiðskuskilaboðunum, eins og Sepa-beingreiðsla.  
9. Smellið á „Vista“.


