---
title: Ekki er hægt að hætta við vinnu sem er skráð á notanda
description: Ekki er hægt að hætta við vinnu sem er skráð á notanda
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
ms.openlocfilehash: 1d7b0140d0c2724234a549ca4dfb23109012654abe0e60fcea1f98e8f17c153a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748692"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>Ekki er hægt að hætta við vinnu sem er skráð á notanda

Villukóði WAX708

## <a name="symptoms"></a>Einkenni

Kerfið sýnir eftirfarandi villuboð:

> Ekki er hægt að hætta við vinnu sem er skráð á notanda.

## <a name="cause"></a>Orsök

Verki er læst af notanda og er ekki hægt að hætta við. Opnaðu vinnukennið og opnaðu svo flipann **Almennt** til að staðfesta þetta. Ef verkið er læst verður reiturinn **Staða verks** stilltur á *Í vinnslu* og reiturinn **Læst af** stilltur á notandakenni.

## <a name="resolution"></a>Upplausn

Til að hætta við verkið skal fylgja eftirfarandi skrefum.

1. Fara í **Vöruhússtjórn \> Reglubundin verkefni \> Hreinsa \> Hætta við vinnu**.
1. Tilgreinið kenni verksins sem á að hætta við í svæðinu **Vinnukenni**.
1. Veljið **Í lagi**.
1. Veljið **Já** til að staðfesta að hætta skuli við verkið.

Frekari upplýsingar er að finna á [Hætta við vöruhúsavinnu vegna frábrigðameðhöndlunar](../../warehousing/cancel-warehouse-work.md).
