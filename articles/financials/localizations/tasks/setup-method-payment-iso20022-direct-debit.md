---
title: Setja upp greiðsluhátt fyrir ISO20022-beingreiðsla
description: Þessi verklýsing sýnir hvernig á að setja upp greiðsluhátt viðskiptavinar fyrir ISO20022 beingreiðsla eða hvers kyns aðra greiðslugerð sem notar rafræn skýrslugerð.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d3c6d8157803e0a8d33520a0cd64fb725e8c9a3
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848648"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>Setja upp greiðsluhátt fyrir ISO20022-beingreiðsla

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

