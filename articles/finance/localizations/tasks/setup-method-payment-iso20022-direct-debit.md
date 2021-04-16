---
title: Setja upp greiðsluhátt fyrir ISO20022-beingreiðsla
description: Þessi verklýsing sýnir hvernig á að setja upp greiðsluhátt viðskiptavinar fyrir ISO20022 beingreiðsla eða hvers kyns aðra greiðslugerð sem notar rafræn skýrslugerð.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c6a692553867d7e8679099210dc44b9d9e4d0f1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838683"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>Setja upp greiðsluhátt fyrir ISO20022-beingreiðsla

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]