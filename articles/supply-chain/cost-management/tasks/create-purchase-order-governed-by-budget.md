---
title: Stofna innkaupapöntun sem stjórnast af fjárhagsáætlun
description: Nota þetta ferli til að stofna innkaupapöntun sem er athuguð í tiltækri fjárhagsáætlun.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e2bfec4d7d38ef95d1f0ce3bd89938337ecf731
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572050"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]