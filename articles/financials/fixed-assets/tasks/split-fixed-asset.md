---
title: Skipta eign
description: Þessi leiðarvísi fyrir verk mun skipta hlutfall eitt eignabók á nýtt eignabók.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6be9de64265a4d7b5c91af3ee8acfce80c78e0f1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566893"
---
# <a name="split-a-fixed-asset"></a>Skipta eign

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísi fyrir verk mun skipta hlutfall eitt eignabók á nýtt eignabók.  Það notar hlutverk Bókhaldara og sýnigögn USMF.


## <a name="create-a-new-fixed-asset"></a>Búa til nýja eign
1. Fara í Eignir > Eignir > Eignir.
2. Smellið á „Nýtt“.
3. Færa inn eða veljið gildi í svæðinu eignaflokkur.
4. Athugið númer eignar til að nota seinna í ferlinu skipta.
5. Í reitinn Heiti skal slá inn gildi.
6. Lokaðu skjámyndinni.

## <a name="split-a-fixed-asset"></a>Skipta eign
1. Finna og veljið eignir sem skipta á í listanum.
2. Í listanum skal smella á tengilinn í valinni línu.
3. Smelltu á bækur.
    * Veljið bók til að skipta á nýju eignina.  
4. Smellið á Aðgerðir.
5. Smellt er á skipta Eign.
6. Sláðu inn eða veldu gildi í reitnum Á eign.
7. Í reitnum Á bók skal smella á fellilistahnappinn til að opna leitina.
8. Færa inn dagsetningu í dagsetningarsvæði Færslunnar.
9. Færið inn tölu í svæðinu prósenta.
10. Sláið inn eða veljið gildi í reitnum heiti færslubókar.
11. Smellið á „Í lagi“.

## <a name="post-the-journal-transaction"></a>Bókið færslubókarfærsla.
1. Fara í Eignir >°Færslubókarfærslur°> Eignabók.
2. Veljið færslubók sem er stofnuð með skipta ferlinu á listanum.
3. Smellið á „Línur“.
    * Staðfestið stofnaðar færslubókarlínur .  Leiðrétting kaupvirðisfærsla er stofnuð fyrir upprunalegu eignina til að minnka virði eftir prósentu sem tilgreind er við að skipta ferlinu.  Kaupfærsla er stofnuð fyrir nýju eignina fyrir sömu upphæð.  
4. Smellið á „Bóka“.

