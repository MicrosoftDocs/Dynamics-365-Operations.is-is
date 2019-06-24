---
title: Uppfæra verktakamiða lánardrottna og búa til skýrslu
description: Þetta ferli fer í gegnum bókun á reikningi lánardrottins með meðfylgjandi upplýsingar um verktakamiða og myndun skýrslu um verktakamiða.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Iceland
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 579bb2219f5059604dcd6cc1a1404793d52ada1e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557347"
---
# <a name="update-vendor-invoice-declarations-and-generate-the-report"></a>Uppfæra verktakamiða lánardrottna og búa til skýrslu

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

