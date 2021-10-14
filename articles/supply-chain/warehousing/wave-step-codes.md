---
title: Kóðar bylgjuskrefs
description: Þetta efni veitir yfirlit yfir bylgjuskrefakóða og hvernig þeir eru notaðir.
author: Mirzaab
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c32e795fcb12be02d9c9324051101fa378935303
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572242"
---
# <a name="wave-step-codes"></a>Kóðar bylgjuskrefs

[!include [banner](../includes/banner.md)]

Bylgjuskrefakóðar eru kóðar sem notendur geta sett upp og notað til að tengja sérstök tilvik bylgjuaðferða við samsvarandi sniðmát. Sniðmátin innihalda sniðmát fyrir áfyllingu, gámagerð, prentun merkimiða, byggingu álags og flokkun.

Þegar bylgjuskrefakóðar eru ekki notaðir, verða notendur að slá inn frjálsan texta til að vísa í ákveðið sniðmát frá bylgjuaðferðartilvikinu. Frjáls texti er viðkvæmur fyrir villum, vegna þess að notendur verða að ganga úr skugga um að bylgjuskrefatextinn sem þeir bæta við fyrir tiltekna bylgjuþrepaðferð í bylgjusniðmáti samsvari nákvæmlega bylgjuskrefatextanum í marksniðinu.

Bylgjuskrefakóðar fyrir ákveðna gerð bylgjuskrefa eru settir upp á aðskildri síðu. Fyrir hvert tilvik um bylgjuþrep í bylgjusniðmát sem krefst bylgjuþrepskóða verður að velja bylgjuskrefakóðann í fellilistanum. Val í fellivalmynd kemur í staðinn fyrir frjálsan texta og hjálpar til við að draga úr hættu og áhrifum mannlegra mistaka. Uppsetningarkóðar eru notaðir til að tengja bylgjuþrep aðferð í bylgjusniðmát við marksnið fyrir aðferðina.

> [!NOTE]
> Notkun kóðaeiginleika bylgjuskrefa er valkvæð. Hún er virkjum í öllu fyrirtækinu fyrir alla lögaðila.

## <a name="setup-demo"></a>Setja upp kynningu 

Fyrir þessa kynningu verða kynningargögn að vera sett upp og þú verður að nota kynningarfyrirtækið **USMF**.

### <a name="enable-wave-step-codes"></a>Virkja kóða bylgjuskrefs

Fylgdu þessum skrefum til að kveikja á bylgjuskrefakóða.

1. Farðu í **Stjórnun eiginleika**.
2. Veldu til að virkja eiginleikann sem heitir **Kóði bylgjuskrefa í öllu fyrirtækinu**.

Allir fyrirliggjandi frjálsir textar bylgjuskrefa í öllum lögaðilum eru uppfærðir í nýja uppbygginguna. Eftir að þessari uppfærslu er lokið fyrir alla lögaðila er eiginleikinn virkur. Ef ekki er hægt að virkja eiginleikann fyrir einn eða fleiri lögaðila er hann ekki virkur fyrir neina lögaðila.

Meðan á virkjuninni stendur er staðfesting gerð við uppfærslu gagna. Ef uppfærsla mistekst færðu villuboð. Uppfærsla gæti mistekist vegna eftirfarandi árekstra:

- Tvíteknir frjálsir textar bylgjuskrefa eru til.
- Sérsnið er til staðar.
- Frjáls texti bylgjuskrefa sem er tengdur dæmi um aðferð við bylgjuþrep passar ekki við gerð sniðmátsins.

Eftir að þú hefur leyst alla árekstra sem eru greindir við staðfestingarnar geturðu reynt aftur að virkja eiginleikann.

Þegar eiginleikinn hefur verið virkjaður verður síðan **Bylgjuskrefakóðar** (**Vöruhúsastjórnun \> Uppsetning \> Bylgjur \> Bylgjuskrefakóðar**) í boði. Þessi síða sýnir bylgjuskrefakóða sem voru uppfærðir þegar eiginleikinn Kóði bylgjuskrefa í öllu fyrirtækinu var virkjaður.

### <a name="create-new-wave-step-codes"></a>Stofna nýja bylgjuskrefakóða

Þú getur notað síðuna **Bylgjuskrefakóðar** til að búa til og eyða bylgjuskrefakóðum.

Sérhver nýr bylgjuskrefakóði og það tilheyrandi auðkenni verður að vera sérstakt fyrir allar tegundir bylgjuskrefa og verður að skilgreina þær fyrir ákveðna gerð bylgjuskrefa.

### <a name="apply-wave-step-codes"></a>Beita bylgjuskrefakóðum

Eftir að þú hefur skilgreint viðeigandi bylgjuskrefakóða er hægt að beita þeim á bylgjuferlaaðferðirnar.

Til að beita bylgjuskrefakóða, farðu í viðeigandi marksniðmát. Hér eru marksniðmát sem bylgjuskrefakóðarnir eru tilnefndir til að benda á:

- **Sniðmát áfyllingar:** Vöruhúsakerfi \> Uppsetning \> Áfylling \> Áfyllingarsniðmát
- **Hlaða sniðmát:** Vöruhúsastjórnun \> Uppsetning \> Álag \> Sniðmát hleðslu
- **Raða sniðmátum:** Vöruhúsastjórnun \> Uppsetning \> Pökkun \> Sniðmát fyrir útleið
- **Gámunarsniðmát:** Vöruhúsakerfi \> Uppsetning \> Gámar \> Gámaröðunarsniðmát
- **Sniðmát fyrir prentunarmerki:** Vöruhúsastjórnun \> Uppsetning \> Beining skjals \> Sniðmát bylgju

Sniðmátin á þessum lista eru notuð þegar þeim er vísað frá bylgjuferlisaðferð sem er valin í bylgjusniðmát. Þegar bylgjuskrefakóðinn á bylgjuferlisaðferð í bylgjusniðmáti passar bylgjuskrefakóðann í einni af sniðmátategundunum er sniðmátinu beitt.

### <a name="sample-scenario"></a>Dæmi

Eftirfarandi aðferð hjálpar til við að tryggja að endurnýjunarsniðmátið sem þú bjóst til verður beitt fyrir bylgjusniðmát.

1. Farðu í **Vöruhúsastjórnun \> Uppsetning \> Bylgjur \> Bylgjuskrefakóðar**, og stofnaðu bylgjuskrefakóða fyrir gerðina **Endurnýjun**.
2. Farðu í **Vöruhúsakerfi \> Uppsetning \> Áfylling \> Áfyllingarsniðmát** og stofnaðu áfyllingarsniðmát.
3. Veldu áfyllingar sniðmátið, veldu bylgjuskrefakóðann sem þú bjóst til fyrir gerðina **Áfylling**.
4. Farðu í **Vöruhúsastjórnun \> Uppsetning \> Bylgjur \> Bylgjusniðmát** og veldu bylgjusniðmátið sem þú ætlar að nota.
5. Í sniðmátinu á flýtiflipanum **Aðferðir** velurðu aðferðina **Áfylling**.
6. Í reitnum **Bylgjuskrefakóði** velurðu bylgjuskrefakóðann sem þú valdir í áfyllingarsniðinu.

Þú framkvæmir þessi skref fyrir hvern lögaðila.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]