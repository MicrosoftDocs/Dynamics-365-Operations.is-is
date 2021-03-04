---
title: Staðfesting lotu og númeraplötu
description: Í þessu efnisatriði er lýst hvernig eigi að setja upp og nota staðfestingu runu og númeraplötu úr fartæki.
author: Mirzaab
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a953b677b1188750241772d7ae966a1dba77b92e
ms.sourcegitcommit: 9f32389715b226c11e74c53547527e0a8b51e300
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514303"
---
# <a name="batch-and-license-plate-confirmation"></a>Staðfesting lotu og númeraplötu

[!include [banner](../includes/banner.md)]

Staðfesting runu gerir kleift að staðfesta að rétt runa sé valin úr fartækinu. Í fyrstu tiltekt á vinnustöð fyrir vörur með „runu yfir“ eingöngu, þar sem runa yfir gefur til kynna runusvið sem er hærra en staðsetningin í leitarstigveldinu verður að staðfesta að runan sem er valin sé sú sama og er í tiltektarlínu.

Staðfesting númeraplötu gerir kleift að staðfesta að rétt númeraplata sé tekin til úr fartækinu Þegar tiltektarvinna á sér stað úr stigstaðsetningu verður að staðfesta að númeraplatan sem er tekin til sé sú sama og sú sem tengist verkinu. Ef vinna er hafin með því að skanna númeraplötu er þessu staðfestingarskrefi sleppt.

## <a name="where-it-applies"></a>Þar sem það á við

Staðfesting á við við eftirfarandi kringumstæður:

- Runustaðfesting á við um tiltekt í upphafi á vörum með runu yfir.
- Staðfesting á númeraplötu á við um tiltekt úr stigstaðsetningum.

> [!IMPORTANT]
> Áfylling er ekki studd fyrir staðfestingu númeraplötu. Engin staðfestingarskref númeraplötu eru stofnuð þegar verið er að framkvæma áfyllingarvinnu.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Uppsetning staðfestingar á runu og númeraplötu

Hægt er að stilla staðfestingu á runu og númeraplötu úr valmynd í fartæki.

1. Færið inn uppsetningu á verkstaðfestingu í valmynd fartækisins.  
1. Veljið valmöguleikann fyrir staðfestingu á annaðhvort runu eða númeraplötu. Báðir valmöguleikar eru í boði fyrir tiltektarvinnu þar sem sjálfkrafa staðfesting er ekki virkjuð.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]