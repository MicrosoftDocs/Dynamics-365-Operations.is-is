---
title: Staðfesting á tiltekt hluta
description: Einingatiltekt gerir þér kleift að staðfesta hverja birgðaeiningu í tiltektar- eða talningarvinnu í fartæki.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f9da533998341de60d210e196baae64d285d372
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818849"
---
# <a name="piece-picking-confirmation"></a>Staðfesting á tiltekt hluta

[!include [banner](../includes/banner.md)]

Einingatiltekt gerir þér kleift að staðfesta hverja birgðaeiningu í tiltektar- eða talningarvinnu í fartæki. Í tiltekt er hægt að staðfesta verkmagn sem fara þarf fram upp að því marki sem tilgreint er í tiltektarverki. Fyrir talningu er hægt að skanna birgðirnar sem verið er að telja og fylgjast með heildarupphæðinni.

Þegar einingatiltekt er virkjuð er staðfesting afurðar sjálfkrafa valin. Fyrir tiltekt af vinnugerð er hægt að stilla hámarksfjölda hluta. Það gerir þér kleift að setja hámark á fjölda eininga sem þarf að staðfesta í verkferlinu. Hámarksmagnið byggist á núverandi verkeiningu sem verið er að vinna. Verk af gerðinni talning leyfir ekki hámark.

Einnig er hægt að nota magn og mælieiningu (UOM) sem tengist skönnuðu strikamerki. Þetta virkar fyrir móttöku á innflæði, þar á meðal móttöku á blandaðri númeraplötu, vöru í innkaupapöntun, vöru í flutningspöntun og hleðsluvöru. Þetta virkar einnig fyrir einingatiltekt þar sem skönnun á strikamerki bætir magninu við heildarfjölda staðfestra eining sem fara úr mælieiningu á strikamerkinu í verkeininguna. Við talningu á mælieiningu á strikamerki staðfestir að magnið er leyfilegt fyrir talningu á röðunarflokknum, er magninu bætt við heildarfjölda.

## <a name="where-it-applies"></a>Þar sem það á við

Einingatiltekt gengur fyrir alla talningavinnu og fyrir fyrstu tiltekt í öllum tegundum vinnu. Einingatiltekt á ekki við ef vörunni er stjórnað af raðnúmerum eða ef um er að ræða framleiðslutiltekt eða kanban-tiltekt úr númeraplötustaðsetningu og varan er stillt á millistigsvigtun.

## <a name="set-up-piece-picking"></a>Uppsetning einingatiltektar

1.  Í valmyndaratriði fartækis skaltu opna uppsetningarskjámyndina fyrir vinnustaðfestingu: Vöruhúsakerfi > **Vöruhúsakerfi** > **Uppsetning** > **Fartæki** > **Valmyndaratriði fartækis**. 
2. Opnaðu Uppsetning vinnustaðfestingar í valmyndaratriði fartækis.

Eftirfarandi valkostir verða tiltækar til vals þegar gerð vinnu er tiltekt eða talning.


|           Valkostur           |                                                                            lýsing                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Staðfesting einingartiltektar | Tiltækt fyrir tínslu og talningu. Staðfesting vöru er sjálfkrafa valin. Gerir kleift að staðfesta hverja birgðaeiningu úr fartækinu. |
|  Hámarksfjöldi eininga  |                   Tiltækt fyrir tiltektarvinnu ef staðfesting einingatiltektar er virkjuð. Stillir takmörkun á fjölda eininga sem þarf að staðfesta.                   |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]