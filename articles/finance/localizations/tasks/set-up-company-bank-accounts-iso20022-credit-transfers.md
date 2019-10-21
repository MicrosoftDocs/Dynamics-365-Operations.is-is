---
title: Setja upp bankareikninga fyrirtækis fyrir ISO20022-kreditfærslur
description: Þetta Leiðbeiningar sýnir hvernig á að setja upp bankareikningsupplýsingar fyrir fyrirtæki sem þarf fyrir myndun greiðsluskrár.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bbbf55ed28ad2131d7e1253dd44842d85d39315
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174910"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Setja upp bankareikninga fyrirtækis fyrir ISO20022-kreditfærslur

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

