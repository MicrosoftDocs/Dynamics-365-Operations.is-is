--- 
title: "Mynda rafræn skjöl fyrir greiðslur með því að nota skilgreiningu sniðs í rafrænni skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur notað skilgreiningarsnið fyrir rafræna skýrslugerð (ER) til að búa til rafræn skjöl til að vinna úr greiðslum."
author: NickSelin
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a5d958d3b55bfa76f3cfbb3c1a289e4e89c49146
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="generate-electronic-documents-for-payments-using-a-format-configuration-for-electronic-reporting-er"></a>Mynda rafræn skjöl fyrir greiðslur með því að nota skilgreiningu sniðs í rafrænni skýrslugerð (ER)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur notað skilgreiningarsnið fyrir rafræna skýrslugerð (ER) til að búa til rafræn skjöl til að vinna úr greiðslum. Hægt er að framkvæma þessum skrefum í GBSI dæmi fyrirtækinu.

Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningu með snið á greiðsluskjali".


## <a name="change-the-configuration-of-the-electronic-payment-method"></a>Breyta grunnstillingu rafrænu greiðsluaðferðinni
1. Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.
2. Víxla hlutanum Skráarsnið til að víkka, ef þörf krefur.
3. Nota Síu á Flýtiræsistikunni til að leita að færslum. Til dæmis síu á í Greiðsluaðferðarsvæðinu með gildið rafræna
4. Smellið á „Breyta“.
5. Stilla Almenn rafræn skýrslugerð reitinn á Já.
    * Veldu já til að nota almenna rafræna skýrslumynstrið fyrir myndun greiðsluskráa.  
6. Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.
7. Velja BACS (UK upphugsað) skilgreining á sniði.
8. Smellið á „Vista“.
9. Lokið síðunni.

## <a name="test-the-format-of-generated-payment-files"></a>Prófa snið greiðsluskráa
1. Fara í Viðskiptaskuldir > Greiðslur > Greiðslubók.
2. Smellið á „Nýtt“.
3. Í listanum skal merkja valda línu.
4. Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.
5. Í listanum skal smella á tengilinn í valinni línu.
    * Velja VendPay  
6. Smellið á „Vista“.
7. Smellið á „Línur“.
8. Í reitinn fyrirtæki skal slá inn „DEMF“.
    * DEMF  
9. Á Svæðinu reikningur skal tilgreina gildin „DE-01001“.
    * DE - 01001  
10. Slá inn „greiðsla“ í reitinn Lýsing.
    * Greiðsla  
11. Í reitnum Debet skal slá inn tölu.
    * 1000  
12. Smellið á flipann Greiðslu.
13. Í reitnum greiðsluaðferð skal smella á fellilistahnappinn til að opna leitina.
14. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Velja rafrænt gildi.  
15. Í listanum skal smella á tengilinn í valinni línu.
16. Smellið á „Vista“.
17. Smelltu á Mynda greiðslur.
18. Í reitnum greiðsluaðferð skal smella á fellilistahnappinn til að opna leitina.
19. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Velja rafrænt gildi.  
20. Í listanum skal smella á tengilinn í valinni línu.
    * Velja rafrænt gildi.  
21. Í reitinn Skráarheiti skal slá inn gildi.
    * Til dæmis, skrifið „greiðsla“.  
22. Í reitnum Bankareikningur skal smella á fellilistahnappinn til að opna leitina.
23. Í listanum skal smella á tengilinn í valinni línu.
    * Velja GBSI OPER gildi.  
24. Smellið á „Í lagi“.
25. Smellið á „Í lagi“.
    * Greina stofnaða greiðsluskrá á XML-sniði. Bera saman við hannað útlit skjals og færslueigindir skilgreinda greiðslu.  


