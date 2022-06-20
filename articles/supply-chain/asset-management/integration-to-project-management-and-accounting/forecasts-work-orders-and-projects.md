---
title: Spár, verkbeiðnir og verk
description: Þessi grein útskýrir spár og samþættingu verkbeiðna við verkefnastjórnun og bókhaldseininguna í eignastýringu.
author: johanhoffmann
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 80f0380d50a0c050242846c0c3e70bc1a0bd6bf5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880452"
---
# <a name="forecasts-work-orders-and-projects"></a>Spár, verkbeiðnir og verk

[!include [banner](../../includes/banner.md)]

 

Í eignastjórnun hjálpar samþætting við eininguna **Verkefnisstjórnun og bókhald** við að hámarka kostnaðareftirlit, svo að notendur geta fylgst með kostnaði við spár um gerð viðhaldsverka og verkbeiðnivinnslur.

Rakning á spám um gerðir viðhaldsverka krefst tveggja stillinga:

1. Veldu verkefni í **Eignastýring** > **Uppsetning** > **Breytur eignastýringar**, og síðan á flipanum **Eignir** > á flýtiflipanum **Verkefni**, í reitnum **Verkefni viðhaldsspá**, veldu verkefni.

2. Þegar þú stofnar sjálfgefna línu gerðar viðhaldsstarfs er aðgerðarnúmer sjálfkrafa stofnað fyrir línuna á síðunni **Sjálfgefin tegund viðhaldsverka** (**Eignastjórnun** > **Uppsenting** > **Vinnslur** > **Sjálfgefnar gerðir viðhaldsverka**).

Spár um gerðir viðhaldsverka þjóna tvennum tilgangi: 

- Þú getur fylgst með kostnaði við spár um gerðir viðhaldsverka í einingunni **Verkefnisstjórnun og bókhald**. 
- Spár eru færðar sjálfkrafa yfir í verkbeiðnaverkefni þegar þú velur tegund viðhalds í verkbeiðnivinnslu.

Til að fylgjast með kostnaði við verkbeiðnavinnslur verður þú fyrst að setja upp verkbeiðnaverkefni. Frekari upplýsingar eru í [Verkuppsetning verkbeiðni](../setup-for-work-orders/work-order-project-setup.md).

## <a name="work-order-job-projects"></a>Verkbeiðnaverkefni

Þegar þú býrð til verkbeiðnivinnslu í verkbeiðni ræðst verkbeiðniverkefnið af uppsetningu foreldraverkefnis fyrir verkbeiðnir á síðunni **Verkuppsetning verkbeiðni** (**Eignastjórnun** > **Uppsetning** > **Verkbeiðni** > **Uppsetning verkefnis**).

Verkbeiðnaverkefni eru mynduð með því að nota samsetningu af eftirfarandi upplýsingum um verkbeiðni:

- Verkbeiðnigerðin sem valin var í verkbeiðninni 
- Virk staðsetning sem tengist eigninni í verkpöntunarvinnslunni
- Eignagerðin sem tengist eigninni í verkpöntunarvinnslunni  
- Áætlaðir upphafs- og lokatímar sem eru stilltir í verkbeiðninni  

Sumar þessara upplýsinga er hugsanlega ekki að finna í vinnupöntun. Þess vegna er leitin að yfirverki verkbeiðni gerð með því að nota fyrirliggjandi samsetningu gagna og velja verkefnisauðkenni sem samsvarar gögnum um verkbeiðni.

Til dæmis, á eftirfarandi mynd, vegna þess hvernig eignategundin **Vörubíll vél** er sett upp, verður hver vinnupöntunarvinna sem er búin til með eignategundinni **Vörubíll vél** að vera undirverkefni verkefnis ID 000186.

![Mynd 1.](media/01-integration-to-pma.png)

Tilgangurinn með auðkenni verkefnisins í vinnupöntunarstörfinu, og tilheyrandi athafnanúmeri, er að rekja kostnað sem er tengdur vinnu pöntunarstarfinu og eigninni sem er valin á það, í einingunni **Verkefnisstjórnun og bókhald**. (Til að skoða auðkenni verkefnisins og aðgerðarnúmerið, veldu **Eignastýring** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** og veldu síðan verkbeiðnina. Á flýtiflipanum **Línulýsing** sýnir reiturinn **Verkkenni** auðkenni verksins og reiturinn **Aðgerðarnúmer** sýnir númer aðgerðar.) Sjá frekari upplýsingar um kostnaðarstýringu í eignastýringu [Stjórnun kostnaðar og dagsetningar](../controlling-and-reporting/cost-and-date-control.md).

Eftirfarandi mynd sýnir myndrænt yfirlit yfir verkbeiðniverk og skyldar aðgerðir verkefnis.

![Mynd 2.](media/02-integration-to-pma.png)

