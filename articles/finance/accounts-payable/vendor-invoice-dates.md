---
title: Dagsetningar reiknings lánardrottins
description: Þessi grein lýsir dagsetningum sem birtast á reikningum lánardrottins. Það útskýrir einnig hvernig eigi að stilla bókunardagsetningu sjálfkrafa.
author: sunfzam
ms.date: 2/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 022fd0ce07fbb4c54afcf7334c1c9411e01dcf26
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775273"
---
# <a name="vendor-invoice-dates"></a>Dagsetningar reiknings lánardrottins

[!include [banner](../includes/banner.md)]

Þessi grein lýsir dagsetningum sem birtast á reikningum lánardrottins. Það útskýrir einnig hvernig eigi að stilla bókunardagsetningu sjálfkrafa.

Á **Útskýrður reikningur seljanda í bið** síðu sýnir reikningshausinn fjórar dagsetningar: **Reikningur móttekinn dags**, **reiknings**, **·**, og **Gjalddagi**. Þegar reikningur lánardrottins er búinn til eru eftirfarandi dagsetningar slegnar inn sjálfgefið:

- **Móttökudagsetning reiknings** – Þessi reitur er stilltur á núgildandi dagsetningu kerfis.
- **Bókunardagsetning** – Þessi reitur er stilltur á núgildandi dagsetningu kerfis. 
- **Gjalddagi** – Dagsetningin í þessum reit er reiknuð samkvæmt bókunardagsetningu og greiðsluskilmálum.
- **Reikningsdagsetning** – Reiturinn er sjálfgefið auður. Hinsvegar er hægt að færa inn gildi eftir þörfum. Í því tilviki er dagsetningin í reitnum **Gjalddagi** endurreiknuð miðað við dagsetningu reiknings og greiðsluskilmála.

Stundum gæti reikningur lánardrottins verið í biðstöðu í langan tíma eftir að tímabilinu lýkur. Þegar hann er tilbúinn til bókunar er gamla bókunardagsetning síðasta bókunartímabils áfram notuð. Því tímabili hefur hinsvegar verið lokað. Þar af leiðandi verður starfsmaður viðskiptaskulda að breyta öllum bókunardagsetningum handvirkt í nýja bókunartímabilið fyrir alla reikninga í bið sem voru búnir til áður.

Eiginleikinn sem lýst er í þessari grein gerir þér kleift að stilla bókunardagsetningu sjálfkrafa í samræmi við kröfur fyrirtækisins.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Færibreytur til að breyta sjálfkrafa bókunardagsetningu lánardrottnareiknings

Fylgdu þessum skrefum til að stilla sjálfkrafa bókunardagsetningu fyrir reikninga lánardrottins.

1.  Farðu í **Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**.
2.  Á flipanum **Fjárhagur og virðisaukaskattur**, í reitnum **Stilla bókunardagsetningu sjálfkrafa**, skal velja eitt af eftirfarandi gildum:

    - **Engin breyting** – Kerfið breytir ekki bókunardagsetningu sjálfkrafa meðan á bókun stendur. Gildið er sjálfgefið valið.
    - **Breyttu alltaf bókunardagsetningu í kerfisdagsetningu** – Bókunardagsetningu breytist sjálfkrafa í kerfisdagsetningu við bókun.
    - **Breyttu bókunardagsetningu í kerfisdagsetningu þegar bókunardagsetningartímabili er lokað eða í bið** – Bókunardagsetningu breytist sjálfkrafa í kerfisdagsetningu við færslu, en aðeins ef samsvarandi tímabil færsludagsetningar hefur stöðuna **Lokað** eða **Á bið**.
    - **Breyttu færsludagsetningu í fyrsta dag nýs tímabils þegar færsludagsetningartímabili er lokað eða í bið** – Bókunardagsetningu er breytt í fyrsta dag nýja opna tímabilsins, en aðeins ef samsvarandi tímabil birtingardagsins hefur stöðuna **Lokað** eða **Á bið**.

> [!NOTE]
> Ef nýja bókunardagsetningin sem var sjálfvirk leiðrétt er á nýju reikningsári verður bókunardagsetning reikningsins ekki uppfærð. Notandinn mun fá villuna „Fjárhagsárið hefur breyst. Vinsamlegast athugaðu og sláðu inn birtingardagsetninguna aftur." Bókunardagsetning reiknings verður að vera uppfærð í nýja dagsetningu reikningsárs til að geta bókað.

## <a name="impact-of-posting-date-changes"></a>Áhrif breytinga á bókunardagsetningu

Þegar bókunardagsetningu á lánardrottnareikningi í bið er breytt hefur breytingin eftirfarandi áhrif:

- **Lokadagur**

    - Ef reiturinn **Reikningsdagsetning** er auður er gjalddaginn endurreiknaður miðað við nýja bókunardagsetningu og greiðsluskilmála.
    - Ef reiturinn **Reikningsdagsetning** var stilltur áður hefur breyting bókunardagsetningar ekki áhrif á gjalddagann.

- **Dagsetning staðgreiðsluafsláttar**

    - Ef reiturinn **Reikningsdagsetning** er auður er nýja bókunardagsetningin notuð til að reikna staðgreiðsluafslátt.
    - Ef reiturinn **Reikningsdagsetning** var stilltur áður er staðgreiðsluafslætti ekki breytt.

- **Gengi** – Gengisdagsetningin er ákvörðuð með stillingunni á valkostinum **Uppfæra lánardrottnalykil með reikningsdagsetningu** á flipanum **Reikningur** á síðunni **Færibreytur viðskiptaskulda** (**Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**).

    - Ef þessi valkostur er stilltur á **Já**, hinn **Dagsetning reiknings** er notað, og **Birtingardagur** breyting hefur ekki áhrif á gengi krónunnar.
    - Ef þessi valkostur er stilltur á **Nei** er bókunardagsetningin notuð til að reikna gengið. Þegar bókunardagsetningin er uppfærð eru bókhalds- og skýrsluupphæðir endurreiknaðar. Þar af leiðandi þarf að villuleita samsvörun aftur.

## <a name="validation"></a>Villuleit

Tveir aðrir reitir á flipanum **Reikningur** á síðunni **Færibreytur viðskiptaskulda** (**Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**) hafa áhrif á vinnslu reiknings:

- Ef **Athugaðu reikningsnúmerið sem notað er** reiturinn er stilltur á **Hafna afritum innan reikningsárs**, verður bókunardagsetningin notuð til að athuga með tvítekna reikninga við bókun reikninga.
- Ef reiturinn **Krefjast dagsetningar skjals á reikningi lánardrottins** er stilltur á **Villuvalkostur** er gerð krafa um reitinn **Reikningsdagsetning í haus reiknings í bið**. Ef reikningsdagsetning er síðar en bókunardagsetning birtast villuboð.
