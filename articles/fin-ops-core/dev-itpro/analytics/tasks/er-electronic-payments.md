---
title: Rafræn skýrslugerð Mynda rafræn skjöl fyrir greiðslur með skilgreiningu á sniði
description: Í þessu efni er útskýrt hvernig á að nota nýja skilgreiningu rafræns skýrslugerðarsniðs til að mynda rafræn skjöl fyrir úrvinnslu greiðslna.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6dd39b3faba90b38b837cd5167b216f9faa31d82
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570217"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a>Rafræn skýrslugerð Mynda rafræn skjöl fyrir greiðslur með skilgreiningu á sniði

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur notað skilgreiningarsnið fyrir rafræna skýrslugerð (ER) til að búa til rafræn skjöl til að vinna úr greiðslum. Hægt er að framkvæma þessum skrefum í GBSI dæmi fyrirtækinu.

Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningu með snið á greiðsluskjali”.


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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]