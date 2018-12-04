---
title: "Kostnaðargreining framleiðslupöntunar"
description: "Þessi skrá veitir upplýsingar um kostnaðargreiningar sem er hægt að gera fyrir loknar og gildandi framleiðslupantanir. Hægt er að greina áætlaðan kostnað og raunkostnað með því að nota síðuna Útreikningur á verði eða skýrsluna Kostnaðarmat og kostnaðarútreikningur. Hægt er að skoða upplýsingar um áætlaðan kostnað og raunkostnað (og magn) fyrir hverja íhlutavöru, leiðaraðgerð og óbeinan kostnað."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 40ac5108216fd6d9eb5cd6e76fefd66828a7da84
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="production-order-cost-analysis"></a>Kostnaðargreining framleiðslupöntunar

[!include [banner](../includes/banner.md)]

Þessi skrá veitir upplýsingar um kostnaðargreiningar sem er hægt að gera fyrir loknar og gildandi framleiðslupantanir. Hægt er að greina áætlaðan kostnað og raunkostnað með því að nota síðuna Útreikningur á verði eða skýrsluna Kostnaðarmat og kostnaðarútreikningur. Hægt er að skoða upplýsingar um áætlaðan kostnað og raunkostnað (og magn) fyrir hverja íhlutavöru, leiðaraðgerð og óbeinan kostnað.

Raunkostnaðurinn fyrir framleiðslupöntun er byggð á skráðri notkun efnis og leiðaraðgerða. Hægt er að fara í ítarlegar færslur um skráða efnisnotkun, leiðaraðgerðir og óbeinan kostnað fyrir framleiðslupöntun í skjámyndinni **Framleiðslubókun**.

## <a name="variance-analysis-for-a-completed-production-order"></a>Greining frávika fyrir framleiðslupöntun sem lokið hefur verið við
Frávikin endurspegla samanburð á skráðum verkþáttum framleiðslu og útreikningum staðlaðs kostnaðarverðs fyrir framleiðsluvöruna. Frávikin endurspegla ekki samanburð við áætlaðan kostnað framleiðslupöntunarinnar. Skráðir verkþættir framleiðslu innihalda notkun hráefnis og leiðaraðgerðir ásamt tengdum óbeinum kostnaði, og magnið sem skráð er sem lokið. Eftirfarandi fjórar gerðir af frávikum eru reiknuð út:

-   Lotustærðarfrávik
-   Framleiðsla magnfrávika
-   Frávik framleiðsluverða
-   Framleiðsla staðgengilsfrávika

Eftirfarandi skýringarmynd sýnir fjögur frávik sem útskýra mismuninn á milli raunkostnaðar framleiðslupöntunar og útreiknaðs kostnaðar innan kostnaðarfærslu vörunnar þegar lokið var við framleiðslupöntunina. 

![Frávik sem útskýra mismun í lokinni framleiðslupöntun](./media/control.jpg) 

Hægt er að greina framleiðslufrávik með því að nota síðuna **Frávik** eða skýrsluna **Framleiðslufrávik**. Notið valkosti um birtingu til að skoða einstök frávik eftir vöru og rekstrartilföngum, eða eftir kostnaðarflokki. Reglur um niðurbrot kostnaðar innan birgðafæribreyta ákvarðar hvort að frávikin verða rakin eftir kostnaðarflokki. Einnig er hægt að nota sýnimöguleikana **ein**, **margar**, og **samtals** til að skoða samantekt frávika. Nákvæmar upplýsingar um frávik hjálpa við að skilja orsakir hvers fráviks. Til þess að sjá fyrir frávik áður en lokið er við framleiðslupöntun, greinið hinar nákvæmu upplýsingar sem eru gefnar í skýrslunni **Kostnaðaráætlun og kostnaðarútreikningur**.

## <a name="cost-analysis-for-current-production-orders"></a>Kostnaðargreining gildandi framleiðslupantana.
Aðskildar skýrslur veita upplýsingar fyrir hverja færslugerð. Notið þessar skýrslur til að greina kostnað fyrir skráða framleiðsluverkþætti. Upplýsingar eru aðeins birtar fyrir núverandi framleiðslupantanir með stöðuna **Byrjað** eða**Tilbúið**.

-   **Hráefni í vinnslu**- Skýrslan telur upp þær færslur tiltektarlista sem eru skráðar á móti núverandi framleiðslupöntunum frá og með tiltekinni færsludagsetningu. Skýrslan gefur til kynna íhlutamagn sem var útgefið og kostnaðarmagnið fyrir hverja færslu. Notið valskilyrði fyrir einstakan íhlut. Til dæmis er hægt að prenta upplýsingar um útgefið magn íhluta á móti viðeigandi framleiðslupöntunum. Útgefið magn er ekki uppfært með magni sem er skráð sem lokið fyrir yfirvöruna. Þess vegna getur magn hráefnis í vinnslu verið ýkt.
-   **Verk í vinnslu**- Skýrslan telur upp leiðar- (eða vinnslu-) færslur sem hafa verið skráðar gegn núverandi framleiðslupöntunum frá og með tiltekinni færsludagsetningu. Skýrslan gefur til kynna vinnutímana, upphæðina og magnið (bæði gott magn og villumagn) sem er skráð fyrir hverja færslu. Það felur einnig í sér upplýsingar eins og aðgerðarnúmerið, Kenni aðgerðar og rekstrartilföng. Skýrslan birtir einnig heildartíma og heildarupphæð allra færslna á móti framleiðslupöntuninni og magn þess sem hefur verið skráð sem tilbúið.
-   **Óbeinn kostnaður í vinnslu**− Skýrslan telur upp óbeinan kostnað sem er búinn að myndast gegn framleiðslupöntunum. Þessi gögn eru byggð á skráðri notkun leiðaraðgerða og íhluta frá og með tiltekinni færsludagsetningu. Skýrslan gefur til kynna gerð óbeins kostnaðar (álag eða taxta), kostnaðarskjalskóða óbeina kostnaðarins og kostnaðarupphæð hverrar færslu. Skýrslan veitir ekki upplýsingar um leiðarspjaldið eða tiltektarlistafærsluna sem myndaði óbeina kostnaðinn.
-   **Kostnaðarútreikningur framleiðslu í vinnslu** − Skýrslan telur upp sameinaða notkun efnis, leiðaraðgerðir og óbeinan kostnað á móti framleiðslupöntununum frá og með tiltekinni færsludagsetningu.
-   **Afurðir í vinnslu**− Skýrslan telur upp núverandi framleiðslupantanir og færslurnar sem skráðar eru sem lokið frá og með tiltekinni færsludagsetningu.


<a name="additional-resources"></a>Frekari upplýsingar
--------

[Algengur uppruni framleiðslufrávika](common-sources-of-production-variances.md)




