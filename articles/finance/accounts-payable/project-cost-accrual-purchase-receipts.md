---
title: Uppsöfnun á kostnaði verks á innkaupapöntunum
description: Þetta efnisatriði lýsir því hvernig hægt er að rekja uppsafnaðan verkkostnað úr innkaupapöntunum í Microsoft Dynamics 365 Finance.
author: sunfzam
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7ae2f57e0104a30492363f1576962d36a2a1b04b
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595231"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a>Uppsöfnun á kostnaði verks á innkaupapöntunum

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig hægt er að rekja uppsafnaðan verkkostnað úr innkaupapöntunum í Microsoft Dynamics 365 Finance. 

Reikningar fyrir verk berast oft síðar en vörur og þjónusta eru afhent, sem kann að hafa töluverð áhrif á afkastavísa verkefna (Afkastavísa). Mikilvægt er að það sé hægt að rekja þessar færslur í bæði fjárhags- og verkefnaskýrslum.

Eftirfarandi dæmi lýsir þessum aðstæðum. 

Contoso Consulting hefur komið á fót nýjum skýjarekstri. Innkaupapöntun er stofnuð til að kaupa tölvu fyrir verkefnið. Tölvan mun kosta $1500 og uppsetningarþjónusta mun kosta $150. Lánardrottinn hefur afhent og sett tölvuna upp, en reikningur hefur ekki enn borist Contoso Consulting. Stjórnanda verksins langar að sjá kostnaðaruppsöfnun verkefnisins upp á $1650 áður en reikningurinn er afhentur. Þessi kostnaður ætti einnig að endurspeglast í fjárhagsskýrslum fyrirtækisins í mánuðarlok. 

Uppsafnaðan kostnað þarf að skrá bæði á fjárhagslegu stigi og verkstig fyrir skýrslugerð. Hægt er að rekja fjárhagslega uppfærslu afurðarinnar fyrir vöru- og innkaupaflokka. 

Fyrir vörur, á síðunni **Færibreytur viðskiptaskulda**, veljið valkostinn **Bóka innhreyfingarskjöl afurða í fjárhag**.
[![Færibreytusíða viðskiptaskulda.](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Fyrir innkaupategundir, á síðunni **Stefnuregla tegundar** skal velja reglurnar **Innkaup** og síðan **Safna upp innkaupakostnaði á kvittun** fyrir hvern innkaupaflokk.
[![Stefnureglusíða vegna flokka.](./media/accruals2-1024x569.png)](./media/accruals2.png) 

Reikningarnir **Útgjöld innkaupa óreikningsfærð** og **Uppsöfnun innkaupa** í **Bókunaruppsetningu** verða notaðir þegar fylgiskjöl sem eru tengd við innhreyfingarskjal afurða eru bókuð.

Notum þetta sama dæmi til að sjá hvernig bókun innhreyfingarskjals afurða hefur áhrif á fjárhag og verkupplýsingar. 

**1. skref:** Stofna og staðfesta nýja innkaupapöntun fyrir verkefnið til að skrá innkaup á tölvu fyrir $1500 og uppsetningarþjónustu fyrir $150.
[![Stofna nýja innkaupapöntun.](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Þegar innkaupapöntun er staðfest eru færslur fyrir ráðstafaðan kostnað stofnaðar fyrir verkið. 
[![Færslur stofnaðar.](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Færslur fyrir ráðstafaðan kostnað munu hafa reitinn **Færsluuppruna** stilltan á **Innkaupapöntun**. Stofnun og staðfesting innkaupapöntunar stofnar ekki færslur fyrir verkefni. 

**2. skref:** Vörur og þjónustu eru afhentar og innhreyfingarskjal afurða er skráð. 

Bókun innhreyfingarskjals afurða er myndað og bókar fylgiskjalið í fjárhag. Fylgiskjal mun skuldfæra innkaupaútgjöld, óreikningsfærðan lykils og kreditfæra lykil uppsafnaðra innkaupa. 
[![Færslur fylgiskjals.](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Bókun innhreyfingarskjals afurða munu nota bókunaruppsetningu fyrir innkaupategundir og afurðir og ekki bókunaruppsetningu verktegundirnar. Til að endurspegla rétt fjárhagsleg áhrif uppsöfnunar innkaupa þarf þessi uppsetning að vera samstillt. 

Hægt er að varpa innkaupaflokka sem verktegundir á síðunni **Innkaupategund**.
[![Síða innkaupaflokks.](./media/accruals7-1024x390.png)](./media/accruals7.png)

**3. skref:** Stofnaðu reikning lánardrottins 

Bókun innhreyfingarskjals afurða ekki áhrif á upplýsingar um verk. Sem hjáleið er hægt að mynda drög að reikningi lánardrottins beint eftir bókun innhreyfingar innkaupapantana. Farðu á síðuna **Innkaupapöntun** á &gt; **Reikningsflipanum** &gt; **Mynda** &gt; **Reiknings**. Þetta stofnar reikningsskjal í bið sem uppfærir verkupplýsingar. 

Stofnun á lánardrottinsreikningsdrögum myndar verkfærslur í bið. 
[![Verkfærslur í bið.](./media/accruals8-1024x225.png)](./media/accruals8.png) 

Á síðunni **Ráðstafaður kostnaður** verður færslum sem voru stofnaðar í 1. skrefi lokað og nýjar færslur verða stofnaðar til að endurspegla kostnaðarráðstöfun af reikningi lánardrottins í bið. Í reitnum **Færsluuppruni** fyrir ráðstafaðan kostnað verður stillt á **Lánardrottinsreikning**.
[![Síðan Ráðstafaður kostnaður.](./media/accruals9-1024x200.png)](./media/accruals9.png)

Reikningur lánardrottins mun haldast í biðstöðu þar til að sjálfur reikningur lánardrottins berst.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
