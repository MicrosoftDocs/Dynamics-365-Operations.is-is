---
title: "Uppsöfnun kostnað verks innhreyfingar innkaupapantana"
description: "Þetta efnisatriði lýsir því hvernig uppsafnaðar verkkostnað innhreyfingar hægt sé að rekja í Microsoft Dynamics 365 Aðgerðum fyrir innkaup."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 27a0a71095dce46c0119b32a92f8c4dce0f42e43
ms.lasthandoff: 03/31/2017


---

# <a name="project-cost-accrual-on-purchase-receipts"></a>Uppsöfnun kostnað verks innhreyfingar innkaupapantana

Þetta efnisatriði lýsir því hvernig uppsafnaðar verkkostnað innhreyfingar hægt sé að rekja í Microsoft Dynamics 365 Aðgerðum fyrir innkaup. 

Reikningar fyrir verk oft kemur síðar vörur og þjónustur eru sendar, sem kann að hafa viðeigandi áhrif á verk afkastavísar (Afkastavísa). Skýrslur það mikilvægt að hægt sé að rekja færslurnar í bæði fjárhagsvíddir og verk.

Eftirfarandi dæmi sýnir þetta. 

Contoso Aðstoðar hefur verið ræst nýtt verk virkjun skýinu. Innkaupapöntun er stofnuð til að kaupa tölvu fyrir verkið. Tölvunni verður $1500 og uppsetningu þjónustu verður kostnaðarbreytingum $150. Lánardrottinn hefur verið afhentar og uppsett á tölvunni, en reikningur hefur ekki enn náð Aðstoðar Contoso. Stjórnanda verksins óskað að sjá verks kostnaður uppsöfnun $1650 áður en reikningurinn er afhent. Einnig ætti að endurspeglast þennan kostnað í fyrirtækisins mánuði lok fjárhagsskýrslur. 

Uppsafnaður kostnaður þarf að skrá fjárhagslegar stig og verkstig fyrir skýrslugerð. Í Dynamics 365 fyrir Aðgerðir, hægt að rekja fjárhagsleg uppfærsla innhreyfingarskjals afurða fyrir tegundum vöru og innkaup. 

Fyrir vörur, á við **Færibreytur viðskiptaskulda** síðunni, veljið sem **Bóka innhreyfingarskjöl afurða í fjárhag** valkost.
[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Fyrir innkaupategundir, á við **tegundarstefnureglan** síðu, skal velja **Innkaup** reglur og velja svo **Uppsöfnuð innkaupakostnaðar á kvittun** fyrir hverja innkaupategund.
[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png) 

Í **útgjöld Innkaupa óreikningsfærð** og **uppsöfnun Innkaupa** í **Bókunaruppsetning** verður notað þegar fylgiskjöl sem eru tengdar við innhreyfingarskjal afurða eru bókaðar.
[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png) 

Með þessu sama dæmi, let's sjá hvernig bókun innhreyfingarskjals afurða verður áhrif á fjárhag og verkupplýsingar. 

**1. skref:** Stofna og staðfesta nýja innkaupapöntun til að skrá innkaup tölvu fyrir $1500 og uppsetningu fyrir $150 verksins.
[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Þegar innkaupapöntun er staðfest, ráðstafaðan kostnað eru stofnaðar fyrir verkið. 
[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Hafa færslur fyrir ráðstafaðan kostnað fyrir **Færsluuppruna** stillt á **Innkaupapöntun**. Stofnun og innkaupapöntun er staðfest ekki að stofna færslur fyrir verk. 

**2. skref:** Vörur og þjónustu fá afhentar og innhreyfingarskjal afurða er skráð. 

Bókun innhreyfingarskjals afurða mynda og bóka fylgiskjalið í fjárhag. Fylgiskjal verður debet útgjöld innkaupa, óreikningsfærð lykils og kredit lykil uppsafnaðra innkaupa. 
[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Bókun innhreyfingarskjals afurða verður að nota bókunaruppsetninguna fyrir innkaupategundir og afurðir og ekki bókunaruppsetningu verktegundirnar. Til að endurspegla rétt fjárhagsleg áhrif uppsöfnunar innkaupa, þessa uppsetningarforritið þarf að vera samstilltar. 

Það er hægt að varpa innkaupaflokka sem verktegundir á í **innkaupategund** síðu.
[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)

**Skref 3:** Búa til drög reikning lánardrottins. 

Í Dynamics 365 aðgerða bókun innhreyfingarskjals afurða hefur ekki áhrif á upplýsingar um verk. Er lausn sem tókst að mynda reikning lánardrottins drög beint eftir bókun innhreyfingar innkaupapantana. Farið í **Innkaupapöntun** síðu &gt;**Reiknings flipanum**&gt;**Mynda**&gt;**Reiknings**. Þetta stofnar skjal biðreikningur sem uppfærir verkupplýsingar. 

Stofna lánardrottinsreikning drög mynda verkfærslur í bið. 
[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

Í því **Ráðstafaður kostnaður** síðu færslur stofnaðar í þrepi 1 verður lokað og verður að stofna nýjar færslur til að endurspegla kostnaður ráðstöfun úr reikningi lánardrottins í bið. Í **færsluuppruna** fyrir ráðstafaðan kostnað verður stillt á **lánardrottinsreikning**.
[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)

Reikningur lánardrottins á að haldast í biðstöðu þar til reikning lánardrottins raunverulega berst.


