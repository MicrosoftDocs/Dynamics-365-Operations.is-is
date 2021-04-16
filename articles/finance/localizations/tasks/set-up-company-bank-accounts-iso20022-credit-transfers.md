---
title: Setja upp bankareikninga fyrirtækis fyrir ISO20022-kreditfærslur
description: Þetta Leiðbeiningar sýnir hvernig á að setja upp bankareikningsupplýsingar fyrir fyrirtæki sem þarf fyrir myndun greiðsluskrár.
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
ms.openlocfilehash: a3ddcae4a53fffa07bd386174811c12150f2f162
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819481"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Setja upp bankareikninga fyrirtækis fyrir ISO20022-kreditfærslur

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]