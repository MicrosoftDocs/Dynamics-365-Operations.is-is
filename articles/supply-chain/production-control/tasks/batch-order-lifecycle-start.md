---
title: Ferill runupöntunar frá stofnun til upphafs
description: Þetta ferli fer í gegnum fyrsti hluti lífsferlisins runupöntun.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6484c1954ff4cc600938adb07b5384f1edce8bf7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "343122"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a>Ferill runupöntunar frá stofnun til upphafs

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli fer í gegnum fyrsti hluti lífsferlisins runupöntun.

Frá stofnun, kostnaður mat og yfir framleiðslu vinnsluröðun til raunveruleg upphafsdagsetning fyrir runupöntun.



Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. 



Skilyrði til að keyra ferlið með annarri gagnamengi eru útgefin afurð með virka útgáfu formúlu og leiðarútgáfa.


## <a name="create-a-batch-order"></a>Stofna runupöntun
1. Fara í Allar framleiðslupantanir.
2. Smellt er á Ný runupöntun
3. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
4. Smellið á Stofna.
5. Nota flýtiafmörkun til að sía í reitnum afurð með gildið „b“.

## <a name="view-production-formula-and-expected-co-products"></a>Skoða framleiðsluformúlu og áætlaða aukaafurðir
1. Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.
2. Smellt er á Formúlu.
3. Lokið síðunni.
4. Smellt er á aukaafurðir.
5. Lokið síðunni.

## <a name="estimate-the-batch-order"></a>Áætla runupöntunina
1. Smellt er á Mat.
2. Smellið á „Í lagi“.
3. Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.
4. Smellt er á Skoða útreikningsupplýsingar.
5. Lokið síðunni.

## <a name="release-the-batch-order"></a>Losa runupöntunina
1. Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.
2. Smellið á „Gefa út“.
3. Smellið á „Í lagi“.

## <a name="schedule-production-jobs"></a>Áætla framleiðsluverk
1. Í Aðgerðarrúðunni er smellt á Áætlun.
2. Smella á Áætla verk.
3. Veljið Nei í svæðinu Takmarkaða afkastaveita.
4. Veljið Nei í svæðinu Takmarkað efni.
5. Smellt er á Í lagi.
6. Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.
7. Smellt er á Allar vinnslur.
8. Lokið síðunni.

## <a name="start-the-batch-order"></a>Ræsið runupöntunina
1. Smellið á „Byrja“.
2. Smellið á flipann „Almennt“.
3. Veljið „Nei“ á svæðinu „Bóka tiltektarlista núna“.
4. Smellið á „Í lagi“.
5. Smellið á „Skoða“ á aðgerðarúðunni.
6. Smellt er á tiltektarlista.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Lokið síðunni.
9. Lokið síðunni.
10. Smellt er á Leiðarspjald.
11. Í listanum skal smella á tengilinn í valinni línu.
12. Lokið síðunni.
13. Lokið síðunni.

