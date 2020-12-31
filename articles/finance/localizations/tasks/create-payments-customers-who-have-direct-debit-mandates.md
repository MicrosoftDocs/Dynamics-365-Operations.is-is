---
title: Stofna greiðslur fyrir viðskiptavin sem hefur beingreiðsluumboð
description: Þetta verk fer í gegnum hvernig á að mynda ISO20022-beingreiðsluskrá fyrir viðskiptavin sem hefur skilgreint beingreiðslu og reikning til greiðslu.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a4714f1f1b24554684219fc1d766b4b87cff7bb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444479"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>Stofna greiðslur fyrir viðskiptavin sem hefur beingreiðsluumboð

[!include [banner](../../includes/banner.md)]

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
11. Smellt er á Í lagi.
12. Smellt er á Í lagi.
13. Smellt er á Stofna greiðslur.
