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
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: dbf0e49b1156c54cd37bbbe57ca564cdbc45fb2d
ms.contentlocale: is-is
ms.lasthandoff: 06/20/2017

---

# <a name="system-grouping-on-an-open-work-list"></a>Kerfisflokkun á opnum verkefnalista

[!include[banner](../includes/banner.md)]

Með því að nota kerfið flokkunarsvæði, er hægt að sía opna verkefnalistinn án þess að þurfa til þess að breyta fartæki valmyndaratriði.
Þar sem það á við um flokkun kerfið vinnur síun verkefnalista á haussvæðið einni vinnustöð. Ekki er hægt að nota kerfið flokkun á netinu stigasvæðum síu.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Settu upp kerfisflokkun í opinn verkefnalista
Notið eftirfarandi skrefum til að setja upp kerfi flokkun á opnu verkefnalista.

-   Úr valmyndaratriði fartæki, veljið **Greiðslumáta: Óbeina** og **Kóða Verkþættinum: Birtingu opinna verkefnalistinn**. Eftirtaldir valkostir verða í boði. Þessir valkostir eru nauðsynleg fyrir flokkun á opnu verkefnalistinn kerfið. 

| Valkostur        | lýsing   | 
| ------------- | ------------- |
| Leyfa flokkun kerfi   | Gerir kerfið groping fyrir vinnustöðina valmyndaratriði listann.| 
| Kerfisflokkunarsvæði   | Aðeins tiltækt ef **Leyfa kerfið vinnu** er stillt á **Já**. Velja svæðið sem ákvarða hvernig tiltektarvinna verður flokkuð fyrir starfsmenn. Til dæmis, ef þú velur **ShipmentId** svæðinu starfsmaður verður skanna Sendingarkennið til að flokka vinnuna tiltekt. Öll vinna fyrir sendingunni er síðan úthlutað til starfsmanns. Þessi reitur krefst þess að stofnað sé valmyndaratriði til að nota fyrirliggjandi vinnu sem er flokkuð af kerfinu. Notkun á **Kerfið flokkun merki** til að upplýsa viðkomandi hvað skanna. |
| Kerfisflokkunarmerki   | Aðeins tiltækt ef **Leyfa kerfið vinnu** er stillt á **Já**. Færið inn upplýsingar um starfsmann um hvað á að skanna þegar tiltekt vinnu er flokkuð. Til dæmis, ef verið er að nota reitinn **ShipmentId** til að flokka tiltektarvinnu eftir sendingu væri hægt að færa inn Sendingarkenni í reitinn. Þessi reitur krefst þess að stofnað sé valmyndaratriði til að nota fyrirliggjandi vinnu sem er flokkuð af kerfinu. Einnig verður að velja reitinn til að flokka eftir í reitnum **Kerfisflokkunarsvæði**.|