Þegar ný verkbeiðnivinnsla er mynduð í verkbeiðni er verkbeiðniverk sjálfkrafa búið til fyrir vinnsluna. Fjárhagslegar víddir eignarinnar sem tengjast vinnslu á verkbeiðni eru sjálfkrafa fluttar yfir í verkbeiðniverkið.

Verkefnastarfsemin sem er búin til vegna vinnslu á verkbeiðni hefur tengdar upplýsingar sem fylgja henni. Þessar upplýsingar snúast um gerð viðhaldsverka, gerðarafbrigði viðhaldsverka og viðskipti. Þau eru gagnleg ef þú býrð til dæmis til innkaupapöntun úr verkbeiðni (sjá [Innkaup](../work-orders/procurement.md)), eða ef þú notar eininguna **Verkefnisstjórnun og bókhald** fyrir tímaskráningu.

Ef eignin var sett upp á virkri staðsetningu en er seinna sett upp á annarri virkri staðsetningu, eru fjárhagsvíddir sem tengjast nýju virku staðsetningunni sjálfkrafa uppfærðar á eigninni. Síðan, þegar þú býrð til verkbeiðnivinnslu fyrir eignina fær verkbeiðniverkið fyrir verkbeiðnivinnsluna sjálfkrafa fjárhagsvíddirnar sem nú tengjast eigninni. Þar af leiðandi, þegar þú notar virkar staðsetningar er alltaf hægt að rekja kostnað á virkum staðsetningum þar sem eign var sett upp á hverjum tíma. Sjálfvirk uppfærsla fjárhagsvídda tryggir fullkominn rekjanleika kostnaðar við stjórnun og skýrslugerð verkefna.

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Verkbeiðniverk, líftímastöður verkbeiðnil, verkþrep og gerðir verka

Til að tryggja að líftímastöður verkbeiðna og tengdra verkstiga á verkbeiðnum séu notaðar rétt skaltu íhuga tengsl varðandi við eininguna **Verkefnisstjórnun og bókhald**:

- Í einingunni **Verkefnisstjórnun og bókhald** eru verkstig sett upp á verkgerðum á síðunni **Færibreytum verkefnisstjórnunar og bókhalds**.  
- Á síðunni **Færibreytur verkefnisstjórnunar og bókhalds** notarðu gátreitina til að velja viðeigandi verkgerðirnar fyrir allar verkgerðirnar sem þú ætlar að nota. Á eftirfarandi myndum hafa fimm stig (**Stofnað**, **Áætlað**, **Tímaáætlað**, **Í ferli** og **Lokið**) verið valin fyrir verkgerðirnar **Tími og efni** og **Innra**. Þessi fimm stig eru mikilvæg bæði fyrir vinnslur innra viðhaldsvinnlsa og viðhaldsþjónustu.
- Í einingunni **Eignastýring** eru verkefnategundir skilgreindar af verkefnahópunum sem þú settir upp á síðunni **Uppsetning vinnuverkefna** > **Verkefnahópur** flipanum (**Eignastýring** > **Uppsetning** > **Verkbeiðnir** > **Uppsetning verkefnis**).  
- Verkhóparnir sem eru settir upp á síðunni **Uppsetning verkbeiðniverks** eru notaðir þegar þú býrð til verkbeiðnir. Þegar verkbeiðni er stofnuð er verkbeiðniverk sjálfkrafa búið til fyrir verkbeiðnina.  
- Í hvert skipti sem líftímastaða verkbeiðni verða að hafa tengt verkefnastig.  
- Verkstigið sem tengist líftímastöðu verkbeiðni verður að skilgreina sem virkt stig fyrir verkhópinn sem er skilgreindur í verkbeiðniverkinu. Verk verkbeiðninnar er sjálfkrafa myndað í verkbeiðni.
- Þegar þú býrð til nýja verkbeiðni er sjálfvirk úthlutun á verkbeiðniverki byggð á uppsetningunni á síðunni **Verkuppsetning verkbeiðni**.  

Eftirfarandi myndir sýna tengingar milli verkhópa í verkbeiðni, tengdar verkgerðir, verkstig og líftímastöður verkbeiðna.

![Mynd 3.](media/03-integration-to-pma.png)

![Mynd 4.](media/04-integration-to-pma.png)

![Mynd 5.](media/05-integration-to-pma.png)

Nánari upplýsingar um hvernig setja skal upp verk verkbeiðna er að finna í [Verkuppsetning verkbeiðni](../setup-for-work-orders/work-order-project-setup.md). Upplýsingar um hvernig skal stofna líftímastöður verkbeiðna er að finna í [Líftímastöður verkbeiðna](../setup-for-work-orders/work-order-lifecycle-states.md).

Eftirfarandi mynd sýnir myndrænt yfirlit yfir hin ýmsu verkefni sem eru búin til í einingunni **Eignastýring** til að gera samþættingu við eininguna **Verkefnisstjórnun og bókhald**. Það sýnir einnig verkferla sem verkefnin tengjast.

![Mynd 6.](media/06-integration-to-pma.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]