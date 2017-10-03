--- 
title: "Vinnutímasniðmát stofnuð"
description: "Sniðmát vinnutíma skilgreina vinnustundir yfir vikuna og eru notaðir til að mynda vinnutíma fyrir tímabil."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ff1978f127a014e75619a4bbbb9b6ff3a3ad7c7a
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="create-working-time-templates"></a>Vinnutímasniðmát stofnuð

[!include[task guide banner](../../includes/task-guide-banner.md)]

Sniðmát vinnutíma skilgreina vinnustundir yfir vikuna og eru notaðir til að mynda vinnutíma fyrir tímabil. Þessi verklýsing sýnir hvernig á að skilgreina sniðmát vinnutíma með því að nota eiginleikar vinnutímaröðunar til flokkunar á vinnutímabilum. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.

1. Farið í Öll vinnusvæði > Líftímastjórnun tilfanga.
2. Smellt er á sniðmát vinnutíma.

## <a name="create-working-time-template"></a>Stofna sniðmát vinnutíma.
1. Smellið á „Nýtt“.
2. Færa inn gildi í reitnum sniðmát vinnutíma.
3. Í reitinn Heiti skal slá inn gildi.
4. Stækka Mánudagur hluti.
5. Smelltu á Bæta við.
6. Í reitinn Frá skal slá inn tíma.
    * Tilgreina tímasetningu þegar verk hefst á morgnana.  
7. Í reitinn Til í skal slá inn tíma.
    * Tilgreina tímasetningu þegar starfsmenn taka hlé fyrir hádegisverð.  
8. Smelltu á Bæta við.
9. Í reitinn Frá skal slá inn tíma.
    * Tilgreina tímasetningu þegar vinna hefst aftur eftir hádegisverð.  
10. Í reitinn Til í skal slá inn tíma.
    * Tilgreina lok vinnudagur.  

## <a name="replicate-working-times-to-all-week-days"></a>Afrita vinnutíma á allir dagar í viku
1. Smellt er á afrita dag.
    * Afrita skilgreiningar vinnutíma frá Mánudegi yfir á Þriðjudag.  
2. Smellið á „Í lagi“.
3. Smellt er á afrita dag.
    * Afrita skilgreiningar vinnutíma frá Mánudegi til Miðvikudegi.  
4. Í reitnum til vikudags skal velja valkost.
5. Smellið á „Í lagi“.
6. Smellt er á afrita dag.
    * Afrita skilgreiningar vinnutíma frá Mánudegi til Fimmtudag.  
7. Í reitnum til vikudags skal velja valkost.
8. Smellið á „Í lagi“.
9. Smellt er á afrita dag.
    * Afrita skilgreiningar vinnutíma frá Mánudegi til Föstudags.  
10. Í reitnum til vikudags skal velja valkost.
11. Smellið á „Í lagi“.

## <a name="define-time-slots-for-special-operations"></a>Skilgreina tímahólf fyrir sérstakar aðgerðir
1. Stækka Föstudagur hluti.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í reitinn eiginleiki skal slá inn eða veldu gildi.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í reitinn eiginleiki skal slá inn eða veldu gildi.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Merkja helgardagar ekki hægt að sækja
1. Stækka Laugardagur hluti.
2. Velja skal Já í svæði Lokað fyrir afhendingu.
3. Stækka Sunnudagur hluti.
4. Velja skal Já í svæði Lokað fyrir afhendingu.


