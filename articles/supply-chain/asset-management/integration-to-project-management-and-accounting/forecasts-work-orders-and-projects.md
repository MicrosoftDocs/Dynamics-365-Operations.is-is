---
title: Spár, verkbeiðnir og verk
description: Þetta efni útskýrir spár og samþættingu verkbeiðni við verkefnastjórnun og bókhaldseininguna í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886817"
---
# <a name="forecasts-work-orders-and-projects"></a>Spár, verkbeiðnir og verk

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Í eignastjórnun er samþætting við eininguna **Verkefnisstjórnun og bókhald** gerð til að hámarka kostnaðareftirlit, sem gerir notendum kleift að fylgjast með kostnaði við spár um gerð viðhaldsverka og verkbeiðnivinnslur.

Til að rekja spár um gerðir viðhaldsverka verður að gera tvær stillingar:

1. Veldu verkefni á tenglinum **Eignastýring** > **Uppsetning** > **Færibreytur eignastýringar** > **Eignir** > flýtiflipanum **Verk** > reitnum **Verk viðhaldsspár**.

2. Í **Sjálfgefnar gerðir viðhaldsverka**, þegar þú býrð til sjálfgefna línu af gerð viðhaldsverks er aðgerðarnúmer sjálfkrafa búið til fyrir línuna (**Eignastýring** > **Uppsetning** > **Vinnslur** > **Sjálfgefnar gerðir viðhaldsverka**).

Spár um gerð viðhaldsverka þjóna tvennum tilgangi: Þú getur fylgst með kostnaði við spár um viðhaldsgerðir í einingunni **Verkefnisstjórnun og bókhald**. Ennfremur eru spár færðar sjálfkrafa yfir í verkbeiðnaverkefni þegar þú velur tegund viðhalds í verkbeiðnivinnslu.

Til að fylgjast með kostnaði við verkbeiðnavinnslur verður þú fyrst að setja upp verkbeiðnaverkefni. Sjá kaflann [Uppsetning verkbeiðniverka](../setup-for-work-orders/work-order-project-setup.md) fyrir lýsingu á ferlinu.

## <a name="work-order-job-projects"></a>Verkbeiðnaverkefni

Þegar þú býrð til verkbeiðnivinnslu í verkbeiðni ræðst verkbeiðniverkefnið af uppsetningu foreldraverkefnis fyrir verkbeiðnir í **Eignastjórnun** > **Uppsetning** > **Verkbeiðni** > **Uppsetning verkefnis**.

Verkbeiðnaverkefni eru mynduð með því að nota samsetningu af eftirfarandi upplýsingum um verkbeiðni:

- Verkbeiðnigerðin sem valin var í verkbeiðninni 
- Virk staðsetning sem tengist eigninni í verkpöntunarvinnslunni
- Eignagerð sem tengist eigninni í verkpöntunarvinnslunni  
- Áætlaður upphafs- og lokatími stilltur á verkbeiðnina  

Hugsanlegt er að ekki séu allar upplýsingar sem nefndar eru hér að ofan að finna í verkbeiðni. Þess vegna er leitin að yfirverki verkbeiðni gerð með því að nota fyrirliggjandi samsetningu gagna og velja verkefnisauðkenni sem samsvarar gögnum um verkbeiðni.

Dæmi: Á myndinni hér að neðan þýðir uppsetning eignategundarinnar „Vél í vörubíl“ að hver verkbeiðnivinnsla sem er mynduð með þá eignagerð verður undirverkefni verkkennis „000186“.

![Mynd 1](media/01-integration-to-pma.png)

Tilgangur verkkennis í verkbeiðnivinnslu og tengt númer verkþáttar (**Eignastjórnun** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** > veldu verkbeiðni í lista > flýtiflipann **Upplýsingar um línu** > reitnum **Verkkenni** og reitnum **Verkþáttanúmer**) er að fylgjast með kostnaði sem tengist verkbeiðnivinnslunni og eigninni sem er valin í verkbeiðnivinnslunni í einingunni **Verkefnisstjórnun og bókhald**. 

Á myndinni hér að neðan sérðu myndrænt yfirlit yfir verkbeiðniverk og skyldar aðgerðir verkefnis.

![Mynd 2](media/02-integration-to-pma.png)

