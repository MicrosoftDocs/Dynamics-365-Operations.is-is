---
title: Stofna innkaupapöntun sem stjórnast af fjárhagsáætlun
description: Nota þetta ferli til að stofna innkaupapöntun sem er athuguð í tiltækri fjárhagsáætlun.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0054745394d6a21599d8f07605f78ffdd7f575ab
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150540"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Stofna innkaupapöntun sem stjórnast af fjárhagsáætlun

[!include [banner](../../includes/banner.md)]

Nota þetta ferli til að stofna innkaupapöntun sem er athuguð í tiltækri fjárhagsáætlun. Þessi skráning notar USMF sýnigagnafyrirtæki.


## <a name="review-the-budget-control-configuration"></a>Yfirfara skilgreiningu fjárhagsáætlunarstýringar
1. Fara í Fjárhagsáætlun > Uppsetning > fjárhagsáætlunarstýring > uppsetning fjárhagsáætlunarstýringar.
2. Smella á flipann Tiltækt fjármagn úr fjárhagsáætlun.
3. Smella á flipann Skjöl og færslubækur
4. Smella á flipann Skilgreina reglur fjárhagsáætlunarstýringar
5. Smella á flipann Skilgreina fjárhagsáætlunarflokka
6. Lokið síðunni.

## <a name="create-the-purchase-order-header"></a>Stofna haus innkaupapöntunar
1. Fara í innkaup og aðföng > innkaupapöntun  > allar innkaupapantanir.
2. Smellið á „Nýtt“.
3. Færa inn eða veljið gildi í svæðinu lánardrottnalykill.
4. Útvíkka eða draga saman hlutann Almennt.
5. Í reitnum Dagsetning reikningsskila skal stilla dagsetningu á „2016-01-01“.
6. Smellið á „Í lagi“.

## <a name="add-a-purchase-order-line"></a>Bæta við innkaupapöntunarlína
1. Slá inn eða velja gildi í reitnum innkaupategund.
2. Stilla magn á „2“.
3. Í reitinn eining skal slá inn eða velja gildi.
4. Stilla Einingarverð á „10000“.
5. Smelltu á Fjárhagur.
6. Smellt er á Dreifa upphæðum.
7. Í reitnum Fjárhagslykill skal tilgreina gildin „601300-001-023--“.
8. Lokið síðunni.

## <a name="perform-budget-checking"></a>Framkvæma athugun á fjárhagsáætlun
1. Smelltu á Fjárhagur.
2. Smella á Framkvæma athugun á fjárhagsáætlun
3. Smelltu á Fjárhagur.
4. Smella á athugun á villum eða viðvörunum í fjárhagsáætlun
5. Smellið á „Loka“.

