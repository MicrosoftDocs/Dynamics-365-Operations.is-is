--- 
title: "Setja upp og mynda aldursgreiningarupplýsingar fyrir viðskiptakröfur"
description: "Þessari handbók hjálpar til við að setja upp skilgreiningu aldursgreiningar, greina aldur stöðu viðskiptavinar og skoða stöðu í á listanum aldursgreindar stöður og síðan Innheimtu."
author: mikefalkner
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2e9f393acaa47d485a583b99ace459474f30be6a
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Setja upp og mynda aldursgreiningarupplýsingar fyrir viðskiptakröfur

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessari handbók hjálpar til við að setja upp skilgreiningu aldursgreiningar, greina aldur stöðu viðskiptavinar og skoða stöðu í á listanum aldursgreindar stöður og síðan Innheimtu. Þessi skráning notar sýnigögn USMF fyrirtækis


## <a name="create-an-aging-period-definition"></a>Stofna skilgreiningu aldurstímabils
1. Fara í Skuldir og innheimta > Uppsetning > Skilgreiningar aldurstímabila.
2. Smellið á „Nýtt“.
3. Í reitnum Skilgreining aldurstímabils skal slá inn gildi.
4. Í reitinn Lýsing skal slá inn gildi.
5. Stutt er á  bæta við til að setja inn nýja aldurstímabil.
6. Í svæðinu Tímabil skal færa inn lýsingu til að sýna á skýrslur aldurstímabils.
7. Í reitnum Eining skal slá inn tölu.
8. Í reitnum Millibil skal velja valkost.
    * Fjárhagstímabil samsvarar tímabili í dagatali fjárhags. Dagur, vika, mánuður, ársfjórðungur og ár skilgreina stærð tímabila eftir gerð. Ótakmarkað velur allar færslur fyrir eða eftir fyrra tímabil, allt eftir hvort það er fyrsta eða síðasta tímabil.  
9. Í reitnum Öldrunarvísir skal velja valkost.
10. Veljið tímabil efst í hnitanetinu. Uppfæra lýsingu til að lýsa elsta tímabil í skilgreiningu aldurstímabils
11. Í svæðinu Tímabil skal færa inn nýja lýsing aldurstímabilið.
12. Lokið síðunni.

## <a name="age-the-balances"></a>Aldursgreina stöður
1. Fara í Skuldir og innheimta > Reglubundin verk > Aldursgreina stöður viðskiptavinar.
2. Velja skilgreiningu aldurstímabils sem var stofnaður í svæðinu skilgreiningu Aldurstímabils.
    * Hægt er að hafa eina virka skyndimynd fyrir hverja skilgreiningu aldurstímabils.  
    * Allir viðskiptavinir eru keyrðir í gegnum vinnslu að sjálfgefnu. Hægt er að nota þetta val til að reikna út einstakt safn viðskiptavinahópa.  
    * Veljið dagsetningu úr færslunnar sem verður notað fyrir aldursgreiningu.  
    * Velja skal "frá og með" dagsetningu fyrir aldursgreiningu. Sjálfgefið gildi er í dag en ef þetta svæði er breytt í Valin dagsetning, er hægt að velja dagsetningu sem óskað er. Fyrir runuvinnslu, notið Dagsins í dag.  
3. Útvíkka svið Fyrirtækisins. Hægt er að velja fyrirtæki sem verða teknar með í skyndimyndar. Núgildandi fyrirtæki er sjálfvirkt valið.
4. Smellt er á í Lagi til að vinna skyndimyndar. Það tekur smá tíma fyrir sleði að hverfa og athuga í skilaboðamiðstöð eftir skilaboðum.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>Skoða stöðu á listanum Aldursgreindar stöður og síðunni Innheimta
1. Fara í skuldir og innheimta > Innheimta > Aldursgreindar stöður.
    * listasíðu sýnir stöðu viðskiptavinar. Aldursgreiningartáknið sýnir aldurstímabilið fyrir elsta færslunnar.  
2. Velja skal viðskiptavin með stöðu.
3. Útvíkka skal svæði Aldursgreiningar í  upplýsingakassa til að skoða aldursgreindar stöður.
    * Skilgreining aldurstímabils fyrir upplýsingakassann er tekið úr sjálfgefnu skilgreining aldurstímabils sem tilgreint er í færibreytum. Hægt er að breyta henni með því að nota valmyndina Innheimta.  


