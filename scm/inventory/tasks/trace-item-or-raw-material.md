--- 
title: "Rekja vöru eða hráefni"
description: "Þetta ferli sýnir hvernig á að nota vörurakning til að auðkenna þar sem vörur eða hráefni hafa verið notaðar eða eru í notkun."
author: pjacobse
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: c4b093af672b2d4e1a2c91cd55470f9072d992c3
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="trace-an-item-or-raw-material"></a>Rekja vöru eða hráefni

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig á að nota vörurakning til að auðkenna þar sem vörur eða hráefni hafa verið notaðar eða eru í notkun. Með þessu ferli er hægt að greina vöru, rekja hann til baka í uppruna og svo áframrekja í gegnum framleiðslu og sölu á endanlegu vöruna. Hægt er að nota ferlið til að rannsaka viðskiptavini sem verða fyrir áhrifum, sölupantana sem verða fyrir áhrifum og fleira. Þessi aðferð notar sýnigögn fyrirtækisins USP2.


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>Rekja vöru með afturábak með þekkt rununúmer 
1. Farið í Birgðastjórnun > Fyrirspurnir og skýrslur > Rakningarvíddir > Vörurakning.
2. Í reitnum Vörunúmer velurðu P9100.
3. Í listanum skal smella á tengilinn í valinni línu.
4. í reitnum Áfram eða afturábak Veljið 'Afturábak' 
5. Í rununúmer reitinn, velja „as-12-344-01"
6. Í listanum skal smella á tengilinn í valinni línu.
7. Smellið á „Í lagi“.

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>Auðkenna vöru, rekja áfram og gera greiningu
    * Topphnútur trés sem birtist hér táknar magn á lager valinnar vöru og runu. Nauðsynlegt er að útvíkka hnúta í tré til að finna vöru sem á að keyra áframrakningu fyrir.   
1. Í trénu, Útvíkka 'hnúta sem er lýst fyrir neðan og veljið svo síðasta hnútinn.
    * Útvíkka: ' P9100 / 1 / 10 / as-12-344-01 ● 2 tunna ● 7.00 gal \P9100 ● Tiltekið ● sölupöntun 000072 22/12/2015 ● -1 tunna ● -4.00 gal ● Svæði = 1, Vöruhús = 10, rununúmer = as-12-344-01 \P9100 ● Framleiðsla B-000050 ● 12/9/2015● 7 tunna ● 27.00 gal ● Svæði =1,Vöruhús =10,Rununúmer =as-12-344-01 ● hliðarafurðir: P9101' og veldu síðan þann hnút.     
2. í trénu, Útvíkka 'hnúta lýst fyrir neðan og veljið svo þann hnút',
    * Frá hnút sem var nýverið valinn, Útvíkka ' M9103 ● framleiðslulínu B-000050 ● 12/9/2015 ● -160.00 lb ● Stærð = 70, Litur = í lagi, Svæði = 1, Vöruhús = 10, rununúmer = App01' og veldu síðan þann hnút.  
3. Smellt er á Rakning frá hnút.
4. Smellt er á Áfram.
5. Í aðgerðasvæðinu er smellt á rekja.
    * Það eru nokkrar rakningarkosti sem veita upplýsingar um viðskiptavini sem verða fyrir áhrifum af vörunni sem verið er að rekja, og sölupantanir sem tengjast vörunni sem hafa og hafa ekki verið sendar.   
6. Smellt er á Viðskiptavini.
7. Lokið síðunni.
8. Í aðgerðasvæðinu er smellt á rekja.
9. Smellt er á Sölupantanir sem voru sendar.
10. Lokið síðunni.


