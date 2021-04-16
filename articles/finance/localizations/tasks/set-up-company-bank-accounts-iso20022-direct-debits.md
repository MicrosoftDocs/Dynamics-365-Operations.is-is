---
title: Setja upp bankareikninga fyrirtækis fyrir ISO20022-beingreiðslur
description: Þetta Leiðbeiningar sýnir hvernig á að setja upp og bankareikningsupplýsingar fyrir fyrirtæki sem þarf fyrir myndun greiðsluskrár viðskiptavina.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 319bf71982987296a8270f596f8d2bb518dd1790
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819457"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>Setja upp bankareikninga fyrirtækis fyrir ISO20022-beingreiðslur

[!include [banner](../../includes/banner.md)]

Þetta Leiðbeiningar sýnir hvernig á að setja upp og bankareikningsupplýsingar fyrir fyrirtæki sem þarf fyrir myndun greiðsluskrár viðskiptavina. Þessi aðferð notar snið ISO-20022 beingreiðslu sem dæmi. Aðrar snið útheimt kannski auka upplýsinga vegna uppsetningar eins og kenni fyrirtækis eða bankaauðkennisnúmer (Sort-kóða).



Þetta verkefni var stofnuð með því að nota sýnigögn fyrirtækisins DEMF.



Þetta er annað af fimm ferlum sem lýsa greiðsluferlinu viðskiptavinar með grunnstillingar fyrir rafræna skýrslugerð.


## <a name="set-up-the-iban-and-swift-codes"></a>Setja upp IBAN- og swift-kóða
1. Farið í Reiðufjár- og bankastjórnun > Bankareikningar.
2. Nota flýtiafmörkun til að sía í reitnum bankareikningur með gildið „DEMF OPER“.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Til dæmis: smellið á "DEMF OPER' til að opna upplýsingar um bankareikning.  
4. Smellið á „Breyta“.
5. Útvíkka eða draga saman aukakenni hluta.
6. Í reitinn IBAN skal slá inn gildi.
    * Til dæmis færðu inn 'DE89370400440532013000'.  
7. Í svæðinu SWIFT-kóði færðu inn gildi.
    * Til dæmis færðu inn 'DEUTDEFF'.    Vinsamlegast Athugið að SWIFT\BIC er ekki krafist fyrir margar greiðslusnið hins vegar er mælt með að slíkt sé skráð fyrir bankareikning.  
8. Smellið á „Vista“.

## <a name="set-up-a-bank-account-for-the-legal-entity"></a>Setja upp bankareikning fyrir lögaðila
1. Fara í Fyrirtækisstjórnun > Fyrirtæki > Lögaðilar.
2. Smellið á „Breyta“.
3. Útvíkka eða draga saman hluta upplýsingar bankareiknings.
4. Í reitnum Bankareikningur skal smella á fellilistahnappinn til að opna leitina.
5. Í listanum skal smella á tengilinn í valinni línu.
    * Til dæmis: Velja bankareikning "DEMF OPER".  
6. Smellið á „Vista“.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]