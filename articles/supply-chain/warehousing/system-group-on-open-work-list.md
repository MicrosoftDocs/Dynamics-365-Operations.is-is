---
title: "Kerfisflokkun á opnum verkefnalista"
description: "Í þessu efnisatriði er lýst hvernig eigi að sía opna vinnu í fartæki."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d9ca6b0d4a9909d419d6241a044336d7a02aea02
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="system-grouping-on-an-open-work-list"></a>Kerfisflokkun á opnum verkefnalista

[!include [banner](../includes/banner.md)]

Með því að nota kerfið flokkunarsvæði, er hægt að sía opna verkefnalistinn án þess að þurfa til þess að breyta fartæki valmyndaratriði.
Þar sem það á við um flokkun kerfið vinnur síun verkefnalista á haussvæðið einni vinnustöð. Ekki er hægt að nota kerfið flokkun á netinu stigasvæðum síu.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Settu upp kerfisflokkun í opinn verkefnalista
Notið eftirfarandi skrefum til að setja upp kerfi flokkun á opnu verkefnalista.

-   Úr valmyndaratriði fartæki, veljið **Greiðslumáta: Óbeina** og **Kóða Verkþættinum: Birtingu opinna verkefnalistinn**. Eftirtaldir valkostir verða í boði. Þessir valkostir eru nauðsynleg fyrir flokkun á opnu verkefnalistinn kerfið. 

|        Valkostur         |                                                                                                                                                                                                                                                                         lýsing                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Leyfa flokkun kerfi |                                                                                                                                                                                                                                                 Gerir kerfið groping fyrir vinnustöðina valmyndaratriði listann.                                                                                                                                                                                                                                                  |
| Kerfisflokkunarsvæði | Aðeins tiltækt ef <strong>Leyfa kerfið vinnu</strong> er stillt á <strong>Já</strong>. Velja svæðið sem ákvarða hvernig tiltektarvinna verður flokkuð fyrir starfsmenn. Til dæmis, ef þú velur <strong>ShipmentId</strong> svæðinu starfsmaður verður skanna Sendingarkennið til að flokka vinnuna tiltekt. Öll vinna fyrir sendingunni er síðan úthlutað til starfsmanns. Þessi reitur krefst þess að stofnað sé valmyndaratriði til að nota fyrirliggjandi vinnu sem er flokkuð af kerfinu. Notkun á <strong>Kerfið flokkun merki</strong> til að upplýsa viðkomandi hvað skanna. |
| Kerfisflokkunarmerki |                       Aðeins tiltækt ef <strong>Leyfa kerfið vinnu</strong> er stillt á <strong>Já</strong>. Færið inn upplýsingar um starfsmann um hvað á að skanna þegar tiltekt vinnu er flokkuð. Til dæmis, ef verið er að nota reitinn <strong>ShipmentId</strong> til að flokka tiltektarvinnu eftir sendingu væri hægt að færa inn Sendingarkenni í reitinn. Þessi reitur krefst þess að stofnað sé valmyndaratriði til að nota fyrirliggjandi vinnu sem er flokkuð af kerfinu. Einnig verður að velja reitinn til að flokka eftir í reitnum <strong>Kerfisflokkunarsvæði</strong>.                       |


