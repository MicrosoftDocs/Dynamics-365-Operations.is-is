--- 
title: "Stofna beingreiðsluumboð fyrir viðskiptavin"
description: "Þessi leiðarvísi fyrir verk sýnir stofnun umboð fyrir beingreiðsla -og nota hana á reikningi."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e1ac289c261922f013b679eecfb054390b8aef73
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Stofna beingreiðsluumboð fyrir viðskiptavin

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísi fyrir verk sýnir stofnun umboð fyrir beingreiðsla -og nota hana á reikningi.


## <a name="create-a-bank-account"></a>Stofna skal bankareikning.
1. Farið í Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir.
2. Veljið til dæmis U.S. 001
3. Í aðgerðasvæðinu er smellt á Viðskiptavinur.
4. Smellt er á bankareikninga.
5. Smellið á „Nýtt“.
6. Í reitinn Bankareikningar skal slá inn gildi.
7. Í reitinn Heiti skal slá inn gildi.
8. Í reitinn IBAN skal slá inn gildi.
9. Í reitinn Gjaldmiðill skal slá inn gildi.
10. Smellið á „Vista“.
11. Lokið síðunni.
12. Farið í Reiðufjár- og bankastjórnun > Bankareikningar > Bankareikningar.
13. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
14. Í listanum skal smella á tengilinn í valinni línu.
15. Smellið á „Breyta“.
16. Útvíkka aukakenni hluta.
17. Færa inn gildi í reitnum Kenni beingreiðslu.
18. Í reitinn IBAN skal slá inn gildi.
19. Lokið síðunni.
20. Lokið síðunni.

## <a name="define-the-electronic-payment-method"></a>Skilgreina rafrænu greiðsluaðferðina
1. Farðu í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.
2. Smellið á „Nýtt“.
3. Færa inn gildi í svæðinu greiðsluaðferð.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Greiðslugerð fyrir aðferð umboð fyrir beingreiðsla verður að vera Rafrænar greiðslur.
6. Velja skal Já í svæðinu krefjast umboðs.
7. Lokið síðunni.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Bæta umboð fyrir beingreiðsla við viðskiptavin
1. Farið í Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir.
2. Veljið til dæmis U.S. 001
3. Smellið á „Breyta“.
4. Útvíkka hlutann sjálfgildi Greiðslu.
5. Færa inn eða velja gildi í reitnum greiðsluaðferð.
6. Útvíkka hlutann sjálfgildi Greiðslu.
7. Útvíkka hlutann umboð fyrir beingreiðsla.
8. Smelltu á Bæta við.
9. Færa inn eða veljið gildi í svæðinu bankareikning.
10. Sláið inn eða veldu gildi í reitnum Bankareikningur Lánardrottins.
11. Færið inn fjölda greiðslna sem búist er við fyrir þetta umboð.
12. Smellið á „Í lagi“.
13. Smelltu á Prenta.
14. Smellt er á umboðsskýrsla.
15. Lokið síðunni.
16. Smellið á „Breyta“.
17. Færðu inn dagsetningu í svæðinu dagsetning undirskriftar
18. Smella á Já.
19. Færðu inn Staðurinn þar sem umboðið var undirritað
20. Smellið á „Í lagi“.
21. Lokið síðunni.

## <a name="create-a-free-text-invoice-with-mandate"></a>Stofna reikningur með frjálsum texta með umboði
1. Fara í Viðskiptakröfur > Reikningar > Allir reikningar með frjálsum texta.
2. Smellið á „Nýtt“.
3. Veljið þann viðskiptavin sem umboðið var bætt við.
4. Færa inn eða velja gildi í reitnum Kenni beingreiðsluumboðs.


