--- 
title: "Setja upp viðskiptavini bankareikninga viðskiptavina fyrir ISO20022-beingreiðslur"
description: "Þetta verk fer í gegnum uppsetningu á bankareikning viðskiptavinar og í umboð viðskiptavinar fyrir beingreiðsla sem eru nauðsynlegar til að mynda greiðsluskrá fyrir viðskiptavin eins og ISO20022-beingreiðslu."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
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
ms.openlocfilehash: 5b4652b76e089d6beb2ce1513d06cf07a5ea3195
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>Setja upp viðskiptavini bankareikninga viðskiptavina fyrir ISO20022-beingreiðslur

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta verk fer í gegnum uppsetningu á bankareikning viðskiptavinar og í umboð viðskiptavinar fyrir beingreiðsla sem eru nauðsynlegar til að mynda greiðsluskrá fyrir viðskiptavin eins og ISO20022-beingreiðslu. Eftir því hvaða greiðslusnið viðskiptavar er sett upp gæti verið krafist viðbótarupplýsinga, sem ekki er fjallað um í þessu ferli, vegna viðskiptavinar eða bankareikningur viðskiptavinar. 

Þetta verkefni var stofnuð með fyrirtækis sýnigögnum DEMF með aðalaðsetur lögaðila í Þýskalandi.



Þetta er fjórða af fimm ferlum sem lýsa greiðsluferlinu viðskiptavinar með grunnstillingar fyrir rafræna skýrslugerð.


## <a name="set-up-a-customer-bank-account"></a>Uppsetning bankareikningur viðskiptavinar
1. Farið í Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir.
2. Nota flýtiafmörkun til að finna færslur Til dæmis, sía svæðið með gildið 'DE-010'.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Í aðgerðasvæðinu er smellt á Viðskiptavinur.
5. Smellt er á bankareikninga.
6. Smellið á „Nýtt“.
7. Í reitinn Bankareikningar skal slá inn gildi.
8. Í reitinn Heiti skal slá inn gildi.
    * Til dæmis má færa inn 'EUR bank'.  
9. Færa inn eða veljið gildi í svæðinu bankaflokkur.
10. Í reitinn IBAN skal slá inn gildi.
    * Til dæmis færðu inn 'DE36200400000628808808'.  
11. Í svæðinu SWIFT-kóði færðu inn gildi.
    * Til dæmis færðu inn 'COBADEFFXXX'.  Vinsamlegast Athugið að SWIFT\BIC er ekki krafist fyrir margar greiðslusnið hins vegar er mælt með að slíkt sé skráð fyrir bankareikning.  
12. Smellið á „Vista“.
13. Lokið síðunni.
14. Smellið á „Breyta“.
15. Útvíkka hlutann sjálfgildi Greiðslu.
16. Færa inn eða veljið gildi í svæðinu bankareikning.

## <a name="add-a-direct-debit-mandate"></a>Bæta við umboði fyrir beingreiðslu
1. Útvíkka hlutann umboð fyrir beingreiðsla.
2. Smelltu á Bæta við.
3. Sláið inn eða veldu gildi í reitnum Bankareikningur Lánardrottins.
    * Veljið til dæmis DEMF OPER.  
4. Færðu inn dagsetningu í svæðinu dagsetning undirskriftar
5. Smellt er á Já til að staðfesta uppfærslu dagsetningar .
6. Sláðu inn eða veldu gildi reitnum Í staðsetning undirskriftar.
7. Í Áætlað fjölda greiðslur svæðinu, færið inn tölu.
8. Smellið á „Í lagi“.
9. Smellið á „Vista“.


