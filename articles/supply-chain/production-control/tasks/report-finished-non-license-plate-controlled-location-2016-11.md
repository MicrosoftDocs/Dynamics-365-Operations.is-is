---
title: Skrá sem lokið í ekki númeraplötustýrð staðsetningu (Notkun, maí 2016)
description: Þessi verkefnaleiðbeiningar sýnir dæmi um skýrslugerð sem lokið á staðsetningu sem ekki – númeraplötustýrð.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9aeac631e32876d6c19cb964f28e65491137049a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204497"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>Skrá sem lokið í ekki númeraplötustýrð staðsetningu (Notkun, maí 2016)

[!include [banner](../../includes/banner.md)]

Þessi verkefnaleiðbeiningar sýnir dæmi um skýrslugerð sem lokið á staðsetningu sem ekki – númeraplötustýrð. Gildandi vinnureglu er skilyrði fyrir þetta verk. Fyrri verkefnaleiðbeiningar sýna uppsetningu vinnureglu. Þessi leiðarvísi fyrir verk krefst AX forrit 7.0.1 eða síðar.




## <a name="set-up-an-output-location"></a>Setja upp staðsetningu úttaks
1. Fara á fyrirtækisstjórnun > Tilföng >Tilfangaflokka.
2. Á listanum, veljið tilfangaflokk 5102
3. Smella á Breyta.
4. Í úttaksvöruhús svæðinu veljið 51.
5. Í staðsetning úttaks svæðinu sláið inn 001.
    * Staðsetning 001 ekki númeraplötustýrð staðsetningu. Hægt er að setja upp staðsetningu úttaks ekki númeraplötu aðeins ef gildandi vinnureglu er til fyrir staðsetningarinnar.  

## <a name="create-a-production-order-and-report-it-as-finished"></a>Stofna framleiðslupöntun og skrá sem lokið.
1. Lokið síðunni.
2. Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.
3. Smella á Ný framleiðslupöntun.
4. Í vörunúmer svæðið sláið inn L0101.
5. Smellið á Stofna.
6. Á Aðgerðasvæðinu skal smellt á framleiðslupöntun.
7. Smellt er á Mat.
8. Smellt er á Í lagi.
9. Smellt er á Byrja.
10. Smellt er á flipannAlmennt.
11. Veljið ‚Aldrei‘ í reitnum Sjálfvirk uppskriftarnotkun.
12. Smellt er á Í lagi.
13. Smellið á Bóka sem tilbúið.
14. Smellt er á flipannAlmennt.
15. Velja skal Já í reitnum leyfa villu.
16. Smellt er á Í lagi.
17. Í aðgerðasvæðinu er smellt á vöruhús.
18. Smellt er á Upplýsingar um vinnu
    * Þegar framleiðslupöntunin var skráð sem lokið, engin vinna var mynduð fyrir frágangur. Þetta gerist vegna þess að vinna regla er skilgreind sem kemur í veg fyrir vinnu búnar til þegar afurð L0101 er skráð sem lokið á staðsetningu 001.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]