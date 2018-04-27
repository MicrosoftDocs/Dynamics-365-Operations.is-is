--- 
title: "Skilgreina fjárhagsvíddir"
description: "Þessi leiðarvísir fyrir verk sýnir hvernig bætt er við einingu afrita fjárhagsvídd og sérstillta fjárhagsvídd."
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0b72acf763f0f6dbc64c3e00986bc9eb0e366bb5
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="define-financial-dimensions"></a>Skilgreina fjárhagsvíddir

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísir fyrir verk sýnir hvernig bætt er við einingu afrita fjárhagsvídd og sérstillta fjárhagsvídd.  Leiðbeiningarnar nota USMF sýnigögn fyrirtækið.


## <a name="create-an-entity-backed-financial-dimension"></a>Stofna fjárhagsvídd afritaðra eininga.
1. Fara í fjárhag > Línurit yfir lykla > Víddir > Fjárhagsvíddir.
2. Smellið á „Nýtt“.
3. Í reitnum Notandagildi úr reit skal velja kerfisskilgreinda einingu til að byggja fjárhagsvíddir á. 
4. Í reitinn Heiti víddar skal slá inn gildi til að lýsa fjárhagsvídd.
    * Heitið getur verið annað en kerfisskilgreind eining en má ekki innihalda bil eða sérstafi.  
5. Smellið á Virkja.
    * Virkjun fjárhagsvíddar uppfærir töflu með fjárhagsvíddarheitinu og fjarlægir eyddum víddum. Hægt er að færa inn víddargildi áður en fjárhagsvídd er virkjuð en fjárhagsvídd er ekki hægt að nota fyrr en hún er virkjuð.  
6. Smellið á skilaboðin Loka við virkjun.
7. Smellið á Virkja.
    * Hægt er að tímasetja virkjun víddar þannig að hún keyri í runu á tilteknum degi og tíma.  
8. Smellt er á víddargildi.
    * Sum víddargildi eru bundin fyrirtæki. Hægt er að staðfesta hvort þær eru bundnar fyrirtæki með því hvort heiti fyrirtækisins er sýnt í lista yfir víddargildi.  

## <a name="create-a-custom-financial-dimension"></a>Stofna sérstillta fjárhagsvídd
1. Lokið síðunni.
2. Smellið á „Nýtt“.
3. Á Nota virði frá svæðinu, veljið <Custom dimension>.
4. Í reitinn Heiti víddar skal slá inn gildi til að lýsa fjárhagsvídd.
    * Heitið getur ekki innihaldið bil eða sérstafi.  
    * Einnig er hægt að tilgreina lykilsíu til að takmarka magn og gerð upplýsinga sem hægt er að færa inn víddargildi fyrir.   
    * Hægt er að færa inn stafi sem eru þeir sömu og fyrir hvert víddargildi eins og stafi eða bandstrik. Einnig er hægt að færa inn tákn (#) og merki (&) sem frátakara fyrir stafi og tölustafi sem breytast í hvert skipti sem víddargildi eru stofnuð. Nota skal númeratákn (#) sem frátakara fyrir tölustafi og merki (&) sem frátakara fyrir stafi.  Dæmi: Til að takmarka víddargildi við stafina CC og þrjár tölur færirðu inn CC-### sem sniðsíu.  
5. Smellið á Virkja.
    * Virkjun fjárhagsvíddar uppfærir töflu með fjárhagsvíddarheitinu og fjarlægir eyddum víddum. Hægt er að færa inn víddargildi áður en fjárhagsvídd er virkjuð en fjárhagsvídd er ekki hægt að nota fyrr en hún er virkjuð.  
6. Smellið á Virkja.
    * Hægt er að tímasetja virkjun víddar þannig að hún keyri í runu á tilteknum degi og tíma.  
7. Smellt er á víddargildi.
8. Smellið á „Nýtt“.
9. Í svæðinu Víddargildi skal slá inn nafn til að lýsa því fjárhagsvíddargildi.
10. Í reitnum Lýsing skal færa inn lýsingu sem lýsir fjárhagsvíddargildi.


