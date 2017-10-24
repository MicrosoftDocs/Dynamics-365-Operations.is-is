---
title: "Taka til elstu runu í fartæki"
description: "Þetta efnisatriði lýsir uppsetningu og notkun á valmöguleikum til að taka til elstu runu úr fartæki."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 25056886b1a18dbaef12c8732a1fd0bd92a6d04b
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a>Taka til elstu runu í fartæki

[!include[banner](../includes/banner.md)]

Hægt er að komast í skilgreininguna **Taka til elstu runu** í gegnum valmynd í fartæki og hún gerir þér kleift að þvinga eða láta starfsmenn í vöruhúsi vita að þeir eigi að taka til elstu rununa í núverandi staðsetningu.  

## <a name="where-it-applies"></a>Þar sem það á við
Taka til elstu runu er skilgreint í valmyndaratriðum fartækis og orsakar tiltekt á neðangreindum runum vara.

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>Hvernig á að setja upp skilgreiningu á Taka til elstu runu 
Fyrir vörur sem eru stilltar þannig að þær notist við fyrirliggjandi verk er hægt að stilla **Tína elstu runu** á **Engin**, **Aðvara** eða **Þvinga** úr valmynd fartækis.

**Engin**: Starfsmenn fá engin skilaboð og þeim er heimilt að taka til hvaða runu sem er í staðsetningunni.

**Aðvara** og **Þvinga**: Listi yfir elstu runu(r) með elsta lokadeginum birtist fyrir ofan runustjórnun þegar starfsmaður velur runu. Ef staðsetningu er stýrt af númeraplötu birtist listi yfir númeraplötur sem hafa elstu rununa fyrir ofan númeraplötustjórnun. 
-   **Aðvara**: Ef starfsmaður velur númeraplötu eða runu sem ekki birtist á listanum er stjórnunin auð og aðvörun birtist um að það sé eldri runa sem þarf að velja. Til að geta haldið áfram vinnu getur starfsmaður valið sömu númeraplötu eða runu aftur.  
-   **Þvinga**: Starfsmenn munu áfram fá skilaboðin um að það sé eldri runa sem á að taka til.

