---
title: Vinnutímasniðmát stofnuð
description: Sniðmát vinnutíma skilgreina vinnustundir yfir vikuna og eru notaðir til að mynda vinnutíma fyrir tímabil.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ef913777c8e2aa14af21e28ed56362e31b3d70a1a52e988a90ad94f59b77b70
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741262"
---
# <a name="create-working-time-templates"></a>Vinnutímasniðmát stofnuð

[!include [banner](../../includes/banner.md)]

Sniðmát vinnutíma skilgreina vinnustundir yfir vikuna og eru notaðir til að mynda vinnutíma fyrir tímabil. Þessi verklýsing sýnir hvernig á að skilgreina sniðmát vinnutíma með því að nota eiginleikar vinnutímaröðunar til flokkunar á vinnutímabilum. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.

1. Farið í **Vinnusvæði > Líftímastjórnun tilfanga**.
1. Veljið **Sniðmát vinnutíma**.

## <a name="create-working-time-template"></a>Stofna sniðmát vinnutíma.

1. Veljið **Nýtt**.
1. Færa inn gildi í reitnum **Sniðmát vinnutíma**.
1. Í reitinn **Heiti** skal slá inn gildi.
1. Stækka **Mánudagur** hlutann.
1. Veljið **Bæta við**.
1. Í reitinn **Frá** skal slá inn tíma.
    * Tilgreina tímasetningu þegar verk hefst á morgnana.  
1. Í reitinn **Til** í skal slá inn tíma.
    * Tilgreina tímasetningu þegar starfsmenn taka hlé fyrir hádegisverð.  
1. Veljið **Bæta við**.
1. Í reitinn **Frá** skal slá inn tíma.
    * Tilgreina tímasetningu þegar vinna hefst aftur eftir hádegisverð.  
1. Í reitinn **Til** í skal slá inn tíma.
    * Tilgreina lok vinnudagur.  

## <a name="replicate-working-times-to-all-week-days"></a>Afrita vinnutíma á allir dagar í viku

1. Veljið **Afrita dag**.
    * Afrita skilgreiningar vinnutíma frá Mánudegi yfir á Þriðjudag.  
1. Veljið **Í lagi**.
1. Veljið **Afrita dag**.
    * Afrita skilgreiningar vinnutíma frá Mánudegi til Miðvikudegi.  
1. Í reitnum **Til vikudags** skal velja valkost.
1. Veljið **Í lagi**.
1. Veljið **Afrita dag**.
    * Afrita skilgreiningar vinnutíma frá Mánudegi til Fimmtudag.  
1. Í reitnum **Til vikudags** skal velja valkost.
1. Veljið **Í lagi**.
1. Veljið **Afrita dag**.
    * Afrita skilgreiningar vinnutíma frá Mánudegi til Föstudags.  
1. Í reitnum **Til vikudags** skal velja valkost.
1. Veljið **Í lagi**.

## <a name="define-time-slots-for-special-operations"></a>Skilgreina tímahólf fyrir sérstakar aðgerðir

1. Stækka **Föstudagur** hlutann.
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
1. Í reitinn **Eiginleiki** skal slá inn eða velja gildi.
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
1. Í reitinn **Eiginleiki** skal slá inn eða velja gildi.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Merkja helgardagar ekki hægt að sækja

1. Stækka **Laugardagur** hlutann.
1. Velja skal *Já* í reitnum **Lokað fyrir afhendingu**.
1. Stækka **Sunnudagur** hlutann.
1. Velja skal *Já* í reitnum **Lokað fyrir afhendingu**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]