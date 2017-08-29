--- 
title: "Setja upp bankareikninga fyrirtækis fyrir ISO20022-kreditfærslur"
description: "Þetta Leiðbeiningar sýnir hvernig á að setja upp bankareikningsupplýsingar fyrir fyrirtæki sem þarf fyrir myndun greiðsluskrár."
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4e55a4727555f781b6880103abb1a38c5d0d5b78
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Setja upp bankareikninga fyrirtækis fyrir ISO20022-kreditfærslur

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta Leiðbeiningar sýnir hvernig á að setja upp bankareikningsupplýsingar fyrir fyrirtæki sem þarf fyrir myndun greiðsluskrár. Setja upp upplýsingar sem þarf til að mynda ISO 20022 snið fyrir millifærsla fjármuna, en eftir sniðinu gæti þurft frekari upplýsingar, eins og kenni fyrirtækis eða bankaauðkennisnúmer (sort-kóða). 

Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF.

Þetta annað ferli af fimm sem sýna greiðsluferlinu lánardrottins með því að nota grunnstillingar fyrir rafræna skýrslugerð. Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="set-up-iban-and-swift-code"></a>Uppsetning IBAN- og swift-kóði
1. Farið í Reiðufjár- og bankastjórnun > Bankareikningar.
2. Nota flýtiafmörkun til að sía í reitnum bankareikningur með gildið „DEMF OPER“.
3. Smellið á DEMF OPER til að opna upplýsingar bankareiknings
4. Smellið á „Breyta“.
5. Útvíkka aukakenni hluta.
6. Í reitinn IBAN skal slá inn 'DE89370400440532013000'.
7. Í svæðinu swift-kóði færðu inn 'DEUTDEFF' .
    * Athugið að SWIFT\BIC er ekki krafist fyrir margar greiðslusnið hins vegar er mælt með að slíkt sé skráð fyrir bankareikning.  
8. Smellið á „Vista“.

## <a name="set-up-bank-account-for-the-legal-entity"></a>Setja upp bankareikning fyrir lögaðila
1. Fara í Fyrirtækisstjórnun > Fyrirtæki > Lögaðilar.
2. Smellið á „Breyta“.
3. Útvíkka hlutann upplýsingar bankareiknings.
4. Færa inn eða veljið gildi í svæðinu bankareikning.
5. Smellið á „Vista“.


