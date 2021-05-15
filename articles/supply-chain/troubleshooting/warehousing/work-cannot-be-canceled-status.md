---
title: Ekki er hægt að hætta við vinnu vegna stöðu hennar
description: Ekki er hægt að hætta við vinnu vegna stöðu hennar
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924256"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>Ekki er hægt að hætta við vinnu vegna stöðu hennar

Villukóði WAX2190

## <a name="symptoms"></a>Einkenni

Kerfið sýnir eftirfarandi villuboð:

> Ekki er hægt að hætta við vinnu %1 því að hún er með stöðuna %2.

## <a name="cause"></a>Orsök

Ekki er hægt að hætta við verkið í núverandi stöðu.

Vinnuhaus eða vinnulínur eru ekki með væntanlegt gildi **Vinnustöðu**. Reiturinn **Vinnustaða** í vinnuhausnum er ekki stilltur á *Opið* eða *Í vinnslu*.

## <a name="resolution"></a>Upplausn

Til að hætta við verkið skal fylgja eftirfarandi skrefum.

1. Fara í **Vöruhússtjórn \> Reglubundin verkefni \> Hreinsa \> Hætta við vinnu**.
1. Tilgreinið kenni verksins sem á að hætta við í svæðinu **Vinnukenni**.
1. Veljið **Í lagi**.
1. Veljið **Já** til að staðfesta að hætta skuli við verkið.

Frekari upplýsingar er að finna á [Hætta við vöruhúsavinnu vegna frábrigðameðhöndlunar](../../warehousing/cancel-warehouse-work.md).
