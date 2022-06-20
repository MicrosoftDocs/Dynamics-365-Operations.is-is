---
title: Dagsetningar reiknings lánardrottins
description: Þessi grein lýsir dagsetningum sem birtast á reikningum lánardrottins. Einnig er útskýrt hvernig kerfið er sett upp þannig að það stilli sjálfkrafa bókunardagsetninguna.
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
ms.openlocfilehash: 943a84407d022c2c05bc534a35a2b5d44a94653e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876413"
---
# <a name="vendor-invoice-dates"></a>Dagsetningar reiknings lánardrottins

[!include [banner](../includes/banner.md)]

Þessi grein lýsir dagsetningum sem birtast á reikningum lánardrottins. Einnig er útskýrt hvernig kerfið er sett upp þannig að það stilli sjálfkrafa bókunardagsetninguna.

Á síðunni **Upplýsingar um reikning lánardrottins í bið** sýnir reikningshausinn fjórar dagsetningar: móttökudagsetningu reiknings, reikningsdagsetningu, bókunardagsetningu og gjalddaga. Þegar reikningur lánardrottins er búinn til eru eftirfarandi dagsetningar slegnar inn sjálfgefið:

- **Móttökudagsetning reiknings** – Þessi reitur er stilltur á núgildandi dagsetningu kerfis.
- **Bókunardagsetning** – Þessi reitur er stilltur á núgildandi dagsetningu kerfis. 
- **Gjalddagi** – Dagsetningin í þessum reit er reiknuð samkvæmt bókunardagsetningu og greiðsluskilmálum.
- **Reikningsdagsetning** – Reiturinn er sjálfgefið auður. Hinsvegar er hægt að færa inn gildi eftir þörfum. Í því tilviki er dagsetningin í reitnum **Gjalddagi** endurreiknuð miðað við dagsetningu reiknings og greiðsluskilmála.

Stundum gæti reikningur lánardrottins verið í biðstöðu í langan tíma eftir að tímabilinu lýkur. Þegar hann er tilbúinn til bókunar er gamla bókunardagsetning síðasta bókunartímabils áfram notuð. Því tímabili hefur hinsvegar verið lokað. Þar af leiðandi verður starfsmaður viðskiptaskulda að breyta öllum bókunardagsetningum handvirkt í nýja bókunartímabilið fyrir alla reikninga í bið sem voru búnir til áður.

Eiginleikinn sem lýst er í þessari grein gerir þér kleift að setja kerfið upp þannig að það stilli sjálfkrafa bókunardagsetningu í samræmi við kröfur fyrirtækisins.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Færibreytur til að breyta sjálfkrafa bókunardagsetningu lánardrottnareiknings

Fylgdu þessum skrefum til að gera kerfinu kleift að breyta bókunardagsetningu sjálfkrafa fyrir lánardrottnareikning.

1.  Farðu í **Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**.
2.  Á flipanum **Fjárhagur og virðisaukaskattur**, í reitnum **Stilla bókunardagsetningu sjálfkrafa**, skal velja eitt af eftirfarandi gildum:

    - **Engin breyting** – Kerfið breytir ekki bókunardagsetningu sjálfkrafa meðan á bókun stendur. Gildið er sjálfgefið valið.
    - **Alltaf breyta bókunardagsetningu í kerfisdagsetningu** – Kerfið breytir bókunardagsetningu sjálfkrafa í kerfisdagsetningu við bókun.
    - **Breyta bókunardagsetningu í kerfisdagsetningu þegar bókunardagsetningartímabil er lokað eða í bið** – Kerfið breytir bókunardagsetningu í kerfisdagsetningu við bókun, en aðeins ef samsvarandi tímabil bókunardagsetningar er með stöðuna **Lokið** eða **Í bið**.
    - **Breyta bókunardagsetningu í fyrsta dag nýs tímabils þegar bókunardagsetningartímabil er lokað eða í bið** – Kerfið breytir bókunardagsetningu í fyrsta dag nýs opins tímabils, en aðeins ef samsvarandi tímabil bókunardagsetningar er með stöðuna **Lokið** eða **Í bið**.

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

    - Ef þessi valkostur er stilltur á **Já** er reikningsdagsetningin notuð og breyting bókunardagsetningar hefur ekki áhrif á gengið.
    - Ef þessi valkostur er stilltur á **Nei** er bókunardagsetningin notuð til að reikna gengið. Þegar bókunardagsetningin er uppfærð eru bókhalds- og skýrsluupphæðir endurreiknaðar. Þar af leiðandi þarf að villuleita samsvörun aftur.

## <a name="validation"></a>Villuleit

Tveir aðrir reitir á flipanum **Reikningur** á síðunni **Færibreytur viðskiptaskulda** (**Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**) hafa áhrif á vinnslu reiknings:

- Ef reiturinn **Athuga notað reikningsnúmer** er stilltur á **Hafna tvítekningum innan fjárhagsársins** notar kerfið bókunardagsetningu til að leita að tvíteknum reikningum við bókun reiknings.
- Ef reiturinn **Krefjast dagsetningar skjals á reikningi lánardrottins** er stilltur á **Villuvalkostur** er gerð krafa um reitinn **Reikningsdagsetning í haus reiknings í bið**. Ef reikningsdagsetning er síðar en bókunardagsetning sýnir kerfið villuboð.
