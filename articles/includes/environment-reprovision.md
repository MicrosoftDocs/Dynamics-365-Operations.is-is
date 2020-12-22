---
ms.openlocfilehash: f6bf4b6c946ebc63d3d84140f762cd4b789deb03
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459227"
---
Þegar gagnagrunnur er afritaður á milli umhverfa þarf að keyra endurúthlutunarverkfæri áður en afritaði gagnagrunnurinn nær fullri virkni til að tryggja að allir Commerce-íhlutir séu uppfærðir.

> [!IMPORTANT]
> Mælt er með því að þetta ferli sé keyrt hvort sem Commerce-íhlutir eru notaðir eða ekki þar sem virkni Commerce er hluti af öllum tegundum umhverfis. 

Áður en haldið er áfram þarf að ganga úr skugga um að eftirfarandi skilyrði séu uppfyllt:
1. Ef þú ert að uppfæra í útgáfuna frá júlí 2017 (einnig kölluð 7.2) 7.2.11792.56024 skaltu nota eftirfarandi X++ bráðabætur forrits í umhverfi viðtökustaðar áður en gagnauppfærslan er keyrð í því umhverfi. Þetta kemur í veg fyrir að fjöldi af villum komi upp við gagnauppfærsluna:

    - KB 4036156 – uppfærsla á lítilli útgáfu Retail – „númeraröð vöruvíddasamsetningar er ekki tilgreind.“ Þessi lagfæringarpakki inniheldur einnig KB 4035399 og KB 4035751. Athugið að til að nota þennan pakka þarf verkvangsuppfærsla 9 eða nýrri að vera til staðar. Ef óvissa er um það skal setja upp nýjustu tvíundaskrár.
    
2. Ef þú ert að uppfæra úr Microsoft Dynamics AX 2012 skaltu nota eftirfarandi X++ bráðabætur forrits í umhverfi viðtökustaðar áður en gagnauppfærslan er keyrð:
    - KB 4033183 - Dynamics AX 2012 R2 eða Dynamics AX 2012 R3 Pre-CU8 uppfærsla fyrir annað en smásölu mistekst ef hlutur finnst ekki fyrir dbo.RETAILTILLLAYOUTZONE.
    - KB 4040692 - Dynamics AX 2012 R3 í Microsoft Dynamics 365 for Operations 7.2 uppfærsla mistekst vegna tvítekningar í atriðisorðaskrá RetailSalesLine í SalesLineIdx.
    - KB 4035490 - Afkastatengt vandamál með uppfærsluforskrift svæðisins GeneralJournalAccountEntry í MainAccount.


Fylgdu þessum leiðbeiningum til að keyra endurúthlutunarverkfæri umhverfisins.

1. Í samnýttu eignasafni skaltu velja **Virkjanlegan hugbúnaðarpakka**.
2. Sæktu endurúthlutunarverkfæri umhverfis.
3. Í eignasafninu fyrir verkið þitt skaltu velja **Virkjanlegan hugbúnaðarpakka**.
4. Veldu **Nýr** til að stofna nýjan pakka.
5. Sláðu inn heiti og lýsingu fyrir pakkann. Þú getur notað **Endurúthlutunarverkfæri umhverfis** sem heiti pakkans.
6. Hlaðið upp pakkanum sem var sóttur áðan.
7. Á síðunni **Umhverfisupplýsingar** fyrir markumhverfið skal velja **Vinna með** > **Nota uppfærslur**.
8. Veldu endurúthlutunarverkfæri umhverfis sem var hlaðið upp áðan og veljið svo **Nota** til að nota pakkann.
9. Fylgist með framvindu uppsetningar pakkans. 

Frekari upplýsingar um hvernig á að nota virkjanlegan pakka má finna í [Virkjanlegur pakki notaður](../deployment/create-apply-deployable-package.md). Frekari upplýsingar um hvernig á að nota virkjanlegan pakka handvirkt má finna í [Uppsetning virkjanlegs pakka](../deployment/install-deployable-package.md).
