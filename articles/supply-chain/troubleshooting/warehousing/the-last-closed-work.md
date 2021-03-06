---
title: Síðasta lokaða vinnulína verður að vera ganga frá
description: Síðasta lokaða vinnulína verður að vera ganga frá
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924376"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a>Síðasta lokaða vinnulína verður að vera ganga frá

Villukóði WAX1285

## <a name="symptoms"></a>Einkenni

Kerfið sýnir eftirfarandi villuboð:

> Síðasta lokaða vinnulína verður að vera Ganga frá.

## <a name="cause"></a>Orsök

Ekki er hægt að hætta við verkið í núverandi stöðu.

Í síðustu vinnulínunni er reiturinn **Staða verks** stilltur á *Lokaður*, en reiturinn **Vinnugerð** er ekki stilltur á *Frágangur*.

## <a name="resolution"></a>Upplausn

Til að hætta við verkið skal fylgja eftirfarandi skrefum.

1. Fara í **Vöruhússtjórn \> Reglubundin verkefni \> Hreinsa \> Hætta við vinnu**.
1. Tilgreinið kenni verksins sem á að hætta við í svæðinu **Vinnukenni**.
1. Veljið **Í lagi**.
1. Veljið **Já** til að staðfesta að hætta skuli við verkið.

Frekari upplýsingar er að finna á [Hætta við vöruhúsavinnu vegna frábrigðameðhöndlunar](../../warehousing/cancel-warehouse-work.md).
