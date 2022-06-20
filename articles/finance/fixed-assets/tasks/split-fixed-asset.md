---
title: Skipta eign
description: Þessi grein útskýrir hvernig á að skipta hlutfalli af einni eignabók í nýja eignabók.
author: moaamer
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d7fe30702717f960a42fb2a118e0d12587024f5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880789"
---
# <a name="split-a-fixed-asset"></a>Skipta eign

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir hvernig á að skipta hlutfalli af einni eignabók í nýja eignabók. 

## <a name="create-a-new-fixed-asset"></a>Búa til nýja eign

1. Í yfirlitssvæðinu opnarðu **Einingar \> Eignir \> Eignir \> Eignir**.
2. Veljið **Nýtt**.
3. Í reitnum **Eignaflokkur** skal færa inn eða velja gildi. Athugið númer eignar til að nota seinna í ferlinu skipta.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Lokaðu skjámyndinni.

## <a name="split-a-fixed-asset"></a>Skipta eign

Áður en afskrifaðri eign er skipt ætti að breyta stöðu eignabókar handvirkt úr **Lokað** í **Opin**. Þetta skref er áskilið vegna þess að staða bókar verður að vera **Opin** ef bóka þarf færslur fyrir eignina (til dæmis fyrir afskráning sölu). Einnig verður að kveikja á **Leyfa margar færslur í einu fylgiskjali** færibreytunni á flipanum **Almennt** á síðunni **Færibreytur fjárhagsbókar**. Eftir að stöðu eignabókar er breytt og margar færslur innan eins fylgiskjala hafa verið leyfðar, skal ljúka við eftirfarandi skref til að skipta eigninni.

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

1. Í yfirlitssvæðinu opnarðu **Einingar \> Eignir \> Færslubókarfærslur \> Eignabækur**.
2. Veljið færslubók sem er stofnuð með skipta ferlinu á listanum.
3. Veldu **Línur**.

    - Staðfestið stofnaðar færslubókarlínur .
    - Leiðrétting kaupvirðisfærsla er stofnuð fyrir upprunalegu eignina til að minnka virði eftir prósentu sem tilgreind er við að skipta ferlinu.
    - Kaupfærsla er stofnuð fyrir nýju eignina fyrir sömu upphæð.

4. Veldu **Bóka**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
