--- 
title: "Stofna og flytja út greiðslur lánardrottna með ISO20022-greiðslusniði"
description: "Þetta ferli sýnir hvernig á að stofna greiðslulínur í greiðslubók lánardrottins og mynda greiðsluskrá lánardrottins með því að nota dæmi um ISO2022 millifærsla fjármuna."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cc90bc86cd489b124a806c480632dd53ba47f3f
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Stofna og flytja út greiðslur lánardrottna með ISO20022-greiðslusniði

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig á að stofna greiðslulínur í greiðslubók lánardrottins og mynda greiðsluskrá lánardrottins með því að nota dæmi um ISO2022 millifærsla fjármuna. 

Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF.

Þetta fimmta ferli af fimm sem sýna greiðsluferlinu lánardrottins með því að nota grunnstillingar fyrir rafræna skýrslugerð. Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="create-payment-lines"></a>Stofna greiðslulínur
1. Fara í Viðskiptaskuldir > Greiðslur > Greiðslubók.
2. Smellið á „Nýtt“.
3. Í listanum skal merkja valda línu.
4. Sláið inn eða veldu gildi í reitnum heiti.
5. Smellið á „Línur“.
6. Smellt er á Greiðslutillögur
7. Smellt er á Stofna greiðslutillögu
8. Útvíkka Færslur til að taka hluta.
9. Smellt er á Síu.
10. Á listanum, veljið línuna fyrir töflu Lánardrottna reitinn fyrir lánardrottnalykil.
11. Í reitinn Skilyrði skal slá inn eða veldu gildi.
    * Þú getur notað hvaða skilyrði sem er til að velja lánardrottnafærslur til að greiða, í þessu dæmi notaðu DE-001 sem lánardrottnalykil.  
12. Smellið á „Í lagi“.
13. Smellið á „Í lagi“.
14. Smellt er á Stofna greiðslur.

## <a name="generate-an-iso20022-payment-file"></a>Mynda ISO20022-greiðsluskrá


