---
title: "Staðfesting einingartiltektar"
description: "Í þessu efnisatriði er því lýst hvernig eigi að setja upp og nota staðfestingu einingartiltektar úr fartæki."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 62b637b81a522c353067248deea79cfbf98518e9
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="piece-picking-confirmation"></a>Staðfesting einingartiltektar

[!include[banner](../includes/banner.md)]

Einingatiltekt gerir þér kleift að staðfesta hverja birgðaeiningu í tiltektar- eða talningarvinnu í fartæki. Í tiltekt er hægt að staðfesta verkmagn sem fara þarf fram upp að því marki sem tilgreint er í tiltektarverki. Í talningarvinnu geturðu skannað birgðirnar sem þú ert að telja og fylgst með heildarmagninu.

Þegar einingatiltekt er virkjuð er staðfesting afurðar sjálfkrafa valin. Fyrir verktegundina tiltekt er hámarksfjöldi eininga virkjaður. Það gerir þér kleift að setja hámark á fjölda eininga sem þarf að staðfesta í verkferlinu. Hámarksmagnið byggist á núverandi verkeiningu sem verið er að vinna. Verk af gerðinni talning leyfir ekki hámark.

Einnig er hægt að nota magn og mælieiningu (UOM) sem tengist skönnuðu strikamerki. Þetta virkar fyrir móttöku á innflæði, þar á meðal móttöku á blandaðri númeraplötu, vöru í innkaupapöntun, vöru í flutningspöntun og hleðsluvöru. Þetta virkar einnig fyrir einingatiltekt þar sem skönnun á strikamerki bætir magninu við heildarfjölda staðfestra eining sem fara úr mælieiningu á strikamerkinu í verkeininguna. Ef talning á mælieiningu á strikamerki staðfestir að magnið er leyfilegt fyrir talningu á röðunarflokknum, er magninu bætt við heildarfjölda.

## <a name="where-it-applies"></a>Þar sem það á við

Einingatiltekt gengur fyrir alla talningavinnu og fyrir fyrstu tiltekt í öllum tegundum vinnu. Einingatiltekt á ekki við ef vörunni er stjórnað af raðnúmerum eða ef um er að ræða framleiðslutiltekt eða kanban-tiltekt úr númeraplötustaðsetningu og varan er stillt á millistigsvigtun.

## <a name="set-up-piece-picking"></a>Uppsetning einingatiltektar

1.  Í valmyndaratriði fartækis skaltu opna uppsetningarskjámyndina fyrir vinnustaðfestingu: Vöruhúsakerfi > **Vöruhúsakerfi** > **Uppsetning** > **Fartæki** > **Valmyndaratriði fartækis**. 
2. Opnaðu Uppsetning vinnustaðfestingar í valmyndaratriði fartækis.

Eftirfarandi valkostir verða tiltækar til vals þegar gerð vinnu er tiltekt eða talning.

| Valkostur        | lýsing   | 
| ------------- | ------------- |
| Staðfesting einingartiltektar   | Tiltækt fyrir tínslu og talningu. Staðfesting vöru er sjálfkrafa valin. Gerir kleift að staðfesta hverja birgðaeiningu úr fartækinu. | 
| Hámarksfjöldi eininga     | Tiltækt fyrir tiltektarvinnu ef staðfesting einingatiltektar er virkjuð. Stillir takmörkun á fjölda eininga sem þarf að staðfesta. |  

