---
title: Skipta eign
description: Þetta efni útskýrir hvernig skal skipta hlutfalli einnar eignabókar á nýtt eignabók.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4e001a6fdf390c6211ba85aa327b60dcdf16d9e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178253"
---
# <a name="split-a-fixed-asset"></a>Skipta eign

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta efni útskýrir hvernig skal skipta hlutfalli einnar eignabókar á nýtt eignabók. Það notar hlutverk Bókhaldara og sýnigögn USMF.


## <a name="create-a-new-fixed-asset"></a>Búa til nýja eign
1. Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Fastafjármunir > Fastafjármunir**.
2. Veljið **Nýtt**.
3. Í reitnum **Eignaflokkur** skal færa inn eða velja gildi. Athugið númer eignar til að nota seinna í ferlinu skipta.  
4. Í reitinn **Heiti** skal slá inn gildi.
5. Lokaðu skjámyndinni.

## <a name="split-a-fixed-asset"></a>Skipta eign
1. Finna og veljið tengil í eignir sem skipta á í listanum.
2. Veldu **Bækur**. Veljið bók til að skipta á nýju eignina.  
3. Veljið **Aðgerðir**.
4. Velu **Skipta eign**.
5. Sláðu inn eða veldu gildi í reitnum **Á eign**.
6. Í reitnum **Til bókar** skal velja fellilistahnappinn til að opna leitina.
7. Færa inn dagsetningu í reitinn **Færsludagsetning**.
8. Færið inn tölu í reitnum **Prósenta**.
9. Sláið inn eða veljið gildi í reitnum **Heiti færslubókar**.
10. Veljið **Í lagi**.

## <a name="post-the-journal-transaction"></a>Bókið færslubókarfærsla.
1. Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Dagbókarfærslur > Dagbók fastafjármuna**.
2. Veljið færslubók sem er stofnuð með skipta ferlinu á listanum.
3. Veldu **Línur**.

    - Staðfestið stofnaðar færslubókarlínur .  
    - Leiðrétting kaupvirðisfærsla er stofnuð fyrir upprunalegu eignina til að minnka virði eftir prósentu sem tilgreind er við að skipta ferlinu.  
    - Kaupfærsla er stofnuð fyrir nýju eignina fyrir sömu upphæð.  

4. Veldu **Bóka**.

