--- 
title: "Uppfæra reikningsskýrslu lánardrottins og mynda skýrsluna (Ísland)"
description: "Þetta ferli fer í gegnum bókun á reikningi lánardrottins með meðfylgjandi upplýsingar um verktakamiða og myndun skýrslu um verktakamiða."
author: mrolecki
manager: AnnBe
ms.date: 05/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Iceland
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c990ed78fa237314130371a9d4eed442c9b816af
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="update-vendor-invoice-declarations-and-generate-the-report-iceland"></a>Uppfæra reikningsskýrslu lánardrottins og mynda skýrsluna (Ísland)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli fer í gegnum bókun á reikningi lánardrottins með meðfylgjandi upplýsingar um verktakamiða og myndun skýrslu um verktakamiða. Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF með land aðalaðsetur lögaðila uppfært í Ísland.


## <a name="post-a-vendor-invoice"></a>Bóka reikning lánardrottins
1. Fara í Viðskiptaskuldir > Reikningar > Reikningabók.
2. Smellið á „Nýtt“.
3. Í reitnum Heiti velurðu ‚APInvoice‘.
4. Smellið á Línur.
5. Í reitinn Lykill skal færa inn gildin 'IS-001'.
6. Í reitinn Reikningur skal færa inn "IS-001-01".
7. Í reitnum Kredit skal slá inn tölu.
8. Í reitinn Mótlykill skal tilgreina gildin '200130--'.
9. Smellið á flipann Reikningur.
10. Í reitinn Skjal skal slá inn gildi.
11. Í reitnum Reikningsdagsetning er dagsetning í dag rituð.
12. Í reitnum Verktakamiðar skal smella á fellilistahnappinn til að opna leitina.
13. Í listanum velurðu flokkinn Verktakamiðar.
14. Smellið á „Bóka“.

## <a name="generate-an-invoice-declaration"></a>Mynda verktakamiða
1. Fara í Viðskiptaskuldir > Fyrirspurnir og skýrslur > Reikningur > Skýrsla um verktakamiða lánardrottins.
2. Í reitnum Yfirvöld skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Dagsetning er rituð í reitinn Frá dags.
5. Í reitinn Til dagsetningar skal slá inn dagsetningu.
6. Merkið við gátreitinn Stofna skýrsluskrá.
7. Í reitinn Heiti skal slá inn ‚Skýrsla um verktakamiða lánardrottins (IS)‘.
8. Merkið við gátreitinn Stofna textaskrá.
9. Í reitinn Heiti skal slá inn ‚Skýrsla um verktakamiða lánardrottins yfirlýsing (IS)‘.
10. Smellið á „Í lagi“.


