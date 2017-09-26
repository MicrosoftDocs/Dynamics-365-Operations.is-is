--- 
title: "Stofna bankareikning lánardrottins"
description: "Þessi verklýsing sýnir hvernig á að stofna bankareikning fyrir lánardrottinn."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e84432faf32e519059a21d2b56e320a46599c1e8
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-vendor-bank-account"></a>Stofna bankareikning lánardrottins

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna bankareikning fyrir lánardrottinn. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.

1. Farið í innkaup og aðföng > Lánardrottnar > Allir lánardrottnar.
2. Veljið lánardrottinn sem á að stofna bankareikning fyrir, og smellið síðan á tengil á kenni lánardrottnalykils
3. Í aðgerðasvæðinu er smellt á lánardrottinn.
4. Smellt er á bankareikninga.
5. Smellið á „Nýtt“.
6. Í reitinn Bankareikningar skal slá inn gildi.
    * Þetta Kenni verður notuð til að auðkenna bankareikninginn á lánardrottinsfærslu.  
7. Í reitinn Heiti skal slá inn gildi.
8. Færa inn eða veljið gildi í svæðinu bankaflokkur.
9. Veljið valkost í svæðinu gerð leiðarnúmers.
    * Þetta er Gerð leiðarnúmers sem notað er fyrir alþjóðlegar greiðslur.  
10. Í reitinn Bankareikningsnúmer skal slá inn gildi.
11. Í svæðinu SWIFT-kóði færðu inn gildi.
12. Í reitinn IBAN skal slá inn gildi.
    * Iban-númeri verður að vera á réttu sniði. Til dæmis er hægt að nota DE89370400440532013000.  
    * Staða bankareikningsins er Virkur ef Virkri dagsetningu hefur verið náð og lokadagur er ekki liðinn. Einnig er hann virkur ef svæðin Virka dagsetningu og dagsetning Gildistíma eru auð. Ef dagsetningarnar í svæðunum Virk dagsetning og Lokadagur eru báðar í framtíðinni er ekki hægt að gera rafrænar greiðslur. Aðrar greiðslugerðir eru mögulegar og bankareikningurinn er virkur.  
13. Víkka út hlutann Uppsetning.
14. Í svæðinu Textakóði færðu inn gildi.
    * Þetta svæði tilgreinir kóða sem mun birtast á bankayfirliti viðtakanda.  
15. Í reitinn skilaboð til banka skal slá inn gildi.
16. Færa inn gildi í tilvísunarsvæði gjaldeyrisviðskipta.
    * Þetta er Tilvísunarnúmer fyrir hvers kyns framvirkt eða fast gengi.  
17. Í reitinn gjaldmiðill skal slá inn eða veldu gildi.
    * Þegar fyrirframkvittanir eru gefin út, gefur þessa kafla yfirlit yfir stöðu þeirra (í bið eða samþykkt).  
18. Stækka aðsetur Hluti.
19. Víkkið út hlutann fyrirframkvittun.
20. Útvíkka hlutann upplýsingar Tengiliðar.
21. Í reitinn Símanúmer skal slá inn gildi.
22. Lokið síðunni.
23. Smellið á „Breyta“.
24. Stækkið hlutann Greiðslur.
25. Í svæðinu bankareikningur, veljið lykil sem hefur verið rétt nýlega stofnuð.
26. Smellið á „Vista“.
    * Aðsetrið má erfa frá bankaflokki, ef slíkt er tilgreint, eða hægt er að bæta honum við hér.  