Þegar ný verkbeiðnivinnsla er mynduð í verkbeiðni er verkbeiðniverk sjálfkrafa búið til fyrir vinnsluna. Fjárhagslegar víddir eignarinnar sem tengjast vinnslu á verkbeiðni eru sjálfkrafa fluttar yfir í verkbeiðniverkið. Verkþátturinn sem var stofnaður fyrir vinnslu verkbeiðni er með tengdar upplýsingar í viðhengi varðandi gerð viðhaldsverka, afbrigði af viðhaldsverkum og viðskipti. Þessi gögn eru gagnleg ef þú býrð til dæmis til innkaupapöntun úr verkbeiðni (sjá [Innkaup](../work-orders/procurement.md)), eða ef þú notar eininguna **Verkefnisstjórnun og bókhald** fyrir tímaskráningu.  

Ef eignin var sett upp á virkri staðsetningu og sú eign er seinna sett upp á annarri virkri staðsetningu, eru fjárhagsvíddir sem tengjast nýju virku staðsetningunni sjálfkrafa uppfærðar á eigninni. Þar af leiðandi, þegar þú býrð til verkbeiðnivinnslu fyrir eignina fær verkbeiðniverkið fyrir verkbeiðnivinnsluna sjálfkrafa fjárhagsvíddirnar sem nú tengjast eigninni. Þetta þýðir að þegar þú notar virkar staðsetningar er alltaf hægt að rekja kostnað á virkum staðsetningum þar sem eign var sett upp á hverjum tíma. Sjálfvirk uppfærsla fjárhagsvídda tryggir fullkominn rekjanleika kostnaðar við stjórnun og skýrslugerð verkefna.  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Verkbeiðniverk, líftímastöður verkbeiðnil, verkþrep og gerðir verka

Til að tryggja rétta notkun á líftímastöðum verkbeiðna og tengdum verkstigum á verkbeiðnum skaltu íhuga tengsl varðandi við eininguna **Verkefnisstjórnun og bókhald**:

- Í einingunni **Verkefnisstjórnun og bókhald** eru verkstig sett upp á verkgerðum í **Færibreytum verkefnisstjórnunar og bókhalds**.  
- Í **Færibreytum verkefnisstjórnunar og bókhalds** skaltu muna að velja viðeigandi gátreiti verkstigs fyrir allar verkgerðirnar sem þú ætlar að nota. Á myndinni hér að neðan hafa fimm stig **Stofnað** - **Áætlað** - **Tímaáætlað** - **Í ferli** - **Lokið** verið valin fyrir verkgerðirnar „Tími og efni“ og „Innra“. Þessi fimm stig eru mikilvæg bæði fyrir vinnslur innra viðhalds og viðhaldsþjónustu.  
- Í **Eignastjórnun** eru verkgerðir skilgreindar af verkhópunum sem þú settir upp í skjámyndinni **Uppsetning verkbeiðniverks** > tenglinum **Verkflokkur**.  
- Vkerhóparnir sem eru settir upp í **Uppsetning verkbeiðniverks** eru notaðir þegar þú býrð til verkbeiðnir. Þegar verkbeiðni er stofnuð er verkbeiðniverk sjálfkrafa búið til fyrir verkbeiðnina.  
- Líftímastöður verkbeiðni verða allar að hafa tengt verkefnastig.  
- Verkstigið sem tengist líftímastöðu verkbeiðni verður að skilgreina sem virkt stig fyrir verkhópinn sem skilgreindur er í verkbeiðniverkinu. Verk verkbeiðninnar er sjálfkrafa myndað í verkbeiðni.  
- Þegar þú býrð til nýja verkbeiðni er sjálfvirk úthlutun á verkbeiðniverki byggð á uppsetningunni í **Verkuppsetningu verkbeiðni** (**Eignastjórnun** > **Uppsetning** > **Verkbeiðnir** > **Uppsetning verkefnis**).  

Tengingar milli verkhópa í verkbeiðni, tengdar verkgerðir, verkstig og líftímastöður verkbeiðna eru sýndar á myndunum hér að neðan.  

![Mynd 3](media/03-integration-to-pma.png)

![Mynd 4](media/04-integration-to-pma.png)

![Mynd 5](media/05-integration-to-pma.png)

Sjá [Uppsetning verkbeiðniverka](../setup-for-work-orders/work-order-project-setup.md) varðandi hvernig eigi að setja upp verkbeiðniverk og [Líftímastöður verkbeiðna](../setup-for-work-orders/work-order-lifecycle-states.md) varðandi hvernig eigi að búa til líftímastöður verkbeiðna.

Myndin hér að neðan sýnir myndrænt yfirlit yfir hin ýmsu verkefni sem eru búin til í einingunni **Eignastjórnun** til að leyfa samþættingu við eininguna **Verkefnisstjórnun og bókhald**, svo og vinnuferlum sem verkefnin tengjast.

![Mynd 6](media/06-integration-to-pma.png)

