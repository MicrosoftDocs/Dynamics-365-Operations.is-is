---
title: "Stofna framleiðslupöntun"
description: "Þessi verklýsing sýnir hvernig á að stofna framleiðslupöntun."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 730adcea0ac59f683ecae8cbb62025bd7db75c55
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-production-order"></a>Stofna framleiðslupöntun

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna framleiðslupöntun. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta er fyrsta ferlinu af sjö sem útskýrir lífsferli framleiðslupöntunar.


## <a name="create-a-production-order"></a>Stofna framleiðslupöntun
1. Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.
2. Smella á Ný framleiðslupöntun.
3. Sláið inn „D0001“ á svæðinu „Vörunúmer“.
4. Í reitinn Afhending skal færa inn dagsetningu.
    * Dagsetning afhendingar gefur til kynna þegar framleiðslupöntunin ætti að ljúka til að afhenda á réttum tíma. Þessi dagsetning er hægt að nota í áætlunarferli. Til dæmis er hægt að raða pöntunina afturábak frá afhendingardagsetningu.  
5. Stillið magn á „20“.
    * Athugasemd: Svæðið Uppskrift birtir sjálfkrafa númer allra virkra uppskrifta fyrir gildandi vöru, en hægt er að breyta Uppskrift fyrir framleiðslupöntunina með því að velja virka Uppskrift af lista yfir samþykktar uppskriftaútgáfur.    Svæði fyrir númer leiðar birtir sjálfkrafa númer allra virkra leiða fyrir gildandi vöru, en hægt er að breyta leið fyrir framleiðslupöntunina með því að velja virka leið af lista yfir samþykktar leiðarútgáfur.  
6. Smellið á „Stofna“.

## <a name="validate-the-production-order"></a>Villuleita framleiðslupöntunina
1. Í listanum skal smella á tengilinn í valinni línu.
    * Smelltu á tengil fyrir númer framleiðslupöntunar sem var nýlega stofnuð. Þetta opnar upplýsingasíðunni fyrir pöntunina.  
2. Smellið á „Breyta“.
3. Í reitinn Afhending skal færa inn dagsetningu.
    * Til dæmis er hægt að breyta afhendingardagsetningu fyrir framleiðslupöntunina.  
4. Smellið á „Vista“.
5. Lokið síðunni.

## <a name="update-the-bom"></a>Uppfæra Uppskrift
1. Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.
2. Smellt er á uppskrift.
    * Opna síðuna Uppskriftar til að villuleita gögn Uppskriftar sem var afritað úr sjálfgefnum gögnum þegar framleiðslupöntunin var stofnuð. Í þessari aðferð þarf að uppfæra magn fyrir Uppskrift.  
3. Smellið á „Breyta“.
4. Færið inn númer í reitnum „Magn“.
    * Breytingu á magni í uppskriftarlínu hefur áhrif á kostnaðarmat á efnisnotkun fyrir framleiðslupöntunina.  
5. Smellið á „Vista“.
6. Lokið síðunni.

## <a name="update-the-production-route"></a>Uppfæra „Framleiðsluleið“.
1. Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.
2. Smellt er á Leiðinni.
    * Opna síðuna Leið til að villuleita gögn í framleiðsluleiðinni sem var afritað úr sjálfgefnum upplýsingum þegar pöntunin var stofnuð. Í þessari aðferð þarf að uppfæra magn fyrir eina af aðgerðunum í framleiðsluleiðinni.  
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Smellið á „Breyta“.
5. Í svæðinu framleiðslumagn færðu inn númer
    * Ef Vinnslutími er breytt hefur það áhrif á áætlaður leiðarnotkun og kostnað framleiðslupöntunar.  
6. Smellið á „Vista“.
7. Lokið síðunni.

