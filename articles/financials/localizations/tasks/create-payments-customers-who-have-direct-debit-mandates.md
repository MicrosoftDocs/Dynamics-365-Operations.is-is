--- 
title: "Stofna greiðslur fyrir viðskiptavin sem hefur beingreiðsluumboð"
description: "Þetta verk fer í gegnum hvernig á að mynda ISO20022-beingreiðsluskrá fyrir viðskiptavin sem hefur skilgreint beingreiðslu og reikning til greiðslu."
author: mrolecki
manager: AnnBe
ms.date: 10/14/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: acd6a8076288d8d1d1aa05af33e306c6a29780f7
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>Stofna greiðslur fyrir viðskiptavin sem hefur beingreiðsluumboð

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta verk fer í gegnum hvernig á að mynda ISO20022-beingreiðsluskrá fyrir viðskiptavin sem hefur skilgreint beingreiðslu og reikning til greiðslu. Stofna og bóka reikning er valfrjáls. Í stað þess að láta borga reikning geturðu valið umboð í færslubók áður en mynduð er greiðsluskrá, til að styðja við aðstæður fyrirframgreiðslu viðskiptavinar.



Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF.



Þetta er fimmta af fimm ferlum sem lýsa greiðsluferlinu viðskiptavinar með grunnstillingar fyrir rafræna skýrslugerð. Áður en hægt er að ljúka þessu verki, verður að klárað fyrri verkefni. Fyrst þarf að flytja inn skilgreiningar rafænnar skýrslugerðar fyrir greiðsla viðskiptavinar, að skilgreina greiðsluhátt fyrir greiðslur og setja upp þínar fyrirtækis og viðskiptavinar. 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a>Bóka reikningur með frjálsum texta með upplýsingum fyrir beingreiðsla
1. Fara í Viðskiptakröfur > Reikningar > Allir reikningar með frjálsum texta.
2. Smellið á „Nýtt“.
3. Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.
    * Þú getur til dæmis valið DE-010.  
4. Færa inn eða velja gildi í reitnum greiðsluaðferð.
    * Til dæmis: velja Rafræna.  
5. Færa inn eða velja gildi í reitnum Kenni beingreiðsluumboðs.
6. Smella á bæta Við línu.
7. Í reitinn Lýsing skal slá inn gildi.
8. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
9. Færið inn númer í reitnum „Einingarverð“.
10. Smellið á „Bóka“.
11. Smellið á „Í lagi“.

## <a name="create-a-payment"></a>Stofna greiðsla
1. Fara í Viðskiptakröfur > Greiðslur > Greiðslubók.
2. Smellið á „Nýtt“.
3. Sláið inn eða veldu gildi í reitnum heiti.
4. Smellið á „Línur“.
5. Smellt er á Greiðslutillögur
6. Smellt er á Stofna greiðslutillögu
7. Útvíkka Færslur til að taka hluta.
8. Smellt er á Síu.
9. Á listanum, veljið línuna fyrir töflu fyrir færslur viðskiptavinar og reitinn greiðsluhátt.
    * Þú getur notað hvaða skilyrði sem er til að velja færslur viðskiptavinar til að greiða. Í þessu dæmis skal nota rafrænt sem greiðsluaðferð til að sía færslur.  
10. Í reitinn Skilyrði skal slá inn eða veldu gildi.
11. Smellið á „Í lagi“.
12. Smellið á „Í lagi“.
13. Smellt er á Stofna greiðslur.

## <a name="generate-a-payment-file"></a>Mynda greiðsluskrá


